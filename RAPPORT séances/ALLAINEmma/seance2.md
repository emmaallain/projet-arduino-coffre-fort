Pendant la deuxième séance, on a rendu le programme lié à l’cran et au keypad plus complet voir dans morceaux de code LCD keypad servo moteur :
-si la carte ne contient aucun mot de passe sauvegardé, alors on demande à l’utilisateur de choisir son mot de passe détail à régler, 
on affichera par la suite des étoiles à chaque chiffre choisi.

-si la carte contient un mot de passe alors on demande à l’utilisateur de le rentrer.
Problème rencontré :je n’arrive pas à afficher « saisir mot de passe » à l’instant où le mot de passe choisi est validé. 
Soit il s’affiche tout le temps de la loop, soit il s’affiche que dans le « if key ».

-si l’utilisateur appuie sur A alors on valide le mot de passe saisi et on regarde si il est bon ou non. 

-si il est bon, on affiche « password okay » « door open »

-si il est pas bon, on lui demande de réessayer. Par la suite on comptera le nombre de tentatives pour envoyer une alarme sur le téléphone du propriétaire si ça se veut récurrent.

J’ai essayé dans le code d’insérer un autre void créermdp(). Mais je n’ai pas réussi alors j’ai inséré une boucle while. 

Ensuite on a également testé le servomoteur et son fonctionnement, pour ensuite pouvoir penser à comment ouvrir et fermer la porte. 
Il a fallu télécharger une libraire <servo.h> pour bénéficier de toutes les fonctionnalités. 
On a rencontré un problème, on s’est rendu compte que le servomoteur fourni était à boucle infini et ne pouvait s’arrêter tandis que dans 
notre situation on voulait un servo moteur qui tourne d’un point A à un point B puis qui se stabilise. On a donc changé de servomoteur SG90.

Une fois que nous avions compris le fonctionnement, on a intégré une première partie au code principale, en lui disant que si le mot de passe était bon alors il devait tourner à 90degrés. 
De plus si  l’utilisateur appuie sur la touche « # » alors la porte se refermedes modifications vont être apportées car on va probablement devoir 
définir une position initiale du moteur qui sera liée à notre système d’ouverture. 

https://www.carnetdumaker.net/articles/controler-un-servomoteur-avec-une-carte-arduino-genuino/
