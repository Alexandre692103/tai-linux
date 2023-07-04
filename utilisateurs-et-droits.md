# Les utilisateurs et les droits


## Sommaire

* Gestion des utilisateurs et des groupes
* gestion des droits UGO
* Gestion des ACL

## Gestion des utilisateurs et des groupes

### Gestion des utilisateurs

un utilisateur est identifié par :
* un login
* un identifiant numérique (UId)
* un groupe principal
* une liste de groupes secondaires

L'administrateur S'appelle root et a l'UId 0.

Pour crée un utilisateur :
* `useradd thierry`
* commende complète : `useradd -m -d /home/thierry - /bin/bash thierry`

  Pour crée un groupe apprents :
  * `groupeadd apprenants`

Pour ajouter thierry au groupe apprenants :
 *  `usermod -aG apprenants thierry`

Pour afficher la liste des groupes de l'utilisateur thierry
* `groups thierry`

Mise en pratique :
* crée un utilisateur "webapp" groupe principal www-data groupe secondaire applis dossier principal //home/system/webapp shell /bin/false
```bash
sudo mkdir /home/system
sudo groupadd www-data
sudo groupadd applis
sudo useradd -m -d /home/system/webapp -g www-data -G applis -N -s /bin/false webapp
```

* changer son mot de passe ? `passwd`
* arrété le debian poweroff
* apt install sudo

  # Installation d'un serveur Debian

  1. Installer la machine
  * mettre un mot de passe root simple et qui marche en azzrty et en qwerty
  * décocher `interface de bureau` `gnome` et **coche "serveur SSH*""*

  * 2 Se connecter sur la machine, et devenir root avec `su -`
    3 Changer le mot de passe root, avec un mot de passer Sécurisé, en utilisent `passwd`
    4. Installer sudo avec `apt install sudo`
    5. Donner les droits sudo à l'utilisateur de base (ici hb) : `usermod - aG sudo hb`
    6. Vérifier que le a bien récupéré le groupe : `groups hb`
    7. Couper complèment la session root + la session hb (fermer la connexion SSH) puis se reconnecter.
    8. Rechercher puis appliquer les mise à jour :
    ```bash

    ```
