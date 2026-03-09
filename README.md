# Système de Veille Automatisée (Data & IA)

Infrastructure de collecte et d'analyse d'actualités technologiques basée sur n8n et Docker.

## Description du projet

Ce système automatise la surveillance de sources d'informations spécialisées en Data Science et Intelligence Artificielle. Le projet a évolué d'un simple agrégateur vers une solution d'analyse sémantique.

### Phase 1 : Collecte et filtrage (RSS)
* Monitoring de 5 flux RSS ciblés.
* Filtrage temporel des données pour assurer une rétention sur 24 heures.
* Routage des flux bruts vers un webhook Discord.

### Phase 2 : Analyse et enrichissement (IA)
* Intégration d'un moteur d'analyse LLM (NVIDIA/OpenRouter).
* Génération automatique de synthèses pour chaque article.
* Classification par niveau de priorité : CRITIQUE, IMPORTANT, INFO.
* Traitement des données via un script JavaScript pour assurer la validité du format JSON et la gestion des erreurs de l'IA.
* Mise en forme des données en Embeds Discord avec code couleur dynamique.



## Architecture technique

* **docker-compose.yml** : Orchestration des conteneurs pour l'instance n8n.
* **workflow-veille.json** : Logique complète du workflow (Noeuds RSS, LLM, Code, HTTP Request).

## Installation

1. Déployer l'infrastructure :
   `docker-compose up -d`

2. Configuration du workflow :
   * Importer le fichier `workflow-veille.json` dans l'interface n8n.
   * Configurer les credentials pour le modèle de langage (API Key).
   * Renseigner l'URL du webhook dans le noeud de destination Discord.

## Technologies utilisées

* n8n (Auto-hébergé)
* Docker & Docker Compose
* LLM (Analyse textuelle)
* JavaScript (Normalisation des données)
Docker & Docker Compose

LLM (Analyse textuelle)

JavaScript (Normalisation des données)
