
# Guide de Formation Administrateur Dataiku DSS

### WARNING : Synthèse générée par GPT4 d'un training de 4 semaines délivrée par Dataiku pour un pilot de formation des administrateurs patenaires de la solution.
### basé sur la version Cloud Stack de la solution. (cf. https://doc.dataiku.com/dss/latest/installation/index.html)
### Cas d'usage suivant : sur AWS. ( documentation associée : https://doc.dataiku.com/dss/latest/installation/cloudstacks-aws/index.html)

## 1. Configuration et Gestion des Audit Trails et du Serveur d'Événements

### Pistes d'Audit dans Dataiku DSS
- **Accès** : Dans l'interface d'administration de Dataiku DSS, naviguez vers la section "Sécurité".
- **Activation** : Localisez et activez les options pour les pistes d'audit.
- **Configuration** : Choisissez votre méthode de stockage préférée pour les logs (base de données, fichier).

### Serveur d'Événements
- **Documentation** : [Consultez la documentation Dataiku pour les instructions spécifiques à l'Event Server.](https://doc.dataiku.com/dss/latest/operations/audit-trail/eventserver.html)
- **Déploiement** : Déployez l'Event Server, typiquement via Docker ou directement sur un serveur.
- **Intégration** : Configurez Dataiku DSS pour rediriger les événements audités vers ce serveur.

## 2. Surveillance de DSS, Utilisation du Disque et Configuration des Rapports d'Utilisation

### Surveiller l'Utilisation du Disque sur AWS
- **Outils** : Utilisez AWS CloudWatch pour surveiller l'espace disque des instances EC2 exécutant Dataiku DSS.
- **Alertes** : Configurez des alertes pour vous notifier en cas de dépassement des seuils d'espace disque.

### Rapports d'Utilisation dans Dataiku DSS
- **Accès** : Allez dans l'onglet "Monitoring" de l'interface administrateur.
- **Configuration** : Incluez les métriques désirées, telles que l'utilisation du disque.

## 3. Automatisation des Projets : Macros et Scénarios

### Création et Exécution de Scénarios
- **Création** : Dans un projet Dataiku, créez un nouveau scénario.
- **Déclencheurs** : Sélectionnez le type de déclencheur (manuel, programmé, événementiel).
- **Étapes** : Ajoutez des étapes au scénario, telles que l'exécution d'un script ou d'une recette.

### Exemple de Macro Personnalisée
- **Documentation** : repo pluggin & macro.
- **Utilisation** : Une macro peut être utilisée pour automatiser des tâches de maintenance à travers plusieurs projets.

## 4. Configuration de Spark

### Configuration d'un Cluster Spark sur AWS
- **AWS EMR** : Utilisez AWS EMR pour configurer un cluster Spark.
- **Connexion dans Dataiku DSS** : Créez une nouvelle connexion de type Spark et spécifiez les détails de votre cluster EMR.

### Exemple de Configuration Optimale de Spark
- **Documentation** : repo Documentation & stuff.

## 5. Bonnes Pratiques pour la Création de Connexions

### Sécurisation des Connexions aux Bases de Données
- **IAM** : Utilisez des rôles IAM pour gérer l'accès et sécuriser les connexions.
- **Gestion des Secrets** : Stockez les informations sensibles dans AWS Secrets Manager.

### Configuration d'une Connexion PostgreSQL sur AWS RDS
- **Nouvelle Connexion** : Dans Dataiku DSS, créez une connexion et remplissez les détails fournis par AWS RDS.

## 6. Configuration de l'Exécution Conteneurisée

Configurer l'exécution conteneurisée pour les jobs Dataiku sur AWS ECS est essentiel pour une gestion efficace des ressources et une meilleure scalabilité. Voici les étapes principales :

- **Rôle IAM** : Assurez-vous que le rôle IAM utilisé par le service ECS a les permissions nécessaires pour accéder à Dataiku DSS et aux autres ressources AWS nécessaires.
- **Exemple de Dockerfile** : repo Documentation & Stuff.

## 7. Utilisation de l'API Publique Dataiku



L'API publique de Dataiku DSS offre une porte d'entrée puissante pour l'automatisation et l'intégration poussée des processus administratifs et de gestion de projet au sein de Dataiku. Cette section vise à fournir une compréhension approfondie des rôles API et de l'exploitation efficace de la documentation technique de Dataiku.



### Comprendre les Rôles API



- **Rôles API** : Dans Dataiku DSS, l'accès via l'API est contrôlé par des rôles spécifiques assignés à chaque clé API. Ces rôles définissent les permissions et sont hérités directement de l'utilisateur auquel la clé API est associée. Pour les tâches administratives, il est essentiel que l'utilisateur associé à la clé API possède les rôles adéquats pour accomplir les actions requises.

- **Création de Clés API** : Les clés API sont générées dans l'interface utilisateur de Dataiku DSS, sous la section \"Sécurité\" de l'administration. La gestion sécurisée de ces clés est cruciale pour maintenir l'intégrité de la sécurité de votre instance DSS.



### Documentation Technique sur l'API Publique


- **Accès à la Documentation** : repo Documentation & Stuff.

- **Exemples Pratiques** :

  - Automatisation des déploiements de projets.

  - Gestion des environnements de code et datasets.

  - Exécution et monitoring des scénarios et jobs.


### Exemple d'Intégration avec l'API

privé
