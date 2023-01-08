###RTL-SDR install on Linux Mint

##Commands:
sudo apt-get update
sudo apt-get install cmake libusb-1.0-0.dev git build-essential -y
git clone git://git.osmocom.org/rtl-sdr.git
cd rtl-sdr/
mkdir build
cd build
cmake ../ -DINSTALL_UDEV_RULES=ON
sudo make && sudo make install
sudo ldconfig
sudo cp ../rtl-sdr.rules /etc/udev/rules.d/

##Prepping your sdr
First you will need to create a new file `blacklist-rtl.conf` in the directory `/etc/modprobe.d`

sudo nano /etc/modprobe.d/blacklist-rtl.conf
ADD this one line `blacklist dvb_usb_rtl28xxu`

##Now save the config file and restart your machine


##Testing the SDR
rtl_test -s 2400000

