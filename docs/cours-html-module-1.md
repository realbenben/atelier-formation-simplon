#les balises de bases

h1,h2,h3,h4 etc....  se sont les balises titres
p   la balise text
span text en italique
strong text en gros et gras
ul>li faire des listes
a liens vers d autre pages 
img balise image
div, section sert a regrouper plusieur balise dans un container (utile pour le css)
nav la balise pour faire une navigation

Dans ce chapitre, nous allons élever un peu la barre :

a. Créer des listes ordonnées et non ordonnées
b. Modifier la taille, la couleur et le type de police
c. Modifier la couleur d'arrière-plan
d. Aligner le texte
###################################################################################
Allons plus loin maintenant en créant des listes ordonnées c'est-à-dire des listes numérotées, comme ci-dessous :

    À la ligne 8, la liste ordonnée commence avec la balise ouvrante <ol> ("ordered list").
    À la ligne 9, on ouvre une balise <li> , puis on écrit le texte du premier élément de la liste et enfin on ferme avec </li>.
    Aux lignes 10 à 12, on fait la même chose qu'à la ligne 9 pour le deuxième, le troisième et le dernier élément de la liste.
    À la ligne 13, on termine la liste ordonnée la balise fermante </ol>.

Notez qu'on écrit un élément par ligne avec <li> et </li> et que ces 4 éléments de liste sont imbriqués dans la balise <ol></ol>.

Les listes ordonnées sont parfaites pour rendre un texte lisible lorsqu'il s'agit d'énumérer des choses. Comme c'est une "double-balise", n'hésitez pas à revenir à l'exercice précédent pour vous remémorer sa syntaxe !
###################################################################################
Les listes ordonnées conviennent quand on veut représenter une suite, un ordre ou une hiérarchie mais pour établir une liste à la Prévert ?

<h2>Inventaire de Jacques Prévert</h2>
<ul>
    <li>Une douzaine d'huîtres</li>
    <li>Six musiciens</li>
    <li>Un raton laveur</li>
</ul>

Voyez-vous une différence ?

    En premier, on ouvre la liste non ordonnée avec la balise <ul> ("unordered list").
    Puis on ajoute chaque élément entre les balises <li> comme pour les listes ordonnées.
    En dernier lieu, pour annoncer la fin, on ferme la balise </ul>.

    Voilà à quoi ressemble une liste non ordonnée :

<ul>
    <li> un élément </li>
    <li> un autre élément </li>
</ul>

###################################################################################
Voilà une chose de faite ! Vous savez maintenant créer des listes ordonnées et non ordonnées.

Compliquons un peu les choses : imaginez une liste ordonnée dont chaque point contient lui-même une liste non ordonnée imbriquée à l'intérieur ? Une liste de listes en sorte. L'éditeur vous montre un exemple. Appuyez sur Soumettre ma réponse pour visualiser le résultat !

Rappelez-vous : vous avez déjà imbriqué des balises : la dernière balise ouverte est la première fermée. Voici un exemple :

 <ul><li> un seul élément ! </li></ul>
###################################################################################

 Nous allons désormais nous concentrer sur l'apparence visuelle de notre page. Rappelez-vous : la structure c'est HTML, le style c'est CSS !

On peut intégrer du code CSS directement dans les balises HTML : on l'appelle CSS inline, à la différence du code CSS contenu dans un fichier séparé. C'est un bon début pour se familiariser avec ce langage.

Mais avant d'attaquer ce nouveau challenge, apprenons à commenter notre code. Nous avons le droit d'annoter notre code, pour mieux le comprendre ou garder des informations en mémoire, sans que ces notes soient affichées par le navigateur.

###################################################################################

Vous rappelez-vous des attributs src et href que l'on a ajoutés respectivement dans la balise <img> et la balise <a> ? Et bien, on peut ajouter des attributs à toutes les balises !

Quand la balise n'est pas auto-fermante comme <a>, on place l'attribut dans la balise ouvrante. C'est donc le cas pour <p> également.

