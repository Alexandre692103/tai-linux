# Commandes de base sous Linux


## Sommaire

* Manipulation des fichiers et des répertoires
*  Gestion des users et des droits
*  gestion des logiciels
*  Commandes avancées

  # # Concepts Généraux
commande : logiciel lancé sans interface graphique
KISS : *Kepp It Simple and Stupid* - chaque commande ne fait qu'une seule chose, on enchaine les commandes pour faire des actions complexes
Chaîner des commandes: on utilise le `|`

Les redirections :
* \> : crée et ecrit dans un fichier : exemple : `sort /etc/passwd > /tmp/users_tries.txt`
* \>\> : ajoute à la suite du fichier : `date >> /tmp/date.txt`
aide sur une commande : `man` + la commande, exemple : `man ls`
  
### Manipulation des fichiers et des répertoires

* oû suis-je ? `pwd` pour *print working directory*
* afficher le contenu d'un dossier ? `ls` pour **l**i**s**t
*  changer de répertoire courant ? `cd` + le répertoire, (pour *change directory*) par exemple `cd /tmp`
* `cd` sans argument ramène dans le répertoire personnel
* `cd -` revient au dossier précédent
* crée un fichier vide ? `touch`
* èditer un fichier ? `nano` + le nom du fichier
*  compresser un fichier/dosier ? `tar` + nom de l'archive + nom du fichier/dossier à compresser
*  sans compression : `tar cvf archive.tar /home/barth/projets`
*  avec compression : `tar czvf archive.tar.gz /home/barth/projets`
* extraire une archive tar ? `tar xzvf glpi. glpi.tar.gz`
* afficher le contenu d'un fichier ? `cat` + chemain vers le fichier
* compter le nombre de lignes dans fichier ? `wc -l` + chemin vers le fichier (pour *word count*)
*  afficher la fin d'un fichier ? `tail` + le chemin vers le fichier (*tail* signifie *queue*)
*  afficher en temps réel la fin d'un fichier ? `tail -f` + chemin vers le fichier
*  afficher le début d'un fichier ? `head` + le nom du fichier
*  afficher les lignes du fichier /etc/passwd qui contienne le mot "barth" ? `grep barth /etc/passwd`
*  

Mise en pratique :
* combien d'utilisateurs de mon système utilisent bash ? => `grep bash /etc/passwd | wc -l`


 
