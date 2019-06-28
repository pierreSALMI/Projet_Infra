# VPN 
## Mise en place du Serveur
### Téléchargement
Pour que le serveur fonctionne il vas falloir installer différentes librairies et un script
* librairies
```
yum install openvpn
```
* script
```
wget http://git.io/vpn
```

## Mise en place d'un client
Pour que le client fonctionne il faut installer `OpenVPN` et récupérer le fichier `.opvn` générer par le serveur.
Une fois fini, lancé le fichier `.opvn` puis faite un `ip a` 

