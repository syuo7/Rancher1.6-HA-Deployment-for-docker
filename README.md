# Rancher1.6-HA-Deployment-Guide for docker

# Requirment
You need at least 5 of the node(VM, BareMetal or Cloud)  
 * Every node requirment for Docker ( Recommend >=18.06 )

Requirment Port
* Between Master Node Connections
  * MariaDB(3306), MaxScale(3307), GaleraCluster(4444,4567,4568,5405)

# Architecture
![Rancher Deployment Architecture](/Rancher_Architecture.PNG?raw=true "Rancher Deployment Architecture")

  
# Installation Step
* Install the Below repo on 1st Node  ( First of Rancher Master node )
  * https://github.com/syuo7/rancher-master-1
* Install the Below repo on 2st Node  ( Second of Rancher Master node )
  * https://github.com/syuo7/rancher-master-2
* Install the Below repo on 3st Node  ( Third of Rancher Master node )
  * https://github.com/syuo7/rancher-master-3
* Install the Below repo on 4st Node 
  * https://github.com/syuo7/rancher-docker-keepalived-haproxy
* Install the Below repo on 5st Node 
  * https://github.com/syuo7/rancher-docker-keepalived-haproxy

# How to Run
## Run for Rancher HA Nodes
* ``docker-compose up`` on the 1st Node
* Wait for about 1minutes to complete running.
* ``docker-compuse up`` on the 2st Node
* ``docker-compose up`` on the 3st Node
## Run for HAproxy Nodes
* Read for the README guide following below Link and do it initial setup ( Priority, Interface, etc..).
  * https://github.com/syuo7/rancher-docker-keepalived-haproxy
* ``docker-compose up`` on the 4st Node
* ``docker-compose up`` on the 5st Node

Finally, Check for connecting to Rabcher UI via VIP.
Thanks.
