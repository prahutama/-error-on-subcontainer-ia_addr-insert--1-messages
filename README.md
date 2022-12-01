# systemd :

cp /lib/systemd/system/snmpd.service /etc/systemd/system/snmpd.service

sed -i 's/Lsd/LS6d/' /etc/systemd/system/snmpd.service

systemctl daemon-reload

systemctl restart snmpd

# Tanpa systemd :

sed -i 's/Lsd/LS6d/g' /etc/default/snmpd

sed -i 's/Lsd/LS6d/g' /etc/init.d/snmpd

service snmpd restart
