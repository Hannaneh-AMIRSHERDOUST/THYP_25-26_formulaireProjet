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

## Diagramme Entité-Relation
```mermaid
erDiagram
    PROJECT {
        int id
        string nom
        string description
        string technologies
        string niveau
    }
    USER {
        int id
        string nom
        string email
    }
    PROJECT ||--o{ USER : "assigné à"
