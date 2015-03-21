#How-To

# Simplest library for displaying animated GIF and Images on same ImageView #

Library has been implemented to be the simplest yet strongest of options available out there...
You can display animated gifs with various configurations and also display Image view with all possible default support of Android for ImageView using a single View Component.


# Implementation #
**AnimatedGifImageView** is the View class that is derived from ImageView. Therefore along with supporting all features for ImageView it also supports AnimatedGifs.

Library provides overloaded methods for setting your GIF you can use _` setAnimatedGif(String filePath, TYPE streachType) `_ or _` setAnimatedGif(int rawResourceId, TYPE streachType) `_ or _` setAnimatedGif(byte[] byteArray, TYPE streachType) `_ depending on your requirements.

Checkout the sample for more details.