*This guide is licensed under the MIT license, you can view the license here: https://github.com/Hugo22O/A-Guide-To-Install-PRET-on-Termux/blob/master/LICENSE*

# A-Guide-To-Install-PRET-on-Termux
A guide helping you install PRET on Termux. 

After trying to install PRET on Termux I faced some problems, as I couldn't find a guide on how to install PERT on Termux I figured I could make my own and spare you an hour trying to install PRET. :D 

# Table of contents
* Table of conents
* Installing Termux on your device



## Installing Termux on your android device

*If you already have termux installed, go ahead and skip this step.*

Termux is an Android terminal emulator and Linux environment app that works directly with no rooting or setup required, we will be using Termux to run PRET. Download & install Termux from the playstore: https://play.google.com/store/apps/details?id=com.termux or F-Droid: https://f-droid.org/packages/com.termux/ After having Termux installed open up the app. 

## Installing Python 2 & Git

Alright, you now have Termux session open and it will look like this: 

![](https://puu.sh/CbMAs/52fe2813f6.png)

Type in the following: 
`pkg upgrade`
Then..
`pkg update`
After you've done that install Python 2 (__not version 3__) by typing: `pkg install python`
Then install git by typing: `pkg install git` 

If you've done everything correctly you have now installed python and git. 

## Installing colorama & pysnmp
For colored output and SNMP support we need to install the third party modules colorama and pysnmp which can be done by typing in: 
`pip2 install colorama pysnmp`

Colorama and pysnmp should now be installed, we can now get into the last 2 steps of installing PRET! 

## Downlaoding PRET with Git. 

Now we've installed Python2, colorama & pysnmp it is time to download PRET, you can do so by typing: `git clone https://github.com/RUB-NDS/PRET` PRET should now be ready for use. 

## How to run PRET? 

Open a Termux session and type in `cd PRET`, you should now be in the PRET folder. Once you're there type in `python2 pret.py` this will scann for printers on your local network that have an open port 9100. You can also add the following arguments:

```
usage: pret.py [-h] [-s] [-q] [-d] [-i file] [-o file] target {ps,pjl,pcl}

positional arguments:
  target                printer device or hostname
  {ps,pjl,pcl}          printing language to abuse

optional arguments:
  -h, --help            show this help message and exit
  -s, --safe            verify if language is supported
  -q, --quiet           suppress warnings and chit-chat
  -d, --debug           enter debug mode (show traffic)
  -i file, --load file  load and run commands from file
  -o file, --log file   log raw data sent to the target
  ```
  
  For more information on how to use PRET and the official source you can take a look here: https://github.com/RUB-NDS/PRET

## Troubleshooting

* Make sure you followed all steps listed above and installed the correct dependencies. 
* Make sure you type `python2` instead of `python` otherwise pret.py won't run. 
* If you're still getting an error/shebang try this: `export LD_PRELOAD=${PREFIX}/lib/libtermux-exec.so`
and then restart Termux session.

## Sources, Notes and/or referentions

* https://termux.com/ | 03/12/18
* https://github.com/RUB-NDS/PRET | 03/12/18
* http://hacking-printers.net/wiki/index.php/Main_Page | 03/12/18
* https://github.com/Hugo22O/A-Guide-To-Install-PRET-on-Termux | 03/12/18
  
# __!!! === GUIDE IS WIP &&& NOT DONE === !!!__
