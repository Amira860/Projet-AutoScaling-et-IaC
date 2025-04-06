
# Projet Kubernetes - Autoscaling et Monitoring

## Description

Ce projet met en place un environnement Kubernetes complet pour surveiller un cluster Redis (master-replica) avec :

- **Backend Node.js** (serveur API simple pour interagir avec Redis)
- **Frontend** (application web pour tester le backend)
- **Prometheus** (pour monitorer les métriques des applications et de l'infrastructure)
- **Grafana** (pour visualiser les métriques et créer des dashboards)

Un système **d'autoscaling** est également mis en place pour ajuster dynamiquement le nombre de pods en fonction de la charge CPU.

---

## Technologies utilisées

- **Kubernetes** (Minikube)
- **Docker**
- **Redis**
- **Node.js**
- **Prometheus**
- **Grafana**
- **Metrics-server**

---

## Démarche à suivre pour exécuter le projet

1. **Cloner le projet**

```bash
git clone <URL_DU_DEPOT>
cd <nom_du_dossier>
```

2. **Lancer le script d'automatisation**

Un script Bash `deploy.sh` est fourni pour tout déployer automatiquement :

```bash
chmod +x deploy.sh
./deploy.sh
```

Le script va automatiquement :

- Déployer l'application Node.js et Redis.
- Déployer Prometheus et Grafana.
- Configurer l'autoscaling sur Redis.

3. **Accéder aux différentes interfaces**

Après exécution du script, Minikube affichera les URLs d'accès pour :

- **Frontend**
- **Backend**
- **Prometheus**
- **Grafana**

---

## Connexion Grafana

- **Utilisateur** : `admin`
- **Mot de passe** : `admin`

---

## Auteurs

- **ASSAM Amira**
- **KADIR Lydia**

---
