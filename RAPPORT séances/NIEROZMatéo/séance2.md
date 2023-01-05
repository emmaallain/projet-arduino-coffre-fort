Lors de cette séance, je me suis occupé du servomoteur pour vérouiller ou dévérouiller la porte de notre coffre. J'ai donc effectuer des recherches sur internet pour
(en premier lieu) le faire fonctionner.
https://ledisrupteurdimensionnel.com/arduino/controler-un-servomoteur-avec-une-plaque-arduino-servo-sg90/

On obtient: 

![image](https://user-images.githubusercontent.com/119796961/210824330-351aa59c-93e2-4842-b7fe-4b9ff34da277.png)

et le code dans "Morceaux de codes".

Dans le code pour le servomoteur, j'ai du installer une bibliothèque <Servo.h>, puis j'ai appris ce qu'était le "attach" en arduino, cela veut dire tout simplement que ça attache un objet de type Servo à une broche spécifique 9 ou 10! Puis on utilise une boucle for pour faire foncnctionner le servomoteur:

-for (positionDuServo = 0; positionDuServo <=180; positionDuServo++) pour faire une demie rotation dans le sens antihoraire.
- for(positionDuServo = 180; positionDuServo >= 0; positionDuServo--) pour faire une demie rotation dans le sens horaire.

Le resultat et que l'hélice tourne en continue, sur la photo, c'est un moteur à rotation continue qu'on à changé juste après par un servomoteur. Nous avons donc les rotations et il fallait ensuite comprendre comment l'utiliser pour notre coffre puis il a fallu connecter avec le code d'Emma pour pouvoir déclencher 1/4 de rotation si le mot de passe est valide et ainsi dévérouiller la porte.

J'ai donc effectuer le montage du servomoteur avec l'ecran lcd et le keypad:

![image](https://user-images.githubusercontent.com/119796961/210830069-017d02b1-dd3c-4e25-a6cd-84aa8cd03337.png) . 

j'ai effectuer des recherches avec Emma pour comprendre comment relier le code du servomoteur avec le reste (++ partie Emma).
La principale difficuté était que le moteur ne s'arretait pas de tourner puis il y avait des erreurs de code qu'on a résolu, ce lien nous a aider :https://drive.google.com/drive/folders/1JuVGipwd0wnzirywer-KwHxcv9DY0xW8


et a la fin du TD, on a reussi à obtenir ceci: https://youtube.com/shorts/78rOJIli7kU?feature=share

Comme l'a dit Emma, au prochain TD, on s'occupera de la position initiale du moteur à l'interieur du coffre, on continuera notre code biensur pour finir la partie Mot de passe et ouverture/fermeture du coffre. Puis on commencera la partie bluetooth ou alors le moyen de paiment.


http://www.mon-club-elec.fr/pmwiki_reference_arduino/pmwiki.php?n=Main.Servoattach
