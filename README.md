# GAN
M1 Informatique - Apprentissage automatique

Thierry WEN

Génération de visage

D'après la documentation et le programme pris sur :
https://medium.com/datadriveninvestor/generating-human-faces-with-keras-3ccd54c17f16

Données :
https://www.kaggle.com/gasgallo/faces-data-new
https://www.kaggle.com/gasgallo/lag-dataset

L'ensemble du dataset contient 11 682 images de visage.

***
### Modèle d'origine

Le modèle d'origine se trouve dans le dossier ```/original```. Ce dossier contient le programme d'origine ainsi que le résultat de la génération d'image produit par ce même programme dans le dossier ```/original/generated_images```.

L'architecture du réseau de neurone de ce programme est composé d'un générateur contenant 2 couches de conv2d contenant chacune 256 neurones à la ligne 97 et 102 puis 2 couches contenant 128 neurones à la ligne 107 et 112.

Le discriminateur contient quand à lui 4 couches contenant succèssivement 64, 128, 256 et 512 neurones.

Le programme s'éxécute avec en entrée des images de 64\*64 RGB avec une epoch de 4000 et l'éxécution du programme a nécessité environ **16h de compilation**.
Le programme génère tous les 100 epochs une image qui a était généré par le générateur et au préablement discriminé par le discrimateur.

***
### Ma contribution

Le programme se situe à la racine du dossier.

Par rapport au modèle d'origine, j'ai modifié le générateur dans la fonction ```build_generator()``` à la ligne 82 pour qu'il contient 4 couches de conv2d, respectivement à la ligne 97, 102, 107 et 112, contenant succéssivement 64, 128, 256 et 512 neurones sans modifier autre chose.

J'ai modifié de tel sort que chaque couche du générateur contient le même nombre de neurone que chacune des couches du discriminateur, pensant naïvement qu'en augmentant le nombre de neurone, le générateur produirait de meilleure image.

L'éxécution du programme a nécessitait environ **45h de compilation** (~~Je ne souhaite pas réitérer l'expérience~~).