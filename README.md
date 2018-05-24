RASPI HONEYPOT
==========

Script for running a Honey Pot Raspberry Pi

To install, copy these scripts to your Raspberry Pi and execute:
chmod +x ./*.sh
./honeypotcreate.sh 

To start the XRDP honeypot run the following command:
./honeypotstart.sh
(or the actual xrdp command)
sudo /etc/xrdp/xrdp.sh start

The login of failed attempts will be located at:
/var/log/xrdp.log

You can filter for failed logins in a very crude manner:
./honeypotloggedcredentials.sh
(or the actual xrdp command)
sudo cat /var/log/xrdp.log | grep USER:

...and check the raw log by typing:
./honeypotrawlog.sh
(or the actual xrdp command)
sudo cat /var/log/xrdp.log

If you would like to have some live monitoring, which shows the logged credentials and the current date every 30 seconds, type:
./honeypotmonitor.sh

