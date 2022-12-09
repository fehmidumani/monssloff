# monssloff
 Monitoring ssl offload specific case

● What to monitor and how 

On SSL offloading server with a Hardware:

● 4 times Intel(R) Xeon(R) CPU E7-4830 v4 @ 2.00GHz
● 64GB of ram
● 2 tb HDD disk space
● 2 x 10Gbit/s nics

● Around 25000 requests per second are handled with the server.


**Intro**

Creating SSL offloading helps keeping web server running smoothly. In our case, since there are 25000 requests per second and only have 2x 10 Gbps interfaces (10 Gbps max traffic from internet), we assume that the average size of the packets serving will not be larger than 48kB. 


**What to monitor?**

First check the server for the availability.
Check key services for the availability.
Check the resource for the possible bottleneck, 

The resources are divided into two categories:
On the variable ressources for the SSL Offloading server such as CPU, RAM, Bandwidth. 
And the other one with constant resources or the resources not changing frequently.

Note. Since our system only has capacity for 10 Gbps traffic incoming from the internet and 10 Gbps for the traffic toward web server, make sure that you pay more attention to the bandwidth usage. In our case it is noted that the server should have enough processing power (total of 56 cpu cores), As well as 64GB of RAM should be plenty.


**How to monitor?**

Use any fault management/monitoring tool such as Nagios/Zabbix and either get the statistics via:
Agents such as NRPE,
SNMP walk or
SNMP traps if you want to be botherd only in case of an event.

You can also make custom script to gether the info from your system.

Thank you.
