

sudo raspi-config

-> Interfacing -> SPI aktivieren
-> Interfacing -> seriell: Hardware UART aktivieren
optional -> Network -> Wifi credentials

sudo apt-get update
sudo apt-get upgrade
sudo apt-get install git

Im Homeverzeichnis:
git clone -b spi https://github.com/anyn99/ic880a-gateway.git
cd ic880a-gateway
sudo ./install.sh spi

cd /opt/ttn-gateway/bin
-> local_conf.json wie benötigt ändern