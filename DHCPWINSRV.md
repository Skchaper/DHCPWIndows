## Configurer la carte réseau de la machine virtuelle en Réseau Interne

**Mode réseau interne**

![CHOIX_RESEAU_INTERNE.png](https://github.com/Skchaper/DHCPWIndows/blob/main/PHOTOS_QU%C3%8ATE_DHCP_WINDOWS/CARTE_RESEAU_IPv4_SERVEUR/CHOIX_RESEAU_INTERNE.PNG)

**Création du DHCP**



**Terminer de configurer le serveur DHCP**




**Configurer l'adresse IPv4 du serveur DHCP**

- Depuis les paramètres **Réseau et Internet**, sur la machine serveur, cliquer sur **Modifier les options d'adaptateur** : 

![MODIFIER_OPTIONS_ADAPTATEUR.png](https://github.com/Skchaper/DHCPWIndows/blob/main/PHOTOS_QU%C3%8ATE_DHCP_WINDOWS/CARTE_RESEAU_IPv4_SERVEUR/MODIFIER_OPTIONS_ADAPTATEUR.PNG)

- Clique droit sur la carte réseau, sélectionner **Propriétés** :

![CLIC_DROIT_PROPRIETES.png](https://github.com/Skchaper/DHCPWIndows/blob/main/PHOTOS_QU%C3%8ATE_DHCP_WINDOWS/CARTE_RESEAU_IPv4_SERVEUR/CLIC_DROIT_PROPRIETES.PNG)

- Dans l'onglet suivant, double clic sur **Protocole Internet version 4 (TCP/IPv4)** :

![DOUBLE_CLIC.png](https://github.com/Skchaper/DHCPWIndows/blob/main/PHOTOS_QU%C3%8ATE_DHCP_WINDOWS/CARTE_RESEAU_IPv4_SERVEUR/DOUBLE_CLIC.PNG)

- Cocher la case **Utiliser l'adresse IP suivante**, renseigner l'IPv4 du serveur désirée ainsi que le masque de sous-réseau :

![IPv4_MASQUE](https://github.com/Skchaper/DHCPWIndows/blob/main/PHOTOS_QU%C3%8ATE_DHCP_WINDOWS/CARTE_RESEAU_IPv4_SERVEUR/IPv4_MASQUE.PNG)
![IPv4_SERVEUR](https://github.com/Skchaper/DHCPWIndows/blob/main/PHOTOS_QU%C3%8ATE_DHCP_WINDOWS/CARTE_RESEAU_IPv4_SERVEUR/IPv4_SERVEUR.PNG)

Le serveur DHCP possède la bonne IPv4.

## Configurer le service DHCP pour qu'il fournisse des adresses IP de la plage 172.20.0.100 - 172.20.0.200 sur le réseau 172.20.0.0/24






**Fournir des adresses IP de la plage 172.20.0.100 - 172.20.0.200 sur le réseau 172.20.0.0/24**



## Un client qui rejoint le réseau obtient une adresse IP dans la plage donnée par le DHCP.

- Le client a bien obtenu une adresse IPv4 grâce au DCHP :
![]()

## Mettre en place une attribution statique pour une machine cliente particulière dont l'adresse MAC permet d'obtenir l'adresse 172.20.0.10

- Clic droit sur le serveur DHCP, cliquer sur **Gestionnaire DHCP** :

![GESTIONNAIRE_DHCP.png](https://github.com/Skchaper/DHCPWIndows/blob/main/PHOTOS_QU%C3%8ATE_DHCP_WINDOWS/IPv4_DEPUIS_MAC/GESTIONNAIRE_DHCP.PNG)

- Depuis **Réservations**, clic sur **Action** puis sur **Nouvelle réservation...** :

![CLIC_ACTION.png](https://github.com/Skchaper/DHCPWIndows/blob/main/PHOTOS_QU%C3%8ATE_DHCP_WINDOWS/IPv4_DEPUIS_MAC/CLIC_ACTION.PNG)
![NOUVELLE_RESERVATION.png](https://github.com/Skchaper/DHCPWIndows/blob/main/PHOTOS_QU%C3%8ATE_DHCP_WINDOWS/IPv4_DEPUIS_MAC/NOUVELLE_RESERVATION.PNG)

- Définir l'adresse MAC de la machine et l'adresse IP qui lui sera automatiquement attribué :

![IPv4_DEPUIS_MAC](https://github.com/Skchaper/DHCPWIndows/blob/main/PHOTOS_QU%C3%8ATE_DHCP_WINDOWS/IPv4_DEPUIS_MAC/IPv4_DEPUIS_MAC.PNG)

## Poste une procédure au format markdown permettant pas à pas d'obtenir cette configuration ainsi que les tests associés

Le serveur DHCP possède un nom d'hôte adapté à son rôle (Exemple: SRV-DHCP) ainsi qu'une configuration IP correcte.
La configuration du serveur permet bien aux client d'obtenir une adresse IP par le serveur DHCP dans la plage d'adresse donnée.
Le client qui possède la réservation n'obtient pas une autre IPv4, même si il demande un renouvellement.
La procédure est claire et permet effectivement lorsqu'elle est appliquée de répondre aux critères du challenge


