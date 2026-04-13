# Projet décisionnel – Crédit Breton

**Analyse des demandes de prêts immobiliers avec Power BI**

---

## Présentation du projet

Ce projet est né d’une réflexion simple : comment aider des conseillers bancaires à prendre des décisions plus rapides et plus fiables concernant l’octroi de crédits immobiliers ?

Pour y répondre, j’ai travaillé sur un cas fictif inspiré d’un réseau bancaire appelé *Crédit Breton*. L’idée était de partir de données brutes issues d’un fichier Excel et de construire un **outil d’aide à la décision** sous Power BI.

L’objectif n’était pas seulement technique, mais aussi métier : comprendre les critères de décision et les traduire en indicateurs clairs.

---

## Objectifs

À travers ce projet, j’ai cherché à :

* Réduire le temps nécessaire pour analyser un dossier de prêt
* Améliorer la qualité et la cohérence des données
* Mettre en place des indicateurs simples pour piloter l’activité
* Apporter une première aide à la décision grâce à un score emprunteur

---

## Démarche

Le projet s’est déroulé en plusieurs étapes.

### 1. Nettoyage des données

J’ai commencé par analyser le fichier source (Excel), dans lequel plusieurs incohérences étaient présentes :

* valeurs aberrantes (ex : nombre d’enfants très élevé)
* catégories non harmonisées (ex : “PACS” / “Pacsé”)
* formats de dates différents

J’ai donc utilisé Power Query pour corriger et structurer ces données.

---

### 2. Réflexion métier

Avant de construire le dashboard, j’ai essayé de me mettre à la place d’un conseiller bancaire.

Je me suis posé la question :
*Quels éléments sont vraiment importants pour décider d’accorder un prêt ?*

Cela m’a permis de structurer l’analyse autour de :

* la situation financière
* la stabilité des revenus
* la capacité de remboursement

---

### 3. Mise en place d’un score emprunteur

J’ai ensuite créé un indicateur permettant de simplifier la prise de décision.

Ce score repose sur quelques règles simples :

* refus si l’âge + durée du prêt dépasse un certain seuil
* refus si les revenus sont trop irréguliers
* vérification de la capacité de remboursement mensuelle

L’objectif est d’avoir une première lecture rapide du risque associé à un dossier.

---

### 4. Création du dashboard Power BI

Le tableau de bord est structuré en plusieurs pages :

#### Indicateurs clients

* suivi des montants de prêts (accordés, refusés, en cours)
* moyenne des montants
* alerte visuelle pour les montants élevés
* filtres temporels pour analyser l’évolution
![Indicateurs](docs/screenshots/Indicateurs%20client.png)

#### Performance des agences

* carte des agences
* nombre de demandes par agence
* classement des agences
* taux d’acceptation
![Performance](docs/screenshots/Performance%20agences.png)

#### Analyse socio-professionnelle

* évolution des demandes selon la catégorie socio-professionnelle

#### Liste détaillée

* accès aux dossiers clients avec filtres pour une analyse plus fine

---

## Outils utilisés

* **Power BI Desktop** (visualisation et modélisation)
* **Power Query** (nettoyage et transformation)
* **DAX** (calcul des indicateurs et du score)
* **Excel** (source de données)

---

## Structure du projet

* `/data` : données sources
* `/pbix` : fichier Power BI
* `/docs` : captures d’écran + rapport détaillé

---