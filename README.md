# VPN 
## Mise en place du Serveur
### Téléchargement
Pour que le serveur fonctionne il vas falloir installer différentes librairies et un script
* librairies
```
yum install -y openvpn easy-rsa
```
* script
```
wget http://git.io/vpn
```

Une fois le script installer lancé le et suivez les instructions données.
Il faudra aussi ouvrir le Firewall selon le port et protocol utilisé (de base port:1194 protocole:udp)
```
firewall-cmd --add-port:[port]/[protocol] --permanent
```
Redemarrer le firewall
```
firewall-cmd --reload
```


## Mise en place d'un client
Pour que le client fonctionne il faut installer `OpenVPN` et récupérer le fichier `.opvn` générer par le serveur.
Une fois fini, lancé le fichier `.opvn` puis faite un `ip a` pour vérifier que la connexion a bien fonctionner.

