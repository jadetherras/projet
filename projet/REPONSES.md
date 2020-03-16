#Projet programmation orientée objet (SSV)

##REPONSES du groupe *N* (*Reibel Mathieu* & *Therras Jade*) 

*************************************************
##Q1.1

-on utilise les fonctions contains() et isColliding() pour realiser les traitements des operateurs, afin d'eviter la duplication de code relative à ces fonctionnalités. On a déjà fait une surcharge de fonction pour l'opérateur >.

*************************************************
##Q1.2


-L'operateur << est externe, il n'y aurait pas de sens d'écrire out.operator<<(class) car cela demanderait de modifier la class de out.
Les operateur =, > et & definit entre deux circularBody sont en internes, puisqu'ils demandent de conparer les éléments de différentes instances d'une même classe. On préserve ainsi l'encapsulation.
Pour l'opérateur > entre un circularBody et un Vec2d, on compare des types différents donc définir en interne n'aurait pas de sens même si cela reste possible, on définit donc en externe.

*************************************************
##Q1.3


-La plupart des gros objets (CircularBody et Vec2d) passent par référence constante, sauf quand il doivent être modifiés (on enlève le const pour les set). Un passage par valeur fait une copie lourde, les minimiser permet une optimisation du programme.
pour l'operateur > défini en externe, on est obligé de faire une copie puisque l'acces aux méthodes donne la posibiliter de modifier les accès privés.

*************************************************
##Q1.4


-De manière générale, on recherche les méthodes ne devant modifier aucun argument, les prédicats, comme les méthodes get dont le rôle est de retourner les attributs, les méthodes de contains et isColliding.
