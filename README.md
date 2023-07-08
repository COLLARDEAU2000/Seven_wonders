I. Idée de simplification
Nous avons décidé de simplifier notre jeu en apportant quelques modifications et en éliminant certaines fonctionnalités complexes.

Étant donné notre manque d'expérience dans ce domaine, nous avons décidé de ne pas implémenter la Socket Programmation(qui permet plusieurs joueurs sur différents hosts de jouer le jeu ensemble). À la place, nous développons une version du jeu où les joueurs partageront le même écran. De plus, nous avons pensé qu'il serait plus logique de n'avoir que 2 joueurs sur le même écran, pas plus, alors nous avons décidé de développer la version DUEL du jeu. Cependant, au final, on n’a pas pu développer la fonctionnalité de Free City (la 3ème joueur dans la version Duel. Du coup, on a fait le jeu de version normal avec seulement 2 joueurs.

Les Merveilles ne fourniront que des points de victoire, sans autres récompenses telles que des pièces ou des effets spéciaux.

Nous n'utiliserons pas les cartes avec des effets compliqués dans notre jeu. Vous pouvez trouver la liste des cartes que nous utiliserons dans l'annexe.

Nous modifierons légèrement les coûts des cartes et des étapes pour équilibrer le jeu, étant donné que notre jeu est conçu pour seulement 2 joueurs.

Nous envisageons d'utiliser une taille de fenêtre fixe pour l'interface du jeu afin d'éviter la complexité de la programmation responsive.

Les cartes et les merveilles dans l'interface du jeu seront représentées sous forme de texte plutôt que d'images.

Normalement les points de victoire apportées par des cartes violets sont calculés au fin du jeu, mais ici, dans notre jeu on les calcule dès au moment qu’elles sont jouées.

Normalement les points de victoire apportées par des cartes vertes sont calculées dès au moment qu’elles sont jouées, mais ici, dans notre jeu on les calcule au fin du jeu.

Pas de chainement des cartes (par exemple si on a joué une carte => la carte après est e en meme chaine que cette carte sera gratuite)

II. Répartie des tâches pour la livraison 3
Pour la livraison 3, nous avons défini les tâches suivantes pour chaque membre de l'équipe :

Minh :

Authentification
Écran GameScreen
Contrôle des branches
Correction du projet
Djamila :

Codage de l'interface de tous les écrans du jeu
Diagramme UML
Amina :

Traitement des données pour le jeu (données sur les cartes et les merveilles)
Ajout de journaux (Loggers) dans l'application
Christian :

Codage de la classe PurpleCard
Achèvement de la logique du jeu
Anna :

Rédaction du rapport
Réalisation des tests
Préparation de la présentation
III. Résultats
Une fois que l'utilisateur a démarré le jeu, l'écran d'authentification apparaîtra, nécessitant l'authentification de deux joueurs pour pouvoir jouer au jeu. Le formulaire renverra une erreur si l'utilisateur laisse des champs vides ou si les informations de connexion des deux utilisateurs sont erronées. image

Si l'utilisateur n'a pas de compte, il peut s'inscrire en cliquant sur le bouton "Inscription". Cela affichera l'écran d'inscription, où l'utilisateur pourra créer un compte. Le formulaire générera une erreur si des champs sont laissés vides, si l'e-mail n'est pas au format "a@b.c" ou si les deux champs de mot de passe ne correspondent pas. image

Une fois que 2 utilisateurs se sont authentifiés avec succès, l'écran d'accueil apparaît. Cet écran comporte 5 boutons : image

"Jouer" pour commencer une partie image

Quand on tape sur une carte, les informations avec les options d'actions disponible pour cette cartes seront afficher dans un dialog dans le centre de l'écran image

Quand une carte est jouée, elle est ajoutée dans la liste des cartes jouées image

Tous les évènements comme âge suivant, guerre commence ou jeu termine va afficher dans le dialog dans le centre de l'écran image

"Profil joueur 1" pour afficher l'historique de jeu du premier utilisateur

"Profil joueur 2" pour afficher l'historique de jeu du deuxième utilisateur image

"Tutoriel" pour afficher les règles du jeu image

"Déconnecter" pour se déconnecter les 2 utilisateurs du jeu.

Particulièrement, on a pu intégré avec succès la partie back-end dans notre jeu. C'est une fontionalité qui rend notre jeu plus riche et unique. On a utilisé Firebase qui fournit des services gratuites comme héberger BDD (dans leur Real-time Database) et aussi l'authentification. Pour connecter et communiquer avec Firebase, on a utilisé les requêtes HTTPS (en utilisant la librairie java.net)

On essaie de créer un compte "java@test.com" image image
=> Le compte est bien enregitré dans la BDD image

Quand on termine de jouer une partie, le résultat de la partie est bien enregistré dans la BDD, dans l'information des 2 utilisateurs image image image

Vous pouvez aller voir notre BDD via ce lien vers Firebase: https://console.firebase.google.com/u/0/project/wonders-e2863/overview. On vous a envoyé un lien d'invitation pour pouvoir accéder dans le BDD via votre mail de Dauphine: olivier.cailloux@lamsade.dauphine.fr.

Vous pouvez tester le jeu avec 2 comptes là:

java@test.com - 12345678
dauphine@test.com - 12345678
IV. UML pour livraison 3
UMLmanuel.pdf

V. Annexe
Méthodologie de travail :
Pour garantir la qualité de notre code, respecter les délais et assurer une bonne communication entre les membres de notre équipe, nous avons suivi une méthodologie de travail efficace. Voici les pratiques que nous avons mises en place pour le développement de notre application :

Récupération des dernières mises à jour : Avant de commencer à coder, nous avons effectué une mise à jour du projet en récupérant les dernières modifications à partir du référentiel. Cela nous a permis de travailler sur la version la plus récente de l'application et d'éviter les conflits de version.

Utilisation de branches de travail : Pour éviter de modifier directement la branche principale, nous avons créé des branches de travail à partir de la branche "release-1" et nous avons travaillé sur ces branches. Cela nous a permis de travailler en toute sécurité sur des versions distinctes de l'application et d'éviter les conflits avec les autres membres de l'équipe.

Tests unitaires : Avant de soumettre une classe pour intégration dans le projet, nous l'avons testée de manière approfondie. Nous nous sommes assurés que nos tests couvraient tous les cas d'utilisation possibles de la classe.

En suivant ces pratiques, nous avons pu garantir la qualité de notre code, éviter les conflits entre les membres de l'équipe et respecter les délais de livraison.

Nous avons également documenté chaque classe et chaque méthode que nous avons développée afin de faciliter la compréhension du code par les autres membres de l'équipe. De plus, nous avons régulièrement sauvegardé notre code et l'avons partagé avec les autres membres de l'équipe pour éviter toute perte de données.

Pour la gestion de projet, nous avons utilisé Trello. Cet outil nous a permis de collaborer en temps réel, de répartir efficacement les tâches et de suivre facilement l'état de chaque tâche, ce qui a favorisé une communication fluide au sein de l'équipe.

image
Lien vers le rapport de livraison 1 :
https://github.com/oliviercailloux-org/projet-dream-team-7-wonders/blob/release-1/RAPPORT%20java%20Final.pdf

Lien vers le rapport de livraison 2 :
https://github.com/oliviercailloux-org/projet-dream-team-7-wonders/blob/release-2/README.md

Liste des cartes et des merveilles dans notre jeu
image image image image
Règles du jeu de la version DUEL
https://cdn.1j1ju.com/medias/c8/d6/88-7-wonders-rule.pdf - Page 7
