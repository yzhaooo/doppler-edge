# doppler-edge

## system description

### WiFi network setup

TP-link router setup:
192.168.0.1
admin/admin

Router Settings:
            WAN Connection Type:		Dynamic IP
            Network Name (SSID):		occupancy
          Network Security Type:		Most Security (WPA2-PSK)
           Network Security Key:		occupancy

static ip of the beaglebone black:
192.168.0.103
log in beaglebone:
ssh root@192.168.0.103

static ip of the raspberry pi:
192.168.0.200
log in raspberry:
ssh pi@192.168.0.200
raspberry

setup static ip on raspberry:
Edit /etc/dhcpcd.conf following: http://raspberrypi.stackexchange.com/questions/37920/how-do-i-set-up-networking-wifi-static-ip

login beaglebone: root
run: python acq_buffer_two_web.py
make sure web service is running in background (webserver2.py): ps -ef | grep python
http://192.168.0.103/index.html
