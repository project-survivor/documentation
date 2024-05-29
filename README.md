# **Explications de chaque Design Pattern - Vampire Survivor**

### **Table des matières**
- [I. Pattern de création](#i-pattern-de-création)
    - [Abstract Factory](#abstract-factory)
        - [Création du personnage](#création-du-personnage)
        - [Création des équipements](#création-des-équipements)
        - [Création des sorts](#création-des-sorts)
    - [Factory Method](#factory-method)
        - [Création des armes](#création-des-armes)
- [II. Pattern structurel](#ii-pattern-structurel)
- [III.Pattern comportemental](#iii-pattern-comportemental)

# I. Pattern de création

## Abstract Factory

### Création du personnage 

Lors de la création du personnage, possibilité de choisir sa classe (mage, guerrier, assassin, archer) avec pour chacune des spécificités, ainsi que sa race (humain, elfe, orc) avec pour chacune des spécificités

> Fichier UML : [character.abstract-factory](UML/Abstract%20Factory/character.abstract-factory.plantuml)

### Création des équipements

Le joueur aura un équipement pour chacune des parties de son corps (tête, torse, jambes) et le matériel de l'armure (légère, moyenne, lourde) avec pour chacune des spécificités. 

Un magicien commencera avec un équipement léger par défaut, un guerrier avec un équipement moyen par défaut et un archer avec un équipement léger par défaut. En bref, en fonction de la classe du personnage, l'équipement de base sera différent.

Un équipement aura des statistiques (défense, vitesse, etc) qui pourront être améliorées au cours de la partie.

> Fichier UML : [equipment.abstract-factory](UML/Abstract%20Factory/equipment.abstract-factory.plantuml)


## Factory Method

### Création des armes

Le joueur aura une arme de base, et pourra en acheter ou en trouver d'autres au cours de la partie.
Les types d'armes sont : épée, arc, baguette magique

> Fichier UML : [weapon.factory-method](UML/Factory%20Method/weapon.factory-method.plantuml)

### Création des sorts

Le joueur commencera avec 1 ou 2 sorts en fonction de sa classe (mage, chasseur, et guerrier). Il pourra en apprendre d'autres au cours de la partie. En bref, si tu es Mage, cela va instancier deux sorts de Mage, etc.

> Fichier UML : [spell.factory-method](UML/Factory%20Method/spell.factory-method.plantuml)

## Création des ennemis 

Le but étant de créer différents types d'ennemis comme des zombies, des vampires ou des loups-garous en fonction du niveau ou de la zone.

> Fichier UML : [enemy.factory-method](UML/Factory%20Method/enemy.factory-method.plantuml)

# Prototype

## Clone des ennemis

Le but étant de cloner les ennemis pour éviter de les recréer à chaque fois qu'ils apparaissent. Il y a un registre qui va stocker les ennemis clonés qui permet de stocker des ennemis qui ont déjà été copiés.

> Fichier UML : [enemy.prototype](UML/Prototype/enemy.prototype.plantuml)

# II. Pattern structurel

## Decorator

### Ajouter des caractéristiques aux sorts

Pour chacun de ces sorts, un élément pourra lui être affecté afin de modifier les statistiques/caractéristiques :
- Feu
- Glace
- Terre
- Air

> Fichier UML : [spell.decorator](UML/Decorator/spell.decorator.plantuml)

# III. Pattern comportemental

