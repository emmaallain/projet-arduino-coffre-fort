EN COMMUN. Notre travail durant cette séance c’est porté sur le fonctionnement de l’écran et du key-pad de notre coffre-fort. Mais aussi sur la conception du coffre, allons-nous faire une porte a aimant ? Une Système de monnaie ? Pour la porte, nous allons plutôt utiliser un servomoteur car on peut l’utiliser en 5V, pas comme l’aimant (12V). Et pour le système de paiement, nous utiliserons des jetons grâce aux capteurs lasers et non des pièces car c’est assez complexe.
Ensuite pour ce qui est de ma partie, j’ai essayé de comprendre le fonctionnement du clavier matricielle 4x4. Pour cela j’ai dû inclure dans mon programme une bibliothèque< Keypad.h> afin de pouvoir utiliser les fonctionnalités de celui-ci et de le reconnaitre. 
Le clavier se connecte directement sur la carte Arduino. On va récupérer les informations du clavier sous forme de matrice qui va se traduire automatiquement en caractère du clavier. 
Dans chaque étape j’ai mis un Serial.begin() pour voir ce qu’il se passait.  
Dans le voidloop on inscrit dans une variable ce que on va acquérir. 
On voulu commencer à tester les mots de passe. On a rencontré un problème au moment de tester si le mot de passe mis était également le mot de passe initialement prévu. Car quand on acquiert l’information c’est un caractère et non un string du coup on ne pouvait pas comparer. Il fallait juste convertir la donnée en string. 
Ensuite on a mis en commun nos deux programmes pour connecter l’écran LCD au clavier. On a donc rajouté au code des LCD.print(key). 
On a également commencé a rajouté une propriété sur la touche « c » qui va supprimer tout le texte écrit sur l’écran. 

![image](https://user-images.githubusercontent.com/119605830/207627820-3fd78aa0-6bda-47bd-aead-5aea52b29e62.png)

![image](https://user-images.githubusercontent.com/119605830/207630702-6acc5933-8461-4c76-9f67-26d144a5b08e.png)

![image](https://user-images.githubusercontent.com/119605830/207631184-81eb49f2-3e0c-4930-baae-ec695f486214.png)

Sources: https://arduino-france.site/lcd-1602/#5
https://forum.arduino.cc/t/conversion-char-en-string/301946

