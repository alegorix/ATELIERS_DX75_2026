# Projet : Help Wanted - Entraide Communautaire

Bienvenue dans le projet **Help Wanted**. Cette plateforme est un mur d'annonces numériques conçu pour transformer le voisinage en réseau de solidarité. Les habitants peuvent y poster des demandes d'aide ou proposer leurs services.

---

## Détails de l'organisation
* **Durée :** 5 séances de 4 heures (20h au total).
* **Équipe :** Groupes de 2 à 4 personnes.
* **Stack Technique :** PHP (PDO) / MySQL / Bootstrap 5.

---

## Objectifs du workshop
L'enjeu est de construire une plateforme de mise en relation fonctionnelle :
1.  **Concevoir** une base de données gérant plusieurs catégories et types d'annonces.
2.  **Développer** un système de filtrage dynamique (catégories, type d'aide).
3.  **Gérer** des états de données (Annonce "Active" vs "Terminée").
4.  **Créer** une interface intuitive pour la publication et la consultation.

---

## Fonctionnalités Minimales

### 1. Administration (Privé)
* **Inscription & Connexion :** Identification des membres du quartier.
* **Mes Annonces :** Espace personnel pour créer, modifier ou supprimer ses publications.
* **Gestion du Statut :** Marquer une annonce comme "Aide trouvée" pour la retirer des recherches actives.

### 2. Mur d'Entraide (Public)
* **Recherche & Filtres :** Filtrage par catégorie (Bricolage, Jardinage, Cours, etc.) ou par type (Demande / Offre).
* **Fiches Détails :** Affichage complet, date de publication et contact de l'auteur.
* **Badges d'état :** Visualisation claire de l'urgence et du type de service.

---

## Planning des Livrables

### Séance 1 : La Conception
> **Note :** Zéro code autorisé au début de cette séance.
* Élaboration du **Schéma SQL**.
* **Questions clés :** * Faut-il une table séparée pour les catégories ? 
    * Comment lier une annonce à son auteur (jointures) ?
    * Quel type de champ pour gérer l'état (actif/terminé) ?



### Séance 2 à 4 : Le Développement
* **CRUD des annonces :** Création, affichage sur le mur et édition sécurisée.
* **Système de filtres :** Logique PHP pour modifier la requête SQL selon les choix de l'utilisateur.
* **Sécurité :** Vérification que seul l'auteur peut modifier sa propre annonce.
* **Design :** Intégration mobile-first avec Bootstrap 5.

### Séance 5 : Livraison & Démo
* Parcours utilisateur complet : Inscription > Publication > Filtrage.
* Explication de la gestion de l'affichage conditionnel (annonces terminées).

---

## Contraintes de Qualité
* **Sécurité :** Requêtes préparées (**PDO**) obligatoires.
* **Validation :** Empêcher la publication d'annonces vides ou sans catégorie.
* **UX (Expérience Utilisateur) :** * Bouton "Contact" propre (email ou téléphone).
    * Codes couleurs distincts : **Offres** vs **Demandes**.
    * Message d'alerte si aucun résultat ne correspond aux filtres.

---

## Analyse Visuelle & UI

### Le Mur (Landing Page)
* **Barre de filtres :** `form-select` ou boutons "Tags" pour le tri.
* **Le flux :** Grille aérée utilisant `.row-cols-1 .row-cols-md-3`.

### Les Annonces (Cards)
* **Header :** Titre et `badge rounded-pill` pour la catégorie.
* **Body :** Description courte et nom de l'auteur.
* **Footer :** Date et bouton d'action.

### Le défi PHP : Gestion des Statuts
Les annonces "Terminées" doivent être gérées via un algorithme simple dans votre boucle `foreach` :
* Soit elles disparaissent de la vue publique.
* Soit elles sont grisées avec un badge "Aide trouvée !".

---

## Astuces Bootstrap 5
| Composant | Utilité |
| :--- | :--- |
| `.form-select` | Menu de filtrage des catégories. |
| `.card` | Conteneur principal de chaque annonce. |
| `.badge` | Identifier visuellement les types (Bricolage = bleu, Jardin = vert). |
| `.alert-info` | Message "Aucune annonce trouvée". |

