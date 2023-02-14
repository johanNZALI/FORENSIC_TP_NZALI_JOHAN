De nos jours la securite est tres primordiale pour chacun et chaque entreprise et par rapport a ca tout disque externe ou mail recu est analyse. comme le montre notre sujet nous devons analyser une cle USB retrouve et donc par la suite je vais vous montrer comment est ce qu'on procede pour faire cela.

Dans notre cas on a un dossier .zip et a l'interieur de cela il ya l'image de la cle USB en question, il faut tout dabord mettre ce dossier .zip dans notre machine virtuelle. Etant dans notre machine virtuelle on de-zip le dossier et on se met sur le terminal de la machine en mode root et on accede au dossier en ligne de commande. Etant dans le dossier deziper on tape la commande apt install foremost,
![image](https://user-images.githubusercontent.com/125276953/218676554-529257fa-ff55-4373-9a76-98c035ddf031.png)

Foremost est une application pour analyser les disques externes. Lorsqu'on la installer on analyse donc l'image avec la commande foremost USB_Image, ensuite on fait un ls et on accede au output puis dans le output on liste et on accede au png.
![image](https://user-images.githubusercontent.com/125276953/218677026-71b4185c-fb1f-4a07-9dd5-4bdb26b85871.png)


Etant dans ce repertoire on liste pour voir les image qui y sont et on tape la commande eog pour lire les differentes images et ainsi on arriva a retrouver le flag qui se trouve dans l'image 00016520.png et dans l'image 00040392.png.
![image](https://user-images.githubusercontent.com/125276953/218572264-6a1b7da5-d1ab-424f-983f-809635f5a1b8.png)

Ainsi on aura analyser la cle USB retrouver avant de l'inserer sur un ordinateur.
