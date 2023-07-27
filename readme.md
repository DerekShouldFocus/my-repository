FRUIT CLASSIFIER

This model is used to predict CLASSIFY FRUITS. It is trained on an imagenet Resnet-18 model using transfer learning. IT CAN HELP YOU CLASSIFY FRUIT.
FRUIT CLASSIFYING DEMONSTRATION:
  [Imgur](https://i.imgur.com/BuyPuA4.jpg)
  [Imgur](https://i.imgur.com/74GRMHE.jpg)
  [Imgur](https://i.imgur.com/wENZTfO.jpg)
  [Imgur](https://imgur.com/a/71oz6WO.jpg)
## The Algorithm
The algorithim is used by uploading an image of a fruit. It uses a 2GB Jetson Nano, and so it uses it a preflashed SD card flashed from the NVIDIA webpage. It then sends the FRUIT to the transfer learning model. The transfer model then predicts your FRUIT. It will try to guess your FRUIT to the best of its abilities. Then it will print out the FRUIT with its confidence. It is up to the user to interepret the information (WHAT IS THE FRUIT).
Note: IT CAN BE USED TO SORT AND CLASSIFY FRUITS, WHICH IS IMPORTANT IN AN ENVIRONMENT THAT FORCES YOU TO EFFICIENTLY AND ACCURATELY IDENTIFY FRUITS.
## Running this project

1. Connect to your Jetson Nano via VSCODE. 
3. Ensure that you have the proper things installed. The Renet18.onnx and all others like that - the ones that say resnet18.onnx and the final_project2.py. Also, esure that you have the labels.txt file.
4. Since using teh preflashed SD card, there sould be a docker container. This is accesable by implementing this code. Change directories into jetson-inference/build/aarch64/bin. - use this code if your in the home.$ cd jetson-inference/build/aarch64/bin
5. Then run this code -$ ./docker/run.sh --volume /home/(username)/fruits:/fruits        - the code moves the fruits folder into the docker container so that the line from PIL import Image runs without an error.
6. Upload images by dragging them to the test folder and then running the command "imagenet.py --model=$NET/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=$DATASET/labels.txt $DATASET/test/[ your upload name].jpg [analysis file name].jpg

[View a video explanation here](video link)
