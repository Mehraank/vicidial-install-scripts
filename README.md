# VICIDIAL INSTALLATION SCRIPTS (Default is Eastern Time Zone US)
# Centos, Rocky and AlmaLinux Vicidial Install pre_requisites 

```

hostnamectl set-hostname xxxxxx.xxxxx.xxx
### Use YOUR SubDomain

vi /etc/hosts
##Change domain name for actual server ip (xxx.xxx.xxx.xxx   complete domain name    subdomain only)

timedatectl set-timezone America/New_York

yum check-update
yum update -y
yum -y install epel-release
yum update -y
yum install git -y
yum install -y kernel*

#Disable SELINUX
sed -i 's/SELINUX=enforcing/SELINUX=disabled/g' /etc/selinux/config    

reboot

````
  Reboot Before running this script

# Install VICIDIAL scripts

```
cd /usr/src/
git clone https://github.com/Mehraank/vicidial-install-scripts.git
cd vicidial-install-scripts
```

# Alma/Rocky 9 Installer with Dynamic portal, ViciPhone, SSL Cert and Asterisk 16

```
chmod +x alma-rocky9-ast16.sh
./alma-rocky9-ast16.sh
```

Make sure you update your SSL cert location in /etc/httpd/conf.d/viciportal-ssl.conf



# Install a default database with everything setup ready to go

```
chmod +x standard-db.sh
./standard-db.sh
```


# Alma 8 Add on telephony server for a cluster

```
chmod +x Vici-alma-dialer-install.sh
./Vici-alma-dialer-install.sh
```

# Execute Centos7 Vicidial Install
```
chmod +x vicidial-install-c7.sh
./vicidial-install-c7.sh
```

# Execute Alma/Rocky 8 Linux Vicidial Install
```
chmod +x vicidial-install-almalinux.sh
./vicidial-install-almalinux.sh
```


# Install Webphone and SSL cert for VICIDIAL
# DO THIS IF YOU HAVE PUBLIC DOMAIN WITH PUBLIC IP ONLY

```
chmod +x vicidial-enable-webrtc.sh
./vicidial-enable-webrtc.sh
```
