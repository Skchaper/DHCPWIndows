<div align="center"><H1> Quête DHCP Windows </H1></div>

## Pré-requis techniques

> Une VM Windows Server 2022  
> Un client Windows 10 Pro  

_________________________

## Configurer la carte réseau de la machine virtuelle en Réseau Interne
_________________________

**Mode réseau interne**

![CHOIX_RESEAU_INTERNE.png](https://github.com/Skchaper/DHCPWIndows/blob/main/PHOTOS_QU%C3%8ATE_DHCP_WINDOWS/CARTE_RESEAU_IPv4_SERVEUR/CHOIX_RESEAU_INTERNE.PNG)
_________________________

**Création du DHCP**

- Cliquer sur **Gérer** :

![CLIC_GERER.png](https://github.com/Skchaper/DHCPWIndows/blob/main/PHOTOS_QU%C3%8ATE_DHCP_WINDOWS/CREATION_DHCP/CLIC_GERER.PNG)

- Puis sur **Ajouter des rôles et fonctionnaltiés** :

![AJOUTER_ROLES_FONCTIONNALITES.png](https://github.com/Skchaper/DHCPWIndows/blob/main/PHOTOS_QU%C3%8ATE_DHCP_WINDOWS/CREATION_DHCP/AJOUTER_ROLES_FONCTIONNALITES.PNG)

- Cocher **Installation basée sur un rôle ou une fonctionnalité** :

![TYPE_INSTALLATION.png](https://github.com/Skchaper/DHCPWIndows/blob/main/PHOTOS_QU%C3%8ATE_DHCP_WINDOWS/CREATION_DHCP/TYPE_INTALLATION.PNG)

- Sélectionner le serveur sur lequel installer le rôle DHCP dans **Sélection du serveur** :

![SELECTION_SERVEUR.png](https://github.com/Skchaper/DHCPWIndows/blob/main/PHOTOS_QU%C3%8ATE_DHCP_WINDOWS/CREATION_DHCP/SELECTION_SERVEUR.PNG)

- Cliquer sur **Ajouter des fonctionnalités** : 

![AJOUTER_FONCTIONNALITES.png](https://github.com/Skchaper/DHCPWIndows/blob/main/PHOTOS_QU%C3%8ATE_DHCP_WINDOWS/CREATION_DHCP/AJOUTER_FONCTIONNALITES.PNG)

- Cocher la case **Serveur DHCP** dans **Rôles de serveurs** :

![COCHER_DHCP.png](https://github.com/Skchaper/DHCPWIndows/blob/main/PHOTOS_QU%C3%8ATE_DHCP_WINDOWS/CREATION_DHCP/COCHER_DHCP.PNG)

- Sur l'onglet **Serveur DHCP**, cliquer sur **suivant** :

![INFO_DHCP.png](https://github.com/Skchaper/DHCPWIndows/blob/main/PHOTOS_QU%C3%8ATE_DHCP_WINDOWS/CREATION_DHCP/INFO_DHCP.PNG)

- Une fois sur l'onglet **Confirmation**, cliquer sur **Installer** puis attendre le résultat :

![CLIC_INSTALLER.png](https://github.com/Skchaper/DHCPWIndows/blob/main/PHOTOS_QU%C3%8ATE_DHCP_WINDOWS/CREATION_DHCP/CLIC_INSTALLER.PNG)
_________________________

**Terminer de configurer le serveur DHCP**

- Cliquer sur le drapeau en haut à droite, puis sur **Terminer la configuration DHCP** :

![DRAPEAU_TERMINER_CONFIG.png](https://github.com/Skchaper/DHCPWIndows/blob/main/PHOTOS_QU%C3%8ATE_DHCP_WINDOWS/TERMINER_CONFIG_DHCP/DRAPEAU_TERMINER_CONFIG.PNG)

- Sur l'onglet **Description**, cliquer sur **Valider** :

![DESCRIPTION_VALIDER.png](https://github.com/Skchaper/DHCPWIndows/blob/main/PHOTOS_QU%C3%8ATE_DHCP_WINDOWS/TERMINER_CONFIG_DHCP/DESCRIPTION_VALIDER.PNG)

- Enfin, dans l'onglet **Résumé**, cliquer sur **Fermer** : 

![RESUME_FERMER.png](https://github.com/Skchaper/DHCPWIndows/blob/main/PHOTOS_QU%C3%8ATE_DHCP_WINDOWS/TERMINER_CONFIG_DHCP/RESUME_FERMER.PNG)
_________________________

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
_________________________

## Configurer le service DHCP pour qu'il fournisse des adresses IP de la plage 172.20.0.100 - 172.20.0.200 sur le réseau 172.20.0.0/24
_________________________

- Accéder au **Gestionnaire DHCP** : 

![GESTIONNAIRE_DHCP.png](https://github.com/Skchaper/DHCPWIndows/blob/main/PHOTOS_QU%C3%8ATE_DHCP_WINDOWS/CONFIG_SERVEUR_DHCP/GESTIONNAIRE_DHCP.PNG)

- Créer une **Nouvelle étendue** : 

![NOUVELLE_ETENDUE.png](https://github.com/Skchaper/DHCPWIndows/blob/main/PHOTOS_QU%C3%8ATE_DHCP_WINDOWS/CONFIG_SERVEUR_DHCP/NOUVELLE_ETENDUE.PNG)

- Nommer l'étendue :

![NOMMER_ETENDUE.png](https://github.com/Skchaper/DHCPWIndows/blob/main/PHOTOS_QU%C3%8ATE_DHCP_WINDOWS/CONFIG_SERVEUR_DHCP/NOMMER_ETENDUE.PNG)

- Définir la **plage IP**, dans notre cas plage de 172.20.0.100 à 172.20.0.200 :

![PLAGE_IP.png](https://github.com/Skchaper/DHCPWIndows/blob/main/PHOTOS_QU%C3%8ATE_DHCP_WINDOWS/CONFIG_SERVEUR_DHCP/PLAGE_IP.PNG)

- Définir les **Exclusions / retard** s'il y a lieu :

![EXCLUSION_RETARD.png](https://github.com/Skchaper/DHCPWIndows/blob/main/PHOTOS_QU%C3%8ATE_DHCP_WINDOWS/CONFIG_SERVEUR_DHCP/EXCLUSIONS_RETARD.PNG)

- Définir la durée du bail, ici par défaut 8 jours : 

![DUREE_BAIL.png](https://github.com/Skchaper/DHCPWIndows/blob/main/PHOTOS_QU%C3%8ATE_DHCP_WINDOWS/CONFIG_SERVEUR_DHCP/DUREE_BAIL.PNG)

- Cocher **Oui, je veux configurer ces options maintenant** puis cliquer sur suivant :

![OUI_CONFIG_OPTIONS.png](https://github.com/Skchaper/DHCPWIndows/blob/main/PHOTOS_QU%C3%8ATE_DHCP_WINDOWS/CONFIG_SERVEUR_DHCP/OUI_CONFIG_OPTIONS.PNG)

- Attribuer la passerelle par défaut au serveur DHCP : 

![ROUTEUR_ATTRIBUE.png](https://github.com/Skchaper/DHCPWIndows/blob/main/PHOTOS_QU%C3%8ATE_DHCP_WINDOWS/CONFIG_SERVEUR_DHCP/ROUTEUR_ATTRIBUE.PNG)

- S'il y a lieu, renseigner **Nom de domaine et serveurs DNS** :

![RENSEIGNER_NOM_DOMAINE_DNS.png](https://github.com/Skchaper/DHCPWIndows/blob/main/PHOTOS_QU%C3%8ATE_DHCP_WINDOWS/CONFIG_SERVEUR_DHCP/RENSEIGNER_NOM_DOMAINE_DNS.PNG)

- Dans l'onglet **Serveurs Wins** laisser vide et poursuivre : 

![SERVEUR_WINS.png](https://github.com/Skchaper/DHCPWIndows/blob/main/PHOTOS_QU%C3%8ATE_DHCP_WINDOWS/CONFIG_SERVEUR_DHCP/SERVEUR_WINS.PNG)

- Dans **Activer l'étendue**, cliquer sur **Oui, je veux activer cette étendue maintenant** :

![ACTIVER_ETENDUE.png](https://github.com/Skchaper/DHCPWIndows/blob/main/PHOTOS_QU%C3%8ATE_DHCP_WINDOWS/CONFIG_SERVEUR_DHCP/ACTIVER_ETENDUE.PNG)

- Une fois sur cette onglet, cliquer sur **Terminer** :

![CLIQUER_TERMINER.png](https://github.com/Skchaper/DHCPWIndows/blob/main/PHOTOS_QU%C3%8ATE_DHCP_WINDOWS/CONFIG_SERVEUR_DHCP/CLIQUER_TERMINER.PNG)
_________________________

## Un client qui rejoint le réseau obtient une adresse IP dans la plage donnée par le DHCP.

- Le client a bien obtenu une adresse IPv4 grâce au serveur DCHP après le redémarrage :

![IPv4_ATTRIBUE.png](https://github.com/Skchaper/DHCPWIndows/blob/main/PHOTOS_QU%C3%8ATE_DHCP_WINDOWS/Requ%C3%AAte_R%C3%A9ponse%20ping%20et%20ipv4%20fixe%20DHCP/IPv4_ATTRIBUE.PNG)

- Le client ping bien le serveur :

![CLIENT_PING_SERVEUR.png](https://github.com/Skchaper/DHCPWIndows/blob/main/PHOTOS_QU%C3%8ATE_DHCP_WINDOWS/Requ%C3%AAte_R%C3%A9ponse%20ping%20et%20ipv4%20fixe%20DHCP/CLIENT_PING_SERVEUR.PNG)

- Le serveur ping bien le client via l'IP définit par le DHCP :

![SERVEUR_PING_CLIENT.png](https://github.com/Skchaper/DHCPWIndows/blob/main/PHOTOS_QU%C3%8ATE_DHCP_WINDOWS/Requ%C3%AAte_R%C3%A9ponse%20ping%20et%20ipv4%20fixe%20DHCP/SERVEUR_PING_CLIENT.PNG)
_________________________

## Mettre en place une attribution statique pour une machine cliente particulière dont l'adresse MAC permet d'obtenir l'adresse 172.20.0.10

- Clic droit sur le serveur DHCP, cliquer sur **Gestionnaire DHCP** :

![GESTIONNAIRE_DHCP.png](https://github.com/Skchaper/DHCPWIndows/blob/main/PHOTOS_QU%C3%8ATE_DHCP_WINDOWS/IPv4_DEPUIS_MAC/GESTIONNAIRE_DHCP.PNG)

- Depuis **Réservations**, clic sur **Action** puis sur **Nouvelle réservation...** :

![CLIC_ACTION.png](https://github.com/Skchaper/DHCPWIndows/blob/main/PHOTOS_QU%C3%8ATE_DHCP_WINDOWS/IPv4_DEPUIS_MAC/CLIC_ACTION.PNG)
![NOUVELLE_RESERVATION.png](https://github.com/Skchaper/DHCPWIndows/blob/main/PHOTOS_QU%C3%8ATE_DHCP_WINDOWS/IPv4_DEPUIS_MAC/NOUVELLE_RESERVATION.PNG)

- Définir l'adresse MAC de la machine et l'adresse IP qui lui sera automatiquement attribué :

![IPv4_DEPUIS_MAC.png](https://github.com/Skchaper/DHCPWIndows/blob/main/PHOTOS_QU%C3%8ATE_DHCP_WINDOWS/IPv4_DEPUIS_MAC/IPv4_DEPUIS_MAC.PNG)

- Après la demande de renouvèlement, le client obtient l'adresse IP fixe définie :

![IPv4_CLIENT_AVANT.png)](https://github.com/Skchaper/DHCPWIndows/blob/main/PHOTOS_QU%C3%8ATE_DHCP_WINDOWS/Requ%C3%AAte_R%C3%A9ponse%20ping%20et%20ipv4%20fixe%20DHCP/IPv4_CLIENT_AVANT.PNG)



