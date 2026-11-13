# Server Monitoring Dashboard

Tableau de bord de supervision de serveur en temps réel : suivi de l'utilisation CPU, mémoire et disque, détection des dépassements de seuil et alertes par e-mail.

## Fonctionnalités

- Collecte des métriques système en continu avec `psutil` (CPU, RAM, disque)
- Visualisation en temps réel avec Plotly et Streamlit
- Détection d'anomalies par seuil configurable (80 % par défaut)
- Historique des alertes récentes
- Notification par e-mail (SMTP) lors d'un dépassement de seuil

## Stack technique

Python, Streamlit, psutil, Pandas, Plotly, smtplib

## Installation

```bash
pip install streamlit psutil pandas plotly
streamlit run dashboard.py
```

## Configuration

Les seuils d'alerte, l'intervalle de contrôle et les paramètres SMTP se règlent dans `config.py`. Ne publiez jamais d'identifiants réels : renseignez-les localement ou via des variables d'environnement.

## Pistes d'amélioration

- Détection d'anomalies statistique ou par apprentissage automatique
- Supervision de plusieurs serveurs
- Conteneurisation avec Docker
