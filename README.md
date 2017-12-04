# webserver73

start putty og find din ip adresse til den server du vil køre, i mit tilfælge er det fra digital ocean og kan finde den inde i droplets

Inde i putty kan du gemme din ip adresse så du ikke skal skrive den hver gang.

1.
Installer nano

``` 
yum install nano 
```

2.
Installer mysql

``` 
yum install mysql-server 
```

Du kan bruge

``` 
service mysqld start/stop/restart 
```

For at tjekke om det er installeret korrekt kan du bruge

``` 
sudo /usr/bin/mysql_secure_installation 
```

3.
Installer nodejs

``` 
yum install epel-release
yum install nodejs
yum install npm
yum install -g n 
```

opdater nodejs

``` 
n lts 
n 
```

FOR DETTE VIRKER SKAL DU GENSTARTE PUTTY

4.
Installer PM2

``` 
npm install -g pm2 
```

Kør PM2 ved startup

``` 
pm2 startup 
```

5.
Installer git

``` 
yum install git 
```

konfiguration

``` 
git config --global user.name "Dit navn" 
git config --global user.email "Din email" 
```

Du kan tjekke konfigurationen her

``` 
nano ~/.gitconfig 
```

6.
Opret et nøglesæt til at logge ind på github

``` 
ssh-keygen -t rsa 
```

åben den offentlige nølge

``` 
cat ~/.shh/id_rsa.pub 
```
kopier nøglen, gå ind på github, settings, SSH and GPG keys og sæt den ind i new SSH key


7.
Nu skal du oprette en mappe til din app

``` 
mkdir ~/www 
```

Naviger ind i mappen

``` 
cd ~/www 
```

8.
Klon dit repository hvor dit site er

``` 
git clone git@github.com:brugernavn/repository 
```

Når du opdateret dit site skal du huske at pushe til github og så brug pull funktionen og skrive hvilken branch den har, du kan finde din branch inde under github og så repositories.

``` 
git pull git@github.com:brugernavn/repository (hvilken branch bliver brugt) 
```