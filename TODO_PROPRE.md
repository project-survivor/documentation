## Singleton

### Utilité
Le pattern Singleton garantit qu'une classe n'a qu'une seule instance et fournit un point d'accès global à cette instance.

### Pertinence et Exemple
Dans un jeu comme "Vampire Survivor", il peut être utilisé pour les gestionnaires de ressources partagées telles que :
- **Gestionnaire de ressources** : Pour charger et gérer les textures, sons et autres ressources de manière centralisée.
- 🟨 **Gestionnaire de configuration** : Pour lire et écrire des paramètres de jeu à partir d'un fichier JSON ou d'une base de données.
- **Gestionnaire de scènes** : Pour contrôler la transition entre différentes scènes du jeu, comme le menu principal et les niveaux du jeu.

## Factory Method

### Utilité
Le pattern Factory Method définit une interface pour créer un objet, mais laisse les sous-classes décider de la classe à instancier.

### Pertinence et Exemple
- ✅ **Création d'ennemis** : Par exemple, un `EnemyFactory` pourrait créer différents types d'ennemis comme des zombies, des vampires ou des loups-garous en fonction du niveau ou de la zone.
- ✅ **Création de sorts / projectiles** : Une `SpellFactory` pourrait créer différents types de sorts (flèches, boules de feu, etc.) utilisés par les personnages ou ennemis.

## Abstract Factory

### Utilité
Le pattern Abstract Factory fournit une interface pour créer des familles d'objets liés ou dépendants sans spécifier leurs classes concrètes.

### Pertinence et Exemple
- ✅ **Création de personnages** : Une Abstract Factory pourrait être utilisée pour créer des personnages (humain, elfe, orc) et leurs équipements (épée, bouclier, armure) de manière cohérente.
- **Environnements de jeu** : Pour créer des ensembles d'éléments d'environnement (arbres, bâtiments, obstacles) adaptés à différents thèmes (forêt, désert, ville).

## Builder

### Utilité
Le pattern Builder sépare la construction d'un objet complexe de sa représentation afin que le même processus de construction puisse créer différentes représentations.

### Pertinence et Exemple
- 🟨 **Création de personnages complexes** : Utiliser un `CharacterBuilder` pour créer un personnage avec des attributs comme la force, l'agilité, les compétences, et les équipements, en permettant de construire l'objet étape par étape.
- 🟨 **Construction de niveaux** : Un `LevelBuilder` pourrait assembler des niveaux de jeu complexes en ajoutant des ennemis, des objets, et des décorations de manière structurée.

## Prototype

### Utilité
Le pattern Prototype spécifie les types d'objets à créer en utilisant une instance prototype et crée de nouveaux objets en copiant ce prototype.

### Pertinence et Exemple
- ✅ **Clonage d'ennemis** : Pour créer rapidement des ennemis similaires sans répéter le processus d'initialisation. Par exemple, un prototype de vampire pourrait être cloné pour créer de nouveaux vampires avec des attributs légèrement modifiés.
- **Création d'objets magiques** : Des objets comme des potions ou des armes magiques peuvent être clonés à partir de prototypes avec des variations minimes.

## Adapter

### Utilité
Le pattern Adapter permet à des interfaces incompatibles de travailler ensemble en convertissant l'interface d'une classe en une interface attendue par les clients.

### Pertinence et Exemple
- **Intégration de bibliothèques tierces** : Utiliser un Adapter pour intégrer une bibliothèque de physique externe qui n'a pas la même interface que le reste du code du jeu.
- **Compatibilité des contrôleurs** : Adapter différentes API de contrôleurs de jeu pour les rendre compatibles avec l'interface du jeu.

## Bridge

### Utilité
Le pattern Bridge sépare une abstraction d'une implémentation afin qu'elles puissent évoluer indépendamment.

### Pertinence et Exemple
- **Systèmes de rendu et de plateforme** : Séparer l'interface de rendu du jeu de son implémentation spécifique à une plateforme (Windows, macOS, consoles), permettant ainsi de changer ou d'étendre l'implémentation sans modifier l'abstraction.
- **Interface utilisateur** : Séparer la logique de l'interface utilisateur de son rendu graphique pour pouvoir facilement changer l'apparence sans toucher à la logique.

