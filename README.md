# Projet Hypermédias

## Description du projet
Notre projet consiste à développer une **application hypermédia** pour gérer et visualiser des projets.  
Chaque projet contient les informations suivantes, comme demandé dans le formulaire :

- **Nom du projet**  
- **Description**  
- **Technologies utilisées**  
- **Niveau** (débutant / intermédiaire / avancé)  

L'utilisateur peut **ajouter un nouveau projet via un formulaire** et voir tous les projets affichés sur la page principale.  
Les données peuvent être stockées dans **localStorage** ou adaptées pour une base SQL.

---

## Diagramme combiné : Données et Workflow
```mermaid
graph TD
    subgraph Data [Données]
        PROJECT[Project: id, nom, description, technologies, niveau]
        USER[User: id, nom, email]
        PROJECT -->|est assigné à| USER
    end

    subgraph Workflow [Processus]
        A[Formulaire rempli] --> B[Validation des données]
        B --> C[Enregistrement du projet]
        C --> D[Affichage sur la page principale]
    end

    PROJECT --> C
