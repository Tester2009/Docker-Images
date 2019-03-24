# Firebase Tools
A docker to use Firebase Tools.

## Guide

1. Download ```Dockerfile``` from this folder.

2. Go to directory where the ```Dockerfile``` is, and put in new folder name ```Firebase_Tools_Container```

3. Open up terminal and go to the Firebase_Tools_Container directory. Run following command. ```docker build -t firebase_tools_container .``` . It will take some time to update and install required stuff.

4. Check if the image is there, with command ```docker images```. You should see your image named ```firebase_tools_container```.

5. Create your container and open up the port 9005 on both side, so when you want to login to firebase, it will redirect to your docker back. Run following command: ```docker run -it -p 9005:9005 firebase_tools_container```

6. Now your container is up and you are inside linux interative tty. Load up command ```firebase login``` to start login to your GMail.