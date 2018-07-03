# The Things Network: RAK831-based gateway

## Setup based on Raspbian image

- Download [Raspbian Stretch Lite](https://www.raspberrypi.org/downloads/raspbian/)
- Follow the [installation instruction](https://www.raspberrypi.org/documentation/installation/installing-images/README.md) to create the SD card
- [Enable one-time SSH](https://www.raspberrypi.org/blog/a-security-update-for-raspbian-pixel/)
- Use `raspi-config` utility to

        $ sudo raspi-config

    - **Enable SPI** (`5 Interfacing Options -> P4 SPI`)
    - **Enable SSH** (`5 Interfacing Options -> P2 SSH`)
    - Set hostname (`2 Network Options -> N1 Hostname`)
    - Change locale (`4 Localisation Options -> I1 Change Locale`)
    - Change timezone (`4 Localisation Options -> I2 Change Timezone`)

- Make sure you have an updated installation and install `git`:

        $ sudo apt-get update
        $ sudo apt-get upgrade
        $ sudo apt-get install git

- Clone the installer and start the installation

        $ git clone https://github.com/kuanyili/rak831-gateway.git ~/rak831-gateway
        $ cd ~/rak831-gateway
        $ sudo ./install.sh

## Update

If you have a running gateway and want to update, simply run the installer again:

        $ cd ~/rak831-gateway
        $ git pull
        $ sudo ./install.sh