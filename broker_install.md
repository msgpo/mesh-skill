# Broker Installation

- 1)Open Raspberry Pi Terminal
- 2)Execute the following command to update the existing Packages
```
sudo apt-get update
```
- 3)Execute the following command to install mosquitto broker
```
sudo apt-get install mosquitto
```
- 4)Execute the following command to install MQTT Clients such as publishers and subscribers
```
sudo apt-get install mosquitto-clients
```
- 5)Execute the following command to check Mosquitto version.
If its showing mosquitto version 1.4.10 or higher , means broker is installed sucessfully.
#Broker +Configuration

- 1)Execute the following command to navigate in the mosquitto folder which is shown below.
```
cd /etc/mosquitto
```
- 2)Execute the following command to edit mosquitto.conf file which is shown below.
```
sudo nano mosquitto.conf
```

- 3)Now add following 3 lines in mosquitto.conf file which is shown below.
```
port 1883
listener 9001
protocol websockets
```
- 4)Once you above 3 lines please press Ctrl + X and type y and hit enter to save the changes.
- 5)Execute the following command to navigate to the alternate mosquitto configuration folder.
```
cd /etc/mosquitto/conf.d
```
- 6)Remove all files "alternate" configuration files in this directory.
```
sudo rm *.conf
```
- 7)Now you need to restart the mosquitto or MQTT broker. Execute the following command to restart mosquitto or MQTT broker which is shown below.
```
sudo service mosquitto stop
sudo service mosquitto start
```
- 8)Confirm the service started.
```
sudo service mosquitto status
```
- 9)Restart the RPi and again confirm the service started.
```
sudo service mosquitto status
```

