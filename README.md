# 🏥 SeniorAssist — Surveillance Santé par n8n

Système complet de supervision pour personnes âgées, construit avec n8n. Combine surveillance vidéo (Frigate), alertes en temps réel, gestion patients et rapports automatisés.

## 🏗️ Architecture

```
📷 Caméra RTSP → Frigate → n8n → 🚨 Alerte Telegram
                              → 📊 Dashboard soignants
                              → 📋 Rapport journalier/hebdo
```

## 📋 Workflows (15)

| Workflow | Description |
|----------|-------------|
| API Patients | CRUD patients via REST API |
| API Rapports | Gestion et consultation des rapports |
| API Événements | Enregistrement des événements de vie |
| Absence Anormale | Détection d'absence prolongée inhabituelle |
| Actions Portail | Actions déclenchées depuis le portail soignants |
| Alertes Temps Réel | Notification immédiate sur événements critiques |
| Camera Proxy | Proxy flux RTSP caméra |
| Dashboard Supervision | Interface de surveillance globale |
| Détection Chute | IA de détection de chute via analyse vidéo |
| Interface Web | Portail web principal |
| Log Événements | Journalisation de tous les événements |
| Portail Soignants | Interface dédiée au personnel soignant |
| Rapport Hebdomadaire | Synthèse automatique hebdomadaire |
| Rapport Journalier | Bilan quotidien par patient |
| Surveillance Nocturne | Monitoring renforcé la nuit |

## 🛠️ Stack

- **Orchestration** : n8n self-hosted
- **Vidéo** : Frigate (détection objets/chutes) + RTSP
- **Notifications** : Telegram Bot
- **IA** : Ollama local (analyse d'images)
- **Stockage** : PostgreSQL

## 🚀 Import dans n8n

1. Dans n8n → **Workflows** → **Import**
2. Importer les fichiers JSON du dossier `workflows/`
3. Configurer les credentials Telegram et PostgreSQL
4. Configurer l'URL Frigate dans les workflows caméra
