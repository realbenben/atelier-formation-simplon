Regardez le fichier index.html. Plutôt standard, non ? Vous connaissez tout ça : titres, paragraphes, images, listes et tableaux.

Regardez le fichier stylesheet.css. Il contient toutes les informations de style CSS pour mettre en page les éléments HTML (leur position, leur couleur, leur taille, etc.).

Nous avons commenté une ligne cruciale (ligne 4) dans l'onglet index.html. Si vous enlevez les balises ‹!-- et --› au début et à la fin de cette ligne,
vous verrez alors la magie du CSS opérer. Attention ! Ne supprimez surtout pas la balise ‹link›.

################################################################################################################################################################
Le CSS (qui signifie Cascading Style Sheets ou feuilles de style en cascade) est un langage utilisé pour définir l'apparence et la forme d'un contenu en HTML.

Une style sheet décrit ce à quoi doit ressembler le HTML, tout simplement !

On dit que ces feuilles de style sont en cascade car si vous appliquez un style à un élément HTML, il va se répercuter "en cascade" à tous les autres éléments HTML
 qu'il contient.

################################################################################################################################################################

Il faut séparer la forme (CSS) de la structure (HTML) pour deux raisons principales :
lises ‹span›‹/span› ! Tous ces mots ont une police basique mais nous voulons qu'ils soient super canons !
    cela permet d'appliquer le même style à plusieurs éléments HTML sans devoir écrire le code (ex : style="color:red") pour chacun des éléments.
    vous pouvez appliquer une apparence et un formatage identique à plusieurs pages HTML à partir d'un seul fichier CSS.

Jetez un œil au HTML dans l'onglet index.html. Il y a beaucoup de base
################################################################################################################################################################

Nous vous avons montré précédemment comment déclarer un style directement dans les balises HTML, de la manière suivante :

‹p style="color: red"›Texte en rouge !‹/p›

En fait, c'est une façon peu efficace de déclarer les styles utilisés par votre site internet pour les raisons que nous avons déjà mentionnées :
 vous devez écrire le même code
 à de multiples endroits et si vous voulez faire une modification importante de style sur plusieurs éléments, vous devrez modifier chacune des balises une par une.
  Avec un seul fichier CSS, il vous suffira de faire les modifications à un seul endroit !

Il y a deux manières de déclarer du CSS. La première est de mettre votre CSS entre des balises ‹style›‹/style›, directement dans votre fichier HTML.
Ces balises ‹style› s'insèrent entre les balises ‹head›‹/head› de votre fichier HTML.
################################################################################################################################################################
Vous avez vu qu'on pouvait mettre le CSS dans la page HTML en utilisant les balises ‹style›‹/style›. Mais il y a un autre moyen, beaucoup plus pratique.

Vous savez que vous devez écrire votre CSS dans un fichier à part. Mais comment être sûr que le fichier HTML aura accès aux informations de style contenues
 dans le fichier CSS ?

Grâce à une balise ‹link› (comme vous l'avez vu dans

les premiers exercices de ce cours) insérée entre les balises ‹head›‹/head› de votre page HTML. Votre balise ‹link› a besoin de trois attributs :

    Un attribut type qui doit toujours être égal à "text/css".
    Un attribut rel qui doit toujours être égal à "stylesheet"
    Un attribut href qui doit pointer vers l'adresse internet de votre fichier CSS.

Dans l'éditeur à droite, vous pouvez voir deux fichiers : index.html et stylesheet.css.

################################################################################################################################################################

Ceci nous amène à un concept HTML bien pratique : la balise auto-fermante.

Étant donné qu'il n'y a jamais aucun texte entre les balises ‹link› et ‹/link›, il suffit d'utiliser une seule balise qui va servir
 de balise ouvrante et fermante. Comme ceci :

‹link type="text/css" rel="stylesheet" href="adresse du fichier CSS" /›

‹img src="adresse web" /›

La plupart des balises ne sont pas auto-fermantes mais nous vous signalerons celles qui le sont pour vous faire gagner du temps.

################################################################################################################################################################
La syntaxe du CSS est différente de celle du HTML mais ne vous inquiétez pas : c'est facile à apprendre ! Le format de base est le suivant :

sélecteur {
    propriété: valeur;
}

Un sélecteur peut être n'importe quel élément HTML tel que ‹p› ‹div› ‹span› ‹i› ‹img›. Il suffit de retirer les < >.
Par exemple, pour mettre le texte des paragraphes en rouge, il suffit d'ajouter dans le fichier CSS :

p {
    color: red;
}

Une propriété est une caractéristique d'un sélecteur. La famille de police (font-family), la couleur (color) et la taille de police (font-size) sont des caractéristiques qui peuvent être attribuées à un mot ou à des paragraphes dans vos pages web (il y en a beaucoup d'autres !).

Une valeur est - comme son nom l'indique - une valeur possible de la propriété. À la propriété color, on peut attribuer la valeur rouge (red), bleu (blue), noire (black) ou n'importe quelle autre couleur. La propriété font-family peut prendre pour valeur Arial, Verdana, Impact ou toute autre police de caractères. Et ainsi de suite...

Chaque couple propriété/valeur doit se terminer par un point-virgule (;). C'est ce qui permet au CSS de savoir que votre paire est terminée et que vous êtes prêt pour la prochaine.
###############################################################################################################################################################
L'un des autres avantages du CSS est qu'il vous permet de définir plusieurs propriétés pour un même sélecteur. Par exemple, si vous voulez que tous les paragraphes aient la même couleur, la même famille de police et la même taille, il vous suffit d'écrire :

