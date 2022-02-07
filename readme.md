# Comment obtenir le projet
chaque rubrique question contient une série de commandes qui permettent d'effectuer une tâche bien précise.
Elles se doivent d'être exécuter dans l'ordre indiqué.

## question 1
1. `symfony new --full nomDuProjet` creation du projet nomDuProjet

2. `cd nomDuProjet`

3. `touch readme.md` 

4. `composer req symfony/webpack-encore-bundle` installe webpack-encore

5. `npm install` installations des dépendances webpack

6. `npm install bootstrap --save-dev` installation de bootstrap

7. `npm install sass-loader@^9.0.1 node-sass --save-dev` installation sass-loader


## Question 2

1. se rendre dans le fichier .env à la base de l'application
2. commenter la ligne concernant la base de données postgresql : `DATABASE_URL="postgresql://symfony:ChangeMe@127.0.0.1:5432/app?serverVersion=13&charset=utf8"`
3. décommenter la ligne `DATABASE_URL="sqlite:///%kernel.project_dir%/var/data.db"`
4. `symfony console doctrine:database:create`
5. `symfony console make:entity Activite`
6. ajouter un champ nom, type String[255] not null
7. ajouter un champ description, type text not null
8. `symfony console make:migration`
9. `symfony console doctrine:migrations:migrate`

## Question 3

1. `composer require fakerphp/faker` installation faker
2. `composer require --dev orm-fixtures` install orm fixture
3. après avoir crée les fixtures, executer `symfony console doctrine:fixtures:load`

## Question 4

1. `symfony console make:crud activite`