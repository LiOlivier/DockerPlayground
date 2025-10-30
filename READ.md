# Docker Playground

## Services
- Application Django (mini_blog) : http://localhost:8000
- Prometheus : http://localhost:9090
- Grafana : http://localhost:3000 (admin/admin)
- cAdvisor : http://localhost:8082
- Adminer (UI Postgres) : http://localhost:8081
- Telegraf (endpoint Prometheus) : http://localhost:9273/metrics

## Démarrage rapide
1) Construire et démarrer le conteneur Django
   - docker compose build mini_blog
   - docker compose up -d mini_blog
   
2) Démarrer le reste de la stack
   - docker compose up -d

## Notes
- Le conteneur Django utilise SQLite par défaut et exécute les migrations au démarrage.
- Prometheus scrute par défaut cAdvisor, Grafana et Telegraf (voir l’onglet Targets dans Prometheus).
- Pour un usage production, préférer gunicorn derrière Nginx et configurer les fichiers statiques.
