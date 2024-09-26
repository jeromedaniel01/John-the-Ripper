<p align="center">
<img align="center" src="https://github.com/WildCodeSchool/tssr-2405-p1-g1-Jhon/blob/main/images/LogoJDR.png">
</p>

# **Présentation de John the Ripper**

## Qu’est-ce que [John the Ripper](https://www.openwall.com/john/) ?

John the Ripper (JTR) est un logiciel [open source](https://www.redhat.com/fr/topics/open-source/what-is-open-source#:~:text=Un%20logiciel%20Open%20Source%20est,l'examen%20par%20les%20pairs.) de déchiffrage de mot de passe. 

Il inclut : 
- l'autodétection des [fonctions de hachage](https://fr.wikipedia.org/wiki/Fonction_de_hachage "Fonction de hachage") utilisées pour stocker les mots de passe
- l'implémentation d'un grand nombre d’algorithmes de cassage
- la reprise d'une attaque après une pause (arrêt de la machine)
- un vaste choix d'options personnalisables

Il est capable d’attaquer les mots de passe hachés avec différentes fonctions de hachage algorithmés tel que : 

| Exemples |
| ---------------- |
| [*MD5*](https://fr.wikipedia.org/wiki/MD5 "MD5") |
| [*Blowfish*](https://fr.wikipedia.org/wiki/Blowfish "Blowfish") | 
| [*Kerberos*](https://fr.wikipedia.org/wiki/Kerberos_\(protocole\) "Kerberos (protocole)") | 
| [AFS](https://fr.wikipedia.org/wiki/Andrew_File_System "Andrew File System") |  
| [*LM hashes*](https://fr.wikipedia.org/wiki/LM_hash "LM hash") de Windows NT/2000/XP/2003 |

Il n’est pas nécessaire d’être physiquement devant la machine ayant les fichiers à hacker, il suffit que la machine ou John the Ripper est installé, dispose de la bibliothèque nécessaire au fonctionnement de ce logiciel et bien entendu un accès à distance à la machine où sont les fichiers hashés.

## Comment fonctionne John the Ripper

John the Ripper importe un fichier contenant les informations d’identifications chiffrées.
Son action consiste à déchiffrer le mot de passe, notamment grâce à une [attaque simple](https://fr.wikipedia.org/wiki/John_the_Ripper#:~:text=John%20dispose%20de%20quatre%20modes,directement%20dans%20un%20des%20modes.), par une [attaque par force brute](https://fr.wikipedia.org/wiki/John_the_Ripper#:~:text=John%20dispose%20de%20quatre%20modes,directement%20dans%20un%20des%20modes.) ou par [attaque incremental](https://fr.wikipedia.org/wiki/John_the_Ripper#:~:text=John%20dispose%20de%20quatre%20modes,directement%20dans%20un%20des%20modes.).

***cf*** : voir le paragraphe "Modes d'action" de la page [Wikipedia](https://fr.wikipedia.org/wiki/John_the_Ripper#:~:text=John%20dispose%20de%20quatre%20modes,directement%20dans%20un%20des%20modes.).

- Pour le ***mode simple***, JDR ajoute un ou plusieurs caractères à la suite du nom d'utilisateur
  
- Pour le ***mode d'attaque par force brute***, il essaie tous les mots contenus dans un dictionnaire. Il est possible d'ajouter différents dictionnaires à JTR, plus ou moins complexes.
  
- Pour le ***mode incremental***, il va essayer toutes les combinaisons de caractères possible, il a le désavantage d'être extrêmement long, suivant la complexité du mot de passe, voir infini si la complexité est trop importante. Afin d’être moins chronophage dans le mode incrémental, il recherche dans un premier temps les caractères les plus utilisés statistiquement.

## L'équipe

- **Julie** était opératrice pour le sprint 1 et Scrum Master pour le sprint 2
- **Jerome** était Product Owner pour le sprint 1 et opérateur pour le sprint 2
- **Mehdi** était opérateur pour le sprint 1 et Product Owner pour le sprint 2
- **Philippe** était Scrum Master pour le sprint 1 et Product Owner pour le sprint 2

## Difficultées rencontrées

JTR n'étant pas installé nativement sur tous les OS, nous avons rencontré quelques difficultés à l'installer sur certains, notamment Ubuntu et Debian.
Il est néanmoins natif à Kali, que nous avons donc privilégié.
L'installation n'est pas impossible sur les autres OS, mais requiert d'installer des paquets complémentaires.

## Tests réalisés

Dans un premier temps nous avons réalisé des tests avec des mots de passe très simples, puis de plus en plus complexes.
JTR est assez rapide avec des mots de passe s'approchant du nom d'utilisateur. En moins de 3 minutes les mots de passe sont trouvés avec le mode simple.
En utilisant l'attaque par force brute, il est légèrement moins rapide si le mot de passe contient moins de 6 caractères, et commence à prendre énormément de temps à partir de 7 caractères.

# [Bonne installation](https://github.com/WildCodeSchool/tssr-2405-p1-g1-Jhon/blob/main/INSTALL.md) et [bonne utilisation](https://github.com/WildCodeSchool/tssr-2405-p1-g1-Jhon/blob/main/USER_GUIDE.md) !
