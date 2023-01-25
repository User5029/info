###ADBS using RTL-SDR

##Install

#Readsb
Respository: https://github.com/wiedehopf/readsb
Install Script: `sudo bash -c "$(wget -O - https://github.com/wiedehopf/adsb-scripts/raw/master/readsb-install.sh)"`

#Webpage
Respository: https://github.com/wiedehopf/tar1090#tar1090
Intsall Script: `sudo bash -c "$(wget -nv -O - https://github.com/wiedehopf/tar1090/raw/master/install.sh)"`

#Then reboot your machine


###The next section is only running the ADBS software when you want it

##Only run when you want it to

`sudo systemctl disable tar1090`
`sudo systemctl stop tar1090`
`sudo systemctl disable readsb`
`sudo systemctl stop readsb`

##Running the program 

`sudo systemctl start tar1090`
`sudo systemctl start readsb`

##Stopping the program

`sudo systemctl stop tar1090`
`sudo systemctl stop readsb`