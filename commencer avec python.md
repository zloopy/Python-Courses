
# Commencer avec PYTHON et la Physique

## IDE - Environnement de codage 

### Installation d'un IDE

Un IDE (Independent Development Environement) - EDI en français - est *l'espace* dans lequel on écrit et on compile notre code. 

Il y a littéralement des centaines d'IDE pour coder en PYTHON, utilisable gratuitement. La majorité sont à télécharger et installer sur votre PC/Mac, et un certain nombre sont utilisable directement sur internet (dans le *nuage*) et donc nécessite aucune installation 

:::info

Voici quelques suggestions d'IDE pour vous, **téléchargeable pour votre ordinateur personnel**: 
- **[Edupython](https://edupython.tuxfamily.org/#t%C3%A9l%C3%A9chargement)** : développé par l'éducation nationale pour l'utilisation par des lycéens. Ne marche que sur *Windows*
- **[SPYDER](https://www.spyder-ide.org/download/)** : Un IDE robuste et utilisable par tout niveau d'expertise. Installable sous toutes plateformes *windows/mac/linux*. [Bonne guide d'installation ici.](https://docs.spyder-ide.org/current/installation.html) 

Voici queqlues suggestion d'IDE **utilisable sur le web** :
- [**Google Colab**](https://colab.research.google.com/) : Un *notebook* basée sur *Jupyter*. Gratuit à utiliser si vous avez un compte Google/Gmail/Gdrive. l'avantage de cette plateform est le fait de pouvoir écrire comme dans un traitement de text ET inclure de bloc de code executable comme dans un IDE ET la possibilité de partage son document avec quelques d'autre. 
- [**Replit**](https://repl.it) : Un IDE dans le *cloud/nuage*. Il suffit de créer son compte gratuit et vous pouvez coder dans beaucoup de langue différentes, dont PYTHON. Pas besoin d'installer quoique ce soit. 
:::

Une fois votre IDE installé vous pouvez commencer avec quelques opérations de base. 

### Interface d'un IDE 

De manière générale votre environnement de codage est divisé en deux partie : 
- l'**Editeur** : comme un traitement de texte, là où vous allez écrire votre programme/code (script).
- la **Console** : l'endroit où s'affichent les résultats de l'execution de votre programme (textes, chiffres ou graphiques), mais là où vous pouvez interagir avec le programme une fois executé. 

Un IDE est essentiellement un traducteur. Vous ecrivez votre programme dans la langue choisie (PYTHON, Java, javascript, C++, Ruby, etc ...), et puis l'IDE traduit ce programme en langage machine (en code binaire composé des $1$ et $0$). 

L'IDE fait cela grâce à un *compilateur*. Execution d'un programme s'appelle donc "compiler le code". 

### Executer un programme 


Afin de compiler votre programme il y a un bouton dans l'interface de votre IDE (souvent en form d'un bouton "play" :arrow_forward:).  Since il existe des raccourcis clavier : `ctrl-F9`. (dans le cas de google colab ou jupyter c'est `ctrl-entrer`)

#### Dans la console

IL y a la possibilité d'executer certains opérations ou fonctions directement dans la console. voilà à quoi ressemble la console : 

```python
>>> 
```
Vous pouvez y écrire une commande comme `print` (pour écrire un texte), et tapper `entrer` et l'executer toute de suite : 

```python
>>> print("Hello World !")
Hello World ! 
```

La console est aussi un calculatrice, c'est à dire vous pouvez écrire le calcule que vous voulez effectuer directement dans la console, appuyer sur `entrer` et obtenir le résultat toute de suite: 
```python
>>> 2*2
4
>>> 2*(3+5)
16
```

Mais vous pouvez aussi définir vous même une fonction (que vous avez codé dans l'éditeur). Une fois votre programme compilé, la fonction est utilisable dans la console. Imaginer que vous avec défini une fonction qui calcule la racien carré d'un nombre, que vous nommez `racineCarre`. Après avoir compilé le programme, vous pouvez, directement dans la console utiliser la fonction comme le suivant : 

```python
>>> racineCarre(16)
4
```



## Règles de syntaxe

PYTHON comme toute langue a des règles de syntaxe et de grammaire à respecter, d'autant plus qu'une langue parlé que la moindre irrespect de ces règles de logique empêcherait l'execution de votre code ! 

Sans entrer trop en détail, il est important de noter que le langage PYTHON est très sensible à certaines règles de syntaxe notamment : 

### Ordre des choses : 
PYTHON lit le code dans l'ordre du haut vers le bas. C'est à dire si vous mentionnez une variable et la définissez *après* il aura du mal à executer le code. 

De la même manière, chaque nouvelle instruction peut remplacer une ancienne instruction en cas de conflit. Exemple : Vous définissez `a = 10` au début du programme, et plus tard vous donnez l'instruction `a = 15`, pour le programme, désormais la variable `a` a une valeur de `15` et non `10`.

### **Majuscule** et **minuscule** 
... ne sont pas pareilles. Une *variable* nommée `variable` n'est pas la même que `Variable` et encore différent que `VariAblE`. Pour PYTHON il s'agit de trois objets différents. 

### "**Ponctuation**" 
... est très important : on ne peut pas remplacer des `: ; , . " " ' '` de manière interchangeable. Au fur et à mesur vous allez apprendre le bon usage de cela, mais il faut vraiment le respecter scrupuleusement 

### Indentation 
de même pour "**l'indentation**" qui est essentielle pour la bonne organisation et structuration de votre programme. Par exemple, considérons les deux exemples suivants : 

```python
if 1>0 :
  print("1 est positif") 

if 1>0 :
print("1 est positif")
```
Dans le 2eme cas il y aura une erreur, car, en raison de manque d'indentation, PYTHON ne reconnait pas que le message à "printer" appartient à la condition précédente. 
La questions d'indentation est particulièrement important dans les "boucles" (`if`, `for`, `while`, etc). De manière générale, tout texte "indenté" qui suit une ligne apartient au même "bloc". 

### Commentaires `#` : 
pour faire un commentaire : Tout text qui suit le symbole `#` est considéré comme un commentaire et NON comme du code à compiler par PYTHON.  Voici deux exemple : 
```python
# définissons un ARRAY avec nos mesures

X = np.array([0, 5, 10, 15, 20])
```
ici le commentaire joue le rôles - presque - de séparateur de sections dans notre programme
```python
Xrad = np.radians(X) #ici on convertit les angles dans la liste X, de degrées en radians
```
ici on s'informe du but de cette ligne de code. 

Vous devez utiliser les commentaires dans votre code, car cela peut vraiment aider à comprendre pourquoi vous avez inclut une ligne, après le fait. 

## Opérations de bases

Une fois installé PYTHON est capable d'un certain nombre d'opération mathématiques et logiques de bases. 

### Opérations arithmétiques

Voici une liste courte des opérations arithmétiques les plus pertinentes pour nous : 


| Symbole |   Operation    | Exemple          |
|:-------:|:--------------:|:---------------- |
|    `*`    | multiplication | `>>2*3` <br> `6` |
|    `/`     | division      |`>>6/3` <br> `2`|
|    `+`     |addition|`>>2+3` <br> `5`|
|   `-`      |soustraction|`>>2-3` <br> `-1`|
|    `**`     |puissance/exposant|`>>2**3` <br> `8`|
|`%`|reste (d'une division euclidéenne|`>>5%2` <br> `1`|
|   `//`    |quotient (d'une div. euclidéenne|`>>5//2` <br> `2`|

### Opérations d'affectation

Même si PYTHON s'écrit preque comme une rédaction mathématique (une des raisons pour laquelle on aime bien PYTHON), il y a des différences entre des symboles identiques. 

L'exemple parfait est le symbole `=`. Dans PYTHON `=` est une **affectation** (un assignement). Cela veut dire que quand vous écrivez ` a = 10`, vous êtes en train d'assigner une valeur (10) a une variable (a). 

Voici donc quelques opérations d'affectation (j'aurais déclaré d'amont que `a = 10`) : 



| Symbole | Opération | Exemple |
| :-------: | :---------: | :------- |
| `+=`        |addition|`a += 3` equivaut `a = a + 3` donc $13$|
|  `*=`       |multiplication|`a *= 3` équivaut `a = a * 3`donc $30$|
|   `**=`     |exponentiation|`a **= 3` équivaut `a = a**3` donc $1000$|

## Bibliothéques

Malgré la présences d'un nombre considérable d'opérations dans une installation basique de PYTHON, on a souvent besoin de pouvoir faire des choses qui ne sont pas possible sans définir nous-me$eme une fonction capable de le faire. 

Par exemple, si l'on voulait calcular la racine carré d'une nombre, il n'existe pas une fonction prédéfinie dans PYTHON. Néanmoins nous pouvons définir une fonction pour calculer la racine carré d'un nombre. Mais si l'on fait ça pour toute opération plus complexe (trigonométrique, logarithmique, etc) le travail peut devenir très laborieux.

Heureusement les gens généreux ont déjà fait ce travail pour nous, et l'ont mis dans une ***bibliothéque***. Une bibliothéque (ou module) est uen collection de fonction définie pour nous, pret à utiliser sans aucun effort de notre part. 

Ces bibliothéques sont groupés souvent par le type de fonction qu'ils proposent. Par exemple, pour visualisation graphique des données, ou pour faire de l'algèbre linéaire, ou la logique symbolique, etc. 

Nous sommes intéressé, en particulier, par trois bibliothéques : 

| Bibliothéque | L'usage |
| ------------ | ------- |
| **Math** |Des opérations mathématiques plus avancées et complexes (e.g. trigonométrique, logarithmiques, etc) |
|**Numpy** |Algèbre linéaire, traitement des séries de données, Data analysis (analyse des données|
|**Matplotlib**|Faire des graphqiues, visualisation des données|

### "Importation" d'une bibliothéque

Si nous voulons utiliser une ou des fonctions dans une bibliothéque il faut le dire au tout début de notre programme en utilisant l'instruction `import`. 

Il y a deux façons d'utiliser cette fonction : 
1. on "importe" TOUTE la bibliothéques. Dans ce cas-là le code est : 
```python
import math as m
```
Ici on donne l'instruction d'important toute la bibliothéque "math" ET on la renomme "m" (pour des raisons que vous allez voir)
2. on "importe" une fonction seulement, avec le code suivant : 
```python
from math import sin
```
Ici on donne l'instruction de chercher dans la bibliothéque "math" et d'importer *seulement* la fonction "sin" (sinus). 

:::info
:information_source:    **A noter :**
- importation d'une bibliothéque dans votre IDE nécessite une connexion internet, si cela n'a jamais été fait avant
- importation d'une seule fonction est *beaucoup* plus rapide qu'uen bibliothéque entière, et donc si vous ne comptais utiliser pas plusieurs fonction, il vaut mieux d'importer seulement la fonction nécessaire. 
:::

Afin d'utiliser la fonction dans une bibliothéque dans votre programme il faut utiliser la notation suivante : `bibliotheque.fonction()`. Par exemple si l'on veut utiliser la fonction `sin` dans la bibliothéque `math` il faut : 
```python
import math as m 

A = m.sin(30)
```
Ici on a renommé `math` comme `m` et on dit au logiciel de chercher la fonction `sin` dans `m` et de l'appliquer à un angle de $30$. 

### Math

### Numpy

### Matplotlib.pyplot

