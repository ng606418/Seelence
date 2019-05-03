* Séance du 01/04 et 05/04 : 
Préparation de la présentation intermédiare du projet et impressions des lunettes avec les imprimantes 3D à notre disposition et avec mes compagnons, création du modèle initial des lunettes.





* Séance du 08/04 : 
Présentation  intermédiaire du projet, avec présentation des lunettes imprimée en 3d et cencée être la base de notre projet "Seelence".
Les pièces n'ayant pas été reçu en ce jour nous n'avons pas pu connecter les capteurs audio comme voulu.





* Séance du 15/04 : 
Récéption des pièces dont deux capteurs audio différents, c'est à nous de les tester et de choisir le plus optimisé à notre projet.

J'ai passé la séance a comprendre et à essayer de faire foncitonner un écran OLED avec les librairies adafruit arduino présent sur Github 

![Ecran](https://startingelectronics.org/tutorials/arduino/modules/OLED-128x64-I2C-display/geekcreit-128x64-oled-display-demo.jpg)

L'écran fonctionne suite à plusieurs test avec un code exemple présent dans la libraire adafruit.(https://github.com/adafruit/Adafruit_SSD1306) et (https://github.com/adafruit/Adafruit-GFX-Library)
(screen du code)
Nous n'avons pas encore toutes les pièces





 
* Séance du 19/04:
J'ai réussis à coder l'écran, il s'avère qu'il n'y a rien de bien compliqué, il suffit de "print" les variables voulu à l'écran sans pour autant faire de boucle ou autre mais il faut bien faire attention à bien identifer l'écran I2C dans le code ainsi que l'adresse de l'écran pour le bon fonctionnement.

![écrancode](https://cdn.discordapp.com/attachments/174213561319555072/573799237054365717/unknown.png)





* Hors séance: 
J'ai travaillé le code Arduino sur un Arduino uno à mon domicile. En mle rensaignant j'ai pu comprendre le fonctionnement des capteurs sonore KY-038(BIG SOUND), ils contiennent deux broches de lecture, une analogique et une digitale .
Ce qui nous intéresse et celle de lecture analogique car elle nous renvoie une valeur numérique entre 0 et 1023 selon l'intensité du son détécté ( en théorié ). 
Mais malheureusement aucun de nos capteurs n'a permit ce bon fonctionnement et ce problème va nous suivre tout au long de la conception.
J'ai dû trouver différentes manières de coder l'arduino pour permettre de détecter et de différencier la position spatial avec les prises digitales et non analogique.( digital : Tout our rien ==> 0 ou 1 )
Mais le mardi 30 avril j'ai trouvé un moyen de lire plus précisément la broche analogique à l'aide de la digitale.

![solution](https://cdn.discordapp.com/attachments/174213561319555072/573799730384207873/unknown.png)





* Hors séance 30/04 :
Au lieu de calibrer les capteurs sur une détéction classique qui en suit l'allumage de la LED témoin et une lecture en continue des perception sonore avec un seuil d'activation. 
"If analogRead(analogPinD) > 550) --> digitalWrite(ledPinD, HIGH);"
J'ai plutôt fais ensorte de lire digitalement avec une fonctioif et dans ce cas là, je lis analogiquement les valeurs reçus et je les compare entre les deux captuers si il y	a une détection des deux capteurs	alors le code va comparer la récetption des deux et voir lequel à détecter une valeur plus importante pour allumer sa led équivalente.									 
Si il n'y a pas de détection sur les deux mais un seul la comparasion analogique est inutile il n'y aura plus qu'à allumer la LED equivalente.

J'ai pu intégrer au code, le Code example donné au cours du TP2 pour permettre d'envoyer les données perçu par le capteur sur un poste central pouvant servir au caloibrage de détection des capteurs et ainsi avoir une idée de la détections exact sur le moniteur en série	 arduino.

En utilisant un deuxième Arduino en réception nous avons pu faire le pont entre les lunettes et le moniteur en série arduino sur le PC.
 * Hors séance 02/05 :
Montage intégrale des lunettes :
![lunette 1](https://scontent-mrs2-1.xx.fbcdn.net/v/t1.15752-9/s2048x2048/59569075_1296272177195489_4285080633471926272_n.jpg?_nc_cat=106&_nc_ht=scontent-mrs2-1.xx&oh=d1af8e4f488eed18e5a41320500cb18d&oe=5D2CA0B7)

![lunette 2](https://scontent-mrs2-1.xx.fbcdn.net/v/t1.15752-9/s2048x2048/59520767_823895367963244_4504789994736451584_n.jpg?_nc_cat=106&_nc_ht=scontent-mrs2-1.xx&oh=be868f81645a156edee68bca2789f52d&oe=5D6219B0)

![lunette 3](https://scontent-mrs2-1.xx.fbcdn.net/v/t1.15752-9/s2048x2048/59301216_451880292251900_891033322522673152_n.jpg?_nc_cat=102&_nc_ht=scontent-mrs2-1.xx&oh=c87ceae44e0fbc1ee9596db20ad66fd5&oe=5D700E31)


* Présentation du projet Vendredi 03 Mai 14h30.

-----------------------------------------------------------------------------------------------------------------------------------
