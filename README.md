# Sujet SAE1.01 - Implémentation d'un besoin client

### 1. Objectif général
L’objectif de cette SAÉ est de développer une première application permettant de répondre à un besoin client, en vous appuyant sur les bases de la programmation acquises à travers la ressource initiation au développement (R1.01). Cette application respectera les normes de codage utilisées dans cette ressource (cf. Guide de programmation).

### 2. Contexte
Les courses de canoë se déroulent en général sur un stade d’eau vive ou sur un parcours aménagé sur une rivière, mais peuvent tout autant être pratiquées sur des rivières naturelles.

Le parcours comporte de 18 à 22 portes matérialisées par des fiches bicolores (blanche et verte ou blanche et rouge) sur une distance d’un minimum de 250 mètres et d’un maximum de 400 mètres. Selon la couleur de la porte, elle doit être prise dans le sens de la rivière (porte blanche et verte) ou en remontant la rivière (porte blanche et rouge). Les portes doivent être franchies dans l’ordre des numéros affichés. Le parcours doit contenir 6 portes en remontée et doit être navigable dans un temps s’approchant de 90 secondes.

La compétition se déroule en deux manches chronométrées. Des pénalités sont ajoutées si le compétiteur touche une porte (2 points par porte touchée) ou s’il rate une porte (50 points). La somme des pénalités est ensuite convertie en secondes et ajoutée au temps des manches (1 point = 1 seconde).

La course comporte N compétiteurs avec N < 50. Chaque compétiteur est numéroté avec un numéro de brassard allant de 1 à N.

### 3. Objectif de l’application
On souhaite aider les arbitres à faire se dérouler la course sans contestation, et en leur fournissant un programme qui leur permettra de saisir les informations de chacun des compétiteurs sur la course effectuée (c’est-à-dire sur les 2 manches).

Pour chaque compétiteur, et pour chacune des 2 manches, on veut pouvoir saisir :

- si la manche est validée (c-à-d si la manche a été terminée, personne n’est tombé à l’eau par exemple),

- et, dans le cas où la manche est validée, son temps en millisecondes, le nombre de portes touchées et le nombre de portes ratées.

On peut alors déterminer son temps compensé, qui est :

`milliseconde + 2*1000*(nombre de portes touchées) + 50*1000*(nombre de portes ratées).`

Lorsqu’un compétiteur n’a pas validé la 1ère manche, les résultats de la seconde manche ne sont pas saisis.

L’application devra permettre de :

1. saisir les données de la course,

2. saisir les résultats de chaque manche (manche par manche),

3. afficher les résultats (temps compensés) de la course dans l’ordre des brassards,

4. afficher le podium de la course (les 3 meilleurs temps).