## Composite

### Utilité
Le pattern Composite permet de composer des objets en structures arborescentes pour représenter des hiérarchies de parties et de tout.

### Pertinence et Exemple
- **Gestion des objets de la scène** : Par exemple, des groupes d'ennemis ou des structures de menus imbriqués peuvent être traités de manière uniforme en utilisant des composites.
- **Système de particules** : Gérer des systèmes de particules où chaque système peut contenir plusieurs émetteurs de particules.

## Decorator

### Utilité
Le pattern Decorator attache dynamiquement des responsabilités supplémentaires à un objet. Il fournit une alternative flexible à la sous-classes pour étendre les fonctionnalités.

### Pertinence et Exemple
- 🟨 **Amélioration des armes** : Par exemple, une épée de base peut être décorée avec des capacités supplémentaires comme des dégâts de feu ou de poison en utilisant des décorateurs comme `FireSwordDecorator` ou `PoisonSwordDecorator`.
- 🟨 **Personnalisation des personnages** : Ajouter des décorateurs pour des compétences ou des pouvoirs spéciaux sans modifier la classe de base du personnage.

## Façade

### Utilité
Le pattern Façade fournit une interface unifiée à un ensemble d'interfaces dans un sous-système. Il définit une interface de haut niveau qui rend le sous-système plus facile à utiliser.

### Pertinence et Exemple
- **Gestion de la complexité du système** : Utiliser une façade pour simplifier l'interaction avec des sous-systèmes complexes comme le rendu graphique, la gestion des entrées, ou l'accès aux ressources.
- **Interface de services** : Une façade pourrait unifier l'accès aux services de jeu en ligne, comme la connexion, le matchmaking et les scores.

## Flyweight

### Utilité
Le pattern Flyweight utilise le partage pour prendre en charge efficacement un grand nombre d'objets de granularité fine.

### Pertinence et Exemple
- 🟨 **Optimisation des ressources** : Utiliser des flyweights pour des objets fréquents comme des particules, des collectibles (pièces d'or, points d'expérience), et des ennemis pour minimiser la consommation de mémoire en partageant les données communes.
- 🟨 **Textures et sprites** : Réutiliser les mêmes textures pour plusieurs instances d'objets visuels.


## Proxy

### Utilité
Le pattern Proxy fournit un substitut ou un placeholder pour un autre objet afin de contrôler l'accès à celui-ci.

### Pertinence et Exemple
- **Contrôle d'accès** : Utiliser un proxy pour gérer l'accès à des objets gourmands en ressources, comme des objets de jeu lourds en mémoire, ou pour ajouter des fonctionnalités de sécurité.
- **Chargement paresseux** : Retarder le chargement d'objets volumineux jusqu'à ce qu'ils soient réellement nécessaires.

## Observer

### Utilité
Le pattern Observer définit une relation de dépendance un-à-plusieurs entre des objets, de sorte que lorsque l'un des objets change d'état, tous ses dépendants en sont informés et mis à jour automatiquement.

### Pertinence et Exemple
- **Système d'événements** : Pour gérer les notifications de changement d'état des objets de jeu, comme les équipements qui changent en fonction des bonus ou les personnages qui réagissent aux changements de l'environnement.
- **Interface utilisateur** : Mettre à jour les éléments de l'interface utilisateur en réponse à des événements du jeu, comme les changements de score ou de santé.

## Strategy

### Utilité
Le pattern Strategy définit une famille d'algorithmes, encapsule chaque algorithme et les rend interchangeables. Le pattern Strategy permet à l'algorithme de varier indépendamment des clients qui l'utilisent.

### Pertinence et Exemple
- 🟨 **Comportements des ennemis** : Permettre aux ennemis d'adopter différentes stratégies de combat ou de déplacement en fonction de leur situation (par exemple, en combat de boss ou en patrouille).
- 🟨 **Gestion des armes** : Utiliser différentes stratégies de tir pour des armes variées (tir en ligne droite, tir en éventail, etc.).

## Command

