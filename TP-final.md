

### Sujet de TP : Sécurisation d'un serveur Debian avec un site e-commerce et d'un conteneur de base de données

#### Contexte
Vous devez sécuriser un serveur Debian hébergeant un site e-commerce ainsi qu'un conteneur contenant une base de données. Vous allez mettre en place des mesures de hardening pour ces deux éléments, déployer un système de détection d'intrusion (IDS) et un outil de monitoring pour surveiller l'état de sécurité et la performance. Vous utiliserez également des outils pour vérifier la sécurité de votre configuration.

#### Matériel fourni
1. **Conteneur 1** : Base de données 
2. **Conteneur 2** : Serveur Debian avec un site e-commerce

#### Objectifs
1. **Hardening du conteneur de base de données** : Renforcer la sécurité du conteneur de base de données.
2. **Hardening du serveur Debian** : Renforcer la sécurité du serveur Debian hébergeant le site e-commerce.
3. **Déploiement et configuration d'un IDS (Snort)** : Installer et configurer Snort pour détecter les intrusions.
4. **Utilisation d'outils de vérification de sécurité** : Utiliser Lynis et Trivy pour évaluer la sécurité des systèmes.
5. **Configuration d'un outil de monitoring** : Mettre en place un système de monitoring pour surveiller l'état de sécurité et la performance.

#### Instructions

1. **Hardening du conteneur de base de données**
   - **Sécuriser les accès**
   - **Sécuriser les données**

2. **Hardening du serveur Debian**
   - **Sécuriser les services**
   - **Sécuriser le site e-commerce**

3. **Déploiement et configuration de Snort**
  
4. **Utilisation des outils de vérification de sécurité** :
   - **Lynis**
   - **Trivy**

5. **Configuration d'un outil de monitoring** :
   - Choisir un outil de monitoring.
   - Configurer la collecte de métriques pour le serveur e-commerce et le conteneur de base de données.
   - Créer des tableaux de bord pour surveiller les performances et les alertes de sécurité.

#### Livrables
1. **Rapport de hardening** :
   - Décrire les mesures de sécurisation appliquées au conteneur de base de données et au serveur Debian.
2. **Configuration de Snort** :
   - Fournir un extrait de la configuration de Snort et une liste des règles appliquées.
3. **Rapport d'audit Lynis** :
   - Inclure le rapport d'audit de Lynis avec les recommandations appliquées.
4. **Rapport de scan Trivy** :
   - Inclure les résultats du scan Trivy et les actions correctives effectuées.
5. **Configuration du monitoring** :
   - Décrire l'outil de monitoring utilisé et fournir des captures d'écran des tableaux de bord configurés.

