# BurgerQuiz

## Accès à l'application

Sur le web, en se rendant à cette adresse : [https://www.desmaths.fr/jeux/burgerquiz/](https://www.desmaths.fr/jeux/burgerquiz/).

En local, en téléchargeant les sources depuis ce repositorie.

Cela évite le temps de latence pour le chargement des vidéos étant donné qu’elles sont enregistrées sur l’ordinateur.

L’application permet d’importer les questions depuis des fichiers .csv (que l’on peut préparer dans un tableur). Trois exemples sont inclus dans le dossier « exemples » sur Dropbox (avec les réponses associées dans le pdf).

En utilisant un navigateur récent, les questions importées et la progression dans le jeu (points obtenus et question en cours) sont enregistrés en local. Il n’y a pas de perte même après une actualisation de la page.

## Commandes dans l’application</h2>

- ``F`` : Permet d’ouvrir un nouveau fichier contenant les questions
- ``R`` : Permet de réinitialiser la partie (points obtenus par les deux équipes et question en cours)
- ``P`` : Permet de rejouer la vidéo en cours (quand une vidéo est affichée à l’écran)
- ``M`` : Ajoute un point à l’équipe Mayo
- ``K`` : Ajoute un point à l’équipe Ketchup
- ``L`` : Retire un point à l’équipe Mayo
- ``J`` : Retire un point à l’équipe Ketchup
- ``Flèche droite`` : Permet d’aller sur la diapo suivante
- ``Flèche gauche`` : Permet de revenir à la diapo précédente

## Création d'un pack de questions personnalisé

Vous pouvez créer votre propre fichier de questions en respectant le modèle cidessous (ne pas hésiter à regarder les exemple).

La première colonne indique le type de diapositive et les suivantes les différents paramètres que l’on peut lui associer :

- V pour afficher une vidéo parmi « generique », « nuggets », « sel-ou-poivre », « menus », « addition », « burger-mort ».
Par exemple : ``V;nuggets``
- I pour afficher une image (présente sur le web).
Par exemple : ``I;Titre;Sous-titre affiché;http://url.de/l-image.png``
- N pour afficher une question Nuggets.
Par exemple : ``N;Question posée;Réponse A;Réponse B;Réponse C;Réponse D``
- S pour afficher une question Sel ou Poivre.
Par exemple : ``S;Thème du Sel ou Poivre;Question posée``
- L pour afficher la liste des Menus.
Par exemple : ``L;Menu 1 : Nom du menu 1;Menu 2 : Nom du menu 2;Menu 3 : Nom du menu 3``
- M pour afficher une question Menu.
Par exemple : ``M;Menu 1 : Nom du menu 1;Question posée``
- A pour afficher une question Addition.
Par exemple : ``A;Thème de l'addition;Question posée``
- B pour afficher une question Burger de la Mort.
Par exemple : ``B;Question posée``

Il est possible d’insérer du code HTML dans les questions tant qu’il n’y a pas de guillemets, de points-virgules ou de retours à la ligne utilisés. Pour mettre du texte entre guillemets, utilisez ceux-ci : ``« »``.
	  
Par exemple, ceci est accepté : ``&lt;strong&gt;Phrase 1&lt;/strong&gt;&lt;br /&gt;« Phrase 2 »&lt;br /&gt;&lt;img src='URL-image' /&gt;``

Si une question ne fonctionne pas, il faut vérifier que le format généré à l’exportation correspond aux modèles précédents (vérifier entre autres qu’il n’y a ni retour à la ligne ni point-virgule ni guillemets au sein d’une question).
