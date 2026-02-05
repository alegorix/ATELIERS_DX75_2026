# Projet : FeelGood - Mood Tracker

Bienvenue dans le projet **FeelGood**. L'objectif est de concevoir une application de "Self-Care" permettant aux utilisateurs de suivre leur état émotionnel au quotidien, d'analyser leurs tendances et de visualiser leur bien-être via des statistiques dynamiques.

---

## Détails de l'organisation
* **Durée :** 5 séances de 4 heures (20h au total).
* **Équipe :** Groupes de 2 à 4 personnes.
* **Stack Technique :** PHP (PDO) / MySQL / Bootstrap 5.

---

## Objectifs de l'atelier
L'enjeu est de construire un outil de suivi de données (**Tracking**) complet :
1.  **Concevoir** une base de données gérant l'historique temporel.
2.  **Développer** une logique métier (limite d'une seule saisie par jour).
3.  **Calculer** des statistiques dynamiques (moyennes, pourcentages).
4.  **Adapter** l'interface visuelle en fonction des données enregistrées.

---

## Fonctionnalités Minimales

### 1. Administration (Privé)
* **Inscription & Connexion :** Accès sécurisé au journal personnel.
* **Saisie du jour :** Sélection de l'humeur (échelle de 1 à 5) et rédaction d'une note.
* **Historique :** Consulter, modifier ou supprimer (CRUD) les notes passées.
* **Tableau de bord :** Visualisation des statistiques (ex: humeur moyenne).

### 2. Visualisation (Le Rendu)
* **Timeline :** Affichage chronologique des humeurs enregistrées.
* **Thème Dynamique :** L'interface change de couleur selon l'humeur du jour ou la moyenne hebdomadaire.
* **Indicateurs :** Graphiques simples ou barres de progression (ex: % de journées positives).

---

## Planning des Livrables

### Séance 1 : La Conception
> **Note :** Zéro code autorisé au début de cette séance.
* Dessin du **Schéma SQL**.
* **Réflexion technique :** * Comment empêcher deux saisies le même jour ? 
    * Quel type de champ pour la date (`DATE`, `DATETIME`, `TIMESTAMP`) ?
    * Comment lier l'humeur à l'utilisateur ?



### Séance 2 à 4 : Le Développement
* **CRUD complet :** Enregistrement et gestion des notes.
* **Logique de contrôle :** Vérifier en PHP si l'utilisateur a déjà posté aujourd'hui avant d'afficher le formulaire.
* **Calculs :** Fonctions PHP pour extraire les moyennes de la base.
* **Design :** Intégration Bootstrap 5.

### Séance 5 : Livraison & Démo
* Présentation du projet final.
* **Démonstration du mode dynamique :** Passage du mode "triste" au mode "joyeux".
* Explication de la requête SQL la plus complexe ou du script de calcul de moyenne.

---

## Contraintes de Qualité
* **Sécurité :** Requêtes préparées (**PDO**) obligatoires.
* **Confidentialité :** Un utilisateur ne doit jamais pouvoir accéder au journal d'un autre (filtrage par `user_id`).
* **UX (Expérience Utilisateur) :** * Ne pas afficher de formulaire vide si la saisie est déjà faite.
    * Formatage des dates (ex: "Lundi 12 Mars" au lieu de "2026-03-12").

---

## Analyse Visuelle & UI

### Le Dashboard (Saisie)
* **Sélecteurs :** 5 boutons cliquables (Emojis/Icônes).
* **Champ texte :** Un `textarea` pour le ressenti personnel.

### La Timeline (Historique)
* **Composants :** Utilisation des `.card` Bootstrap.
* **Badges :** Couleurs sémantiques selon le score (ex: Rouge pour 1/5, Vert pour 5/5).

### Le défi PHP : Personnalisation Dynamique
* **L'Algorithme :** * Moyenne basse > Tons froids/apaisants (bleu, gris).
    * Moyenne haute > Tons vifs/chaleureux (jaune, orange).

### Astuces Bootstrap 5
| Composant | Utilité |
| :--- | :--- |
| `.card` | Structurer les notes du journal. |
| `.progress` | Afficher les statistiques de bonheur du mois. |
| `.btn-group` | Aligner proprement les 5 choix d'humeur. |
| `.text-center` | Garder une interface zen et épurée. |

---

> 💡 **Conseil de départ :** Concentrez-vous d'abord sur la **requête SQL** qui vérifie si une entrée existe déjà pour la date du jour. C'est le cœur de votre logique métier.

---
*Projet créé dans le cadre de l'atelier FeelGood - Mood Tracker.*
