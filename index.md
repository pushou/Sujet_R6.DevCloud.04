---
title: SAE 6D01 - Développement Système et Cloud.
---
## Description nationale de la SAE.

**Compétences ciblées:**

– Coordonner des infrastructures modulaires

– Accompagner le développement d’applications

**Objectifs et problématique professionnelle :**

Le professionnel R&T spécialisé en Développement Système et Cloud fait évoluer des applications existantes au sein de
son entreprise en développant de nouvelles fonctionnalités. L’application pouvant déjà être en production et utilisée par des
collaborateurs ou des clients, il ne peut donc pas interrompre l’usage qui en est fait. Il intègre ses apports en utilisant une
approche CI/CD (intégration continue, déploiement continu). Cette approche permet de tester les nouvelles fonctionnalités
en s’assurant de leurs compatibilités avec l’existant avant de planifier leurs mises à disposition auprès des utilisateurs sans
interruption de service.

**Descriptif générique :**

Le professionnel DevCloud met en œuvre la chaîne CI/CD d’une application structurée en microservices, intervient et surveille
les différentes étapes du cycle de développement (dont la gestion des erreurs et des messages). Afin d’assurer le développement des fonctionnalités, il applique la démarche suivante :

– la mise en place de la chaîne d’intégration continue (CI) et ses différents tests ;

– la mise en place de la chaîne de développement continue (CD) incluant la génération du livrable applicatif sous la forme
d’un conteneur et le déploiement automatique de l’application avec ses améliorations ;

– la vérification de la santé du code incluant le monitoring de l’application, un système d’alertes, la prise en compte de la
sécurité à tous les niveaux de l’application et la gestion des messages (incluant les logs) renvoyés par l’application ;

– la planification du déploiement avec le nettoyage des bases de données de l’orchestrateur, l’automatisation du déploie-
ment en tenant compte de l’activité et la gestion d’un backup ;

– la gestion des agents de messages pour la communication entre deux microservices (sous la forme d’une file FIFO par
exemple).


:::{table} **Apprentissages critiques**
:widths: auto
:align: center
|AC              | Description | 
|----------------|-------------|
|AC34.01DevCloud | Concevoir, administrer et superviser une infrastructure Cloud|
|AC34.02DevCloud | Orchestrer les ressources Cloud|
|AC34.03DevCloud | Investiguer sur les incidents et les résoudre afin d’améliorer la qualité et la fiabilité des infrastructures|
|AC35.01DevCloud | Adopter les pratiques de pilotage de projet|
|AC35.02DevCloud | Concevoir, gérer et sécuriser un environnement de microservices|
|AC35.03DevCloud | Gérer son infrastructure comme du code|
|AC35.04DevCloud | Gérer une chaîne d’intégration et/ou de déploiement continu|
:::

## Sujet de la SAE

Nous avons mis en place un pipeline de données depuis votre honeypots TPOT vers le serveur NextCloud de votre entreprise. Vous avez maintenant des logs de sécurité et des logs d'activité de votre honeypots. Il va falloir les exploiter !

### Organisation de la SAE

- Vous travaillez en équipe de 4 à 5 personnes. 
- Vous travaillerez en mode agile et vous utiliserez un outil de gestion de projet (trello, jira, gitlab, etc.) pour gérer votre projet.
Chaque tâche sera décrite avec ses caractéristiques (durée, intervenant, co-validateur..)
Au final un bilan des heures passées par tâche et par analyste(vous) sera réalisé.

- Pour le rapport final, vous utiliserez un outil de type myst markdown et vous le versionnerez sur un repository git.
Il vous permettra de rédiger un rapport de projet collaboratif , avec des sorties au format pdf, html etc.

Vous utiliserez gitlab.iutbeziers.fr comme serveur CI/CD pour le déploiement de votre code et les "github pages" pour le déploiement de votre site web final. Myst permet de travailler sur des Notebook Jupyter en markdown, vous en ferez un par objectif de sécurité.

Chaque équipier devra participer au projet en utilisant des pull/merge requests pour chaque intégration sur une branche dev. 
Un coéquipier co-validera les MR/PR et les "mergera" avec la branche main. 

### Etapes de la SAE et livrables

- Vous vous partagez les indicateurs de sécurité à traiter entre les membres de l'équipe. Chaque indicateur de sécurité donnera lieu à un notebook Python.
  
- Vous décrirez Les indicateurs de sécurité (synthèse, liste noiren, identification viral avec Yara)  que vous allez extraire de chaque source de données (suricata,dionea,cowrie,p0f etc.)., virus)
Il devront être validés par votre responsable (moi). 

- Vous ferez les extractions des données de vos indicateurs avec NuShell. Le but étant d'obtenir des données exploitables  pour vos notebooks via "Panda" et des listes noires d'adresse IP, de noms de domaines, de hash de fichiers, de signatures de virus, etc. Les données de chaque seront stockées sur des repositories gitlab.iutbeziers.fr de façon dynamique.

- Chaque membre de l'équipe devra réaliser un notebook Jupyter pour chaque indicateur de sécurité. Le code Python devra comprendre une "doc string". Des test unitaires seront réalisés avec doctest. Des résultats synthétiques et graphiques seront produits.

- Vous assemblez les notebooks pour obtenir un rapport de sécurité dynamique avec Myst Markdown.  

- Vous déployez votre rapport sur un serveur github avec Myst Markdown.