### Utilité
Le pattern Command encapsule une requête en tant qu'objet, permettant de paramétrer les clients avec des files d'attente, des demandes et des opérations réversibles.

### Pertinence et Exemple
- **Actions du joueur** : Encapsuler les actions du joueur (attaquer, déplacer, utiliser un objet) en commandes, permettant de les mettre en file d'attente, de les annuler ou de les répéter.
- **Système de tutoriel** : Enregistrer et rejouer des actions pour guider le joueur à travers les étapes du tutoriel.

## State

### Utilité
Le pattern State permet à un objet de modifier son comportement lorsque son état change. Il apparaît comme si l'objet changeait de classe.

### Pertinence et Exemple
- **États des personnages** : Gérer les états d'un personnage comme normal, empoisonné, enragé, etc., en modifiant son comportement en fonction de son état actuel.
- **Phases de niveau** : Gérer les différentes phases d'un niveau de jeu (exploration, combat, boss) en changeant l'état de la scène.

## Memento

### Utilité
Le pattern Memento capture et externalise l'état interne d'un objet sans violer l'encapsulation, permettant à l'objet de revenir à cet état plus tard.

### Pertinence et Exemple
- **Sauvegarde des états du jeu** : Permettre de sauvegarder l'état du jeu à des moments critiques et de restaurer cet état plus tard, par exemple pour des fonctionnalités de sauvegarde/chargement ou de retour en arrière.
- **Undo/Redo** : Permettre aux joueurs d'annuler ou de rétablir leurs actions dans des interfaces complexes ou des puzzles.

## Mediator

### Utilité
Le pattern Mediator définit un objet qui encapsule la façon dont un ensemble d'objets interagit. Le Mediator favorise la faible connexion en évitant que les objets se réfèrent explicitement les uns aux autres.

### Pertinence et Exemple
- **Gestionnaire de jeu** : Un `Game Manager` pourrait servir de médiateur pour gérer les interactions entre les différents systèmes du jeu (système de combat, IA, gestion des ressources), évitant ainsi le couplage direct entre eux.
- **Système de dialogue** : Gérer les interactions entre différents personnages dans un jeu de dialogue complexe.

## Chain of Responsibility

### Utilité
Le pattern Chain of Responsibility évite de coupler l'expéditeur d'une requête à son destinataire en donnant à plus d'un objet la possibilité de traiter la requête. Il enchaîne les objets récepteurs et passe la requête le long de la chaîne jusqu'à ce qu'un objet la traite.

### Pertinence et Exemple
- **Gestion des entrées** : Traiter les entrées du joueur à travers une chaîne de gestionnaires, où chaque gestionnaire vérifie et traite la requête ou la passe au suivant (par exemple, gestion des déplacements, des interactions avec les objets, des attaques).
- **Traitement des événements** : Gérer les événements de jeu (collisions, déclenchements de pièges) en passant l'événement à travers une chaîne de gestionnaires.

## Template Method

### Utilité
Le pattern Template Method définit le squelette d'un algorithme dans une méthode, en déléguant certaines étapes aux sous-classes. Le Template Method permet aux sous-classes de redéfinir certaines étapes de l'algorithme sans changer la structure de l'algorithme.

### Pertinence et Exemple
- **IA des ennemis** : Définir un algorithme générique pour le comportement des ennemis avec des étapes spécifiques comme "détecter le joueur", "se déplacer vers le joueur", et "attaquer", que les sous-classes peuvent redéfinir.
- **Génération de niveaux** : Définir un processus de génération de niveaux avec des étapes comme "placer les ennemis", "placer les obstacles", et "ajouter les trésors", que les sous-classes peuvent personnaliser.

## Iterator

### Utilité
Le pattern Iterator fournit un moyen d'accéder séquentiellement aux éléments d'un agrégat sans exposer sa représentation sous-jacente.

### Pertinence et Exemple
- **Parcours des collections** : Utiliser un itérateur pour parcourir des collections d'objets de jeu, comme des listes d'ennemis, des items dans l'inventaire, ou des éléments de la carte.
- **Système de dialogue** : Parcourir les lignes de dialogue d'une conversation entre personnages.

