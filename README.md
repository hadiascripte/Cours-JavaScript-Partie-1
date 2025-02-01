
## Qu'est-ce que JavaScript

Le  JavaScript est un langage de script multi-plateforme et orienté objet.
C'est un langage léger qui doit faire partie d'un environnement hôte (un navigateur web par exemple) pour qu'il puisse être utilisé sur les objets de cet environnement. (MDN)

1. Eenvoi de la requette
2. Exécution du back-end
3. Envoi du HTML/ CSS/ JavaScript
4. Exécution du front-end
## Les outils pour coder le JS

### 1. Éditeurs de code / IDE
Visual Studio Code (VS Code) – Léger, puissant, avec de nombreuses extensions.
Sublime Text – Rapide et personnalisable.
WebStorm – IDE spécialisé en JavaScript, payant mais très complet.
### 2. Navigateurs et outils de développement
Chrome DevTools – Outils intégrés à Google Chrome pour déboguer et analyser du code.
Firefox Developer Tools – Similaire à Chrome DevTools, avec des outils avancés pour CSS et JavaScript.
### 3. Gestionnaires de paquets
npm (Node Package Manager) – Le plus utilisé pour installer des bibliothèques JavaScript.
Yarn – Alternative à npm, plus rapide dans certaines conditions.
### 4. Environnements d’exécution
Node.js – Permet d’exécuter du JavaScript en dehors du navigateur, utile pour le backend.
Deno – Une alternative à Node.js avec des fonctionnalités de sécurité améliorées.
### 5. Plateformes de test en ligne
CodePen – Idéal pour tester du code HTML, CSS et JavaScript rapidement.
JSFiddle – Similaire à CodePen, avec plus d’options pour collaborer.
JSBin – Un autre outil en ligne pour tester du JavaScript en direct.
## Lier son fichier JavaScript

Pour lier un fichier JavaScript à une page HTML, on utilise la balise ***<script>*** dans le fichier HTML.

### 1. Lier un fichier JavaScript externe
C'est la méthode la plus courante. On utilise l'attribut src pour spécifier le chemin du fichier JavaScript.

Exemple :
Si ton fichier JavaScript s’appelle script.js et qu’il est dans le même dossier que ton fichier HTML :

```
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ma Page</title>
</head>
<body>

    <h1>Bonjour</h1>

    <!-- Lien vers le fichier JavaScript -->
    <script src="script.js"></script>

</body>
</html>
```
👉 Bonnes pratiques :

Place la balise ***<script>*** juste avant la fermeture de <body> pour que le script se charge après le HTML.

Ajoute ***defer*** pour exécuter le script après le chargement du HTML sans bloquer l'affichage :
```
<script src="script.js" defer></script>
```

### 2. Écrire du JavaScript directement dans le HTML

Tu peux aussi écrire du JavaScript directement dans un fichier HTML en plaçant le code entre des balises ***<script>*** :

```
<script>
    console.log("Hello, JavaScript !");
</script>
```
Mais cette méthode est moins recommandée pour des projets structurés, car elle mélange HTML et JavaScript.
## Les commentaires
### 1. Commentaires sur une seule ligne
On utilise // pour écrire un commentaire sur une seule ligne.

```
// Ceci est un commentaire sur une seule ligne
let x = 10; // Variable x avec une valeur de 10
```

### 2. Commentaires sur plusieurs lignes
On utilise /* ... */ pour écrire un commentaire qui s'étend sur plusieurs lignes.

```
/* Ceci est un commentaire
   sur plusieurs lignes */
let y = 20;
 ```
 
Ces commentaires sont utiles pour expliquer le code ou désactiver temporairement une portion de code sans la supprimer.
## La syntaxe

// console.log("Coucou");
// let maSuperVariable = "Hello";
## Les variables

En JavaScript, on utilise var, ***let*** ou ***const*** pour déclarer des variables.
```
let nom = "Alice"; // Variable modifiable
const age = 25; // Variable constante, non modifiable
var ville = "Paris"; // Ancienne façon de déclarer une variable (éviter son usage)

```

Copie de mon code
```
// ************ La variable ************ C'est un espace de stockage où l'on y met des données
// A ne pas utiliser
var unTexte = "Voici un texte";
// console.log(unTexte);

// ici la donnée CONST ne bougera pas. On ne peut pas changer le contenu de la variable. On devra obligatoirement aller le modifier dans la CONST d'origine.
const prenom = "justine";
// console.log(prenom);

// Ici LET permet de modifier le contenu de la variable en indiquant simplement le nouveau contenu avec le nom de la vaiable en question. Nous n'avons pas besoin d'aller modifier le contenu de la variable dans le LET initial
// Attention il faut que la console.log soit fait après la saisie de la variable pour que cette dernière soit affichée dans la console.
let unChiffre = 24;
unChiffre = 22;
// console.log(unChiffre);

let chaine = "Je suis l'une des chaines de caractères";
```
## La concaténation

Ajouter des variables avec des + (pour des petites concaténations.)
```
let nouvelleChaine =
    "Chaine précédente: " +
    chaine +
    ". J'ajoute encore un contenu. Que je dois toujours mettre entre guillemets sans oublier d'ajouter les points et les espaces.";
// console.log(nouvelleChaine);

// Ajouter des variables avec `` (en ouvertoure) et ${ qui contiendra le nom de la variable
let autreConcatenation = `Chaine précédente: ${chaine}. J'ajoute encore un contenu. Que je dois toujours mettre entre guillemets sans oublier d'ajouter les points et les espaces.`;

// console.log(nouvelleChaine);
// console.log(autreConcatenation);
```
## Les types de données

