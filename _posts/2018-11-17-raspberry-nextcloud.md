---
category: Veille
published: false
---
## Installation d'un serveur NextCloud sur un RaspBerry

Depuis Windows/Linux/OSX

1. Télécharger la dernière version de l'image [NextCloud](https://ownyourbits.com/nextcloudpi/#download) pour RaspBerry 
2. [Ecraser la carte SD avec l'image récupérrée](https://www.raspberrypi.org/documentation/installation/installing-images/mac.md)
3. Créer un fichier vide _ssh_ à la raçine de la partition de boot du RaspBerry pour permettre l'accès via SSH

### Après avoir installé la carte SD et branché le RaspBerry

1. Se connecter en SSH (Identifiants par défaut: pi / raspberry)
2. Changer le mot de passe
3. sudo ncp-config
4. Activer `nc-webui`
