# Check-RAM-as400-for-Centreon

## Description
A simple shell script to check the ram usage of an IBM i (AS400) server. This is intended for the monitoring tools Centreon.
It uses the Simple Network Management Protocol (SNMP).

It also produce performance data for graphical representation in Centreon.

## Download
To download the pluggin run this command in your pluggin folder :
```
wget https://raw.githubusercontent.com/CorentinTh/Centreon-Check_RAM_as400/master/check_as400_ram
```

## Usage
Run the script using this syntaxe :
```
./check_as400_ram <host_address> <snmp_community> <snmp_version> <critical_threshold> <warning_threshold>
```
* `host_address` : the IP address or the DNS of the server you want to check
* `snmp_community` : the SNMP community
* `snmp_version` : the SNMP version
* `critical_threshold` : the percentage of used RAM that will trigger a CRITICAL message
* `warning_threshold` : the percentage of used RAM that will trigger a WARNING message

## Output exemple
Here is an exemple of the command :
```
./check_as400_ram 192.168.1.114 MyCommunity 1 90 80
OK : RAM, used : 58031172 Kb (43 %), free : 76055484 Kb (56 %) on 134086656 Kb | "used"=58031172;0:26114027;0:29015586;0;0
```

## Credit 
Inspired by this programm : https://www.netexpertise.eu/fr/reseau/supervision/monitorer-ressources-as400-mrtg.html
