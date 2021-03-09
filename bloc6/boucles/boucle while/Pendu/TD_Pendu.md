# Mini - projet : Le pendu

## Présentation du projet :


### Règles du pendu :

Dans un premier temps il faut désigner un joueur qui devra deviner le mot. Pour expliquer plus facilement nous allons partir sur un exemple. Il y a deux joueurs, **le programme python** et Toto.

**Le programme python** pense à un mot et Toto devra le deviner. Pour ce faire, **le programme python** écrit autant de tirets qu’il y a de lettres dans le mot.

 Toto annonce une lettre. La lettre fait-elle partie du mot à deviner ?

    - Si oui, **le programme python** inscrit la lettre à sa place, sur le tiret correspondant, et autant de fois que la lettre apparaît dans le mot.

    - Sinon, **le programme python** dessine le premier trait du pendu.

Le jeu continue jusqu’au moment où l’un des joueurs remporte la partie. C’est-à-dire :

    Toto remporte la partie en découvrant toutes les lettres du mot.
    **le programme python** gagne ayant dépasser le compteur d'erreur.


### Mini projet :

Le programme python doit choisir un mot aléatoire parmi une liste de mots dans un fichier appelé '[fichier.md](./fichier.md)', l'encoder et lancer le jeu du pendu

#### 1ère Etape : Choix du mot

Il faudra dans un premier temps écrire un code qui va aller chercher un mot aléatoirement dans le fichier.

- Pour cela nous utiliserons les fonctions open(), close() et readline() pour manipuler le fichier

Par exemple : 

```python

fichier = open('fichier.md','r')
chaine = fichier.readline() #Chaine vaut 'Aaron\n'
chaine = fichier.readline() #Chaine vaut 'abaissé\n'
fichier.close()
```

Plusieurs choses sont à noter ici : 

- Pour ouvrir un fichier nous utilisons 'open()', le paramètre 'r' permet de juste 'lire' le fichier (Nous n'avons pas besoin de plus ici)

- La fonction readline() permet de lire une ligne du fichier, lorsque j'utilise 5 fois 'readline()' je me place a la ligne 5 du fichier. Il est impossible de revenir à la ligne précédente (Sauf en fermant le fichier et le réouvrant).

- Il faut utiliser 'close()' pour fermer le fichier.

Afin de choisir un mot aléatoirement nous utiliserons la fonction **randint** du module random. 

#### 2ème Etape : Encodage du mot 

Il faudra encoder le mot choisi :

Lorsque j'utilise readline() je me retrouve avec un mot comme  : 'Môt\n'
Cependant pour le jeu il faudrait encoder ce mot en 'mot', les majuscule, les accents et le retour à la ligne '\n' sont enlevés. Pour cela : 

- Pensez a utiliser la fonction lower, les slices (chaine[1:2] par exemple), et à remplacer les accents par leur lettre de base. 

- On considère les accents suivants : é è ê à â ù û î ô 

#### 3ème Etape : Le jeu du pendu 


Une fois le mot à faire deviner trouvé nous pouvons commencer à écrire le code de la fonction pendu() qui permettra de jouer. 

Il faut penser à certaines choses avant de coder comme penser aux étapes successives du jeu (sur feuille). Prenez bien le temps de réfléchir au corps de la fonction, aux variables utilisées cela vous fera gagner du temps lors de l'écriture du code.

On peut décomposer la fonction en plusieur :

- Une fonction qui vérifie qu'une lettre à déjà été choisie (**1**)
- Une fonction qui va remplacer les '-' par la lettre l choisie (**2**)
      
Cela allégera le code du jeu qui est assez long.

Remarque : au plus le code est decomposé au plus votre code sera simple et lisible. Attention de tout de même à ne pas vouloir trop décomposer il faut savoir doser.

Un exemple du code final peut être :
```python 
>>> pendu('fichier.md',22740)
---
Chosissez une lettre : 
e
---     Il vous reste 6 chances

Chosissez une lettre : 
a
---     Il vous reste 5 chances

Chosissez une lettre : 
b
---     Il vous reste 4 chances

Chosissez une lettre : 
n
n--     Il vous reste 4 chances

Chosissez une lettre : 
n
Lettre déjà choisie, réessayez 

Chosissez une lettre : 
s
ns-     Il vous reste 4 chances

Chosissez une lettre : 
r
ns-     Il vous reste 3 chances

Chosissez une lettre : 
t
ns-     Il vous reste 2 chances

Chosissez une lettre : 
a
Lettre déjà choisie, réessayez 

Chosissez une lettre : 
d
ns-     Il vous reste 1 chances

Chosissez une lettre : 
w
ns-     Il vous reste 0 chances

Perdu le mot était " nsi " réessayer !
```




## Bibliographie : 

- Jeu du pendu : « Règle du pendu - Règle de jeux d’intérieur pour enfants », 6 mai 2015. https://www.regles-jeux-plein-air.com/regle-du-pendu/.