p {
    font-family: Arial;
    color: blue;
    font-size: 24px;
}

N'oubliez pas : chaque couple propriété:valeur doit se terminer par un point-virgule !

Note : Si vous avez ajusté le zoom de votre navigateur, les exercices qui utilisent font-size (taille de police) et height (hauteur) ne fonctionneront pas correctement. Pour y remédier, tapez Cmd+0 ou Ctrl+0 pour remettre votre affichage par défaut.

Rappelez-vous de la syntaxe :

    sélecteur {
        propriété: valeur;
    }
###############################################################################################################################################################
Comme vous commencez à mettre de plus en plus de paires de propriété:valeur pour chaque sélecteur CSS, il est important de ne pas oublier les points-virgules ; à la fin de chaque ligne.

Le point-virgule indique au CSS que la paire propriété:valeur est terminée et qu'il est temps de passer à la suivante. Sans point-virgule, cela va devenir confus et votre page ne ressemblera pas à ce que vous voulez.

Rappelez-vous également que toutes les paires de propriété:valeur d'un sélecteur doivent se trouver dans des accolades &#123; }.
###############################################################################################################################################################
Leçon 11/26

Bien ! Vous commencez vraiment à avoir la main.

Comme il est important d'avoir une bonne syntaxe, c'est un bon réflexe d'écrire des commentaires. De bons commentaires vous aideront à vous souvenir pourquoi vous avez fait certaines choses d'une certaine manière (ou pour aider quelqu'un qui souhaiterait comprendre votre code).

Comme vous l'avez vu, les commentaires HTML ressemblent à cela :

‹!-- Commentaire HTML --›

Contrairement aux commentaires CSS qui s'écrivent comme ceci :

/* Commentaire CSS */

Rappelez-vous que l'ordinateur ne prend pas en compte les commentaires quand il interprète le HTML et le CSS. Écrire des commentaires est une très bonne habitude à prendre !
###############################################################################################################################################################

Depuis le début, pour attribuer une valeur à la propriété color avec CSS, vous écrivez color:nomdelacouleur;.

Vous vous êtes peut-être demandé comment faire pour utiliser du mauve ? Ou du bordeaux ? Ou encore du saumon ? Le CSS connaît-il toutes ces couleurs ?

Non, le CSS ne connaît pas le nom de toutes les couleurs ! Mais il peut comprendre des millions de couleurs exprimées en valeur hexadécimale.

Vous avez l'habitude des valeurs décimales avec lesquelles nous comptons tous les jours ! Prenons par exemple le nombre 1432. Chaque chiffre de ce nombre peut prendre des valeurs entre 0 et 9. Donc, chaque chiffre n'a que 10 valeurs possibles. C'est pourquoi on parle de base 10 pour décrire cette forme classique de comptage.

Une valeur hexadécimale est composée de chiffres et/ou de lettres. Le comptage hexadécimal est en base 16 : chaque signe qui compose la valeur est soit un chiffre de 0 à 9 soit une lettre de A à F.

l y a beaucoup d'outils sur Internet pour trouver le code hexadécimal (ou hex) d'une couleur.

Il vous suffit, par exemple, de taper palette couleur hex ou nuancier couleur hex dans votre moteur de recherche.

Les codes hexadécimaux commencent tous par le symbole dièse #. Ils sont composés de six signes (chiffres ou lettres) et ne sont pas sensibles à la casse : les lettres peuvent être écrites en majuscules ou en minuscules, c'est pareil ! #FFC125 et #ffc125 représentent donc la même couleur.
###############################################################################################################################################################

Dans les exercices précédents, vous avez utilisé l'unité px (pour "pixels") pour définir la taille d'une police. Par exemple :

p {
        font-size: 10px;
  }

Un pixel est un point sur votre écran d'ordinateur. Spécifier la taille de police en pixels, c'est très bien si vous voulez que les visiteurs de votre site web voient exactement la même chose que ce qui est affiché sur votre propre écran.

Mais que se passe-t-il si des utilisateurs consultent votre site sur un écran ayant des dimensions très différentes du vôtre, celui d'un smartphone ou d'une tablette par exemple ? C'est ici qu'entrent en scène les em (à ne pas confondre avec les balises ‹em›‹/em› utilisées pour mettre du texte en italique dans le HTML).

L'unité de mesure em est une mesure relative : 1em est égal à la taille de police par défaut de l'écran utilisé. C'est donc parfait pour les smartphones par exemple puisque la taille affichée des textes dépend de la taille de l'écran du smartphone utilisé et non de la taille absolue de vos polices (celle que vous avez choisie quand vous avez codé votre site web).

Une taille de police en em dit seulement : "Hey, 1em, c'est la taille de police utilisée normalement ; la valeur 2em correspond à une taille de police deux fois plus grande ; la valeur 0.5em correspond à une taille de police deux fois plus petite !".

Testons tout cela ! Nous avons créé trois paragraphes différents avec des tailles de police (font-size) égales à 1em, 0.5em et 2em. Désormais, vous pouvez utiliser soit px soit em comme unités de mesure. Nous voulions seulement vous montrer ce qu'étaient les em pour que vous ne soyez pas surpris quand vous en rencontrerez plus tard.
###############################################################################################################################################################

Jusqu'à présent, vous avez utilisé les polices Arial, Verdana, Courier, Impact et Garamond. Mais combien de polices différentes CSS connaît-il ?

Cela dépend. La plupart des ordinateurs vont comprendre les polices de base comme Arial, Verdana, Courier et Garamond mais chacun peut avoir différentes polices installées dans son ordinateur personnel. Heureusement, CSS a des polices intégrées par défaut. Cela permet à n'importe quel utilisateur de voir ce que vous voulez lui montrer. Ces polices intégrées sont de 3 types :

    Serif : dans ce type de police, les extrémités des lettres ont des extensions. La Garamond est une police serif. Faites une recherche sur "serif" pour trouver des exemples.
    Sans-serif : c'est une police sans extensions. L'Arial et la Verdana sont des polices sans-serif.
    Cursive : c'est une police qui ressemble à une écriture manuscrite.

Vous verrez ultérieurement comment importer votre propre police. Ainsi, vous serez sûr que les visiteurs de votre site verront vos pages avec toutes les polices que vous voulez afficher.
###############################################################################################################################################################

Il n'est pas nécessaire d'utiliser directement des valeurs de police par défaut telles que cursive ou sans-serif. Vous pouvez dire à CSS d'essayer plusieurs polices : si la première n'est pas disponible, CSS passera à la suivante et ainsi de suite.

Par exemple, si vous écrivez :

p {
    font-family: Tahoma, Verdana, sans-serif;
  }

CSS va d'abord essayer d'appliquer Tahoma à vos paragraphes. Si l'ordinateur de l'utilisateur n'a pas cette police, alors CSS essaiera d'appliquer Verdana. En cas d'échec, le texte s'affichera finalement en sans-serif.
###############################################################################################################################################################

Dans cet exercice, vous allez réutiliser les concepts vu précédemment.

Dans le fichier stylesheet.css, créez les règles CSS nécessaires pour :

    Mettre le titre ‹h1› en couleur LimeGreen. Attention, il faut utiliser le code héxadécimal de la couleur (recherchez sur Internet).
    Mettre le titre ‹h1› en taille de police 2.5em et avec la police Verdana uniquement.
    Mettre le paragraphe ‹p› en taille de police 1.5em et avec la police Sans-serif au cas où l'utilisateur n'a pas Verdana installée sur son ordinateur.
    Mettre le texte entre les balises ‹span›‹/span› en couleur DodgerBlue. Attention, il faut utiliser le code héxadécimal de la couleur (recherchez sur Internet).
    Mettre le texte entre les balises ‹span›‹/span› avec une taille de police 2x plus grosse que celle du paragraphe ‹p›.
    Cliquez sur soumettre ma réponse pour vérifier vos résultats;

###############################################################################################################################################################

La balise générique ‹div› permet de structurer une page web en blocs. Pour mieux les visualiser il est possible de leur appliquer les propriétés suivantes.

Pour cela, il faut choisir les valeurs de trois propriétés :

    La couleur d'arrière-plan du bloc (background-color), pour laquelle vous choisissez une valeur hexadécimale.
    La hauteur du bloc (height) que vous mesurez en pixels.
    La largeur du bloc (width) en pixels également.

Les exercices ci-après vous donneront un bref aperçu des différents éléments HTML que vous pouvez sélectionner ainsi que quelques exemples de paires propriété:valeur (comme les trois présentées ci-dessus). Nous reviendrons plus en détail sur la sélection d'éléments HTML dans le prochain cours !
###############################################################################################################################################################

De nombreux éléments HTML peuvent faire appel à la propriété border. Elle est tout particulièrement utile pour les tableaux.

La propriété border peut prendre plusieurs valeurs. Par exemple, pour afficher une bordure de 2 pixels, continue et rouge, il suffit d'écrire :

sélecteur {
    border:2px solid red;
}
Les liens hypertexte (balises ‹a›‹/a›) peuvent être mis en forme de la même façon que du texte normal, en utilisant les propriétés color, font-family, font-size, etc.Un lien ‹a›‹/a› est de type inline. Pour respecter la sémantique HTML, il faut l'insérer dans une balise de type bloc.

L'objectif de cet exercice est de créer la structure HTML du bouton.

Le principe du bouton est qu'il soit cliquable afin de diriger l'utilisateur là où vous le souhaitez. Il faut donc utiliser une paire de balises ‹a›‹/a›.
Par défaut, les liens sont soulignés mais il est possible de changer cela avec l'utilisation de la propriété text-decoration.

###############################################################################################################################################################

Un lien ‹a›‹/a› est de type inline. Pour respecter la sémantique HTML, il faut l'insérer dans une balise de type bloc.

L'objectif de cet exercice est de créer la structure HTML du bouton.

Le principe du bouton est qu'il soit cliquable afin de diriger l'utilisateur là où vous le souhaitez. Il faut donc utiliser une paire de balises ‹a›‹/a›.

Note : La balise ‹a› est de type inline, il faudrait donc l'insérer dans une balise de type bloc afin de respecter la sémantique HTML. Mais nous contournerons le problème grâce au CSS par la suite.

ous allez appliquez une mise en forme CSS de base afin de convertir la balise ‹a› en block.

De cette façon, vous pourrez lui appliquer des dimensions et des marges afin de lui donner un rendu de "bouton".

L'objectif de cet exercice est de positionner le bouton.

Nous approfondirons le positionnement dans les exercices à venir mais voici quelques explications pour la compréhension de cet exercice :

    Quand on applique la valeur auto aux marges externes (margin) gauche et droite, cela permet de centrer horizontalement un élément HTML.
    text-align: center est le code qui permet de centrer horizontalement du contenu textuel;


###############################################################################################################################################################
À ce stade, vous avez déjà utilisé un certain nombre d'éléments HTML comme sélecteurs CSS. Vous avez appliqué des styles sur les balises HTML ‹h1›‹/h1› avec le sélecteur CSS h1. Vous avez procédé de la même façon pour les balises ‹p›‹/p› avec le sélecteur p et ainsi de suite.

En fait, tous les éléments HTML peuvent être utilisés comme sélecteurs CSS. Vous pouvez donc modifier des balises ‹ul›, ‹table› et même l'intégralité de ce qui se trouve dans ‹body› en utilisant respectivement comme sélecteur ul, table ou body.
###############################################################################################################################################################

Vous savez qu'il est possible d'imbriquer des éléments HTML les uns à l'intérieur des autres, comme ceci :

      ‹div›
        ‹div›
            ‹p›J'aime les tacos !‹/p›
        ‹/div›
      ‹/div›

Comment faire pour modifier uniquement les ‹p› qui sont à l'intérieur des deux ‹div› et non l'intégralité des ‹p› de la page HTML ?

Il suffit d'utiliser le sélecteur CSS suivant :

      div div p &#123;
        /*votre code CSS!*/
    }
