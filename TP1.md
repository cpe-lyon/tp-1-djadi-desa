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
7. *pwd* ==> permet de donner le chemin complet du dossier courant
8. *echo 'yo' > plop* ==> écrit le mot 'yo' dans un fichier nommé plop. Si la commande est entrée une 2ème fois, aucun autre fichier est créer, il écrase donc le fichier précédent avec la nouvelle expression
9. *echo 'yo' >> plop* ==> écrit la même expression sur la deuxieme ligne du fichier plop
10. La commande *file "nom fichier ou dossier"* permet d'afficher le type de fichier demandé. 
Exemple : *file plop* --> *plop: ASCII text*
Exemple2 : *file initrd.img* --> *initrd.img: symbolic link to boot/initrd.img-5.3.0-29-generic*
11. Après modification de toto, on remarque que titi à lui aussi fait la modification du texte. En supprimant toto, le lien symbolique entre toto et titi est supprimer mais le fichier titi est toujours existant
12. Après création du lien symbolique avec la commande *ln -s titi tutu*, si l'on modifie le fichier *titi*, le fichier *tutu* est modifier aussi. Si le fichier *tutu* est modifié, *titi* est modifier lui aussi. Si *titi* est supprimer, le lien symbolique est brisé et le fichier *tutu* est donc présent mais corrompu. En utilisant la commande *file* on peut voir l'affichage suivant : 
   *file tutu --> tutu: broken symbolic link to titi*
13. *cat /var/log/syslog*. Le raccourci clavier *Ctrl-S* permet d'interrompre le défilement à l'écran. Pour reprendre le défilement, il faut utiliser le raccourci *Ctrl-Q*
14. *head -n 5 /var/log/syslog* ==> affiche les 5 premieres lignes du fichier syslog
   *tail -n 15 /var/log/syslog* ==> affiche les 15 dernières lignes du fichier syslog
   *head -n 20 /var/log/syslog | tail -n 10* ==> affiche les lignes 10 à 20 du fichier syslog
15. *dmesg | less* ==> *dmesg* est une commande de contrôle du noyau permettant de voir en détails son état. la commande *less* à la suite du résultat de la commande dmesg permet un affichage contrôler en affichant le début et en défilant avec la souris jusqu'à la fin. On peut aussi appuyer sur la barre espace afin de sauter à la suite non visible du texte. Enfin, on peut appuyer sur entrée pour sauter ligne par ligne le texte
16. *cat /etc/passwd* ==> affiche le fichier passwd contenant les login, droits de lecture et écriture sur les chemin détaillés etc. La commande manuel de ce fichier est *man passwd*
17. *sort -k1r /etc/passwd* ==> permet de trier le fichier par rapport au tri décroissant de la 1ère colonne
18. 
