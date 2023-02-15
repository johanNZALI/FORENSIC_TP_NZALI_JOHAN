INTRODUCTION

La compromission du site Bosch cvber est une situation très préoccupante car l'attaguant aurait exfiltré des outils secrets très dangereux.La responsabilité aui nous incombe sera de mener une analyse complete pour identifier les outils extiltrés et déterminer l'identité de l'attaquant. Cette analyse va nous permettre de comprendre comment l'attaquant a pu reussir a compromettre le site. Et apres on va devoir donner des recommenations pour corriger ca pour les prochaines fois. Pour cela on va faire une analyse de logs qui va nous permettre de voir les outils infiltres et l'adresse IP de l'attaquant.

METHODOLOGIE

la methode utilise pour mettre en oeuvre notre analyse est une methode classique car on juste taper des commandes pour voir l'historique de la procedure de l'attaquant avec la commande cat .bash_history et ainsi on pu filtrer pour verifier l'activite des utilisateurs et les differentes requetes qu'ls ont eu a faire.
On a pu acceder au fichier access.log ou dedans on a pu voir les differentes requetes emises avec la commande cat access.log|grep -v "GET" et leur reponses on a pu observe des reponses 200 et des 404; puis on isoler les IP qui avaient ce genre de rponses et on a fait un grep de leur adresse IP dans le fichier error.log pour voir quel a ete l'etendu de leur erreur. On a pu reperer des adresses et parmi ces adresses il y'a une qui a servi a se connecter sur le site de Bosh cyber.

RESULTATS

De cette analyse, on a reperer les adresses 176.191.103.12, 140.238.48.138 et 138.66.89.12. Avec la derniere adresse on a pu voir q'il a cacher un dossier zip qui doit s'executer chaque jour et lui remonter les informations retrouves, Ce qui le permettra surement d'avoir les donnees sohaitees.
![image](https://user-images.githubusercontent.com/125276953/219060817-46aad95e-71dd-4153-b6ae-92e3ec43a51c.png)


CONCLUSION

Il s'agissait de faire une analyse des logs pour voir et verifier les outils infiltres et quel est l'adresse IP de l'attaquant

RECOMMANDATION

Mise en place d'une vérification automatique en CI/CD qui empêche le déploiement de l'application si elle est configurée en mode "debug", prévenant ainsi tout risque de compromission à l’avenir
Limiter l'acces au serveur 
Restreindre les modifications des donnees sur le serveur
Utiliser des outils de detection de vulnerabiltes 
Faire une analyse des logs tous jours pour voir si il y'a une ou des failles
Avoir des systemes de changement des mots de passe por plus de securite.

CONCLUSION GENERAL
Pour coclure de dirais que pour avoir une bonne securite il faut mettre en pratique les recommendation de l'ANSSI sur la protection des serveurs et aussi sur l'ensemble de notre systeme.
