joueur : collecter ressources -> bois et pierre

Factory method Unité et Batiment : 
    - Unité : péon, épéiste, unité élite
    - Batiment : forum, caserne, chateau, labo

State : état vaincu pour joueur

Composite : terrain de jeu :
    - Leaf : ressource
    - Composite: espace de terre

Decorator : amélioration des épéistes avec chaine responsabilité pour "pas possible de lancer la 2ème amélioration avant la 1ère, ni la 3ème avant la 2ème."

Flyweight : reduire la mémoirre sur les unités

Observer: 
    - Tenir au courant des ressources colléctés


Créer une classe bois et pierre et ressources
Créer une classe joueur

----

# Points a discuter 

- est-ce que le context de notre state va sur la classe Joueur ou celui du forum ?

----

. Factory Method pour les unités et les bâtiments
Utiliser le Factory Method pour créer des unités et des bâtiments est une bonne idée. Cela permet de centraliser la logique de création, ce qui facilite l'ajout de nouvelles unités ou bâtiments et garantit que les objets sont créés de manière cohérente.

2. State pour l'état vaincu d'un joueur
Le pattern State est approprié pour gérer l'état d'un joueur, en particulier pour représenter l'état vaincu. Ce pattern permet de changer le comportement d'un objet en modifiant son état interne sans utiliser de conditions complexes.

3. Composite pour le terrain de jeu
Le pattern Composite pour représenter le terrain de jeu est une bonne approche. Il permet de traiter les ressources et les espaces de terre de manière uniforme. Cela facilite la gestion et la navigation dans la structure du terrain.

4. Decorator pour l'amélioration des épéistes avec Chain of Responsibility
Combiner Decorator avec Chain of Responsibility pour les améliorations des épéistes est astucieux. Le Decorator permet d'ajouter des fonctionnalités dynamiquement, tandis que la Chain of Responsibility impose un ordre séquentiel pour les améliorations. Cela respecte la contrainte de ne pas pouvoir appliquer la deuxième amélioration avant la première, ni la troisième avant la deuxième.

5. Flyweight pour réduire la mémoire sur les unités
Le pattern Flyweight est idéal pour réduire l'utilisation de la mémoire lorsqu'il y a beaucoup d'instances similaires, comme les unités dans un jeu de stratégie. Il permet de partager les états communs entre plusieurs objets, réduisant ainsi la consommation de mémoire.

6. Observer pour les ressources collectées
Le pattern Observer est bien adapté pour suivre les ressources collectées par les unités. Cela permet de notifier automatiquement les parties intéressées (comme l'interface utilisateur) lorsque des ressources sont collectées, assurant ainsi une mise à jour en temps réel.