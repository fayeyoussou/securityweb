
# Projet Maven Jsp / Hibernate

A brief description of what this project does and who it's for


## Liste des taches
- Creer un projet Maven nomme web nomme securityweb
- Creer Les entites , dto
- creer les couches Dao
- creer les couches dto
- tester
- creer les servlets suivants :
    -   LoginServlet
    -   LogoutServlet
    -   ComptesServlet
    -   DroitServlet
-   Creer une page de connexion index.jsp
-   creer dans le dossier WEB-INF
view\
├── comptes\
│   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├── add.jsp\
│   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└── list.jsp\
├── droits\
│   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├── add.jsp\
│   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└── list.jsp\
├── footer.jsp\
└── header.jsp\




    
## Realisation du Projet
Le Projet a ete realise avec maven
### dossier config
Dans le dossier config nous avons le fichier hibernateUtil qui permet de configurer la connexion avec la base de donnee mysql.\
La classe contient une methode static qui retourne SessionFactory.Ce dernier permet de creer une Session, d'interagir avec la base de donnee , de demarrer une transaction etc...
### dossier controller
Dans le controller nous avons les servlets qui va gerer la logique metier et les chemins . et qui sont reconnus grace a l'annotation @WebServlets. l'argument urlPatterns permet d'assigner plusieurs chemins au servlet et le methods doGet de la classe permet de traiter les requetes get , doPost les requetes post etc ...
il ya aussi certains fonctions et argument notables qui sont appeles a l'interieur comme sendRedirect(qui permet une redirection),HttpServletRequest qui permet de permet de recuperer toutes les informations de la requete et HttpServletResponse qui permet de configurer la reponse a envoyer.
### dossier dao
Il contient toute les methodes configure pour l'interaction avec la base de donnee
### dossier dto
il permet de configurer comment les infos seront transmise au view au lieu de les passer directement entites les dto permettent de transformer les informations des entites en informations lisibles et controlle pour les views;
### webApp
ce dossier contient 
- Le Meta-Inf dont le principal est le manifest.mf qui contient des metas-data(info a propos des donnees) comme la position de certains donnees;
- Le web-inf contient des infos et ressource de l'application comme les template , les vues et aussi des fichier de proprietes.
- Dans le dossier vues nous les fichier qui contiennent l'affichage et la transformation des info interface pour l'utilisateur.
## Authors

- [@youssouphafaye](https://www.github.com/fayeyoussou)


## Maven Commands

To deploy this project run



```bash
  mvn clean // pour nettoyer le projet et supprimer le dossier target
```
```bash
  mvn package // permet de build le projet en fichier jar ou war selon la configuration sur le pom.xml
```

```bash
  mvn install // realise le build et install le projet
```

```bash
  mvn validate // realise les test de validation du projet
```