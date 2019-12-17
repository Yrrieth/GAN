# GAN
M1 Informatique - Apprentissage automatique

Thierry WEN

Génération de visage

D'après la documentation et le programme pris sur :
https://medium.com/datadriveninvestor/generating-human-faces-with-keras-3ccd54c17f16

Données :
https://www.kaggle.com/gasgallo/faces-data-new
https://www.kaggle.com/gasgallo/lag-dataset

***
L'ensemble du dataset contient 11 682 images de visage.

Le modèle d'origine se trouve dans le dossier ```/original```. Ce dossier contient le programme d'origine ainsi que le résultat de la génération d'image produit par ce même programme dans le dossier ```/original/generated_images```.

L'architecture du réseau de neurone de ce programme est composé d'un générateur contenant 2 couches de conv2d contenant chacun 256 neurones puis 2 couches contenant 128 neurones.
Le discriminateur contient quand à lui 4 couches contenant succèssivement 64, 128, 256 puis 512 neurones.
Le programme s'éxécute avec en entrée des images de 64\*64 RGB avec une epoch de 4000 et l'éxécution du programme a nécessité environ **16h de compilation**.
Le programme génère tous les 100 epochs une image qui a était généré par le générateur et au préablement discriminé par le discrimateur.

***
Pour tester, j'ai modifié le générateur pour qu'il contient 4 couches contenant succéssivement 64, 128, 256 puis 512 neurones sans modifier le discriminateur. L'éxécution du programme a nécessitait environ **45h de compilation** (Je ne souhaite pas réitérer l'expérience).

