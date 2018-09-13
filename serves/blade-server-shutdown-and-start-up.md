# Blade server shutdown and start-up

## **To shut down the servers**

1. ssh in to all client nodes `(192.168.0.57 – 192.168.0.67)` and run the shutdown command
2. Then ssh into master node `(192.168.0.56)` and run the shutdown command
3. Then access the Chassis management web Interface \(192.168.0.80\) and shut down the chassis power
4. Then go to the server room and turn off the 2 power switches from the ceiling \(make sure you turn of the right switches as I showed you last week\)
5. 
## **To turn on the servers**

1. Turn on the 2 power switches from the ceiling and wait until you get the front control panel display on the chassis
2. Press the chassis power button and wait for  few minutes until the chassis power status becomes active
3. Then press the server power button in the first slot \(this is the master node\) and wait for it to come online  - you can check the status by accessing the web page \` [https://192.168.0.56](https://192.168.0.56/)\`
4. Once the master node is up, press the power button on for all other nodes one by one and continue to check the cluster status by accessing the web page\` [https://192.168.0.56](https://192.168.0.56/)\`
5. Once you see all nodes online, ssh into all nodes and stop the sendmail client \(service sendmail stop\) on all nodes including the master node
6. Then on the client nodes \(not required on the master node\) update the routing table using the following command \(ip route add \`[192.168.199.222/32](http://192.168.199.222/32)\` via 192.168.0.250 dev eth1\)