JavaScript supporte plusieurs types de données :
```
let nombre = 42; // Nombre
let texte = "Bonjour"; //Chaîne de caractères
let estVrai = true; // Booléen (true ou false)
let liste = [1, 2, 3]; // Tableau
let objet = { nom: "Alice", age: 25 }; // Objet
let valeurNulle = null; // Valeur nulle
let indefini; // Variable non définie (undefined)

```
Copie de mon code:


* Chaine de caratcères: avec guillemets ""
**let string** = "Je suis une chaine de caractères";

* Nombres: sans guillemets
`let number = 24;`

* Booléans: sans guillemets
`let boolean = true;`

* Tableaux: avec crochets **[ ]** et les valeurs s'écrivent allignées
`let array = ["je", "suis", 47, true];`

* Objets: avec accolades {} et les valeurs s'écrivent en colonne avec une clé et une valeur.
`
let object =
 {
    prenom: "audrey",
    age: 33,
    ville: "Bordeaux",
};
`
 Lorsque l'on ne sait pas encore le contenu d'une variable on peut l'écrire comme cela pour la mettre dans la mmémoire.

let arbre;
 Puis plus tard on ajoute
 ```arbre = "sapin";
 console.log(arbre);
 ```
 

## Les opérateurs / opérateurs d'affectation

### Les opérateurs
JavaScript dispose de plusieurs types d’opérateurs :

* Opérateurs arithmétiques : +, -, *, /, %, ** 

* Opérateurs de comparaison : ==, ===, !=, !==, >, <, >=, <=

 * Opérateurs logiques : && (ET), || (OU), ! (NON)


```
let a = 10;
let b = 5;
console.log(a + b); // 15
console.log(a > b); // true
console.log(a === "10"); // false (car types différents)
```
Copie de mon code:
```
console.log(4 + 5);
console.log(4 - 5);
console.log(4 / 5);
console.log(4 * 5);
console.log(4 % 5);
console.log(4 ** 5);
```
### Les opérateurs d'affectations

let total = 0;
total = total + 1;

* Pour ajouter directement 1 ou soustraire 1:

total++
total--

* Pour faire des opérations simplifiée:
total += 5;
total -= 2;
total *= 2;

`console.log(total);`

## Les structures de contrôle

On utilise if, else if, et else pour exécuter du code en fonction d’une condition.

```
let age = 18;
if (age >= 18) {
    console.log("Vous êtes majeur.");
} else {
    console.log("Vous êtes mineur.");
}
```
Copie de mon code
### Les structures de contrôle (if/else)
```
let x = 4;
let y = 2;
```

* La syntaxe est la suivante:
```
if (x > y) {
    alert("Yes x plus gros que y");
 }
 
 else {
     alert("Y plus gros que X");
}
```
```
else if (y > x) {
         alert("Oui Y est plus gros que X");
} else {
  alert("Oui ils sont égaux");
   }
```
* Pour tester si une variable est "true"
```
if (x) {
    console.log("X existe bien !");
}
```
Ceci ne calcule pas l'égalité:
``` 
   if ((x = y)) {
    console.log("Ils sont égaux");
    }
```

* Pour tester l'égalité en type (string, number) et en valeur.
```
if (x === y) {
     console.log("Ils sont égaux !");
 }
 else {
     console.log("Ils ne sont pas égaux !");
      }
```

* Pour tester l'égalité de valeur uniquement, même si le type est différent car ce dernier ne sera pas prit en compte.
```
if (x == y) {
     console.log("Ils sont égaux !");
     } else {
      console.log("Ils ne sont pas égaux !");
      }
```

**||** : ou

**&&** : et

Pour **OU** l'une des conditions doit être remplie:
```
if (x < y || x > 1) {
     console.log("Oui");
     }
```
* Pour **ET** il faut que toutes les conditions soient réunies:
```
 if (x > y && x > 2) {
     console.log("Oui");
```

## Les fonctions

Elle exécute des algorythmes de chose à faire.

### La fonction classique
```
function faireQuelqueChose() {
    console.log("Je fais quelque chose");
    console.log(5 + 6);
xécute des algorythmes de chose à faire
```

 Return sert a retourner une fonction ou à arrêter une éxécution
    xécute des algorythmes de chose à faire
```
    return;
    alert("Calcul terminé !");

```
* Attention, il faut impérativement **"appeler"** la fonction pour qu'elle soit jouée 
`faireQuelqueChose()`

### La fonction flêchée
Ici le paramètre est (a,b). La flêche (= et >) indique qu'il s'agit ici d'une fonction.
```
const addition = (a, b) => {
    console.log(a + b);
};
```
Ici on appelle la fonction en lui donnant les nombres voulus:
```
addition(4, 3);
```
## La portée des variables

`function add2() {`
Cette variable déclaré dans cette fonction, si on lui demande un console.log il ne sera pas lu dans la console parce qu'il n'existe que dans les frontières de sa fonction :

```
let num = 4;
    console.log(num + 2);
}
```

`add2()`

`console.log(num)` Il ne sera pas lu dans la console et sera noté en non défini