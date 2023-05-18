# Commandes Linux
1. Commande "alias"
    - Définit des raccourcis de commandes  
    - Les raccourcis sont créé dans le fichier ~/.bashrc  
        - Exemple d'alias pouvant être mis en fin du fichier ~/bashrc  
            > ll = 'ls -lah --color'  
            > rm = 'rm -v'  
            > update = 'dnf update'  

2. Commande "cat"  
    - Affiche un fichier dans le terminal  
        > cat /home/user/repertoire/fichier  

3. Commande "cd"  
    - Changer de répertoire  
        > cd ..         : accèder au répertoire parent  
        > cd ~          : accèder au répertoire de l'utilisateur  
        > cd /usr/share : accèder au répertoire /usr/share de manière absolu  
        > cd Vidéos     : accéder au répertoire Vidéos de manière relative  

4. Commande "cp"  
    - Copier des répertoires et fichiers
        > cp fichier /dossier/         : copier un fichier dans un répertoire  
        > cp fichier fichier2          : renomer un fichier  
        > cp -i fichier fichier2       : copier un fichier avec confirmation  
        > cp -r /dossier /user/dossier : copier un dossier et son contenu de maniere recursive  
        > cp -v                        : mode verbeux  
