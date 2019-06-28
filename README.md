# VPN 
## Mise en place du Serveur
Nous utiliserons ici un os Linux (debian/ubuntu/centos) pour notre serveur.
### Téléchargement
Pour que le serveur fonctionne il va falloir installer différentes librairies et un script
* librairies
```
yum install -y openvpn easy-rsa
```
* script
```
wget http://git.io/vpn
```

Une fois le script télécharger lancez-le et suivez les instructions données.
Il faudra aussi ouvrir le Firewall selon le port et protocole utilisé (de base port:1194 protocole:udp)
```
firewall-cmd --add-port:[port]/[protocol] --permanent
```
Redemarrer le firewall
```
firewall-cmd --reload
```


## Mise en place d'un client
Pour que le client fonctionne il faut installer `OpenVPN` et récupérer le fichier `.opvn` généré par le serveur.
Une fois fini, lancé le fichier `.opvn` puis faite un `ip a` pour vérifier que la connexion a bien fonctionné.

