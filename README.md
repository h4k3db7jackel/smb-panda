# smb-panda
################-find thousands of vulnerable eternalblue targets in just 15 minutes-##################

	...$$$$$$\................$$$$$$$\............................................$$\...........
	..$$..__$$\...............$$..__$$\...........................................$$.|..........
	..$$./..\__|$$$$$$\$$$$\..$$.|..$$.|.......$$$$$$\...$$$$$$\..$$$$$$$\...$$$$$$$.|.$$$$$$\..
	..\$$$$$$\..$$.._$$.._$$\.$$$$$$$\.|......$$..__$$\..\____$$\.$$..__$$\.$$..__$$.|.\____$$\.
	...\____$$\.$$./.$$./.$$.|$$..__$$\.......$$./..$$.|.$$$$$$$.|$$.|..$$.|$$./..$$.|.$$$$$$$.|
	..$$\...$$.|$$.|.$$.|.$$.|$$.|..$$.|......$$.|..$$.|$$..__$$.|$$.|..$$.|$$.|..$$.|$$..__$$.|
	..\$$$$$$..|$$.|.$$.|.$$.|$$$$$$$..|......$$$$$$$..|\$$$$$$$.|$$.|..$$.|\$$$$$$$.|\$$$$$$$.|
	...\______/.\__|.\__|.\__|\_______/.......$$..____/..\_______|\__|..\__|.\_______|.\_______|
	..........................................$$.|..............................................
	..........................................$$.|..............................................
	..........................................\__|..............................................



the fastest way to find eternalblue targets on kali linux

(probably gonna have a shit tone of bugs and problems cause it took me less than an hour to make)

run it then add your ip address range (only 1 range at a time (example 74.35.0.0/12))

uses multiple other github tools 

=========================requirements============================


1: masscan 


all ya got to do is install the kali repository in the /etc/apt/sources.list file
 
 	'apt update' 
  
	'apt install masscan'


2: python 


you should already have this installed on kali but if you dont just fucking google it people


3: golang

	'apt install golang'

=============================how to use it=================================

	python main.py

	then put your range 

=============================how it works================================

it basicaly uses masscan to find ip addreses that have port 445 open 

then filters the output so that it only shows the open ip address line by line  

then adds 'go run ignore.go'  before each ip address  

then it saves the output as a .sh file

then it runs the .sh file whitch will scan those ip addresses to se if it has a vulnerable version of smb

then it will tell you what is fulnerable and what has a safe version of smb
