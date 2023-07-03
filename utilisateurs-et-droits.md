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
