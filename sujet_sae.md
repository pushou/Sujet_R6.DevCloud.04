## Sujet de la SAE

Nous avons mis en place un pipeline de données depuis votre honeypots TPOT vers le serveur NextCloud de votre entreprise. Vous avez maintenant des logs de sécurité é de votre honeypot. Il va falloir les exploiter !

### Organisation de la SAE

- Vous travaillerez en équipe de 4 à 5 personnes. 
- Vous travaillerez en mode agile et vous utiliserez un outil de gestion de projet (trello, jira, gitlab, etc.) pour gérer votre projet.
Chaque tâche sera décrite avec ses caractéristiques (durée, intervenant, co-validateur..)
Au final un bilan des heures passées par tâche et par analyste(vous) sera réalisé.

- Pour le rapport final, vous utiliserez un outil de type myst markdown et vous le versionnerez sur un repository git.
Il vous permettra de rédiger un rapport de projet collaboratif, avec des sorties au format pdf, html etc.

Vous utiliserez gitlab.iutbeziers.fr comme serveur CI/CD pour le déploiement de votre code et les "github pages" pour le déploiement de votre site web final. Myst permet de travailler sur des Notebook Jupyter en markdown. Vous en ferez un par objectif de sécurité.

Chaque équipier devra participer au projet en utilisant des pull/merge requests pour chaque intégration sur une branche dev. 
Un coéquipier co-validera les MR/PR et les "mergera" avec la branche main. 

### Etapes de la SAE et livrables

- Vous vous partagez les indicateurs de sécurité à traiter entre les membres de l'équipe. Chaque indicateur de sécurité donnera lieu à un notebook Python.
  
- Vous décrirez Les indicateurs de sécurité (synthèse, liste noiren, identification viral avec Yara)  que vous allez extraire de chaque source de données (suricata,dionea,cowrie,p0f etc...).Ils devront être validés par votre responsable (moi). 

- Vous ferez les extractions des données de vos indicateurs avec NuShell. Le but étant d'obtenir des données exploitables  pour vos notebooks via "Panda" et des listes noires d'adresse IP, de noms de domaines, de hash de fichiers, de signatures de virus, etc. Les données de chaque seront stockées sur des repositories gitlab.iutbeziers.fr de façon dynamique.

- Chaque membre de l'équipe devra réaliser un notebook Jupyter pour chaque indicateur de sécurité. Le code Python devra comprendre une "doc string". Des test unitaires seront réalisés avec doctest. Des résultats synthétiques et graphiques seront produits.

- Vous assemblez les notebooks pour obtenir un rapport de sécurité dynamique avec Myst Markdown.  

- Vous déployez votre rapport sur un serveur github avec Myst Markdown.


