# Automated-drip-irrigation-using-rasbery-pi
Introduction 

It is an automated system designed to take good care of your plants while you travel for a long time.The propose is to keep track of humidity levels and once in a while drip some water in your plants if they feel thirst. 

How the system works 

The concept is very simple, the system is composed by the following hardware:      

Arduino (I use the pro mini since it's tiny and you can weld according to your needs)      
Raspberry Pi as an interface to arduino (read sensors, upload new hex files if needed)      
Sensors      
Tiny pump      
Bucket with water      
Gardena micro dipping system      
Android phone to check the status of your plants 

The whole system is controlled by the arduino microcontroller. It checks the humidity sensors every cycle and sets a variable to true or false in case the sole conditions and amount of water on it. If it's dryi, according to a predefined threshold, it will drip water for few seconds or until the sole turns to hidratate enough.

How to use it

Import the Arduino file into an arduino IDE     
Import the android project to your IDE (I use eclipse)     
Copy the bridge file tcp_server.py into your raspberry Pi and set it up under your /etc/rc.local by adding the following line: (sleep 10;python /path/where/you/copied/tcp_server.py)&amp;  
