# John the Ripper

## Retrouver le mot de passe d'un fichier ZIP protégé

### Étapes 1 à 4 : Uniquement pour le test

1) Ouvrir un terminal de commande

   > **Ctrl+Alt+T**

2) Créer un fichier.txt

   `touch test.txt`

3) Remplir le fichier.txt (cmd "ls" pour le test)
   
   `ls > test.txt`

4) Mettre le fichier dans un dossier .zip protegé par un mot de passe

   `zip -e protection.zip test.txt` (créer le mot de passe quand demandé)

### Étapes 5-6 : Remplacer "protection.zip" par le fichier protégé si déjà existant

5) Extraire le mot passe hasher du dossier zip dans un fichier.txt
   
   `zip2john protection.zip > hash.txt`

6) Utiliser John pour décrypter le mot de passe hashé ("cat" dans notre cas, en orange sur l'image ci-dessous)

   `john hash.txt`

![zip](https://github.com/WildCodeSchool/tssr-2405-p1-g1-Jhon/blob/main/images/JohnZIP.png)

## Tester la robustesse des mots de passe utilisateurs d'un serveur

1) Ouvrir un terminal de commande
   
2) Utiliser la commande **unshadow** pour lire les fichiers /passwd et /shadow qui contiennent les hashes (en sudo) et stocker le résultat dans une variable ou un fichier .txt
   
   `sudo unshadow /etc/passwd /etc/shadow > hashinput`

3) Utiliser John pour décrypter les hashes

   `john --format=crypt hashinput`

      - john va lancer l'analyse et effectuer différentes attaques jusqu'à trouver la bonne combinaison.

      - L'option --format permet de préciser le type de hashage utilisé, ici *"crypt"* pour *"generic crypt"*

      - Vous pouvez trouver l'intégralité des formats supportés par JTR [ici](https://pentestmonkey.net/cheat-sheet/john-the-ripper-hash-formats)

4) John va lancer l'analyse et retourner les résultats, comme ci-dessous (mots de passe en orange)

![passwd](https://github.com/WildCodeSchool/tssr-2405-p1-g1-Jhon/blob/main/images/mdpusers.png)

### Vous pouvez retrouver l'intégralité des options de john avec la commande `john --help` ou [ici](https://github.com/WildCodeSchool/tssr-2405-p1-g1-Jhon/blob/main/images/liste_commandes)
