# VPN 
Pour ce tutoriel nous utiliserons des machines sous Centos mais la mise en place fonctionne aussi sous debian ou ubuntu.
Il faudra aussi ouvrir les ports firewall selon le port et protocole utilisé (de base port:1194 protocole:udp)
```
firewall-cmd --add-port:[port]/[protocol] --permanent
```
Redemarrer le firewall
```
firewall-cmd --reload
```

## Mise en place du Serveur
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
Pour ajouter ou révoquer un utilisateur tout ce fait en lancent le script avec les options. 

## Mise en place d'un client
Pour que le client fonctionne il faut installer `OpenVPN` et récupérer le fichier `.opvn` généré par le serveur.
Une fois fini, lancé le fichier `.opvn` puis faite un `ip a` pour vérifier que la connexion a bien fonctionné.

