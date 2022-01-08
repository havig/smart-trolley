This project is part of the coursework in SRM IST with subject code 15EC496L : Major Project. In this project, a smart trolley was designed  with automatic billing and storage system so that shopping can be done easier and quicker.
 Various components like barcode scanner, camera and load cell are embedded in the trolley networking them with the common server. Certain products have bar code readers which are billed using a bar code scanner.  The rest of the products (loose items) like fruits and vegetables are classified based on the image processing algorithm. The image is captured and classified in the common server and based on this classification the items are billed with respect to its weight, measured using a load cell.  
 Moreover,  once a person enters a specific lane,  all the items in that lane are displayed on an LCD screen based on RFID technology attached to each trolley and lane. This is done for the person to easily identify where each commodities are in the aisle. The payment option is done though electronic payments within the trolley itself.
 
 All the python files are included and these are to be run on a raspberry Pi 4 after it's initial setup. The image classification can be trained in a GPU. During run time, the image is sent to server and tested there. The corresponding hardware required and it's logic diagram is included in the report or can be requested to either of the collaborators.
 
Image_classification.py : Training and Testing the fruit/vegetable classification method. Convolution Network Model used is VGG 16 which has been trained for 100 epoch with 5 different classes (can be increased if needed).

Guiwithlogin.py : The Graphical User Interface when the user picks up the cart with username, password and other credentials.

Loadcellexec.py : Calculates the weight of the commodity placed on it.

rfidread.py and rfidwrite.py : Scans fo RFID tags and to find the correct card for it to display what's in the aisle.

server.ipynb : The image is sent to the server using TCP/IP protocol for classification. One end is the sender and the other is the receiver.