Ces attributs servent à attribuer un comportement ou une caractéristique à la balise (la cible du lien ou la source de l'image par exemple).

Pour modifier la taille du texte contenu dans un paragraphe, on peut utiliser l'attribut style. Pour cela, il suffit d'écrire style suivi du signe = et d'indiquer la propriété que l'on souhaite attribuer entre guillemets.

Dans notre cas, il s'agira de la propriété font-size (ce qui signifie "taille de la police" en anglais) mais il faut bien entendu lui donner une valeur : pour cela on utilise la ponctuation : suivie de la taille de police désirée (en chiffres) exprimée en px (pour "pixels"). Voici un exemple :

     <p style = "font-size:12px">
###################################################################################
L'attribut style est un peu magique : il admet une grande variété de valeurs et peut s'associer à la plupart des balises HTML. Par exemple, essayons de changer la couleur d'un titre.

La propriété CSS qui nous intéresse cette fois n'est plus font-size mais color. Pour attribuer la couleur verte, il faudra lui donner la valeur "green" ("vert" en anglais), ce qui donnera color:green. Ajoutez dans la balise ouvrante l'attribut style suivi du signe = puis tapez color:blue entre guillemets. Par exemple :

<h2 style="color:orange">

Si on veut changer à la fois la couleur ET la taille du texte, il n'est pas nécessaire de rajouter un attribut style : il suffit de séparer les deux propriétés par un point-virgule . Par exemple :

<h2 style="color:blue;font-size:14px">

Faites votre choix dans la liste des couleurs disponibles en HTML.

###################################################################################

Si le CSS se limitait à changer la couleur et la taille, on aurait terminé notre
cours mais heureusement vous n'imaginez pas ce qu'il vous reste à apprendre ! On peut aussi changer le type de police ou font-family ("famille de police" en anglais). On l'utilise ainsi :

<h1 style="font-family: Arial">Un titre en police Arial</h1>

    On commence par écrire <h1>Notre titre</h1>.
    Puis, dans la balise ouvrante <h1>, on ajoute l'attribut style suivi de = et on tape "font-family: Arial".

Pour changer, utilisons cet attribut avec d'autres balises, <li> par exemple :

<li style="font-family: Arial">Bonjour !</li>

Comme pour les couleurs, faites votre choix dans la liste des polices disponibles.

###################################################################################

Félicitations ! Vous êtes désormais capable de modifier la couleur, la taille et la famille des polices de votre page web. Pour rappel, on utilise l'attribut style dans la balise ouvrante de la manière suivante :

a. font-size: 16px
b. color: gold
c. font-family: Verdana

   <p style="font-size:16px; color: gold; font-family: Verdana">

Tous ces styles peuvent s'appliquer non seulement aux paragraphes mais aussi aux titres, aux liens et à bien d'autres éléments que nous allons découvrir !

###################################################################################

CSS ne permet pas seulement de modifier l'apparence du texte : il peut aussi contrôler d'autres propriétés d'un élément, par exemple la couleur de l'arrière-plan ("background" en anglais).

Toujours avec l'attribut style. Mais dans ce cas, on écrira "background-color:yellow" pour que la couleur d'arrière-plan devienne jaune (yellow en anglais).

Pour illustrer, voici comment colorer l'arrière-plan d'un paragraphe <p> en jaune :

<p style="background-color: yellow;">Un coup de Stabilo SVP !</p>

###################################################################################
CSS a aussi le pouvoir de déplacer le texte et bien entendu toujours avec l'attribut magique style . Voici quelques exemples :
a. "text-align:left" aligne le texte à gauche
b. "text-align:right" aligne le texte à droite
c. "text-align:center" centre le texte

<h2 style="text-align:right">A droite toute !</h2>
###################################################################################
Revenons à l'apparence des mots. La police, c'est fait, la taille, c'est fait... et pour mettre en gras ?

On pourrait utiliser l'attribut style et la propriété font-weight mais il existe une balise qui a le même effet. La voici :

    Identifiez les mots que vous souhaitez mettre en gras.
    Encadrez-les d'une balise ouvrante <strong> (fort en anglais) et d'une balise fermante </strong>.
    Admirez le résultat !
###################################################################################
Il existe deux façons de mettre en valeur un mot : le gras avec la balise <strong> et l'italique pour une accentuation un peu plus faible .

Là encore, il existe une propriété CSS (font-style) à placer dans un attribut style mais aussi une balise dont l'effet est équivalent. La voici :

    Identifiez les mots que vous souhaitez mettre en italique.
    Encadrez-les d'une balise ouvrante <em> ("emphasize" signifie accentuer en anglais) et d'une balise fermante </em>
    Savourez votre maîtrise du HTML
###################################################################################

C'est la fin de cette leçon et il est temps de contempler tout ce que vous ne saviez pas encore faire il y a quelques heures à peine :

    Faire des listes ordonnées et non ordonnées
    Attribuer une couleur, une taille et un type de police à un texte
    Ajouter des commentaires à un fichier HTML
    Attribuer une couleur à l'arrière-plan d'une page
    Aligner du texte
    Mettre du texte en gras et en italique

Chapeau bas ! (si, en lisant ce compliment, vous avez pensé que le point d'exclamation était en gras, et donc que la balise </strong> devait se situer après, c'est que vous êtes sur la bonne voie...)
###################################################################################
Les tableaux sont pratiques pour présenter des informations sous la forme de lignes et de colonnes. De ce fait, rien ne nous interdit de les utiliser pour réaliser une galerie de photos.

Dans l'éditeur à droite, vous avez maintenant un nouvel onglet stylesheet.css pour visualiser le code CSS attaché à la page index.html. Observez-le et essayez d'imaginer son effet sur la présentation de votre tableau.
###################################################################################

Pour être bien compris, un tableau gagne à être complété d'un en-tête de description.

Idéalement, votre en-tête devra s'étendre sur les 3 colonnes de votre tableau. L'attribut colspan vous permettra d'obtenir ce résultat en lui attribuant la valeur 3 (pour trois colonnes).
###################################################################################
Maintenant que la structure de votre tableau est en place, nous allons le remplir avec des photos en lieu et place des chiffres 1 à 9. Partez à la recherche de 9 images sur internet. Vous ne savez pas comment faire ? Tapez "photos de chats" sur votre moteur de recherche préféré (c'est Qwant, n'est-ce-pas ?).

Rappelez-vous que la balise <img> est une balise auto-fermante. Vous devez donc taper simplement :

<img src="URL" />

###################################################################################
Votre galerie de photos prendrait une autre allure si elle était cliquable. Pour cela, vous allez transformer chaque <img> en un lien en l'imbriquant dans des <a></a> :

<a href="https://simplon.fr">
  <img src="https://simpllon.fr/wp-content/themes/3wa2015/img/logos/big.png">
</a>

Vous pouvez donner la valeur de votre choix à l'attribut href de chaque ` ! Lisez l'astuce si nécessaire.

_

Vous souvenez-vous comment les balises <a> s'écrivent ?

   <a href="URL du SITE"></a>

   Votre galerie d'images est terminée. C'est un aboutissement pour vous !

Vous pouvez maintenant aller encore plus loin en partant de cette base : faire un lien vers la même image mais en plus grand pour faire une effet de zoom, rajouter des cellules dans le tableau, etc.

###################################################################################
