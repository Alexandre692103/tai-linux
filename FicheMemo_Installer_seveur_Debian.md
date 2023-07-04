# Installation d'un serveur Debian


1. Installer la machine
    * mettre un mot de passe root simple et qui marche en azerty et en qwerty
    * décocher "interface de bureau" et "gnome" et **cocher "serveur SSH*""*
    
2. Se connecter sur la machine, et devenir root avec `su -`
3. Changer le mot de passe root, avec un mot de passe sécurisé, en utilisant `passwd`
4. Installer sudo avec `apt install sudo`
5. Donner les droits sudo à l'utilisateur de base (ici hb) : `usermod -aG sudo hb`
6. Vérifier que le user a bien récupéré le groupe : `groups hb`
7. Couper complètement la session root + la session hb (fermer la connexion SSH) puis se reconnecter
8. Rechercher puis appliquer les mises à jour : 
```bash
sudo apt update
# pour metre à jour tous les paquets :
sudo apt upgrade
```