###############################################################################################################################################################
Il y a aussi un sélecteur très spécial qui permet d'appliquer des styles CSS à tous les éléments de la page : le sélecteur *. Par exemple, si vous tapez :

    * {
    border: 2px solid black;
}

Vous allez créer une bordure noire continue de 2 pixels de largeur autour de tous les éléments de la page HTML
L'utilisation de sélecteurs peut paraître un peu complexe mais plus vous les utiliserez, plus vous vous sentirez à l'aise avec.

Dans cet exercice vous allez voir la notion de spécificité des sélecteurs CSS.
Sélectionner les balises ‹p› incluses dans les ‹div› est plus précis que sélectionner toutes les balises ‹p›. Ainsi, les paragraphes se trouvant en dehors des ‹div› seront bleu cyan et ceux à l'intérieur des ‹div› seront rouges. C'est la notion de spécificité des sélecteurs CSS.

Un sélecteur CSS plus précis qu'un autre sera donc prioritaire. C'est le cas dans cet exercice.

###############################################################################################################################################################

Considérez un document HTML comme un arbre avec des éléments partant du tronc principal délimité par ‹html›‹/html›. Les deux premières grosses branches sont ‹head› et ‹body›, puis les branches se multiplient et s'affinent pour donner naissance à des éléments tels que des titres ‹h1› ‹h2› ‹h3›, des tableaux ‹table› ou des paragraphes ‹p›.

