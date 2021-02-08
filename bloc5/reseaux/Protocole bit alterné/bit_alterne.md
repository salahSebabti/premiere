# Protocole du bit alterné 

Le protocole **bit alterné** se situe sur dans la couche 2 du modèle OSI

L'envoie d'un message se ferait comme ceci dans une situation idéale :

## Situation idéale :

![situation_ideale](./Images/situation_ideale.png)

- Bob envoie un message M composé de sous messages : M0, M1, M2

- Alice les recoie **tous** et dans le **bon ordre**

## Situation réelle :

Les paquets peuvent :

- être perdu
- Reçu dans le désordre 

## Principe du protocole :


Un bit de contrôle est créé pour structurer les envoies et réception des messages.


![bit_alt](./Images/bit_alt.png)

Comment cela marche ?

- Bob envoie un message avec un bit de contrôle à 0
- Alice reçoit le message et renvoie un accusé de réception à 0
- Bob ayant reçu un accusé de réception à 0, renvoie un message avec un bit de contrôle à 1 
- Alice reçoit le message et renvoie un accusé de réception à 1
- Bob ayant reçu un accusé de réception à 1, renvoie un message avec un bit de contrôle à 0

Et ce jusqu'à la fin du message.

### Limites du bit alterné :

Dans certaines situations le protocole ne permet pas de transmettre le message en bonne et due forme.

![bit_alt](./Images/erreur_bit.png)

Ici le premier accusé de récepetion a été reçu bien plus tard et cela a empeché le message M2 d'être bien reçu. 

En effet M2 a été **perdu**. Mais l'accusé de réception en 0 de la première tentative d'envoie de M0 a été reçu en retard, Bob considère donc que son message a été parfaitement envoyé 