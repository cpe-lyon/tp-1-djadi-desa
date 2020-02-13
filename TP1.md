# Compte rendu TP1

## Exercice 2 : Prise en main de l'interpréteur de commandes

### Manuel

1. La commande which permet de localiser une commande dans l'arborescence Linux
2. Pour chercher un terme, il faut taper : /"expression" puis entrée. L'expression demandé va alors apparaitre en surligné blanc
3. Pour quitter le manuel, taper sur "q"
4. la commande est *man 6 which*. La section 6 est la section "jeux" du manuel

### Navigation dans l'arborescence des fichiers

1. *cd /var/log*
2. *cd ..*
3. *cd ~*
4. *cd -*
5. *cd /root* ==> La permission est non accordée
6. *sudo cd /root* ==> commande ne fonctione pas. Faire d'abord un *sudo su* puis un *cd /root* pour accéder au dossier /root
7. *mkdir dossier1 dossier2*
    *touch dossier1/fichier1*
    *mkdir dossier2/dossier2.1 dossier2/dossier2.2*
    *touch dossier2/dossier2.2/fichier2 dossier2/dossier2.2/fichier3*
8. rm permet de supprimer un fichier mais il ne supprime pas un dossier. 
9. Pour supprimer un dossier, il faut utiliser l'option -r soit la commande *rm -d dossier*
10. Il ne peut pas supprimer dossier2 avec cette commande car il est rempli de dossier et fichiers
11. *rm -r dossier2*

### Commandes importantes

1. *date* permet d'afficher l'heure + date d'aujourd'hui. La commande *time* permet de calculer le temps que mettra un processus (exemple commande *wget* télécharge via un lien https)
2. Les fichiers commençant par un point sont des fichiers cachés dans le dossier
3. *which ls* ==> se situe dans /usr/bin/ls
4. Il n'existe pas d'entrée de manuel pour la commande *ll*. Cette commande est un raccourci de la commande *ls -alF*.
5. *ls /bin* ==> affiche tous les fichiers dans le dossier /bin
6. *ls ..* ==> permet d'afficher les fichiers et dossier présent dans le dossier parent par rapport au répertoire courant
7. 
