# Commandes Linux ( Commandes couramment utilisées )
### Pour plus d'options, utiliser le manuel de chaque commande  
- man "nom_de_la_commande"
---
---
## Les commandes courantes Linux
1. Commande "alias"
    - Fonction : Définit des raccourcis de commandes dans le fichier ~/.bashrc  
        > ll = 'ls -lah --color'  
        > rm = 'rm -v'  
        > update = 'dnf update'  

2. Commande "cat"  
    - Fonction : Affiche un fichier dans le terminal  
        > cat /home/user/repertoire/fichier  

3. Commande "cd"  
    - Fonction : Changer de répertoire  
        > cd ..         : accèder au répertoire parent  
        > cd ~          : accèder au répertoire de l'utilisateur  
        > cd /usr/share : accèder au répertoire /usr/share de manière absolu  
        > cd Vidéos     : accéder au répertoire Vidéos de manière relative  

4. Commande "cp"  
    - Fonction : Copier des répertoires et fichiers
        > cp fichier /dossier/         : copier un fichier dans un répertoire  
        > cp fichier fichier2          : renomer un fichier  
        > cp -i fichier fichier2       : copier un fichier avec confirmation  
        > cp -r /dossier /user/dossier : copier un dossier et son contenu de maniere recursive  
        > cp -v                        : mode verbeux  

5. Commande "ls"  
    - Fonction :  liste le contenu des dossiers  
        > ls -a : inclure les entrées débutant par « . »  
        > ls -h : avec -l ou -s, afficher les tailles en format lisible  
        > ls -l : utiliser un format d'affichage long  
        > ls -S : trier selon la taille des fichiers en commençant par le plus gros  
        - Possible de combiner les options  
            > Ex : ls -lah  

6. ...