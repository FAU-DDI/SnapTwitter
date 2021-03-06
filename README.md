# SnapTwitter

This version of SnapTwitter is no longer actively maintained. It has been replaced by a completely reprogrammed version: https://github.com/AGrillenberger/SnapTwitter2

# Old description

## What is SnapTwitter?
SnapTwitter is an extension for the Snap! programming environment ([snap.berkeley.edu](http://snap.berkeley.edu)).

If you want to use this tool in school, feel free to contact me at andreas.grillenberger@fau.de for further information. I am very interested in your feedback on this tool and how you use it in school. Hence, I would appreciate if you contact me and answer me some questions on how you use it.

## What are the requirements for using SnapTwitter?
* Java runtime installed
* internet connection
* Twitter account as this is required for accessing the Twitter API

## How to use SnapTwitter?
SnapTwitter can be downloaded at <http://inf.fu-berlin.de/~grillenb/SnapTwitter-current.zip>

1. Start SnapTwitter by double clicking on  ``SnapTwitter.jar`` or by using the command ``java -jar SnapTwitter.jar`` in the Windows command line or Linux/MacOS terminal.
2. Snap! should load automatically in your default browser with the SnapTwitter blocks preloaded. If this is not the case, start it using http://snap.berkeley.edu/snapsource/snap.html#open:http://localhost:13337/getBlockXML
3. Check if the SnapTwitter blocks were loaded: e.g. there should be a "twitter: prepare" block in the _control_ section

If Snap cannot be started, often using the SnapTwitterNoHTTPS version in step 1 helps.

## Offline usage
SnapTwitter can be used offline when a tweet cache was created. To create such a cache, start SnapTwitter with the parameter ``--createCache`` (``java -jar SnapTwitter.jar --createCache``). Every tweet arriving at the tool will be serialized and stored in a TweetCache file. Hence, after starting SnapTwitter in online mode, you need to start Snap, use the prepare block to authenticate with twitter and connect to the stream with the respective block. When the tweets received counter in SnapTwitter is high enough, you can quit SnapTwitter, then the cache is being written to the file ``tweetCache.ser``in the SnapTwitter folder. Afterwards, using SnapTwitter in offline mode is possible without additional steps.

### Example program
The following images show a small example program using the SnapTwitter blocks. First, after pressing the key ``p``, it establishes a connection to Twitter and initiates the authentication mechanisms (``twitter: prepare``). After pressing ``space``, it connects to the twitter stream (``twitter: connect to stream``), initializes a map view (``twitter: stamp map image``) and then processes all received tweets usijng the ``twitter: for each tweet``. All these tweets are visualized on the map using the ``twitter: show tweet ___ on map`` block, until the key ``s`` is being pressed and the program disconnects from the twitter stream (``twitter: disconnect from stream``)

![Image of example blocks 1](http://fau-ddi.github.io/SnapTwitter/images/example-block1.png) ![Image of example blocks 2](http://fau-ddi.github.io/SnapTwitter/images/example-block2.png) ![Image of example blocks 3](http://fau-ddi.github.io/SnapTwitter/images/example-block3.png) 

## Materials
An example working sheet (in German) and an example program can be found in the "material" folder.

## Contact
Feel free to contact me with questions and ideas concerning SnapTwitter or data management in schools in general:

Andreas Grillenberger  
Computing Education Research Group  
Friedrich-Alexander-Universität Erlangen-Nürnberg  
andreas.grillenberger@fau.de
