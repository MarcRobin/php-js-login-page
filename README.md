# Page de connexion en PHP & JS

### Installation
Pour pouvoir tester cette page de connexion en local, vous devez télécharger un environnement de serveur (xampp, lampp, wamp ou uwamp) pour avoir une base de données avec laquelle la page peut intéragir et executer le php. Il vous suffit ensuite d'importer database.sql dans la BDD puis de placer le dossier login-php dans le dossier web de votre environnement de serveur. 

### Difficultés rencontrées
J'ai voulu mettre en place le fait de pouvoir récupérer son mot de passe en cas d'oubli, mais après plusieurs tests, je n'ai pas réussi à utiliser le protocole d'envoi de mail utilisé par php, il y a encore des parties du code de mot de passe oublié dans les fichiers. J'ai également essayé de faire en sorte qu'en tapant son mail dans le formulaire de connexion, on puisse appuyer sur "Forgot password?" en désactivant la vérification du mot de passe obligatoire dans le formulaire de connexion avec du javascript mais ça ne s'est pas avéré concluant non plus.

### Comment ça marche ?
`index.php` est le fichier contenant la plupart de la logique de la page, il gère les différentes entrées de l'utilisateurs et affiche les pages en fonction des actions de ce dernier.
`DBconnect.php` contient les informations de la base de données (serveur, utilisateur et la base de donnée)
`login.tpl` est un fichier html qui contient l'affichage du formulaire de connexion et du formulaire d'inscription
`logged.tpl` est le fichier qui contient le code html de la page que l'utilisateur voit quand il se connecte avec succès. (Il contient également un peu de php pour indiquer le nom de l'utilisateur)

### Que peut-on améliorer ?
- Retenir le mot de passe de l'utilisateur
- Séparer les morceaux de code contenant la logique du php dans `index.php` dans divers fichiers .php et les appeler dans `index.php`, en particulier les appels de base de données
- Rajouter un peu de css
