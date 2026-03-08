# Système de Veille Automatisée (n8n + Docker)

Ce projet permet de récupérer les actualités Data & IA via 5 flux RSS et de les envoyer sur Discord.

## Contenu du projet
- **docker-compose.yml** : Configuration de l'infrastructure n8n.
- **workflow-veille.json** : Logique n8n (RSS -> Filter 24h -> Discord Embed).

## Installation
1. Lancer avec `docker-compose up -d`.
2. Importer le fichier JSON dans n8n.
