-----------------------------------Setuo configuration-------------------------------

Configuration: Windows 7, port COM3 , ATmega 328

------------------------------------------------------------------------------------
Configuration: Linux Ubuntu 14.04 , port USB0 , ATmega 328

install Arduino IDE links:
- http://blog.opensensors.io/blog/2014/09/13/getting-started-with-arduino-on-linux/
- http://ubuntuhandbook.org/index.php/2015/11/install-arduino-ide-1-6-6-ubuntu/

install Arduino IDE in command line:
~$ sudo apt-get update && sudo apt-get install arduino arduino-core
~$ arduino

** if need config Java 
~$ sudo update-alternatives —config java


++++++++++++++++++++++++++++++++++++Usage+++++++++++++++++++++++++++++++++++++++++++


SETUP MANUAL http://arduino.ua/ru/guide/Libraries


TIME & TEMPARATURE LIBRARY

http://knodit.blogspot.com/2014/05/arduino-ds3231.html - link on tutorial

put files from DS3231_TEST to:

 - C:\Users\admin\Documents\Arduino\libraries\time_temper  - on Windows
 - /home/<username>/Arduino/libraries - on Linux

as

C:\Users\admin\Documents\Arduino\libraries\time_temper\DS3231.cpp
C:\Users\admin\Documents\Arduino\libraries\time_temper\DS3231.h

and use


RELEY LIBRARY 

Simple example: http://zelectro.cc/relayModule
Full example: https://www.aqa.ru/forum/ARDUINO-dlya-avtomatizatsii-akvariuma-268157-page1


ВОЗМОЖНЫЕ ERROR on Linux:

1)DE error - avrdude: ser_open(): can't open device "/dev/ttyACM0": Permission denied

	FIX on Linux: 
	$ sudo usermod -a -G dialout <username>  - заменить <username> 
	$ sudo chmod a+rw /dev/ttyACM0  - заменить имя порта ttyACM0  если нужно например USB0

	http://arduino-er.blogspot.com/2014/08/arduino-ide-error-avrdude-seropen-cant.html

