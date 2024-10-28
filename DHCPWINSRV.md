Configure la carte réseau de ta machine virtuelle en Réseau Interne



Configure le service DHCP pour qu'il fournisse des adresses IP de la plage 172.20.0.100 - 172.20.0.200 sur le réseau 172.20.0.0/24



Un client qui rejoint le réseau obtient une adresse IP dans la plage donnée par le DHCP.



Mettre en place une attribution statique pour une machine cliente particulière dont l'adresse MAC permet d'obtenir l'adresse 172.20.0.10



Poste une procédure au format markdown permettant pas à pas d'obtenir cette configuration ainsi que les tests associés

Le serveur DHCP possède un nom d'hôte adapté à son rôle (Exemple: SRV-DHCP) ainsi qu'une configuration IP correcte.
La configuration du serveur permet bien aux client d'obtenir une adresse IP par le serveur DHCP dans la plage d'adresse donnée.
Le client qui possède la réservation n'obtient pas une autre IPv4, même si il demande un renouvellement.
La procédure est claire et permet effectivement lorsqu'elle est appliquée de répondre aux critères du challenge


