# Boilerplated Organisation

> **Concevoir des composants logiciels et des processus atomiques, réutilisables et adaptables à différents contextes métier.**

---

## À propos

**Boilerplated Organisation** est une organisation dédiée à la conception et au développement de solutions logicielles sur mesure.

Notre équipe est actuellement composée de **trois développeurs et d’un manager**, avec une approche de travail fondée sur trois principes essentiels :

* **Rigueur technique**
* **Autonomie**
* **Esprit critique**

Nous encourageons chaque membre de l’équipe à challenger les choix techniques, fonctionnels et organisationnels lorsqu’une meilleure approche peut être proposée.

La qualité de nos solutions repose autant sur la capacité à exécuter que sur celle à remettre en question les hypothèses initiales.

---

## Notre approche

Nous développons des applications répondant aux besoins spécifiques de nos clients.

Cependant, de nombreux processus métiers reposent sur des problématiques similaires : gestion documentaire, authentification, workflows, notifications, administration, reporting, gestion des utilisateurs, etc.

Notre objectif est donc de transformer progressivement ces fonctionnalités communes en **composants logiciels autonomes, génériques et réutilisables**.

Cette approche permet de :

* réduire le temps de développement des futurs projets ;
* limiter la duplication de code ;
* standardiser les bonnes pratiques techniques ;
* améliorer la maintenabilité des applications ;
* accélérer la livraison de nouvelles solutions ;
* capitaliser sur les développements réalisés pour chaque client.

Chaque projet doit ainsi contribuer progressivement à enrichir notre bibliothèque interne de composants et de solutions réutilisables.

---

## Organisation des projets

Chaque client dispose de son propre environnement applicatif, généralement organisé autour d’un **hub regroupant plusieurs applications indépendantes**.

Nous privilégions actuellement une architecture basée sur des **repositories séparés** plutôt qu’un monorepo.

Une structure type peut être représentée ainsi :

```text
Client
│
├── Hub
│
├── Application A
├── Application B
├── Application C
└── ...
```

Chaque application dispose de son propre repository et doit pouvoir évoluer de manière aussi indépendante que possible.

---

## Documentation

Chaque repository doit progressivement intégrer une documentation structurée permettant aussi bien la maintenance technique que la transmission de connaissances.

La documentation cible comprend notamment :

```text
README.md
├── Présentation du projet
├── Installation
├── Architecture
└── Utilisation générale

docs/
├── technical/
│   └── Documentation technique
│
├── user/
│   └── Manuel utilisateur
│
└── business/
    └── Présentation fonctionnelle et commerciale
```

L’objectif est qu’un nouveau membre de l’équipe puisse comprendre rapidement :

1. **Pourquoi l’application existe**
2. **Quel problème elle résout**
3. **Comment elle fonctionne**
4. **Comment l’installer**
5. **Comment la maintenir**
6. **Comment la présenter à un client**

---

## Standardisation et boilerplates

L’organisation travaille actuellement à la définition de ses standards internes.

À terme, chaque nouveau projet devra pouvoir être initialisé à partir d’un **boilerplate officiel** intégrant notamment :

* la structure standard du repository ;
* la configuration du frontend ;
* la configuration du backend ;
* la connexion à la base de données ;
* Docker et Docker Compose ;
* les conventions de développement ;
* les tests ;
* la documentation ;
* les variables d’environnement ;
* les mécanismes de CI/CD ;
* les standards de sécurité.

La création et l’amélioration de ces boilerplates font partie intégrante du travail d’industrialisation de l’organisation.

---

## Stack technique

Notre stack de référence est actuellement la suivante :

| Couche                   | Technologie                               |
| :----------------------- | :---------------------------------------- |
| **Frontend**             | React + TypeScript                        |
| **Backend**              | FastAPI + Python                          |
| **Base de données**      | PostgreSQL                                |
| **Conteneurisation**     | Docker / Docker Compose                   |
| **Infrastructure Cloud** | AWS — architecture en cours de définition |

Cette stack constitue notre base commune. Des technologies complémentaires peuvent être introduites lorsqu’elles répondent à une justification technique ou métier claire.

---

## Principes de développement

### 1. Réutilisabilité

Avant de développer une nouvelle fonctionnalité, vérifier si un composant existant peut être :

* réutilisé ;
* adapté ;
* généralisé ;
* extrait d’un projet existant.

L’objectif n’est pas uniquement de résoudre le problème du projet actuel, mais également d’identifier ce qui pourrait servir aux projets suivants.

### 2. Atomicité

Lorsque cela est pertinent, les fonctionnalités doivent être conçues comme des composants aussi indépendants que possible.

Une brique réutilisable doit idéalement :

* répondre à un besoin clairement défini ;
* limiter ses dépendances ;
* exposer une interface explicite ;
* être documentée ;
* pouvoir être testée indépendamment.

### 3. Simplicité

Nous privilégions les solutions simples, lisibles et maintenables.

Une architecture complexe doit être justifiée par un besoin réel et non par une préférence technologique.

### 4. Esprit critique

Les décisions techniques peuvent et doivent être challengées.

Toute proposition alternative est bienvenue lorsqu’elle améliore au moins un des éléments suivants :

* simplicité ;
* performance ;
* sécurité ;
* maintenabilité ;
* expérience utilisateur ;
* vitesse de développement ;
* réutilisabilité.

---

## Démarrage d’un projet

### Prérequis

L’environnement de développement nécessite généralement :

* **Node.js** — version LTS recommandée ;
* **Python 3.11+** ;
* **Docker** ;
* **Docker Compose** ;
* **Git**.

Selon le projet, des dépendances supplémentaires peuvent être précisées dans son propre `README.md`.

### Cloner le repository

```bash
git clone <repository-url>
cd <repository-name>
```

### Configurer l’environnement

Lorsque le projet utilise un fichier d’exemple :

```bash
cp .env.example .env
```

Configurer ensuite les variables nécessaires conformément à la documentation du projet.

### Lancer l’application

La majorité des projets conteneurisés peuvent être démarrés avec :

```bash
docker compose up --build
```

Pour arrêter les services :

```bash
docker compose down
```

---

## Culture d’ingénierie

Nous cherchons à construire une organisation capable de **capitaliser sur chaque projet réalisé**.

Un développement n’est donc pas considéré uniquement comme une livraison client.

Il peut également devenir :

* un composant réutilisable ;
* un boilerplate ;
* une amélioration de notre architecture ;
* une nouvelle convention ;
* une documentation ;
* un outil interne ;
* une automatisation ;
* ou une nouvelle capacité proposée aux futurs clients.

Notre objectif à long terme est simple :

> **Ne pas reconstruire deux fois ce qui peut être correctement conçu une seule fois.**