Vous trouverez ici un exemple de représentation de la structure d'un document HTML,structure appelée "Document Object Model".
Parents, enfants, frères

Si vous imaginez la balise ‹html› comme étant le tronc de l'arbre, vous pouvez vous représenter ses deux premières branches ‹head› et ‹body› comme ses enfants. Ces deux balises sont les enfants de ‹html› et ‹html› est leur élément parent. Puisque ‹head› et ‹body› sont tous les deux des enfants directs de ‹html› (il n'y a aucun autre élément entre eux et leur parent), ils sont frères.

Note :

En HTML, il n'y a pas de distinction entre l'enfant (A) d'un élément et les enfants (A1, A2, A3, etc.) de cet enfant A. Ainsi, A1, A2, A3 et A sont tous considérés comme les enfants du premier élément parent (il n'y a pas la notion de "petits-enfants")

###############################################################################################################################################################

Essayons maintenant quelque chose de plus complexe.

Rappelez-vous que vous pouvez atteindre un élément qui est l'enfant d'un autre élément de cette façon :

div div p {
    /* votre CSS */
}

En écrivant div div p &#123; , nous sélectionnons tous les ‹p› imbriqués quelque part dans la page HTML à l'intérieur d'une ‹div›; cette ‹div› est elle-même imbriquée quelque part à l'intérieur d'une autre ‹div›.

Si vous voulez sélectionner un enfant direct, c'est-à-dire un élément qui est directement imbriqué à l'intérieur d'un autre élément et sans aucun autre élément entre les deux, vous devez utiliser le symbole **>**, comme ceci :

div > p {
    /* votre CSS*/
}

En procédant ainsi, seuls les ‹p› qui sont imbriqués directement à l'intérieur d'une ‹div› seront sélectionnés. Cela ne sélectionnera pas les paragraphes qui sont, par exemple, imbriqués dans des ‹div› qui sont elles-mêmes imbriquées dans d'autres ‹div›.
###############################################################################################################################################################


    Le sélecteur p &#123; met par défaut tous les paragraphes ‹p› en bleu;
    Mais le sélecteur div p &#123; est plus spécifique et met tous les parapgraphes ‹p› dans un ‹div› en rouge;
    Mais ce n'est pas le cas des deux derniers paragraphes ‹p›;
    Ils sont bien dans un ‹div› aussi, mais ils ont respectivement un sélecteur .class et #id qui sont eux-même plus spécifiques que le sélecteur div p &#123;. Ils ont donc une couleur particulière;
    Cliquez sur soumettre ma réponse pour passer à la suite;

###############################################################################################################################################################
Le sélecteur **class** est utile quand vous souhaitez appliquer le même style à plusieurs éléments HTML différents. Plutôt que d'appliquer, en la répétant, la même règle aux différents sélecteurs, vous assignez une seule et même class aux éléments HTML concernés, puis définissez le style de cette class dans l'onglet CSS.

