# BDD - SQL : 8h30 à 10h15 et 10h30 à 12h15 sur feuille

![](https://media.giphy.com/media/vISmwpBJUNYzukTnVx/giphy.gif)

## MCD - MLD - MPD

" L’objectif de cette partie est de réaliser un schéma MCD ou MLD en vous basant sur les informations du texte qui suit. "

Une petite boutique de musiques vous approche dans le but d’informatiser sa gestion des stocks. Suite à une longue réunion, voici un résumé concernant les données qui seront les plus utilisées dans la future application.

Les musiques seront le cœur de l’application, il faut pouvoir garder en mémoire son titre, sa durée (en seconde) ainsi que son auteur, attention il n’y a bien toujours qu’un seul auteur. 
Concernant l’auteur, l’idée serait que l’application nous permette de retrouver tous les morceaux d’un auteur en particulier, il nous faut donc enregistrer son nom ainsi que son prénom.
Et enfin, une dernière chose, les musiques pourront faire partie d’une ou plusieurs catégorie, cette information permettra de rechercher les titres du même genre.

## Requete SQL
### Partie 1 :

En vous basant sur le schéma que vous avez réalisé dans la partie 1, réaliser un script SQL permettant de créer la base de données.

### Partie 2 :

Une fois la base de données créée, ajoutez-y des données.

Pour réaliser les requêtes de la partie 4, merci de veiller à avoir au moins les informations suivantes dans votre base de données :

Une musique dont le titre est “chou chou”.
Une musique plus longue que les autres.
Un auteur qui à écrit plus de musique que les autres.
Plusieurs musiques qui ont le mot ‘aime’ dans le titre.
Une catégorie qui n’est liée à aucune musique.
Un auteur qui a pour prénom Mariette et qui est l’auteur de plusieurs musiques

### Partie 3 :

Maintenant que vous disposez d’une base avec des données, il est temps de la questionner.

Réaliser les requêtes suivantes :

1. Requête 1 : 
Afficher toutes les informations de la musique dont le titre est “chou chou”.

2. Requête 2 : 
Afficher le titre des musiques dont le titre comprend le mot ‘aime’.

3. Requête 3 : 
Afficher toutes les informations de la musique ainsi que toutes les informations de l’auteur de la musique la plus longue.

4. Requête 4: 
Afficher le nom de la catégorie qui n’a aucune musique associée.

5. Requête 5 : 
Afficher toutes les informations de l’auteur ainsi que le nombre de musiques réalisées (nommez la colonne nbMusiques) de l’auteur ayant réalisé le plus de musiques.

On va maintenant modifier un peu la base de données, réaliser les requêtes suivantes :

6. Requête 6 : 
Changer le nom de la musique ‘chou chou’ par ‘chou choucroute’.

7. Requête 7 : 
Changez le nom de toutes les musiques de l’auteur Mariette en “c’est nul”.

8. Requête 8 : 
Supprimer la catégorie qui n’a aucune musique associée.


![](https://media.giphy.com/media/143vPc6b08locw/giphy.gif)

## Question de cours : BDD - SQL - PHP
1. Qu'est ce qu'une "Clé primaire" ? une "Cardinalités" ? une "SGBD" ?
2. Quand doit-on ajouter des "Clés étrangère" ?
3. Quelle problème pose la "Redondance" et comment le résoudre ?
4. A quoi sert "l'Union" entre 2 tables ?
5. Comment s'appelle le "langage graphique utilisé pour la conception de programmes informatiques" ?
6. L'héritage PHP est-il multiple ou unique??
7. Comment voulez-vous connecter une base de données MySQL à PHP?
8. Expliquer ‘_construct()’ et ‘_destruct()’.
9. Comment trouvez-vous la longueur d'un tableau?

# CRUD avec PHP/MySQL/POO en MVC : 13h à 14h30 et 14h45 à 16h15 sur PC

![](https://media.giphy.com/media/12BYUePgtn7sis/giphy.gif)

## 1. Mise en place du projet
- Créer un projet Git : soit public, soit privé avec le formateur en administrateur
- La structure du projet sera la suivante :

```
- index.php
- src/
    - model
    - controller
    - views
```

## 2. Base de données
Utilisez la base de données que j'ai appellée « bibliotheque » :

```
abonne
---
 id(PK – AI – INT)
 prenom (VARCHAR)
 nom (VARCHAR)
---

association_abonne_ouvrage
---
id (PK – AI – INT)
id_abonne (INT)
id_ouvrage (INT)
---

ouvrage
---
- id (PK – AI – INT)
- titre (VARCHAR)
- auteur (VARCHAR)
---
```

## 3. Enregistrement des données
En respectant une structure MVC, vous crééez un formulaire pour chaque table, et notamment un formulaire contenant 2 selects ("abonnés" et "ouvrages") pour le formulaire de la table d'association.

Contrôles de saisie :
- Les champs ouvrage.titre, ouvrage.auteur, abonne.prenom, abonne.nom ne doivent pas faire plus de 150 caractères et ne doivent pas être vides.

Les données doivent s'enregistrer en base de données.

## 4. Affichage des données
**Ouvrage et Abonne :**
Pour ces deux tables, vous créérez en MVC :
- Une page qui affiche la liste des éléments, sous forme de tableau
- Une page qui affiche 1 élément
- Un bouton "Editer" qui renvoie vers une page d'édition. L'update doit fonctionner en BDD.
- Un bouton "Supprimer" qui supprime l'élément. La suppression doit fonctionner en BDD.

**Table d'association :**
- Une page qui affiche la liste des associations, sous forme de tableau
- Le tableau contiendra les champs :`Nom | Prénom | Titre de l'ouvrage | Auteur`
- Un bouton "Supprimer" qui supprime l'élément. La suppression doit fonctionner en BDD.

## 5. Bonus
### Requêtes personnalisées
- Afficher le nombre d'abonnés.
- Afficher le nombre d'ouvrages.
- Afficher le nombre d'associations.
- Afficher les ouvrages n'ayant pas été empruntés.
- Afficher les abonnés n'ayant pas emprunté de livre.
- Afficher tous les ouvrages empruntés par 1 abonné, trouvé par son nom (le WHERE doit contenir le nom et pas l'ID, de l'abonné de votre choix).
- Afficher tous les abonnés (meme ceux qui n'ont pas emprunté) ainsi que les ouvrages - pour ceux qui ont emprunté.
- Afficher les ouvrages (meme ceux qui n'ont pas été empruntés), ainsi que les abonnés - pour ceux qui ont été empruntés.

Vous produirez un code :

- Indenté
- Conceptualisé
- Documenté / Commenté
- Optimisé
- Factorisé
- Générique
- Maintenable

# Complément :
Dans `index.php`, vous incluerez le code suivant au tout début du fichier (autoload des classes) :

```php
<?php

/**
 * Autoload Classes
 */
 
const CLASSES_SOURCES = [
    'src',
    'src/model',
    'src/controller'
];

function autoloadClass( $class ) {

    $sources = array_map( function($folder) use($class) {

        return __DIR__ . $folder . '/' . $class . '.php';

    }, CLASSES_SOURCES );

    foreach($sources as $s) {

        if (file_exists( $s ) ) {
            require_once ($s);
        }
    }


}

spl_autoload_register( 'autoloadClass' );
```

Vous pouvez créer un routeur sur la page `index.php` qui écoutera deux à trois paramètres GET : `model`, `method` et éventuellement `id` si besoin.

Ces paramètres permettront de retrouver quelle méthode de quel contrôleur appeler, exemple :

```php

switch ($_GET['model']) {

    case 'ouvrage':
        
        switch ($_GET['method'] :
            case 'index':
                OuvrageController::index();
                break;
            case 'show':
                OuvrageController::show( $_GET['id'] );
                break;
                
        break;

}

```

Vous pouvez réaliser des controllers qui accueilleront une méthode statique par route, exemple :

`OuvrageController.php`

```php
class OuvrageController {

    public static function index() {
    }
    
    public static function show($id) {
    }
}
```

Le contrôleur pourrait être rempli comme suit, en appelant les Model et Vues correspondants :

`OuvrageController.php`

```php
class OuvrageController {

    public static function index() {
    
        $ouvrages = Ouvrage::all();
        include ('ouvrages/index.php');
    
    }
    
    public static function show($id) {
    
        $ouvrage = Ouvrage::find($id);
        include ('ouvrages/show.php');
    }
}
```


Les models pourront être comme suit (pensez à faire un héritage pour la méthode `bdd()` qui se retrouvera dans chaque model !)

```php

class Ouvrage {

    private function bdd() {
        $bdd = new PDO();
        $bdd;
    }
    
    public static function all() {
    
       $bdd = $this->bdd();
       
       $request = 'SELECT * FROM ouvrages';
       $response = $bdd->query($request);
       
       $data = $response->fetchAll(PDO::FETCH_ASSOC);
       return $data;
    }

}

```

Les vues seront de simples fichiers `.php` contenant du HTML et appelant les variables déclarées avant les `include()`.
