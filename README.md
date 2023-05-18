# Commandes Linux ( Commandes couramment utilisées )
### Pour plus d'options, utiliser le manuel de chaque commande  
- man "nom_de_la_commande"
---
---
## Les commandes courantes Linux
1. Commande "pwd"
    - Fonction : Affiche le répertoire ou l'on se trouve
        - Commande :  
        `pwd` ( affiche ou l'on se trouve )  
---
2. Commande "alias"
    - Fonction : Définit des raccourcis de commandes dans le fichier ~/.bashrc  
        > ll = 'ls -lah --color'  
        > rm = 'rm -v'  
        > update = 'dnf update'  
---
3. Commande "cat"  
    - Fonction : Affiche le contenu d'un fichier dans le terminal  
        - Commande :  
        `cat fichier` ( affiche le contenu du fichier )  
---
4. Commande "cd"  
    - Fonction : Changer de répertoire  
        - Commande :  
        `cd ..` ( accèder au répertoire précedent )  
        `cd ~` ( accèder au répertoire de l'utilisateur )  
        `cd /usr/share` ( accèder au répertoire /usr/share de manière absolu )  
        `cd Vidéos` ( accéder au répertoire Vidéos de manière relative )   
---
5. Commande "cp"  
    - Fonction : Permets de copier des répertoires et fichiers  
        - Commande :  
        `cp fichier dossier` ( copier un fichier dans un répertoire )   
        `cp fichier fichier2` ( copier un fichier sous un autre nom de fichier )  
        `cp -r dossier dossier_2` ( copier un dossier et son contenu dans un autre dossier )  
        `cp -v` ( option de copie en mode verbeux )  
---
6. Commande "mv"
    - Fonction : Permet de déplacer ou renomer un fichier ou dossier  
        - Commande :  
        `mv fichier dossier/fichier` ( déplacer un fichier )  
        `mv fichier fichier_bis`  ( renomer un fichier )  
        `mv dossier dossier_1` ( déplacer un dossier )  
        `mv dossier dossier_1/dossier_bis` ( déplacer un dossier et le renomer )  
        `mv dossier dossier_2` ( renome le dossier )  
---
7. Commande "rm"  
    - Fonction :  Supprimer un fichier ou un répertoire  
        - Commande : 
        `rm -i fichier` (supprime un fichier avec confirmation)  
        `rm -f fichier` ( force la suppression )  
        `rm -R dossier` ( supprime le dossier )  
        - Option utile :  
        `rm -v` ( mode verbeux )  
---
8. Commande "mkdir"
    - Fonction : Permet de créer un dossier  
        - Commande :  
        `mkdir dossier` ( crée un dossier )  
        `mkdir dossier1 dossier2 dossier3` ( créé plusieurs dossiers en même temps )  
        `mkdir -p dossier/dossier1/dossier2` ( crée un dossier et dessous-répertoire avec l'option '-p' )  
---
9. Commande "ls"  
    - Fonction :  liste le contenu des dossiers  
        - Commande :  
        `ls -a` ( inclure les entrées débutant par « . » )  
        `ls -h` ( afficher les tailles en format lisible )  
        `ls -l` ( utiliser un format d'affichage long )  
        `ls -R` ( affiche de fàçon récursive )  
        `ls --color` ( affiche en couleur )  
        `ls -S` ( trier selon la taille des fichiers en commençant par le plus gros )  
        - Possible de combiner les options  
            > Ex : `ls -lahSR --color`  
---
10. Commande "file"  
    - Fonction : Détermine le type d'un fichier  
        - Commande :  
        `file nom_du_fichier`  
---
11. Commande "find"
    - Fonction : outils de recherche approfondie de fichiers  
        - Commande :  
        `find . -name "fichier"` ( cherche à partir du répertoire courant )  
        `find /var/log/ -name "syslog"` ( cherche à partir d’un répertoire )  
        `find . -size +10M` ( cherche à partir de la taille )  
        `find . -name "*.odt" -atime 6` ( cherche à partir de la date de dernier accès )  
        `find /var/log -name "syslog" -type d` ( chercher uniquement des répertoires ou des fichiers )  
        `find . -name "fichier" -delete` ( supprimer les fichiers trouvés )  
        `find . -name '*.jpg' -exec chmod 744 {} \;` ( cherche des fichiers et leur éxécute une commande )  
---
12. Commande "grep"  
    - Fonction : recherche de fichier et dossier  
        - Commande :  
        `grep mot_chercher fichier` ( recherche le mot chercher dans un fichier )  
        `grep -n mot_chercher fichier` ( affiche le numéro de ligne )  
        `grep -i mot_chercher fichier` ( permet d'ignoré la casse )  
        `grep -v mot_chercher fichier` ( inverse la recherche )  
        `grep -c mot_chercher fichier` ( affiche le nombre de ligne )  
        `egrep [mM]ot_chercher fichier` ( recherche selon l'expression régilière )  
---
13. Commande "head"  
    - Fonction : lire les 'n' premières lignes d'un fichier  
        - Commande :  
        `head -2 nom_du_fichier` ( affiche les 2 premiere ligne du fichier )  
---
14. Commande "tail"
    - Fonction : lire les 'n' dernières lignes d'un fichier
        - Commande :  
        `tail -2 fichier` ( affiche les 2 dernieres lignes d'un fichier )
        - Option utile :  
        `tail -f` ( afficher les données ajoutées en temps réel lorsque le fichier est modifié )  
---
15. Commande "less"  
    - Fonction : paginer le contenue d'un fichier  
        - Commande :  
        `less fichier` ( affiche le fichier par pagination )  
        `less -N nom_du_fichier` ( afficher avec les numeros de ligne )  
        - les modes de pagination :  
            > Soit avec les flèches directionnelles  
            > Page précédente : 'b'  
            > Page suivante : 'barre espacement'  
            > Quitter : 'q'  
---
16. Commande "more"
    - Fonction : afficher le contenu d'un fichier par page  
        - Commande :  
        `more fichier` ( afficher le fichier et paginer avec les fleches directionnelles)  
        - les modes de pagination :  
            > Soit avec les flèches directionnelles  
            > Page précédente : 'b'  
            > Page suivante : 'barre espacement'  
            > Quitter : 'q' 
---
17. Commande "ln"  
    - Fonction : Crée un lien vers un fichier  
        - Commande :  
        `ln -s fichier fichier_raccourci` (lien raccourci symbolique )  
        `ln fichier fichier_lien` ( lien physique 'deux même fichiers' )  
---
18. Commande "touch"
    - Fonction : Créé un fichier vide ou vide un fichier  
        - Commande :  
        `touch  fichier` ( crée un fichier vide )  
---  
19. Commande "tree"  
    - Fonction : Affiche l'arborescence d'un répertoire  
        - Commande :  
        `tree` ( affiche l'arborescence d'un répertoire)  
---  
20. Commande "wc"  
    - Fonction : Affiche le nombre de ligne,mot,octet d'un fichier  
        - Commande :  
        `wc -l fichier` ( affiche le nombre de ligne )  
        `wc -c fichier` ( affiche le nombre d'octet )  
        `wc -m fichier` ( affiche le nombre de caractère )  
        `wc -w fichier` ( affiche le nombre de mot )  
