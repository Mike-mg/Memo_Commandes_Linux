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
    - Fonction : Affiche le contenu d'un fichier dans le terminal  
        - Commande :  
        `cat /home/user/repertoire/fichier`  

3. Commande "cd"  
    - Fonction : Changer de répertoire  
        - Commande :  
    `cd ..` ( accèder au répertoire parent )  
    `cd ~` ( accèder au répertoire de l'utilisateur )  
    `cd /usr/share` ( accèder au répertoire /usr/share de manière absolu )  
    `cd Vidéos` ( accéder au répertoire Vidéos de manière relative )   

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
---  
---  
---  
---  
---  
---  
6. Commande "cut"  
    - Fonction : recherche par section dans un fichier

        > -c1-5       : permet de sélectionner les colonne de 1 à 5  
        > -c14-       : permet de sélectionner de la ligne 14 à la derniere  
        > -c1-3,14-18 : permet de spécifié plusieurs plages de colonnes  
        > -d et -f    : permet d'afficher des champs avec un délimiteur  
        - Ex : cut -d':' -f1,6 /etc/passwd

7. Commande "file"  
    - Fonction : Détermine le type d'un fichier  
        > file /home/user/repertoire/fichier  

8. Commande "find"
    - Fonction : outils de recherche approfondie de fichiers  
        - Les options les plus courantes :  
        > find . -name "fichier" : cherche à partir du répertoire courant  
        > find /var/log/ -name "syslog" : cherche à partir d’un répertoire  
        > find . -size +10M ( 10k ou 10G ) : cherche à partir de la taille  
        
        - cherche à partir de la date de dernier accès  
        > find . -name "*.odt" -atime 6 ([0=J-1],[1=J-2],[2=J-3],etc)  
        
        - chercher uniquement des répertoires ou des fichiers  
        > find /var/log -name "syslog" -type d ([d=dossier],[f=fichier])  
        > find . -name "*.jpg" -printf "%u" : chercher avec -printf  
        
        - affiche le fichier, un tiret et le nom du propriétaire  
        > find . -name "fichier" -delete : supprimer les fichiers trouvés  
        > find . -name '*.jpg' -exec chmod 600 {} \; : appeler_une_commande  

9. Commande "grep"  
    - Fonction : recherche de fichier et dossier  
        - Les options les plus courantes :  
        > grep -n mot_chercher ~/fichier  : affiche le numéro de ligne  
        > grep -i mot_chercher ~/fichier  : permet d'ignoré la casse  
        > grep -v mot_chercher ~/fichier  : inverse la recherche  
        > grep -c mot_chercher ~/fichier  : affiche le nombre de ligne  
        > egrep [mM]ot_chercher ~/fichier : expressions régilières  

10. Commande "head"  
    - Fonction : lire les 'n' premières lignes d'un fichier  
        > head -2 nom_du_fichier  

11. Commande "less"  
    - Fonction : paginer le contenue d'un fichier  
        > `less fichier`  

    - afficher avec les numeros de ligne  
        > `less -N nom_du_fichier`      
    - les options :  
        - soit avec les flèches directionnelles  
        - 'b' : pour page arriere  
        - 'barre espacement' : page suivante  
        - 'q' : pour quitter  

12. Commande ""
    - Fonction :  
\033[1;34m>> Commande : ln (@commande)
\033[1;35m>> Fonction : crée un lien vers un fichier
\033[1;37m>> Exécution de base : ln
\033[1;37m************************************************************************\n
\033[4mLes options les plus courantes :\033[0m\033[37m\n
>> ln -s fichier fichier_raccourci : lien symbolique (raccourci)
>> ln fichier fichier_lien         : lien physique (deux même fichiers)\n


13. Commande ""
    - Fonction :  
>> Commande : ls (@commande)

>> Détails de la commande :  liste le contenu des fichiers et dossiers

>> Exécution de la commande : ls
***********************************************************************\033[0m\n
\033[4mLes options les plus courantes :\033[0m\033[37m
>> ls -a      : affiche les fichiers et dossiers cachés
>> ls -l      : affiche au format long
>> ls -R      : affiche de fàçon récursive
>> ls --color : affiche en couleur
>> ls -h      : affiche de fàçon plus lisible
\033[1;1;1;1;31m>> info       : les options peuvent être combinées\033[0m\n


14. Commande ""
    - Fonction :  
echo -e "\033[1;37m(#) mkdir : Création de répertoire.(@commande)
\033[1;33m********************************************************************
\033[1;37m
1) création de plusieurs répertoires :
>> mkdir repertoire1 repertoire2 repertoire3\n
2) crée un répertoire dans un sous-répertoire avec l'option (-p) :
>> mkdir -p repertoire/repertoire1/repertoire2\n
3) création par combinaison (partie 1) :
>> mkdir -p repertoire repertoire/repertoire1/repertoire2\n
4) création par combinaison (partie 2) :
>> mkdir -p test/{coucou/{titi,toto},tata\n"


15. Commande ""
    - Fonction :  
echo -e "\033[1;37m(#) more : afficher le contenu d'un fichier par page.(@commande)
\033[1;33m********************************************************************\n
\033[1;37m1) afficher un fichier par page ( avec un pipe '|' ) :
>> cat /home/user/fichier | more\n
2) afficher le fichier directment avec 'more' :
>> more /home/user/fichier\n
3) options utile :
>> page suivante : barre espace.
>> par ligne : touche entrée\n"


16. Commande ""
    - Fonction :  
echo -e "\033[1;33m********************************************************************"
echo -e "\033[1;37m(#) mv : permet de copier et renomer en console.(@commande)
\033[1;33m********************************************************************\n
\033[1;37m1) déplacer un fichier :
>> mv /home/user/fichier /home/user/repertoire\n
2) déplacer un fichier et le renomer :
>> mv /home/user/fichier /home/user/repertoire/fichier2\n
3) déplacer un repertoire :
>> mv /home/user/repertoire1 /home/user/autre_repertoire\n
4) renomer un repertoire ou un fichier :
>> mv /home/user/repertoire1 /home/user/repertoire2
>> mv /home/user/fichier1 /home/user/fichier2\n"



17. Commande ""
    - Fonction :  
echo -e "\033[1;37m************************************************************************
\033[1;34m>> Commande : pwd (@commande)
\033[1;35m>> Fonction : affiche le répertoire ou l'on se trouve
\033[1;37m>> Exécution de base : pwd
\033[1;37m************************************************************************\n
\033[4mLes options les plus courantes :\033[0m\033[37m\n
>> pwd : affiche ou l'on se trouve\n



18. Commande ""
    - Fonction :  


echo -e "\033[1;37m************************************************************************
\033[1;34m>> Commande : rm (@commande)
\033[1;35m>> Fonction : éffacer un fichier ou un répertoire
\033[1;37m>> Exécution de base : rm
\033[1;37m************************************************************************\n
\033[4mLes options les plus courantes :\033[0m\033[37m\n
>> rm -i rm /home/user/fichier : supprime un fichier avec confirmation
>> rm -f /home/user/fichier : force la suppression
>> rm -v : mode verbeux
>> rm -R /home/user/fichier : supprime le contenue mais pas le dossier
\033[1;1;1;1;31m>> info : les options peuvent être combinées\033[0m\n


19. Commande ""
    - Fonction :  


echo -e "\033[1;33m********************************************************************"
echo -e "\033[1;37m(#) tail : lire les 'n' dernières lignes d'un fichier.(@commande)
\033[1;33m********************************************************************\n
\033[1;37m1) La commande tail s'utilise comme suit :
>> tail -2 <fichier>
>> tail -f (permet de suivre l'évolution de la fin d'un fichier)\n"



20. Commande ""
    - Fonction :  


echo -e "\033[1;33m********************************************************************"
echo -e "\033[1;37m(#) touch : pour créé un fichier vide ou vidé un fichier.(@commande)
\033[1;33m********************************************************************\n
\033[1;37m1) La commande touch s'utilise comme suit :
>> touch > <fichier>\n"



21. Commande ""
    - Fonction :  


echo -e "\033[1;37m************************************************************************
\033[1;34m>> Commande : tree (@commande)
\033[1;35m>> Fonction : affiche l'arborescence d'un répertoire
\033[1;37m>> Exécution de base : tree
\033[1;37m************************************************************************\n
\033[4mLes options la plus courante :\033[0m\033[37m\n
>> tree : affiche l'arborescence d'un répertoire\n



22. Commande ""
    - Fonction :  


echo -e "\033[1;33m********************************************************************"
echo -e "\033[1;37m(#) wc : affiche le nombre de ligne,mot,octet d'un fichier.(@commande)
\033[1;33m********************************************************************\n
\033[1;37m1) sans option, 'wc' affichera 3 colonnes :
>> colonne 1 : nombre de ligne
>> colonne 2 : nombre de mot
>> colonne 3 : nombre d'octet\n
2) les options 'wc' :
>> -l : affiche le nombre de ligne
>> -c : affiche le nombre d'octet
>> -m : affiche le nombre de caractère
>> -w : affiche le nombre de mot\n
3) Exemple :
>> wc -l /home/user/fichier
>> wc -c /home/user/fichier
>> wc -m /home/user/fichier
>> wc -w /home/user/fichier\n"

