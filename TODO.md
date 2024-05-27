## Stratégie 

- Faire un pattern Strategy pour changer l'algo en début de jeuu, pendant l'intro, combat avec un boss -> adopter une autre stategie (un temps qui sera différent, le boss peut te faire des dégats différents, etc)
- mob qui va se comporter différemment si y'a un boss ce genre de conneries

## Observer 

- Si le joueur a des équipments qui changent d'état en fonction de bonus/level up

## States

- Objet qui change de comportement en fonction de son état (empoisonnement)

## Flyweight 

- Utiliser pour tout : les particules d'armes (baton magique qui envoie des boules de feu, arc qui envoie des flèches), les collectibles (pièces d'or, point d'expérience), les ennemis, les arbres sur la map etc
- Permet de séparer les données identiques (sprite, couleur, vitesse) aux données propres de chaque objet (position/coordonnées)

## Builder

- Pour le joueur, on va utiliser des méthodes plutôt que d'utiliser le constructeur
- Utilisation du directeur qui va servir comme chef d'orchestre (décider de l'ordre d'instanciation des différents éléments de notre personnage)


## Composite feat Iterator 

- Potentiellement pour les menus => sous menu etc pour gérer les structures imbriqués

## Command 

- Si on est en train de faire une attaque et qu'on change de direction, on peut annuler l'attaque en cours
- Les actions du joueur = une commande

## Mediator 

- Pour le game manager, qui va servir d'intermédiaire entre les différents élements du jeu -> but étant d'eviter le couplage

# Proxy

- A méditer si on doit controler une classe 

## Memento

- Couplage avec la stratégie pour prendre des snapshots sur l'état du jeu
- Sauvegarde des états du jeu (au sens large) qu'on pourra utiliser plus tard

## Prototype

- Permet de cloner les mobs, les particules etc
- Ex : Au lieu de créer chaque vampire à partir de zéro, vous pouvez avoir un prototype pour chaque type de vampire, et chaque fois que vous avez besoin de créer un nouveau vampire, vous pouvez simplement cloner le prototype et modifier les attributs nécessaires. Cela peut vous faire gagner du temps et des ressources, surtout si la création d’un vampire est une opération coûteuse.

## Chain of Responsibility

Dans notre contexte, il peut y avoir une longue chaîne de responsabilités pour gérer différentes actions de l'utilisateur

Exemple de la Flèche du Haut :
L'Utilisateur appuie sur la touche "Flèche du Haut" sur son clavier.
Input Handler (Gestionnaire de l'entrée) reçoit cette requête.
Première Chaîne : Le gestionnaire de l'entrée traite la requête initiale. Si cette requête est une entrée valide (comme une touche de direction), il la passe au prochain gestionnaire approprié.
Handler de la Map (Gestionnaire de la carte) reçoit la requête de l'Input Handler.
Deuxième Chaîne : Le gestionnaire de la carte vérifie si l'action peut être effectuée sur la carte actuelle (par exemple, si le déplacement est possible dans la direction donnée). S'il ne peut pas traiter la requête entièrement, il la passe au prochain gestionnaire.
Handler de la Partie (Gestionnaire de la partie) reçoit la requête.
Troisième Chaîne : Ce gestionnaire traite des aspects globaux du jeu (comme vérifier si le joueur est dans un état où il peut se déplacer). Si nécessaire, il passe la requête au gestionnaire suivant.
Handler du Joueur (Gestionnaire du joueur) reçoit la requête.
Quatrième Chaîne : Enfin, le gestionnaire du joueur effectue l'action, comme déplacer le joueur vers le haut sur la carte.


## Singleton

- Ecriture dans un fichier json pour la sauvegarde de jeu -> le but étant de ne pas écrire plusieurs fois dans le fichier json


## Factory / Abstract Factory

- Factory pour les objets du jeu (armes, potions, etc)
- Abstract Factory pour les personnages (humain, elfe, orc) et les classes (mage, guerrier, assassin, archer)
- Factory Method pour les sorts (sorts de feu, sorts de glace, etc)
- 

## Decorator

- Pour les armes, on commence la partie avec une épée avec degats bruts, si l'arme lvl up on pourra utiliser un decorator FireSwordDecorator ou PoisonSwordDecorator pour la faire évoluer a travers ces décorateurs -> décorateur permet d'ajouter des capacités spéciales à un GameObject 

## Observer

- Pour les personnages, les équipements, les mobs, les objets de la map, etc -> en gros tout ce qui peut changer d'état

# Design pattern spécial Unity

## Object Pool

- Pour les particules, les ennemis, les projectiles, les objets de la map, etc
- Permet de réutiliser les objets déjà créés au lieu d'en créer de nouveaux à chaque fois, ce qui peut être coûteux en termes de performances. -> on va masquer l'objet au lieu de le détruire

dans notre cas, sa rejoint le flyweight pattern car on va réutiliser les objets déjà créés (ennemis, particules, etc) au lieu d'en créer de nouveaux à chaque fois

