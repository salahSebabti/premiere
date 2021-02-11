# la boucle while
---
## exercice de compréhension

### exercice 1

```python
k = 0
while k < 3:
    print(k)
```

executez **à la main** le code ci dessus, que se passe t-il?

```python
i = 0
while i < 3:
    print(i)
    i = i-1
```

executez **à la main** le code ci dessus, que ce passe-t-il?

### exercice 2
ecrire une boucle permettant d'afficher les suites d'entiers suivant:
- de 0 à 10 croissant
- de 5 à 10 croissant
- de 0 à 10 decroissant
- de 5 à 10 decroissant
- les entiers pair de 0 à 10 croissant
- les entiers impair de 0 à 10 croissant

convertissez ces boucles while en boucle for (utiliser un range).

### exercice 3
ecrire une boucle affichant les entiers de 10 à 0 decroissant avec un pas de 2

que se passe-t-il si on part de 11?

corriger la condition de la boucle si besoin

## exercices d'application

### exercice 4
ecrire une fonction "afficherEntre" qui prend en parametre un entier x et qui affiche les entiers de -x à x exclue

```
afficherEntre(5)
>> -4 -3 -2 -1 0 1 2 3 4
afficherEntre(0)
>>
afficherEntre(3)
>> -2 -1 0 1 2
```

### exercice 5
ecrire une fonction "premier" qui prend en parametre un nombre et retourne vrai si il est premier (Rappel: un nombre est premier si et seulement si il est divisible seulement par 1 et lui même)

```
premier(5)
>> true
premier(6)
>> false
premier(3)
>> false
```

### exercice 6
ecrire une fonction "kpremier" qui prend en parametre un entier k et affiche les k premier nombres premier
```
kpremier(3)
>> 1 2 5
kpremier(6)
>> 1 2 5 7 11 13
```

### exercice 7
ecrire une fonction "syracuse" qui prend en parametre un entier k et qui affiche sa [suite de syracuse](https://fr.wikipedia.org/wiki/Conjecture_de_Syracuse) (On appelle suite de Syracuse une suite d’entiers naturels définie de la manière suivante : On part d’un nombre entier plus grand que zèro ; s’il est pair, on le divise par 2 ; s’il est impair, on le multiplie par 3 et on ajoute 1, on s'arrete quand on arrive à 1)
```
syracuse(9)
>> 9 28 14 7 22 11 34 17 52 26 13 40 20 10 5 16 8 4 2 1
syracuse(19)
>> 19 58 29 88 44 22 11 34 17 52 26 13 40 20 10 5 16 8 4 2 1
```


### exercice 8
ecrire une fonction "afficheCarre" qui produit l'affichage suivant:
```
*****
*###*
*###*
*###*
*###*
*****
```

ecrivez une fonction "afficheCarre2" qui prend en parametre un entier k et qui affiche un acrré de "#" de coté k dont les bords sont des "*"

### exercice 9
ecrire une fonction "affiche" qui prend en parametre une chaine de caractere et qui afiche chaque lettre de cette chaine
```
affiche("asdfg")
>> a s d f g
```
### exercice 10
ecrire une fonction "indice" qui prend en parametre une chaine de caractere et un elettre et qui affiche l'indice de **la premiere** occurence de la lettre dans la chaine si le caractere est dans la chaine, n'affiche rien sinon
```
indice("asdfg",f)
>> 3
indice("fasdfg",f)
>> 0
```
### exercice 11
ecrire une fonction "indices" qui prend en parametre une chaine de caractere et un elettre et qui affiche l'indice de **toutes** les occurences de la lettre dans la chaine si le caractere est dans la chaine, n'affiche rien sinon
```
indices("asdfg",f)
>> 3
indices("fasdfg",f)
>> 0 3
```
### exercice 12
ecrire une fonction "cherche" qui prend en parametre une chaine de caractere et une autre chaine de caractere et qui affiche l'indice de **toutes** les occurences de la deuxieme chaine de caractere dans la premiere chaine de caractere

en combien de temps s'execute votre algorithme?

utiliser le code ci dessous pour timer votre temps d'execution:
```
import time

start = time.time()

# your code here
# end

print(f'Time: {time.time() - start}')
```
### exercice 13
ecrire une fonction "devine" qui vous fait deviner un chiffre tiré aléatoirement par la machine:

- la machine tire un chiffre au hasard entre 0 et 99 (randint du module random)
- l'utilisateur rentre un chiffre (input)
- tant que le chiffre de la machine est different de celui de l'utilisateur
- - si le chiffre de la machine est plus grand que celui de l'utilisateur
- - afficher "plus grand"
- - si le chiffre de la machine est plus petit que celui de l'utilisateur
- - afficher "plus petit"
- - l'utilisateur redevine un chiffre

**input** est une fonction python qui **arrete** le l'execution du code tant que l'utilisateur ne rentre pas une valeur en console, il prend en parametre une chaine de caractere à afficher avant d'entrer une valeur, la valeur entrée est la valeur de sortie de la fonction et est de type string
```
x = input("entrez une valeur:")
>> entrez une valeur:
```
l'execution s'arree tant que je n'aurais pas entrer une valeur, si je rentre **en console** "34"
```
print(x)
>> 34
```
34 est une chaine de caractere
```
print(x == 34)
>> False
```

### exercice 14
ecrire une fonction "pascal" qui rend en parametre un entier k et qui affiche un [triangle de pascal](https://fr.wikipedia.org/wiki/Triangle_de_Pascal) à k (valable jusqu'a 4, dans un premier temps, car on est limité par la structure de donnée qu'est la chaine de charactere)
l'affichage sera le suivant:
```
1
11
121
1331
14641
151051
```
comme dis avant, la 5eme ligne est incorrecte car '10' prend 2 caracteres au lieu d'un seul, on ne peut donc pas regarder un caractere mais plusieurs
deux chiffres seront donc séparer par un espace

le but maintenant est maintenant de faire une fonction "pascal2" qui permet d'afficher un triangle de pascal pour avec un nombre illimité de lignes
l'affichage sera le suivant:
```
1 
1 1 
1 2 1 
1 3 3 1 
1 4 6 4 1 
1 5 10 10 5 1
```
un chiffre est donc une suite de nombre suivit **obligatoirement** par un espace, le chiffre un s'ecrira "1 "