Les "class" sont assignées aux éléments HTML grâce à l'attribut class suivi du signe =, comme ceci :

‹h1 class="NomDeLaClass"›‹/h1›
‹p class="NomDeLaClass"›‹/p›

Dans le fichier .css, la class s'écrit comme ceci :

.NomDeLaClass {
    color: red;
}

N'oubliez pas le point "." devant le nom de votre class.

Dans l'exemple ci-dessus, le titre h1 et le paragraphe p seront tous les deux en rouge.
###############################################################################################################################################################

Le sélecteur **id** est utile quand vous souhaitez appliquer un style à un seul et unique élément HTML.

Si le sélecteur class a vocation à être réutilisé plusieurs fois, chaque sélecteur id ne sera utilisé qu'une seule fois sur un site web.

La syntaxe dans le fichier HTML est la suivante :

‹h1 id="NomIdUnique"›‹/h1›

Dans le fichier .css, le sélecteur id s'écrit comme ceci :

#NomIdUnique {
    color: red;
}

N'oubliez pas le dièse "#" devant le nom de votre id.
###############################################################################################################################################################
Dans cet exercice, vous allez rassembler vos nouvelles connaissances et utiliser les deux nouveaux sélecteurs .class et #id.
Vous venez de découvrir les sélecteurs de classe. Il est temps à présent d'aborder les sélecteurs de pseudo-classe.

Un sélecteur de pseudo-classe est un moyen d'accéder à un élément HTML qui se trouve dans un état particulier, par exemple les liens quand ils sont survolés, cliqués ou encore visités.

Il existe un grand nombre de pseudo-classes, vous allez voir ici les plus communs.

La syntaxe d'un sélecteur pseudo-classe dans un fichier CSS est la suivante :

sélecteur:pseudo-classe {
        propriété: valeur;
    }

