# les étapes à suivre
#1- Création du projet:

  composer create-project symfony/website-skeleton nom_du_projet

#2- installation doctrine: bibliothèque fournir des outils puissants pour rendre les interactions avec les bases de données faciles et flexibles.

    a- composer require symfony/orm-pack 

    b- composer require symfony/maker-bundle --dev 

#3-configuration base de donne:

    Les paramètres de la connexion à la base de donne sont stockées dans la variable DATABASE_URL qui existe dans la fichier .env.
    Exemple:
    DATABASE_URL=‘mysql://db_user:db_password@127.0.0.1:3306/db_name’
    db_user: root
    db_password: par défaut vide 
    db_name: nom de votre base par exemple 'crud_symfony'

DATABASE_URL='mysql://root:@127.0.0.1:3306/crud_symfony'

#4- création base de données :

php bin/console doctrine:database:create

#5- Création d’entité:

 php bin/console make:entity
 >nom de classe/entite

#6- Migrations: Création des tables / schémas de la base de données

    a- php bin/console make:migration 
    b- php bin/console doctrine:migrations:migrate 

#7- Création crud

php bin/console make:crud 
  >nom du classe

#8- Exécution du projet

    symfony server:start
