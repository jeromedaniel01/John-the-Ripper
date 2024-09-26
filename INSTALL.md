# Installation de John the Ripper

## Besoins initiaux

- Retrouver le mot de passe d'un fichier zip crypté
- Effectuer une attaque par dictionnaire pour tester la robustesse des mots de passe d’un serveur à partir d’un client
 
## Configuration technique

- Client : Windows 10 avec [Putty](https://www.putty.org/) installé
- Serveur : Linux Kali 6.6.15 avec openssh-server installé et activé
 
## Étapes d'installation

### 1) Se connecter depuis le client sur le serveur avec Putty

***Vous pouvez passer cette étape si vous travaillez directement sur le serveur***
   
- Démarrer Putty, entrer l'adresse IP du serveur et cliquer sur "Ouvrir"

![Putty](https://github.com/WildCodeSchool/tssr-2405-p1-g1-Jhon/blob/main/images/Putty.png)

- Entrer l'identifiant et le mot de passe du serveur

### 2) Mettre à jour les paquets depuis le terminal

  `sudo apt update`

### 3) Installer John the Ripper

  `sudo apt install john`


### 4) Vérifier si Joth the Ripper est correctement installé

  `john`

![Good install](https://github.com/WildCodeSchool/tssr-2405-p1-g1-Jhon/blob/main/images/success.png)


**Se référer à [USER_GUIDE.md](https://github.com/WildCodeSchool/tssr-2405-p1-g1-Jhon/blob/main/USER_GUIDE.md) pour l'utilisation**


## Difficultés et solutions
Certains paquets nécessaires au bon fonctionnement de John The Ripper ne sont pas présents nativement sur certaines distributions Linux, vous devrez peut-être en installer manuellement (suivre les éventuelles messages d'erreur lors de l'exécution)