N'oubliez pas les deux points : entre le sélecteur et la pseudo-classe
oici 3 sélecteurs de pseudo-classe pour les liens (il y en a d'autres). Ils permettent de définir le style pour :

    a:link : un lien non cliqué
    a:visited : un lien qui a été cliqué
    a:hover : un lien survolé par la souris et non cliqué

Un autre sélecteur de pseudo-classe utile est :first-child. Il est utilisé pour appliquer un style uniquement aux éléments qui sont le premier enfant de leur parent.
En fait, vous pouvez sélectionner n'importe quel enfant d'un élément parent en utilisant le sélecteur de pseudo-classe :nth-child(x) où "x" correspond à la place de l'enfant dans la descendance de l'élément parent.

Par exemple :

p:nth-child(2) {
    color: red;
}

Cela va sélectionner les paragraphes p qui sont le deuxième enfant de leur parent.

L'élément représentant l'enfant que l'on veut sélectionner est spécifié juste avant :nth-child. Dans l'exemple ci-dessus, l'élément ciblé est un p. Son élément parent est celui qui le contient.

Cet exercice est un rappel sur les sélecteurs multiples.
Rappelez-vous comment utiliser les sélecteurs pour cibler des éléments imbriqués les uns dans les autres. Si vous avez un paragraphe p dans un div, ce div étant lui-même imbriqué dans un autre div, vous pouvez cibler le paragraphe p en question comme cela :

   div div p {
        /*Votre CSS*/
    }

Ce sélecteur va appliquer le style à tous les paragraphes imbriqués dans deux div, sans toucher aux paragraphes qui ne correspondent pas à ces critères

###############################################################################################################################################################
Maîtriser la position des éléments HTML vous permet d'avoir un contrôle très précis sur le rendu final de vos pages web. Les éléments de type bloc (div, ĥ1, table, p, etc.) ne s'empileront plus forcément les uns sur les autres (à moins que vous ne le souhaitiez).

Chaque élément HTML agit donc comme un conteneur qui peut contenir soit d'autres éléments html soit du texte brut.

Cet exercice propose une illustration du modèle de boîte et les propriétés CSS associées : border, padding, margin. Vous avez utilisé border dans les exercices précédents, vous verrez les autres dans les exercices suivants.
###############################################################################################################################################################
Il est possible de changer le comportement par défaut de l'affichage d'un élément html au moyen de la propriété **display**. Cette propriété peut prendre plusieurs valeurs :

    block : les éléments "block" (div p h1-h5 table) prennent toute la largeur disponible par défaut et se positionnent donc sous l'élément précédent. Vous pouvez leur appliquer des dimensions (width, height) et des marges (margin, padding);
    inline-block :les éléments "inline-block" ont les mêmes caractéristiques que les "block" mais peuvent être disposés sur une même ligne et pas les uns en dessous des autres;
    inline :les éléments "inline" (a span strong em) prennent les dimensions du texte qu'il contiennent. Il n'est pas possible de leur donner des dimensions propres (width, height) ni de leur appliquer des marges externes hautes et basses (margin-top, margin-bottom). Mais ils peuvent avoir des marges internes (padding);
    none :les éléments "none" et leur contenu disparaissent complètement de la page;

###############################################################################################################################################################
Si vous ne constatez pas beaucoup de différence, c'est normal. Les div sont par défaut des éléments de type block.

Comme indiqué, tout élément qui se positionne comme un bloc viendra automatiquement occuper toute la largeur de la page, quel que soit le contenu (ou le peu de contenu) que vous aurez mis à l'intérieur.

Mais, si vous spécifiez un affichage de type inline-block, les éléments html vont venir se positionner les uns à côté des autres.
###############################################################################################################################################################
La valeur inline-block vous permet donc de placer plusieurs blocs sur la même ligne. La valeur inline positionne aussi tous vos éléments les uns à côté des autres mais pas comme des blocs : ils ne conservent pas leur dimension.
###############################################################################################################################################################
La propriété "display" peut aussi prendre comme valeur "none" qui permet de ne pas afficher un élément sur la page web. Un élément HTML qui a cette valeur ne sera pas affiché sur la page et la place qu'il occupait sera libérée afin que les éléments HTML voisins puissent se postionner par rapport à l'emplacement libéré.

Il ne faut pas confondre "display: none" avec "visibility: hidden", les deux servent à masquer un élément HTML, mais avec la seconde solution, la place occupée par l'élément HTML reste vide et n'est pas disponible pour les éléments voisins.
###############################################################################################################################################################
Maintenant que vous connaissez les propriétés d'affichage et le modèle de boîte, plongeons-nous dans les détails concernant le comportement individuel des boîtes.

    La marge externe : margin est l'espace entourant un élément. Plus la marge d'un élément est grande, plus la distance entre cet élément et ceux qui l'entourent sera grande. Nous pouvons ajuster la marge pour rapprocher ou éloigner nos éléments HTML les uns des autres;
    La marge interne : padding est l'espace entre le contenu d'un élément et sa bordure. Nous pouvons ajuster cette valeur avec CSS pour placer les bordures plus ou moins loin du contenu;
    La bordure : border est la bordure de chaque élément (entre margin et padding). C'est ce que l'on rend visible en utilisant la propriété border;
    Le contenu : content est le contenu de la boîte. Par exemple, si on parle d'un élément p, le contenu sera le texte du paragraphe.

Dans l'illustration de cet exercice, il y a des abbréviations TM, TB, TP ils correspondent respectivement aux propriétés "top margin", "top border" et "top padding", soit "marge externe du haut", "bordure du haut" et "marge interne du haut.
Vous verrez qu'il est tout à fait possible de spécifier des valeurs différentes pour le haut, le bas, la gauche et la droite concernant toutes ces propriétés.
###############################################################################################################################################################
Commençons par les marges externes (margin). Ajuster les marges externes va non seulement modifier la position de l'élément relativement à tous les autres éléments de la page, mais aussi relativement aux "frontières" du document HTML.

Dans cet exercice, les tirets rouges représentent les bordures des éléments html et body. Vous constatez que par défaut, body possède déjà des marges sans qu'il y ait besoin de le spécifier. C'est le cas de nombreux éléments qui sont de type block par défaut (body p h1-h5 ...) mais ce n'est pas le cas du div qui est une balise générique.

Le div est donc collé aux bordures de body
###############################################################################################################################################################
Si vous voulez ajuster une marge en particulier, vous pouvez le faire comme cela :

    margin-top: /* Valeur de la marge externe du haut */
    margin-right: /* Valeur de la marge externe de droite */
    margin-bottom: /* Valeur de la marge externe du bas */
    margin-left: /* Valeur de la marge externe de gauche */


Vous pouvez aussi définir toutes les marges externes d'un élément avec la notation raccourcie. Il suffit juste de partir du haut et de tourner dans le sens des aiguilles d'une montre (Haut Droite Bas Gauche), comme cela :

    margin: 1px 2px 3px 4px

###############################################################################################################################################################
ous utilisez la propriété border depuis de nombreux exercices sous la forme suivante :

border: 1px solid black;

Cette syntaxe est en fait une notation raccourcie pour affecter à chaque bordure d'un élément html (haut, bas, gauche, droite). Il est tout à fait possible de préciser à quel côté vous souhaitez appliquer un style spécifique. Il suffit d'utiliser les propriétés suivantes :

    border-top:
    border-bottom:
    border-left:
    border-right:

###############################################################################################################################################################
Tout comme les marges externes margin, les marges internes padding peuvent être définies spécifiquement pour chaque côté d'un élément html.

Si vous voulez ajuster une marge interne en particulier, vous pouvez le faire comme cela :

    padding-top: /* Valeur de la marge interne du haut */
    padding-right: /* Valeur de la marge interne de droite */
    padding-bottom: /* Valeur de la marge interne du bas */
    padding-left: /* Valeur de la marge interne de gauche */


Vous pouvez aussi définir toutes les marges internes d'un élément avec la notation raccourcie. Il suffit juste de partir du haut et de tourner dans le sens des aiguilles d'une montre (Haut Droite Bas Gauche), comme cela :

    padding: 1px 2px 3px 4px

###############################################################################################################################################################
Affecter une marge externe gauche (margin-left) de 50px va déplacer l'élément en question dans la direction opposée, ici à droite.

En CSS, il est aussi possible de donner des valeurs négatives aux propriétés margin et padding. Ainsi, appliquer un margin-left de -50px va déplacer l'élément en question de 50px vers la gauche.
###############################################################################################################################################################
Dans les exercices précédents, vous avez vu différentes façons d'affecter le positionnement d'un élément html en utilisant les propriétés display ou margin.

Il existe cependant d'autres propriétés CSS pour positionner des éléments de manière plus "radicale": float et position.
Le flux courant

Comprendre la notion de "flux" est primordiale pour comprendre comment float et position peuvent affecter le rendu final de vos pages web.
Le "flux" est le comportement par défaut d'affichage de vos éléments html. Il suit l'ordre de déclaration des éléments tel que vous l'avez défini dans la structure de votre document HTML.

Si les propriétés padding et margin n'affectent pas le positionnement des éléments HTML dans le flux, c'est le cas des propriétés float et position.

    le positionnement flottant (float: left|right) : permet de faire "flotter" un élément à gauche ou à droite de son élément conteneur, le contenu qui suit vient naturellement englober l'élément flottant qui est retiré du "flux courant";

###############################################################################################################################################################
En utilisant la propriété float, vous pourrez rencontrer des situations où le comportement de vos éléments HTML n'est pas celui que vous attendiez. Certains éléments se retrouvant les uns au-dessus/dessous des autres.

C'est le cas, dans cet exercice, de l'élément div avec l'id footer. Il devrait se trouver en bas de page. Mais il se retrouve tout en haut car les autres éléments flottent et il a donc pris leur place.

Il existe une propriété CSS qui permet d'annuler ce comportement et de repositionner un élément HTML à son emplacement par défaut :

clear: (left|right|both)

Si vous dites à un élément clear: left, il se déplacera immédiatement en dessous de tout élément flottant sur la gauche. La valeur right a le même effet, mais pour des éléments flottant sur la droite.. Si vous lui dites clear: both, les éléments flottant à gauche et à droite seront pris en compte.
###############################################################################################################################################################
Vous venez de voir la première propriété (float) pour positionner vos éléments HTML de façon "radicale".

Il en existe une deuxième (position) et qui affecte aussi le flux courant selon les valeurs qu'elle peut prendre.

    positionnement statique (position: static) - n'affecte pas le flux.
    En fait c'est la valeur par défaut de tout élément HTML qui est dans le flux courant. Evidemment, cette valeur n'affecte pas le flux courant, elle est utilisée pour ramener un élément HTML qui était hors du flux à sa valeur par défaut;
    positionnement relatif (position: relative) - n'affecte pas le flux.
    Cette valeur permet de décaler un élément dont la position est calculée par rapport à sa position de référence. L'élément reste dans le flux. Cela sert pour effectuer des ajustements de position, comme avec margin par exemple;
    positionnement absolu (position: absolute) - affecte le flux.
    Un élément est positionné en absolu par rapport, soit au premier élément ancêtre lui-même positionné (avec position), sinon à l'élément html. Un tel élément sort complètement du flux courant, là où float positionne un élément par rapport à son parent direct. De plus, il ne prend plus toute la largeur disponible par défaut;
    positionnement fixe (position: fixed) - affecte le flux.
    Très similaire à la valeur absolute, la différence vient du fait que si la position est précisée (top, bottom, left, right), la référence sera la fenêtre du navigateur. De plus, comme son nom l'indique, l'élément restera fixé à sa position, même en cas de défilement vertical;

Important :
Pour les valeurs absolute, relative, fixed si vous ne précisez pas les valeurs de décalage (ex: top: 5px; left: 5px; bottom: 10px; right: 10px;) par rapport au nouveau point de référence, alors les éléments resteront à leur emplacement par défaut dans le flux.

Les deux div de cet exercice sont par défaut en position static. Dans les exercices suivants, vous allez modifier ce comportement par défaut avec les différentes valeurs vues ci-dessus.
###############################################################################################################################################################
Dans cet exercice, vous allez attribuer un positionnement absolu au div enfant.

Son parent n'a pas de position définie, donc le div enfant se positionnera par rapport à l'élément html
###############################################################################################################################################################
Le div "header" est maintenant fixé. Le problème est qu'un élément fixé ne prend plus toute la largeur disponible par défaut. Il va falloir préciser que l'on souhaite que le "header" prenne toute la largeur disponible.

Vous remarquez également que le div "header" se trouve visuellement en-dessous des autres éléments HTML. Cela arrive souvent quand on manipule des éléments hors du flux courant. Or il est préférable que le "header" soit visible par dessus tout autre élément HTML étant donné qu'il est fixé en haut de page. Vous allez utiliser la propriété z-index pour cela.

Cette propriété prend comme valeur un nombre entier. Plus il est élevé (par rapport aux autres z-index), plus votre élément HTML se trouvera au dessus des autres, comme un système de calques qui se superposent.
###############################################################################################################################################################
Dans cet exercice, vous allez mettre les div "menu" et "body" côte à côte.

Il y a deux options possibles :

    la technique float;
    la technique inline-block;

Ici, vous allez utiliser la deuxième technique. Elle a pour avantage que les éléments HTML restetont dans le flux, donc le div "footer" qui est en-dessous restera à sa place (pas besoin de la propriété clear). Mais elle a aussi des inconvénients que vous allez devoir corriger par la suite.
###############################################################################################################################################################
Les div "menu" et "body" devraient se trouver côte à côte grâce à inline-block. Mais ce n'est pas le cas pour deux raisons :

    Entre des éléments HTML positionnés en inline-block, il peut y avoir un espace vide dû au retour à la ligne dans le code HTML. Pour y remédier, il suffit de mettre des commentaires HTML entre les éléments en question;
    Selon les navigateurs, la largeur width d'un élément peut prendre en compte soit la largeur de son contenu, soit cette largeur plus le padding et la border. Un élément peut donc prendre plus de largeur que ce qui est précisé avec width. Pour que width soit égal à la largeur de l'ensemble il faut utiliser la propriété box-sizing: border-box.;

###############################################################################################################################################################
Maintenant que vous connaissez les grands principes du positionnement en CSS, vous allez vous en servir afin de créer un layout de base. C'est-à-dire un modèle de page qui pourra servir comme structure de base pour un site web.

Vous allez reproduire en HTML/CSS le schéma illustré ci-contre.

Quelques précisions avant de commencer :

    Vous connaissez la balise div pour créer des blocs et structurer une page web;
    Le layout que vous allez mettre en page possède une structure HTML utilisant non pas la balise générique div mais de nouvelles balises HTML5 qui ont un sens sémantique, tout comme la balise p pour les paragraphes;
    header : pour l'en-tête d'une page web;
    footer : pour le pied de page;
    nav : pour la navigation, contient généralement les liens du menu;
    section : pour délimiter les parties thématiques d'un site web. Une section peut avoir elle-même un header ou un footer;
    article : pour présenter du contenu;
    aside : pour présenter des informations additionnelles;

Il n'y a pas de restrictions à proprement parler quant à l'organisations des balises : un article peut lui-même avoir un header et un footer, etc.
###############################################################################################################################################################
La structure HTML de base est déjà en place, il n'y a pas besoin d'y toucher. Le code CSS de base est aussi en place.

Pour l'instant cela ne ressemble pas à un layout. Tous les blocs sont par défaut en gris, il est donc difficile de les distinguer.
Dans cet exercice vous allez mettre un peu de couleur pour y voir plus clair.

En fait, toutes les couleurs sont déjà définies dans le code CSS mais elles ne sont pas interprétées car elles sont écrasées par les valeurs indiquées lignes 3 et 7.

Note :
Dans un code CSS, les propriétés sont interprétées dans l'ordre dans lequel elles sont déclarées. Si une même propriété est définie plusieurs fois pour un même élément HTML, c'est la dernière valeur déclarée qui sera retenue. Ceci est vrai sauf si la première propriété contient le mot clé !important.

C'est le cas dans cet exercice : on déclare d'abord une couleur pour toutes les balises (lignes 3 et 7), puis on redéfini par la suite une nouvelle couleur pour chacune de ces balises.
###############################################################################################################################################################
Maintenant que vous distinguez plus clairement la structure HTML du layout, il faut prendre quelques précautions afin de travailler sur une base propre.

Par défaut, la balise body possède des marges margin de 8px. Quand vous travaillez sur une mise en page web, il est préférable d'annuler ces marges afin de pouvoir travailler sur l'ensemble de l'espace disponible. Il serait dommage de se limiter dès le début dans la création du layout à cause de comportements par défaut non souhaités.

C'est aussi le moment de faire en sorte que tous vos blocs soient dimensionnés tel que vous l'indiquez avec width et ce quelque soit la valeur de leur border et padding qui peuvent changés pendant la création du layout. Ainsi, quand vous dites à un bloc de faire par exemple 100px de large, vous êtes sûr que sa largeur totale sera bien de 100px et pas plus.
###############################################################################################################################################################
Maintenant que vous avez une copie de travail propre, vous allez pouvoir commencer à mettre en forme votre layout de site web.

Dans cet exercice, vous allez devoir faire en sorte que le header s'affiche de manière fixe en haut de la page.
Vous allez avoir besoin des propriétés css suivantes : position, left, right et z-index

ous allez faire en sorte que les blocs nav et section soient côte à côte. Pour cela vous allez utiliser la méthode inline-block.

, ils sont toujours l'un en-dessous de l'autre.

Cela est dû à un espace invisible qui se créé quand il y a un retour à la ligne entre la balise fermante du nav et du section. Rappelez-vous, pour y remédier il suffit d'ajouter des commentaires HTML à cet endroit précis.

C'est un point important à vérifier quand vous faites un layout avec des blocs disposés en inline-block.

Vous remarquez que les deux blocs positionnés en inline-block sont alignés vers le bas sur l'axe vertical. C'est le comportement par défaut mais ce n'est pas très esthétique.

Il est préférable que les blocs soient alignés vers le haut et pour cela il faut utiliser la propriété vertical-align.
De manière générale, dès que vous positionnez des éléments avec inline-block il faudra aussi préciser comment ils s'alignent entre eux avec vertical-align.

Bien, le layout commence à prendre forme mais il reste à aligner les blocs article et aside pour qu'ils soient côte à côte.
Dans ce cas précis, vous allez utiliser la méthode float.

Les deux blocs article et aside sont maintenant l'un à côté de l'autre. Mais à cause de la propriété float, ils sont maintenant hors du flux courant. Ils flottent donc à l'intérieur de leur parent section, mais le bloc footer qui se trouve en-dessous de article et aside dans la structure HTML est donc maintenant remonté en haut de son élément parent (section).

Dans cet exercice, vous allez utiliser la propriété clear afin de remettre par défaut le comportement de l'élément auquel elle s'applique (footer). Ainsi il va se positionner comme si les éléments au-dessus étaient restés dans le flux courant.

La valeur de clear à préciser sera both car il faut remettre par défaut à la fois float: left et float: right.

Note :
Après cela vous aurez fini la mise en page d'un layout de base pour un site web. Avec ces exercices vous aurez vu les principes essentiels du positionnement en CSS. Connaître ces astuces est important car il s'agit de la mise en place de la structure visuelle d'un site web.
###############################################################################################################################################################

###############################################################################################################################################################

###############################################################################################################################################################

###############################################################################################################################################################

###############################################################################################################################################################
