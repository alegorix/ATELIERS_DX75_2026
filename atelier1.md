# Projet : MyLink-In-Bio

Bienvenue dans le projet **MyLink-In-Bio**. L'objectif est de développer une plateforme permettant aux utilisateurs de créer une page "vitrine" regroupant tous leurs liens importants (Instagram, TikTok, Portfolio, etc.).

---

## Détails de l'organisation
* **Durée :** 5 séances de 4 heures (20h au total).
* **Équipe :** Groupes de 2 à 4 personnes.
* **Stack Technique :** PHP (PDO) / MySQL / Bootstrap 5.

---

## Objectifs de l'atelier
L'enjeu est de construire un produit complet et fonctionnel :
1.  **Concevoir** la structure de données (Base de données).
2.  **Développer** un espace membre sécurisé.
3.  **Créer** un outil de personnalisation visuelle.
4.  **Assurer** un affichage fluide sur mobile (**Mobile-First**).

---

## Fonctionnalités Minimales

### 1. Administration (Privé)
* **Inscription & Connexion :** Sécurisation des accès.
* **Gestion des liens (CRUD) :** Ajouter, modifier, supprimer des liens (Titre + URL + Icône).
* **Personnalisation :** Modifier la couleur des boutons et le style de l'arrière-plan.
* **Profil :** Mise à jour du nom d'utilisateur et de la biographie.

### 2. Page Publique (Le Rendu)
* **Accessibilité :** Via une URL dynamique (ex: `profile.php?u=mon_pseudo`).
* **Affichage dynamique :** Chargement des liens depuis la base de données.
* **Rendu en temps réel :** Application immédiate du thème choisi par l'utilisateur.

---

## Planning des Livrables

### Séance 1 : La Conception
> **Note :** Zéro code autorisé au début de cette séance.
* Élaboration du **Schéma de Base de Données** (SQL).
* *Questions clés :* Quelles tables ? Quelles relations ? Quels types de champs (`INT`, `VARCHAR`, `TEXT`) ?

### Séance 2 à 4 : Le Développement
* Mise en place du **CRUD** (Create, Read, Update, Delete).
* Gestion des **sessions PHP**.
* Intégration du design avec **Bootstrap 5**.

### Séance 5 : Livraison & Démo
* Présentation du projet final.
* Démonstration des parties "Admin" et "Publique".
* Explication de la structure de données.

---

## Contraintes de Qualité
* **Sécurité :** Zéro injection SQL (utilisation de **PDO** et requêtes préparées).
* **Propreté :** Pas de mots de passe en clair (utilisation obligatoire de `password_hash`).
* **UX :** Gestion des messages d'alerte clairs (mauvais mot de passe, champs vides).
* **Autonomie :** Exploitation de la documentation officielle.

---

## Analyse Visuelle & UI

### Le Header (En-tête)
* **Photo de profil :** Circulaire (défi : upload d'image ou icône par défaut).
* **Nom d'utilisateur :** (ex: `@MonPseudo`).
* **Bio :** Courte description textuelle.

### Les Boutons de Liens
Chaque bouton correspond à une ligne de la table `links`.
* **Design :** Coins arrondis, bordures fines ou ombres (`shadow-sm`).
* **Interactivité :** Effet de survol (`hover`) pour dynamiser l'expérience.

### Personnalisation (Le défi PHP)
L'administrateur doit pouvoir modifier :
* Le fond (couleur unie, dégradé ou image).
* La lisibilité (contraste texte/boutons).

### Astuces Bootstrap 5
| Classe | Utilité |
| :--- | :--- |
| `.container-fluid` | Avec `max-width: 500px` pour l'effet mobile sur bureau. |
| `.rounded-pill` | Pour des boutons style "pilule". |
| `.d-grid .gap-3` | Pour espacer proprement les liens. |
| `.vh-100` | Pour que l'arrière-plan couvre tout l'écran. |

---

> **Conseil de départ :** Ne commencez pas par le design. Assurez-vous d'abord que les données circulent correctement entre vos formulaires et votre base de données. **Le "beau" vient après le "fonctionnel".**
