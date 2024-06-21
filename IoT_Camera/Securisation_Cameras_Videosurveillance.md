# Guide pour Prévenir l'Indexation des Caméras de Vidéosurveillance

## Introduction

L'indexation des caméras de vidéosurveillance expose les flux vidéo à des accès non autorisés. Ce guide fournit des recommandations pour sécuriser vos caméras et minimiser les risques.

## Mesures de Sécurité pour Prévenir l'Indexation

### 1. Configurer Correctement l'Accès à Distance

#### Utiliser un VPN

- **VPN** : Utiliser un réseau privé virtuel (VPN) pour les connexions à distance aux caméras. Cela crée un tunnel sécurisé et chiffré pour accéder aux dispositifs.
- **Configuration** : Assurez-vous que seuls les utilisateurs autorisés peuvent accéder au VPN.

#### Désactiver l'Accès Direct à Internet

- **Configuration LAN** : Configurez les caméras pour qu'elles ne soient accessibles qu'à partir du réseau local (LAN), empêchant l'accès direct via Internet.
- **Utiliser NAT** : Employez la traduction d'adresses réseau (NAT) pour masquer les adresses IP des caméras.

### 2. Sécuriser les Identifiants

#### Changer les Mots de Passe par Défaut

- **Nouveaux mots de passe** : Changez les mots de passe par défaut des caméras immédiatement après l'installation.
- **Caractéristiques** : Utilisez des mots de passe forts avec des lettres, chiffres, et caractères spéciaux.

#### Utiliser des Mots de Passe Forts et Uniques

- **Gestionnaire de mots de passe** : Utilisez un gestionnaire de mots de passe pour créer et stocker des mots de passe complexes.
- **Rotation** : Changez régulièrement les mots de passe pour améliorer la sécurité.

### 3. Mettre à Jour le Firmware

#### Vérifier les Mises à Jour Régulièrement

- **Fabricant** : Consultez régulièrement le site web du fabricant pour les mises à jour de firmware.
- **Notifications** : Activez les notifications automatiques pour les mises à jour, si disponible.

#### Appliquer les Correctifs de Sécurité

- **Immédiat** : Appliquez les correctifs de sécurité dès qu'ils sont disponibles pour corriger les vulnérabilités connues.

### 4. Utiliser des Connexions Sécurisées

#### Préférer HTTPS

- **HTTPS** : Utilisez HTTPS au lieu de HTTP pour les interfaces de gestion des caméras afin de chiffrer les communications.
- **Certificats** : Installez des certificats SSL/TLS pour sécuriser les connexions HTTPS.

#### Utiliser RTSP avec Chiffrement

- **RTSP/RTSP-S** : Utilisez le Real-Time Streaming Protocol (RTSP) avec chiffrement (RTSP-S) pour les flux vidéo.
- **Chiffrement** : Assurez-vous que les flux vidéo sont protégés par un chiffrement adéquat.

### 5. Configurer les Réseaux de Manière Sécurisée

#### Limiter l'Accès aux Ports Nécessaires

- **Pare-feu** : Configurez des règles de pare-feu pour limiter l'accès aux seuls ports nécessaires (comme les ports HTTP/HTTPS et RTSP sécurisés).
- **Port Knocking** : Utilisez des techniques comme le port knocking pour sécuriser davantage l'accès.

#### Désactiver les Services Non Nécessaires

- **Fonctions** : Désactivez les fonctionnalités ou services réseau non essentiels pour réduire la surface d'attaque.

### 6. Éviter les Protocoles Non Sécurisés

#### Ne Pas Utiliser HTTP Non Chiffré

- **HTTP** : Évitez d'utiliser HTTP pour les interfaces de gestion et les flux vidéo.
- **Migration** : Migrez vers des protocoles chiffrés comme HTTPS.

#### Protéger les Communications

- **VPN ou HTTPS** : Utilisez un VPN ou HTTPS pour toutes les communications vers et depuis les caméras.

## Conclusion

En appliquant ces mesures de sécurité, vous réduisez considérablement les risques d'indexation de vos caméras de vidéosurveillance sur Internet. La protection proactive des dispositifs connectés est essentielle pour maintenir la sécurité et la confidentialité des flux vidéo.


## Références

- [Guide de Sécurité IoT de l'ANSSI](https://www.ssi.gouv.fr/guide/guide-de-securite-des-objets-connectes/)
- [Bonnes Pratiques pour la Sécurité des Caméras IP](https://www.cnil.fr/fr/bonnes-pratiques-pour-la-securite-des-cameras-ip)
- [Sécurité des Objets Connectés](https://www.cnil.fr/fr/securite-des-objets-connectes)
- [Shodan](https://www.shodan.io/)
- [Censys](https://censys.io/)
- [Guide de Sécurité des Caméras de Vidéosurveillance](https://www.cnil.fr/fr/securite-des-cameras-de-videosurveillance)