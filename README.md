<div align="center">

```
 ███╗   ███╗ ██████╗ ████████╗ ██████╗ ██████╗  ██████╗ ██╗      ███████╗
 ████╗ ████║██╔═══██╗╚══██╔══╝██╔═══██╗██╔══██╗██╔═══██╗██║      ██╔════╝
 ██╔████╔██║██║   ██║   ██║   ██║   ██║██████╔╝██║   ██║██║      ███████╗
 ██║╚██╔╝██║██║▄▄ ██║   ██║   ██║   ██║██╔══██╗██║   ██║██║      ╚════██║
 ██║ ╚═╝ ██║╚██████╔╝   ██║   ╚██████╔╝██║  ██║╚██████╔╝███████╗ ███████║
 ╚═╝     ╚═╝ ╚══▀▀═╝    ╚═╝    ╚═════╝ ╚═╝  ╚═╝ ╚═════╝ ╚══════╝ ╚══════╝
```

# <span style="color:#00ff00; text-shadow: 0 0 10px #00ff00;">📡 PROTOCOLES DE COMMUNICATION IoT & MESSAGERIE AVANCÉS</span>

### <span style="color:#00ff41;">MQTT • CoAP • AMQP • DDS • XMPP</span>

<p align="center">
  <img src="https://img.shields.io/badge/MQTT-Protocol-00ff00?style=for-the-badge&logoColor=white" alt="MQTT">
  <img src="https://img.shields.io/badge/CoAP-Protocol-00cc00?style=for-the-badge&logoColor=white" alt="CoAP">
  <img src="https://img.shields.io/badge/AMQP-Protocol-008800?style=for-the-badge&logoColor=white" alt="AMQP">
  <img src="https://img.shields.io/badge/DDS-Protocol-006600?style=for-the-badge&logoColor=white" alt="DDS">
  <img src="https://img.shields.io/badge/XMPP-Protocol-004400?style=for-the-badge&logoColor=white" alt="XMPP">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Auteur-hackers__tchad-00ff00?style=for-the-badge&logoColor=black" alt="Auteur">
  <img src="https://img.shields.io/badge/Version-1.0.0-00ff00?style=for-the-badge&logoColor=black" alt="Version">
  <img src="https://img.shields.io/badge/Lignes-2000+-00ff00?style=for-the-badge&logoColor=black" alt="Lignes">
</p>

</div>

---

## 🎨 Animation Matrix Green

```css
/* Style Matrix Green pour rendu web */
.matrix-green {
    color: #00ff00;
    text-shadow: 0 0 5px #00ff00, 0 0 10px #00ff00, 0 0 20px #00ff41;
    font-family: 'Courier New', monospace;
    animation: matrixPulse 2s infinite alternate;
}

@keyframes matrixPulse {
    0% { opacity: 0.8; text-shadow: 0 0 5px #00ff00; }
    50% { opacity: 1; text-shadow: 0 0 20px #00ff41, 0 0 30px #00ff00; }
    100% { opacity: 0.9; text-shadow: 0 0 10px #00cc00; }
}
```

```html
<!-- Code HTML pour animation Matrix -->
<div class="matrix-green">
    <h1>📡 PROTOCOLES IoT AVANCÉS</h1>
    <p>MQTT • CoAP • AMQP • DDS • XMPP</p>
</div>
```

---

## 📋 Table des matières

1. [Introduction générale](#introduction-générale)
2. [MQTT (Message Queuing Telemetry Transport)](#mqtt-message-queuing-telemetry-transport)
3. [CoAP (Constrained Application Protocol)](#coap-constrained-application-protocol)
4. [AMQP (Advanced Message Queuing Protocol)](#amqp-advanced-message-queuing-protocol)
5. [DDS (Data Distribution Service)](#dds-data-distribution-service)
6. [XMPP (Extensible Messaging and Presence Protocol)](#xmpp-extensible-messaging-and-presence-protocol)
7. [Tableau comparatif des protocoles](#tableau-comparatif-des-protocoles)
8. [Guide de sélection de protocole](#guide-de-sélection-de-protocole)
9. [Sécurité commune](#sécurité-commune)
10. [Commandes de vérification](#commandes-de-vérification)
11. [Outils et interfaces de configuration](#outils-et-interfaces-de-configuration)
12. [Glossaire](#glossaire)
13. [Ressources et liens](#ressources-et-liens)
14. [Auteur](#auteur)

---

# Introduction générale

## Qu'est-ce qu'un protocole de communication ?

Un protocole de communication est un ensemble de règles et de conventions qui permettent à deux entités (machines, applications, capteurs, serveurs) d'échanger des informations de manière structurée et compréhensible. Dans le contexte de l'Internet des Objets (IoT), des systèmes industriels, des applications de messagerie instantanée et des architectures distribuées, le choix du protocole est critique pour garantir la performance, la fiabilité, la sécurité et l'interopérabilité.

## Pourquoi ce guide ?

Ce document a pour objectif de fournir une référence complète, technique et pratique sur cinq protocoles majeurs :

- **MQTT** : Le protocole de messagerie publish/subscribe léger pour l'IoT
- **CoAP** : Le protocole web optimisé pour les appareils contraints
- **AMQP** : Le protocole de messagerie d'entreprise robuste
- **DDS** : Le middleware de communication temps réel pour systèmes critiques
- **XMPP** : Le protocole extensible de messagerie instantanée et de présence

## Contexte historique

L'évolution des protocoles de communication a été dictée par les besoins croissants en connectivité. Des premiers protocoles TCP/IP dans les années 1970, aux protocoles web HTTP/HTTPS, puis aux protocoles spécialisés IoT des années 2010, chaque protocole a été conçu pour répondre à des contraintes spécifiques : bande passante limitée, latence faible, fiabilité, sécurité, interopérabilité.

## Public cible

Ce guide s'adresse aux :

- Architectes système
- Développeurs IoT et embarqué
- Ingénieurs réseau et DevOps
- Administrateurs système
- Étudiants en informatique et télécommunications
- Passionnés de cybersécurité et de hacking éthique

---

# MQTT (Message Queuing Telemetry Transport)

## Définition

MQTT est un protocole de messagerie publish/subscribe (pub/sub) léger, conçu pour les environnements à faible bande passante, à latence élevée ou peu fiables. Il repose sur le modèle client/serveur où un broker centralise les échanges entre clients.

## Historique et créateurs

MQTT a été inventé en 1999 par **Andy Stanford-Clark** (IBM) et **Arlen Nipper** (Cirrus Link Solutions, anciennement Eurotech). Il a été initialement développé pour surveigner des pipelines d'huile via des satellites. En 2010, IBM a publié MQTT 3.1 sous licence libre. En 2014, MQTT est devenu un standard OASIS. MQTT 5.0 a été publié en 2019 avec des améliorations majeures.

## Caractéristiques techniques

### Modèle de communication

MQTT utilise un modèle publish/subscribe découplé :

- **Publisher** : Publie des messages sur un topic
- **Subscriber** : S'abonne à un ou plusieurs topics
- **Broker** : Serveur central qui reçoit les messages et les redirige aux abonnés

### Niveau transport

MQTT s'exécute généralement sur TCP/IP, port 1883 par défaut. Le port 8883 est utilisé pour MQTT over TLS/SSL.

### Qualité de service (QoS)

MQTT définit trois niveaux de QoS :

- **QoS 0** : At most once — livraison au plus une fois, sans accusé de réception
- **QoS 1** : At least once — livraison au moins une fois, avec accusé de réception
- **QoS 2** : Exactly once — livraison exactement une fois, avec handshake complet

### Topics et wildcards

Les topics sont des chaînes hiérarchiques séparées par des slashes `/`.

- **Wildcard `+`** : Remplace un seul niveau (ex: `maison/+/temperature`)
- **Wildcard `#`** : Remplace plusieurs niveaux (ex: `maison/etage1/#`)

### Retain message

Un message publié avec le flag `retain` est conservé par le broker et envoyé aux nouveaux abonnés.

### Last Will and Testament (LWT)

Le LWT permet à un client de définir un message qui sera publié automatiquement par le broker si le client se déconnecte de manière inattendue.

### Clean Session / Persistent Session

- **Clean Session = true** : Le broker ne conserve pas les abonnements et messages en attente
- **Clean Session = false** : Le broker conserve les abonnements et les messages QoS 1/2 en attente

## Architecture MQTT

```
┌─────────────────┐         PUBLISH         ┌─────────────────┐
│   Capteur       │ ───────────────────────> │                 │
│   Température   │                          │     Broker      │
└─────────────────┘                          │     MQTT        │
                                             │                 │
┌─────────────────┐         SUBSCRIBE        │   (Mosquitto,   │
│   Application   │ ───────────────────────> │   HiveMQ, etc.) │
│   Mobile        │                          │                 │
└─────────────────┘                          └────────┬────────┘
                                                      │
                                                      │ PUBLISH
                                                      ▼
                                               ┌─────────────────┐
                                               │   Dashboard     │
                                               │   Web           │
                                               └─────────────────┘
```

## Avantages de MQTT

- Très léger (en-tête fixe de 2 octets minimum)
- Faible consommation de bande passante
- Supporte les réseaux peu fiables
- Découplage des producteurs et consommateurs
- Large écosystème et adoption massive
- Sécurité via TLS et authentification

## Inconvénients de MQTT

- Dépendance au broker (single point of failure si non clusterisé)
- Pas de découverte de services native
- Pas de standardisation du format de payload
- Gestion des topics peut devenir complexe

## Cas d'usage

- Domotique et maisons connectées
- Villes intelligentes (smart cities)
- Agriculture de précision
- Surveillance industrielle (IIoT)
- Télémétrie véhicule
- Systèmes de santé connectés

## Entreprises et projets utilisant MQTT

- Amazon Web Services (AWS IoT Core)
- Microsoft Azure IoT Hub
- Google Cloud IoT Core (historique)
- IBM Watson IoT
- Facebook Messenger (ancienne infrastructure)
- Tesla (télémétrie véhicule)
- Siemens, Bosch, Schneider Electric

## Logiciels et implémentations MQTT

### Brokers

- **Eclipse Mosquitto** : Broker open source léger
- **HiveMQ** : Broker enterprise avec clustering
- **EMQ X (EMQX)** : Broker open source haute performance
- **RabbitMQ** : Supporte MQTT via plugin
- **VerneMQ** : Broker distribué Erlang
- **ActiveMQ** : Supporte MQTT via broker

### Clients

- **Paho MQTT** (Eclipse Foundation) : Clients Python, C, Java, JavaScript
- **MQTT.js** : Client JavaScript/Node.js
- **Eclipse Paho Android Service**
- **Mosquitto clients** (`mosquitto_pub`, `mosquitto_sub`)

## Installation et commandes Linux

### Installation Mosquitto sur Debian/Ubuntu

```bash
# Mettre à jour les paquets
sudo apt update && sudo apt upgrade -y

# Installer Mosquitto broker et clients
sudo apt install mosquitto mosquitto-clients -y

# Vérifier le statut du service
sudo systemctl status mosquitto

# Démarrer le service
sudo systemctl start mosquitto

# Activer au démarrage
sudo systemctl enable mosquitto
```

### Commandes de vérification Linux

```bash
# Vérifier que le broker écoute sur le port 1883
sudo netstat -tlnp | grep 1883

# Alternative avec ss
sudo ss -tlnp | grep mosquitto

# Tester la connexion avec netcat
nc -vz localhost 1883

# S'abonner à un topic
mosquitto_sub -h localhost -t "test/topic" -v

# Publier un message
mosquitto_pub -h localhost -t "test/topic" -m "Hello MQTT"

# Publier avec QoS 1
mosquitto_pub -h localhost -t "test/topic" -m "Hello QoS1" -q 1

# Publier avec authentification
mosquitto_pub -h localhost -t "test/topic" -m "secure" -u "user" -P "password"

# Tester TLS/SSL
mosquitto_pub -h localhost -t "test/topic" -m "secure" -p 8883 --cafile ca.crt
```

## Commandes Windows

```powershell
# Vérifier le port avec PowerShell
Test-NetConnection -ComputerName localhost -Port 1883

# Alternative avec netstat
netstat -an | findstr 1883

# Installer Mosquitto via Chocolatey
choco install mosquitto

# Démarrer le service
sc start mosquitto

# S'abonner
mosquitto_sub.exe -h localhost -t "test/topic" -v

# Publier
mosquitto_pub.exe -h localhost -t "test/topic" -m "Hello MQTT"
```

## Configuration Mosquitto

### Fichier de configuration

Sur Linux : `/etc/mosquitto/mosquitto.conf`
Sur Windows : `C:\Program Files\mosquitto\mosquitto.conf`

### Exemple de configuration de base

```conf
# Port standard MQTT
listener 1883

# Autoriser les connexions anonymes
allow_anonymous true

# Fichier de mots de passe
password_file /etc/mosquitto/passwd

# Persistence
persistence true
persistence_location /var/lib/mosquitto/

# Logs
log_dest file /var/log/mosquitto/mosquitto.log
log_type all

# Limites
max_connections 1000
max_inflight_messages 40
max_queued_messages 1000
```

### Configuration avec TLS

```conf
listener 8883
cafile /etc/mosquitto/ca_certificates/ca.crt
certfile /etc/mosquitto/certs/server.crt
keyfile /etc/mosquitto/certs/server.key
require_certificate false
tls_version tlsv1.2
```

### Créer un utilisateur

```bash
# Créer le fichier de mots de passe
sudo mosquitto_passwd -c /etc/mosquitto/passwd monutilisateur

# Ajouter un utilisateur
sudo mosquitto_passwd /etc/mosquitto/passwd autreutilisateur

# Redémarrer Mosquitto
sudo systemctl restart mosquitto
```

## Interfaces de configuration

- **Ligne de commande** : édition directe de `mosquitto.conf`
- **HiveMQ Control Center** : interface web d'administration
- **EMQX Dashboard** : interface web complète
- **MQTT Explorer** : client graphique pour surveiller les topics
- **Node-RED** : interface visuelle de flux MQTT

## Sécurité MQTT

- Utiliser TLS/SSL (port 8883)
- Authentification par nom d'utilisateur/mot de passe
- Authentification par certificats clients (mTLS)
- ACL (Access Control Lists) pour restreindre les topics
- Isoler les brokers par réseau/VLAN
- Surveiller les logs et activer la journalisation
- Mettre à jour régulièrement le broker

## Ressources MQTT

- Site officiel MQTT : https://mqtt.org/
- Documentation OASIS MQTT 5.0 : https://docs.oasis-open.org/mqtt/mqtt/v5.0/mqtt-v5.0.html
- Eclipse Mosquitto : https://mosquitto.org/
- Eclipse Paho : https://www.eclipse.org/paho/
- HiveMQ : https://www.hivemq.com/
- EMQX : https://www.emqx.io/

---

# CoAP (Constrained Application Protocol)

## Définition

CoAP est un protocole de transfert web spécialement conçu pour les appareils contraints (capteurs, microcontrôleurs, réseaux à faible puissance). Il est défini dans la RFC 7252 et s'inspire d'HTTP tout en étant optimisé pour les ressources limitées.

## Historique et créateurs

CoAP a été développé par le groupe de travail **CoRE (Constrained RESTful Environments)** de l'IETF. Les principaux contributeurs incluent **Zach Shelby**, **Carsten Bormann** et d'autres membres de l'IETF. La RFC 7252 a été publiée en juin 2014.

## Caractéristiques techniques

### Modèle de communication

CoAP repose sur un modèle client/serveur de type RESTful, similaire à HTTP. Les clients envoient des requêtes (GET, POST, PUT, DELETE) vers des ressources identifiées par des URI.

### Niveau transport

CoAP utilise UDP comme protocole de transport, généralement sur le port 5683. CoAP over DTLS utilise le port 5684 pour la sécurité.

### Méthodes

- **GET** : Récupérer une ressource
- **POST** : Créer une ressource ou envoyer des données
- **PUT** : Mettre à jour une ressource
- **DELETE** : Supprimer une ressource

### Codes de réponse

CoAP utilise des codes de réponse similaires à HTTP, encodés sur 8 bits :

- **2.01 Created**
- **2.02 Deleted**
- **2.03 Valid**
- **2.04 Changed**
- **2.05 Content**
- **4.00 Bad Request**
- **4.01 Unauthorized**
- **4.04 Not Found**
- **5.00 Internal Server Error**

### Messages

CoAP définit quatre types de messages :

- **CON (Confirmable)** : Message nécessitant une confirmation
- **NON (Non-confirmable)** : Message sans confirmation
- **ACK (Acknowledgement)** : Accusé de réception
- **RST (Reset)** : Réinitialisation

### Observe

L'extension CoAP Observe (RFC 7641) permet à un client de s'abonner à une ressource et de recevoir des notifications automatiques lors de changements, similaire au modèle pub/sub.

### Block-Wise Transfers

L'extension Block (RFC 7959) permet de transférer des payloads volumineux par blocs, ce qui est essentiel pour les appareils avec mémoire limitée.

## Architecture CoAP

```
┌─────────────────┐        GET /sensor/temp       ┌─────────────────┐
│   Client        │ ────────────────────────────> │   Serveur       │
│   (Smartphone)  │                               │   CoAP          │
│                 │ <──────────────────────────── │   (Capteur)     │
└─────────────────┘        2.05 Content           └─────────────────┘
                               UDP Port 5683
```

## Avantages de CoAP

- Très léger, conçu pour les contraintes de CPU et mémoire
- Basé sur UDP, adapté aux réseaux sans fil à faible latence
- Compatible RESTful, facile à intégrer avec HTTP
- Supporte la découverte de ressources (`.well-known/core`)
- Supporte le multicast
- Faible consommation énergétique

## Inconvénients de CoAP

- UDP moins fiable que TCP (mais géré par les mécanismes CON/ACK)
- Moins mature et moins adopté que MQTT
- NAT et pare-feu peuvent poser problème
- Moins d'outils et d'écosystème

## Cas d'usage

- Capteurs sans fil à batterie
- Smart buildings et éclairage connecté
- Réseaux LPWAN (LoRaWAN, NB-IoT)
- Réseaux de capteurs industriels
- Systèmes domotiques légers

## Entreprises et projets utilisant CoAP

- Contiki OS et TinyOS
- RIOT OS
- Eclipse Californium
- ARM mbed
- Zolertia (capteurs Z1, Zoul)
- OpenThread

## Logiciels et implémentations CoAP

### Bibliothèques serveurs

- **Eclipse Californium (Cf)** : Implémentation Java CoAP
- **aiocoap** : Implémentation Python asynchrone
- **libcoap** : Implémentation C
- **node-coap** : Implémentation Node.js
- **CoAPthon** : Serveur et client Python

### Clients

- **Copper (Cu)** : Extension Firefox (obsolète)
- **Eclipse Californium client**
- **aiocoap-client**
- **coap-client (libcoap)**

## Installation et commandes Linux

### Installer libcoap

```bash
# Cloner libcoap
git clone https://github.com/obgm/libcoap.git
cd libcoap

# Compiler et installer
./autogen.sh
./configure --disable-tests --disable-manpages
make
sudo make install
sudo ldconfig
```

### Commandes de vérification Linux

```bash
# Vérifier le port CoAP
sudo netstat -ulnp | grep 5683

# Alternative avec ss
sudo ss -ulnp | grep 5683

# Envoyer une requête GET CoAP
coap-client -m get coap://localhost/sensor/temp

# Envoyer une requête POST
coap-client -m post -e "valeur=25" coap://localhost/sensor/temp

# Envoyer une requête avec Observe
coap-client -m get -s 60 coap://localhost/sensor/temp

# Requête sécurisée DTLS
coap-client -m get coaps://localhost/sensor/temp -k "secretPSK" -u "user"

# Découverte de ressources
.coap-client -m get coap://localhost/.well-known/core
```

## Commandes Windows

```powershell
# Vérifier le port
netstat -an | findstr 5683

# Test avec PowerShell (UDP natif limité)
# Utiliser libcoap compilé avec MinGW ou WSL
```

## Configuration Californium

### Exemple de serveur simple en Java

```java
import org.eclipse.californium.core.CoapServer;
import org.eclipse.californium.core.server.resources.CoapExchange;

public class SimpleCoapServer {
    public static void main(String[] args) {
        CoapServer server = new CoapServer();
        server.add(new CoapResource("sensor") {
            @Override
            public void handleGET(CoapExchange exchange) {
                exchange.respond("temperature: 23.5");
            }
        });
        server.start();
    }
}
```

### Configuration aiocoap en Python

```python
import asyncio
from aiocoap import Context, Message

async def main():
    protocol = await Context.create_client_context()
    request = Message(code=GET, uri='coap://localhost/sensor/temp')
    response = await protocol.request(request).response
    print(response.payload.decode())

asyncio.run(main())
```

## Interfaces de configuration

- **Configuration par code** : intégration dans firmware (Contiki, RIOT)
- **Eclipse Californium** : API Java
- **aiocoap** : scripts Python
- **Node-RED** : nœuds CoAP disponibles

## Sécurité CoAP

- CoAP over DTLS (Datagram TLS) sur port 5684
- Authentification par certificats
- PSK (Pre-Shared Keys)
- Isolation réseau
- Mise à jour des firmwares

## Ressources CoAP

- RFC 7252 : https://tools.ietf.org/html/rfc7252
- RFC 7641 (Observe) : https://tools.ietf.org/html/rfc7641
- RFC 7959 (Block) : https://tools.ietf.org/html/rfc7959
- Eclipse Californium : https://www.eclipse.org/californium/
- aiocoap : https://github.com/chrysn/aiocoap
- libcoap : https://github.com/obgm/libcoap

---

# AMQP (Advanced Message Queuing Protocol)

## Définition

AMQP est un protocole de messagerie orienté message, standard ouvert, conçu pour les systèmes d'entreprise nécessitant fiabilité, sécurité et interopérabilité. Il supporte les modèles point-à-point, publish/subscribe et request/reply.

## Historique et créateurs

AMQP a été initié en 2003 par **John O'Hara** chez JPMorgan Chase. Le but était de remplacer les systèmes de messagerie propriétaires coûteux. AMQP a été développé par un groupe de travail incluant JPMorgan Chase, Red Hat, Cisco, Microsoft, et d'autres. La version 1.0 a été publiée en 2011 et est devenue un standard OASIS et ISO/IEC 19464.

## Caractéristiques techniques

### Modèle de communication

AMQP utilise les concepts suivants :

- **Producer** : Producteur de messages
- **Consumer** : Consommateur de messages
- **Queue** : File d'attente de messages
- **Exchange** : Point de routage des messages
- **Binding** : Lien entre exchange et queue
- **Routing Key** : Clé de routage utilisée par l'exchange

### Types d'exchange

- **Direct** : Route les messages vers les queues dont la routing key correspond exactement
- **Fanout** : Diffuse les messages vers toutes les queues liées
- **Topic** : Route selon des patterns de routing key
- **Headers** : Route selon les en-têtes du message

### Niveau transport

AMQP 1.0 utilise TCP, généralement sur le port 5672. Le port 5671 est utilisé pour AMQPS (AMQP over TLS/SSL).

### Garanties de livraison

AMQP supporte plusieurs modes de livraison :

- **At most once**
- **At least once**
- **Exactly once** (selon implémentation)

### Modèle de message

AMQP 1.0 utilise un modèle de message basé sur des liens (links) entre nœuds, avec des concepts de crédit de flux (flow control) et de transactions.

## Architecture AMQP

```
┌─────────────────┐
│    Producer     │
└────────┬────────┘
         │ Message + routing key
         ▼
┌─────────────────┐
│     Exchange    │
│    (direct/     │
│   topic/fanout) │
└────────┬────────┘
         │
    ┌────┴────┐
    ▼         ▼
┌───────┐ ┌───────┐
│Queue 1│ │Queue 2│
└───┬───┘ └───┬───┘
    │         │
    ▼         ▼
┌───────┐ ┌───────┐
│Consumer│ │Consumer│
└───────┘ └───────┘
```

## Avantages de AMQP

- Très fiable et robuste
- Routage avancé des messages
- Interopérabilité entre implémentations
- Support des transactions
- Sécurité forte (TLS, SASL)
- Maturité et adoption enterprise

## Inconvénients de AMQP

- Plus complexe et lourd que MQTT
- Overhead plus important
- Moins adapté aux appareils très contraints
- Courbe d'apprentissage plus élevée

## Cas d'usage

- Systèmes bancaires et financiers
- E-commerce et traitement des commandes
- Intégration d'applications d'entreprise (EAI)
- Microservices et event-driven architecture
- Systèmes de files d'attente distribuées
- Logs et monitoring centralisés

## Entreprises et projets utilisant AMQP

- JPMorgan Chase
- Red Hat
- Microsoft Azure Service Bus
- RabbitMQ
- Apache Qpid
- StormMQ
- OpenStack

## Logiciels et implémentations AMQP

### Brokers

- **RabbitMQ** : Broker open source très populaire
- **Apache Qpid** : Implémentation open source
- **Apache ActiveMQ** : Supporte AMQP
- **Microsoft Azure Service Bus**
- **Red Hat AMQ**

### Clients

- **Pika** (Python)
- **amqp-client** (Node.js)
- **RabbitMQ Java Client**
- **Qpid JMS**
- **Spring AMQP**

## Installation et commandes Linux

### Installer RabbitMQ sur Debian/Ubuntu

```bash
# Installer les dépendances
sudo apt update
sudo apt install curl gnupg -y

# Ajouter la clé RabbitMQ
curl -fsSL https://packagecloud.io/rabbitmq/rabbitmq-server/gpgkey | sudo apt-key add -

# Ajouter le dépôt
echo "deb https://packagecloud.io/rabbitmq/rabbitmq-server/ubuntu/ $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/rabbitmq.list

# Installer RabbitMQ
sudo apt update
sudo apt install rabbitmq-server -y

# Démarrer le service
sudo systemctl start rabbitmq-server
sudo systemctl enable rabbitmq-server

# Activer le plugin management
sudo rabbitmq-plugins enable rabbitmq_management

# Créer un utilisateur admin
sudo rabbitmqctl add_user admin monpassword
sudo rabbitmqctl set_user_tags admin administrator
sudo rabbitmqctl set_permissions -p / admin ".*" ".*" ".*"
```

### Commandes de vérification Linux

```bash
# Vérifier le statut
sudo systemctl status rabbitmq-server

# Vérifier les ports
sudo netstat -tlnp | grep -E '5672|15672'
sudo ss -tlnp | grep -E '5672|15672'

# Lister les utilisateurs
sudo rabbitmqctl list_users

# Lister les queues
sudo rabbitmqctl list_queues

# Lister les exchanges
sudo rabbitmqctl list_exchanges

# Lister les connexions
sudo rabbitmqctl list_connections

# Vérifier les vhosts
sudo rabbitmqctl list_vhosts
```

## Commandes Windows

```powershell
# Télécharger et installer RabbitMQ
# https://www.rabbitmq.com/install-windows.html

# Vérifier le service
Get-Service RabbitMQ

# Lister les plugins
rabbitmq-plugins.bat list

# Activer le management
rabbitmq-plugins.bat enable rabbitmq_management

# Commandes rabbitmqctl
rabbitmqctl.bat status
rabbitmqctl.bat list_queues
```

## Configuration RabbitMQ

### Fichier de configuration

- Linux : `/etc/rabbitmq/rabbitmq.conf` (format sysctl) ou `/etc/rabbitmq/advanced.config` (Erlang)
- Windows : `%APPDATA%\RabbitMQ\rabbitmq.conf`

### Exemple rabbitmq.conf

```ini
# Port AMQP standard
listeners.tcp.default = 5672

# Port AMQPS (TLS)
listeners.ssl.default = 5671

# Management plugin
management.tcp.port = 15672
management.ssl.port = 15671

# Authentification
loopback_users.guest = false

# Mémoire et disque
vm_memory_high_watermark.relative = 0.6
disk_free_limit.relative = 1.5

# TLS
ssl_options.cacertfile = /etc/rabbitmq/ssl/ca_certificate.pem
ssl_options.certfile = /etc/rabbitmq/ssl/server_certificate.pem
ssl_options.keyfile = /etc/rabbitmq/ssl/server_key.pem
ssl_options.verify = verify_peer
ssl_options.fail_if_no_peer_cert = false
```

## Interfaces de configuration

- **RabbitMQ Management UI** : http://localhost:15672
- **rabbitmqctl** : ligne de commande
- **API HTTP Management** : REST API
- **Prometheus + Grafana** : monitoring

## Sécurité AMQP

- AMQPS avec TLS/SSL
- Authentification SASL (PLAIN, EXTERNAL, etc.)
- ACL et permissions par vhost
- Politiques de mots de passe
- Isolation réseau
- Audit des connexions

## Ressources AMQP

- Site officiel AMQP : https://www.amqp.org/
- RabbitMQ : https://www.rabbitmq.com/
- Apache Qpid : https://qpid.apache.org/
- OASIS AMQP 1.0 : https://www.oasis-open.org/standards/#amqpv1.0
- ISO/IEC 19464

---

# DDS (Data Distribution Service)

## Définition

DDS est un middleware de communication temps réel, basé sur un modèle publish/subscribe décentralisé, conçu pour les systèmes distribués critiques nécessitant une faible latence, une haute disponibilité et une découverte automatique des participants.

## Historique et créateurs

DDS a été développé par **Object Management Group (OMG)** dans les années 2000. Les premières spécifications ont été publiées en 2004. DDS est issu des travaux de plusieurs entreprises, notamment **Real-Time Innovations (RTI)** fondée par **Stanley Schneider**. RTI est l'un des principaux contributeurs et fournisseurs commerciaux de DDS.

## Caractéristiques techniques

### Modèle de communication

DDS utilise un modèle publish/subscribe décentralisé sans broker central. Les participants découvrent automatiquement les topics et les abonnés sur le réseau.

### Entités DDS

- **Domain** : Espace de nommage logique isolant les applications
- **DomainParticipant** : Point d'accès à un domaine
- **Topic** : Canal de données typé
- **Publisher** : Producteur de données
- **Subscriber** : Consommateur de données
- **DataWriter** : Écrit des échantillons de données
- **DataReader** : Lit des échantillons de données

### QoS (Quality of Service)

DDS offre une vingtaine de politiques QoS :

- **RELIABILITY** : Best-effort ou reliable
- **DURABILITY** : Volatile, transient local, transient, persistent
- **DEADLINE** : Garantie de fréquence de publication
- **LATENCY_BUDGET** : Budget de latence
- **LIVELINESS** : Surveillance de la vitalité des publishers
- **HISTORY** : Keep last ou keep all
- **LIFESPAN** : Durée de validité des données
- **OWNERSHIP** : Gestion des publishers exclusifs
- **PARTITION** : Segmentation logique

### Découverte

DDS utilise le protocole **Simple Discovery Protocol (SDP)** et **RTPS (Real-Time Publish-Subscribe)** pour la découverte automatique des participants. RTPS est défini dans la spécification DDSI-RTPS.

### Niveau transport

DDS peut utiliser UDP, TCP, Shared Memory ou transports propriétaires. RTPS fonctionne généralement sur UDP.

## Architecture DDS

```
┌─────────────────────────────────────────────────────────────┐
│                         Domain 0                            │
│  ┌──────────────┐      Topic      ┌──────────────┐         │
│  │  Publisher   │ ── temperature ─>│  Subscriber  │         │
│  │  (Capteur)   │                  │  (Dashboard) │         │
│  └──────────────┘                  └──────────────┘         │
│  ┌──────────────┐      Topic      ┌──────────────┐         │
│  │  Publisher   │ ─── pressure ──>│  Subscriber  │         │
│  │  (Capteur)   │                  │  (Alarme)    │         │
│  └──────────────┘                  └──────────────┘         │
│                                                             │
│              Pas de broker central !                        │
│         Découverte automatique via RTPS                     │
└─────────────────────────────────────────────────────────────┘
```

## Avantages de DDS

- Très faible latence
- Pas de point de défaillance central (brokerless)
- Découverte automatique
- QoS très riches et configurables
- Haute disponibilité et redondance
- Idéal pour les systèmes temps réel critiques

## Inconvénients de DDS

- Complexité élevée
- Courbe d'apprentissage importante
- Moins adapté aux appareils très contraints
- Coût des solutions commerciales
- Configuration QoS complexe

## Cas d'usage

- Systèmes de défense et aérospatiaux
- Automobile autonome (ADAS)
- Systèmes médicaux critiques
- Robotique industrielle
- Smart grid et énergie
- Simulation et jeux sérieux
- Systèmes ferroviaires

## Entreprises et projets utilisant DDS

- RTI (Real-Time Innovations)
- eProsima
- ADLINK Technology
- Object Computing Inc. (OCI)
- PrismTech (maintenant ADLINK)
- ROS 2 (Robot Operating System 2)
- AUTOSAR Adaptive

## Logiciels et implémentations DDS

### Implémentations commerciales

- **RTI Connext DDS**
- **ADLINK OpenSplice**
- **TwinOaks CoreDX DDS**

### Implémentations open source

- **Eclipse Cyclone DDS**
- **eProsima Fast DDS**
- **OpenDDS** (Object Computing)
- **ROS 2 Middleware (rmw)**

## Installation et commandes Linux

### Installer Eclipse Cyclone DDS

```bash
# Cloner le dépôt
git clone https://github.com/eclipse-cyclonedds/cyclonedds.git
cd cyclonedds

# Compiler
mkdir build && cd build
cmake ..
make
sudo make install
```

### Installer ROS 2 avec Fast DDS

```bash
# Ubuntu 22.04
sudo apt install ros-humble-rmw-fastrtps-cpp

# Configurer l'environnement
source /opt/ros/humble/setup.bash
```

### Commandes de vérification Linux

```bash
# Vérifier les ports RTPS
sudo netstat -ulnp | grep 7400
sudo ss -ulnp | grep cyclonedds

# Vérifier les processus DDS
ps aux | grep dds

# Lister les interfaces réseau utilisées
ip addr show

# Test avec ROS 2
ros2 topic list
ros2 topic echo /topic_name
ros2 topic pub /topic_name std_msgs/String "data: Hello DDS"
```

## Commandes Windows

```powershell
# Vérifier les ports
netstat -an | findstr 7400

# Vérifier les processus
Get-Process | Where-Object {$_.ProcessName -like "*dds*"}

# ROS 2 sur Windows
ros2 topic list
ros2 topic echo /topic_name
```

## Configuration DDS

### Exemple de configuration XML Cyclone DDS

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<CycloneDDS xmlns="https://cdds.io/config"
            xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
            xsi:schemaLocation="https://cdds.io/config https://raw.githubusercontent.com/eclipse-cyclonedds/cyclonedds/master/etc/cyclonedds.xsd">
    <Domain id="any">
        <General>
            <NetworkInterfaceAddress>auto</NetworkInterfaceAddress>
            <AllowMulticast>true</AllowMulticast>
            <MaxMessageSize>65500B</MaxMessageSize>
        </General>
        <Discovery>
            <ParticipantIndex>auto</ParticipantIndex>
        </Discovery>
        <Internal>
            <Watermarks>
                <WhcHigh>500kB</WhcHigh>
            </Watermarks>
        </Internal>
    </Domain>
</CycloneDDS>
```

### Configuration QoS en XML

```xml
<dds xmlns="http://www.omg.org/dds/">
    <qos_profile name="ReliableProfile">
        <datawriter_qos>
            <reliability>
                <kind>RELIABLE_RELIABILITY_QOS</kind>
            </reliability>
            <durability>
                <kind>TRANSIENT_LOCAL_DURABILITY_QOS</kind>
            </durability>
        </datawriter_qos>
        <datareader_qos>
            <reliability>
                <kind>RELIABLE_RELIABILITY_QOS</kind>
            </reliability>
        </datareader_qos>
    </qos_profile>
</dds>
```

## Interfaces de configuration

- **Fichiers XML QoS**
- **RTI Admin Console**
- **RTI Shapes Demo**
- **ROS 2 CLI**
- **Code API C/C++/Python**

## Sécurité DDS

- DDS Security (spécification OMG)
- Authentification via certificats
- Chiffrement des données
- Contrôle d'accès basé sur les topics
- Logging et audit
- RTPS Secure (RTPS-SEC)

## Ressources DDS

- OMG DDS : https://www.omg.org/ DDS/
- RTI Connext : https://www.rti.com/
- Eclipse Cyclone DDS : https://cyclonedds.io/
- eProsima Fast DDS : https://www.eprosima.com/
- OpenDDS : https://opendds.org/
- ROS 2 : https://docs.ros.org/

---

# XMPP (Extensible Messaging and Presence Protocol)

## Définition

XMPP est un protocole ouvert de messagerie instantanée, de présence et de communication temps réel, basé sur XML et sur une architecture fédérée décentralisée. Il est extensible via des XEP (XMPP Extension Protocols).

## Historique et créateurs

XMPP a été créé en 1998 par **Jeremie Miller** sous le nom de Jabber. Le projet Jabber a donné naissance au protocole qui a été formalisé par l'IETF en 2004 dans les RFC 3920 et 3921. En 2011, les RFC ont été mises à jour en RFC 6120, 6121 et 6122. La XMPP Standards Foundation (XSF) supervise les extensions XEP.

## Caractéristiques techniques

### Modèle de communication

XMPP utilise une architecture client/serveur fédérée. Chaque utilisateur a un identifiant JID (Jabber ID) de la forme `utilisateur@domaine/resource`.

### Niveau transport

XMPP utilise TCP, généralement sur le port 5222 pour les clients et 5269 pour la fédération serveur-à-serveur. XMPP over TLS utilise les mêmes ports avec STARTTLS.

### Format des messages

Les messages XMPP sont encodés en XML. Un stanza XMPP typique :

```xml
<message to="ami@example.com" from="moi@example.com" type="chat" id="msg123">
    <body>Salut !</body>
</message>
```

### Types de stanzas

- **`<message>`** : Envoi de messages
- **`<presence>`** : Gestion de la présence
- **`<iq>`** : Requêtes/réponses (info/query)

### Extensions XEP

- **XEP-0004** : Data Forms
- **XEP-0045** : Multi-User Chat (MUC)
- **XEP-0048** : Bookmarks
- **XEP-0060** : Publish-Subscribe
- **XEP-0096** : File Transfer
- **XEP-0163** : Personal Eventing Protocol
- **XEP-0234** : File Transfer HTTP
- **XEP-0245** : /me Command
- **XEP-0313** : Message Archive Management (MAM)
- **XEP-0352** : Client State Indication
- **XEP-0363** : HTTP File Upload
- **XEP-0384** : OMEMO Encryption

## Architecture XMPP

```
┌─────────────┐         5222          ┌─────────────┐
│   Client    │ <──────────────────>  │   Serveur   │
│   XMPP      │                       │   XMPP      │
└─────────────┘                       │  example.com│
                                      └──────┬──────┘
                                             │ 5269
                                             │ fédération
                                             ▼
                                      ┌─────────────┐
                                      │   Serveur   │
                                      │  autre.com  │
                                      └──────┬──────┘
                                             │
                                             ▼
                                      ┌─────────────┐
                                      │   Client    │
                                      │   distant   │
                                      └─────────────┘
```

## Avantages de XMPP

- Standard ouvert et décentralisé
- Fédération entre serveurs
- Très extensible via XEP
- Sécurité éprouvée (TLS, SASL)
- Large écosystème de clients et serveurs
- Pas de dépendance à une entreprise unique

## Inconvénients de XMPP

- XML verbeux, consommation de bande passante élevée
- Moins populaire que les messageries propriétaires
- Fragmentation des implémentations XEP
- Complexité de la fédération moderne

## Cas d'usage

- Messagerie instantanée d'entreprise
- Chatbots
- IoT (XMPP for IoT via XEP)
- Jeux en ligne
- Notifications push
- Collaboration en temps réel
- Réseaux sociaux décentralisés

## Entreprises et projets utilisant XMPP

- WhatsApp (ancienne infrastructure basée sur XMPP)
- Jitsi Meet (XMPP via Prosody)
- Movim
- Conversations
- Gajim
- Pidgin
- Openfire

## Logiciels et implémentations XMPP

### Serveurs

- **Prosody** : Serveur open source léger en Lua
- **Openfire** : Serveur Java avec interface web
- **ejabberd** : Serveur Erlang haute performance
- **Tigase** : Serveur Java
- **Metronome IM**

### Clients

- **Conversations** (Android)
- **Gajim** (Linux/Windows)
- **Dino** (Linux)
- **Pidgin** (multiplateforme)
- **Psi**
- **Swift**
- **Monal** (iOS/macOS)

## Installation et commandes Linux

### Installer Prosody sur Debian/Ubuntu

```bash
# Ajouter le dépôt Prosody
sudo apt install lua5.2 liblua5.2 -y

# Télécharger depuis le dépôt officiel
echo "deb http://packages.prosody.im/debian $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/prosody.list
wget https://prosody.im/files/prosody-debian-packages.key -O- | sudo apt-key add -

# Installer
sudo apt update
sudo apt install prosody -y

# Démarrer
sudo systemctl start prosody
sudo systemctl enable prosody
```

### Installer ejabberd

```bash
sudo apt install ejabberd -y
sudo systemctl start ejabberd
```

### Commandes de vérification Linux

```bash
# Vérifier le statut
sudo systemctl status prosody

# Vérifier les ports
sudo netstat -tlnp | grep -E '5222|5269|5280'
sudo ss -tlnp | grep -E '5222|5269|5280'

# Vérifier la résolution DNS SRV
dig SRV _xmpp-client._tcp.example.com
dig SRV _xmpp-server._tcp.example.com

# Tester avec telnet
telnet localhost 5222

# Vérifier les certificats
openssl s_client -connect localhost:5222 -starttls xmpp
```

## Commandes Windows

```powershell
# Vérifier les ports
netstat -an | findstr 5222

# Tester la connexion
Test-NetConnection -ComputerName localhost -Port 5222

# ejabberd Windows
# https://www.process-one.net/en/ejabberd/downloads/
```

## Configuration Prosody

### Fichier de configuration

Linux : `/etc/prosody/prosody.cfg.lua`

### Exemple de configuration

```lua
-- Informations du serveur
VirtualHost "example.com"
enabled = true

-- Modules
modules_enabled = {
    "roster";
    "saslauth";
    "tls";
    "dialback";
    "disco";
    "private";
    "vcard";
    "version";
    "uptime";
    "time";
    "ping";
    "pep";
    "register";
    "muc";
    "muc_mam";
    "carbons";
    "smacks";
}

-- Authentification
authentication = "internal_hashed"

-- Stockage
storage = "internal"

-- Certificats SSL
ssl = {
    key = "/etc/prosody/certs/example.com.key";
    certificate = "/etc/prosody/certs/example.com.crt";
}

-- MUC (salons de discussion)
Component "conference.example.com" "muc"
    name = "Salons Example"
    modules_enabled = { "muc_mam" }

-- Port standard
 interfaces = { "*" }
port = 5222
```

## Interfaces de configuration

- **Fichier Lua** pour Prosody
- **Interface web Openfire**
- **ejabberd Web Admin** : http://localhost:5280/admin
- **Gajim** : client avec configuration avancée

## Sécurité XMPP

- TLS/SSL obligatoire (STARTTLS ou direct)
- SASL authentication (SCRAM-SHA-256, DIGEST-MD5, etc.)
- Certificats de confiance
- OMEMO (chiffrement bout-en-bout via XEP-0384)
- OTR (Off-the-Record)
- ACL et modules de sécurité

## Ressources XMPP

- XMPP.org : https://xmpp.org/
- XEP Registry : https://xmpp.org/extensions/
- Prosody : https://prosody.im/
- ejabberd : https://www.ejabberd.im/
- Openfire : https://www.igniterealtime.org/projects/openfire/
- Conversations : https://conversations.im/

---

# Tableau comparatif des protocoles

| Critère | MQTT | CoAP | AMQP | DDS | XMPP |
|---------|------|------|------|-----|------|
| **Modèle** | Pub/Sub (broker) | Client/Serveur REST | Message Queue / Pub-Sub | Pub/Sub décentralisé | Client/Serveur fédéré |
| **Transport** | TCP | UDP | TCP | UDP/TCP/SHM | TCP |
| **Port standard** | 1883 / 8883 | 5683 / 5684 | 5672 / 5671 | Variable (RTPS UDP) | 5222 / 5269 |
| **Format** | Binaire léger | Binaire léger | Binaire | Binaire/CDR | XML |
| **QoS** | 3 niveaux | CON/NON + Observe | Transactions + modes | Très riches | Dépend des XEP |
| **Découverte** | Non native | `.well-known/core` | Via broker/admin | Automatique RTPS | Serveurs DNS/SRV |
| **Sécurité** | TLS + Auth | DTLS + Auth | TLS + SASL | DDS Security | TLS + SASL |
| **Latence** | Faible | Très faible | Moyenne | Très faible | Moyenne |
| **Bande passante** | Très faible | Très faible | Moyenne | Faible | Élevée (XML) |
| **Complexité** | Faible | Moyenne | Élevée | Très élevée | Moyenne |
| **Cas principal** | IoT, capteurs | Capteurs contraints | Enterprise, finance | Temps réel critique | Messagerie, chat |
| **Standard** | OASIS MQTT 5.0 | RFC 7252 | OASIS/ISO 19464 | OMG | IETF RFC 6120/6121 |
| **Broker** | Oui | Non | Oui | Non | Oui (serveur) |

---

# Guide de sélection de protocole

## Choisir MQTT si...

- Vous avez des capteurs ou appareils IoT avec peu de ressources
- Le réseau est peu fiable ou à bande passante limitée
- Vous voulez un modèle pub/sub simple avec broker
- Vous avez besoin de QoS configurable
- Vous voulez un écosystème mature et largement supporté

## Choisir CoAP si...

- Vous avez des appareils très contraints (6LoWPAN, LoRaWAN)
- Vous voulez une approche RESTful légère sur UDP
- Vous avez besoin de multicast
- Vous voulez intégrer facilement avec HTTP
- La consommation énergétique est critique

## Choisir AMQP si...

- Vous avez besoin d'un système de messagerie d'entreprise robuste
- Vous avez besoin de routage avancé (exchanges, bindings)
- Vous avez besoin de transactions et de fiabilité forte
- Vous intégrez des systèmes hétérogènes
- Vous avez une infrastructure cloud/hybride

## Choisir DDS si...

- Vous avez des systèmes temps réel critiques
- Vous avez besoin de très faible latence
- Vous voulez éviter un point de défaillance central
- Vous avez besoin de QoS riches et granulaires
- Vous travaillez dans l'aérospatial, la défense, l'automobile, la robotique

## Choisir XMPP si...

- Vous voulez de la messagerie instantanée décentralisée
- Vous avez besoin de fédération entre serveurs
- Vous voulez une extensibilité via XEP
- Vous avez besoin de présence et de chat multi-utilisateurs
- Vous voulez éviter les silos propriétaires

---

# Sécurité commune

## Bonnes pratiques générales

1. **Toujours utiliser TLS/SSL** pour chiffrer les communications
2. **Authentifier tous les clients** avec des identifiants forts
3. **Restreindre les permissions** avec des ACL
4. **Isoler les services** par réseau, VLAN ou firewall
5. **Surveiller les logs** et configurer des alertes
6. **Mettre à jour régulièrement** les logiciels
7. **Utiliser des certificats valides** et renouveler avant expiration
8. **Limiter les tentatives de connexion** pour prévenir les attaques par force brute
9. **Sauvegarder les configurations** et tester les restaurations
10. **Auditer régulièrement** les accès et les permissions

## Certificats TLS

### Générer une autorité de certification avec OpenSSL

```bash
# Créer la clé privée de la CA
openssl genrsa -out ca.key 4096

# Créer le certificat auto-signé de la CA
openssl req -x509 -new -nodes -key ca.key -sha256 -days 3650 -out ca.crt \
  -subj "/C=TD/ST=Chad/L=N'Djamena/O=hackers_tchad/CN=hackers_tchad CA"

# Créer une clé pour le serveur
openssl genrsa -out server.key 2048

# Créer une demande de certificat (CSR)
openssl req -new -key server.key -out server.csr \
  -subj "/C=TD/ST=Chad/L=N'Djamena/O=hackers_tchad/CN=mqtt.example.com"

# Signer le certificat avec la CA
openssl x509 -req -in server.csr -CA ca.crt -CAkey ca.key \
  -CAcreateserial -out server.crt -days 365 -sha256
```

---

# Commandes de vérification

## Commandes réseau universelles sous Linux

```bash
# Vérifier les ports ouverts
sudo netstat -tulnp
sudo ss -tulnp

# Scanner un port spécifique
nc -vz host port
nc -vzu host port  # UDP

# Test TCP avec timeout
timeout 5 bash -c 'cat < /dev/null > /dev/tcp/localhost/1883'

# Résolution DNS
dig host.example.com
nslookup host.example.com
host host.example.com

# Traceroute
traceroute host.example.com
mtr host.example.com

# Capture de paquets (nécessite Wireshark/tshark)
sudo tshark -i any -f "tcp port 1883"
sudo tcpdump -i any port 1883 -nn

# Vérifier les processus
ps aux | grep mosquitto
ps aux | grep rabbitmq
ps aux | grep prosody
ps aux | grep java

# Vérifier l'utilisation des ressources
top
htop
iotop
vmstat 1
```

## Commandes réseau universelles sous Windows

```powershell
# Vérifier les ports
netstat -an
Get-NetTCPConnection

# Tester un port
Test-NetConnection -ComputerName localhost -Port 1883

# Résolution DNS
Resolve-DnsName example.com
nslookup example.com

# Traceroute
Test-NetConnection example.com -TraceRoute

# Vérifier les processus
Get-Process | Where-Object {$_.ProcessName -like "*rabbitmq*"}

# Vérifier les services
Get-Service mosquitto
Get-Service rabbitmq
```

## Commandes Docker

```bash
# Exécuter Mosquitto avec Docker
docker run -d --name mosquitto -p 1883:1883 -p 9001:9001 eclipse-mosquitto

# Exécuter RabbitMQ avec Docker
docker run -d --name rabbitmq -p 5672:5672 -p 15672:15672 rabbitmq:3-management

# Exécuter Prosody avec Docker
docker run -d --name prosody -p 5222:5222 prosody/prosody

# Voir les logs
docker logs mosquitto
docker logs rabbitmq
docker logs prosody

# Entrer dans un conteneur
docker exec -it mosquitto sh
docker exec -it rabbitmq bash
```

---

# Outils et interfaces de configuration

## Outils génériques

| Outil | Usage | Plateforme |
|-------|-------|------------|
| **MQTT Explorer** | Visualiser topics MQTT | Windows/Linux/macOS |
| **Node-RED** | Flux visuels IoT | Toutes |
| **Wireshark** | Analyse de paquets | Toutes |
| **Postman** | Tester APIs et protocoles | Toutes |
| **Putty** | Connexion SSH/Telnet | Windows |
| **OpenSSL** | Gestion certificats | Toutes |
| **nmap** | Scan de ports | Linux/Windows |

## Interfaces web

- **RabbitMQ Management** : http://localhost:15672
- **HiveMQ Control Center** : http://localhost:8080
- **EMQX Dashboard** : http://localhost:18083
- **Openfire Admin** : http://localhost:9090
- **ejabberd Web Admin** : http://localhost:5280/admin

---

# Glossaire

- **Broker** : Serveur intermédiaire qui reçoit et redistribue les messages
- **Pub/Sub** : Modèle publish/subscribe où les producteurs et consommateurs sont découplés
- **Topic** : Canal logique de communication
- **Queue** : File d'attente de messages
- **Exchange** : Point de routage AMQP
- **QoS** : Quality of Service, qualité de service garantie
- **TLS/SSL** : Protocoles de chiffrement des communications
- **DTLS** : TLS pour UDP
- **SASL** : Simple Authentication and Security Layer
- **ACL** : Access Control List, liste de contrôle d'accès
- **RTPS** : Real-Time Publish-Subscribe, protocole DDS
- **JID** : Jabber ID, identifiant XMPP
- **XEP** : XMPP Extension Protocol
- **MUC** : Multi-User Chat, salon XMPP
- **LPWAN** : Low Power Wide Area Network
- **M2M** : Machine to Machine
- **IoT** : Internet of Things, Internet des Objets
- **IIoT** : Industrial IoT, IoT industriel
- **REST** : Representational State Transfer
- **XML** : eXtensible Markup Language
- **JSON** : JavaScript Object Notation
- **NAT** : Network Address Translation
- **DTLS** : Datagram Transport Layer Security
- **mTLS** : Mutual TLS, authentification mutuelle par certificats
- **LWT** : Last Will and Testament, testament MQTT

---

# Ressources et liens

## Sites officiels

- MQTT : https://mqtt.org/
- CoAP : https://coap.technology/
- AMQP : https://www.amqp.org/
- DDS : https://www.omg.org/ DDS/
- XMPP : https://xmpp.org/

## Organisations de standardisation

- OASIS : https://www.oasis-open.org/
- IETF : https://www.ietf.org/
- OMG : https://www.omg.org/
- Eclipse Foundation : https://www.eclipse.org/
- XMPP Standards Foundation : https://xmpp.org/about/xmpp-standards-foundation.html

## Documentations et RFC

- MQTT 5.0 : https://docs.oasis-open.org/mqtt/mqtt/v5.0/mqtt-v5.0.html
- RFC 7252 (CoAP) : https://tools.ietf.org/html/rfc7252
- RFC 7641 (CoAP Observe) : https://tools.ietf.org/html/rfc7641
- RFC 7959 (CoAP Block) : https://tools.ietf.org/html/rfc7959
- AMQP 1.0 : https://docs.oasis-open.org/amqp/core/v1.0/os/amqp-core-complete-v1.0-os.pdf
- DDS spécification OMG : https://www.omg.org/spec/DDS/
- RFC 6120 (XMPP Core) : https://tools.ietf.org/html/rfc6120
- RFC 6121 (XMPP IM) : https://tools.ietf.org/html/rfc6121

## Formations et tutoriels

- HiveMQ MQTT Essentials : https://www.hivemq.com/mqtt-essentials/
- RabbitMQ Tutorials : https://www.rabbitmq.com/getstarted.html
- Eclipse IoT : https://iot.eclipse.org/
- ROS 2 Documentation : https://docs.ros.org/en/humble/
- XMPP.org Getting Started : https://xmpp.org/getting-started/

---

# Auteur

<p align="center">
  <img src="https://img.shields.io/badge/Cr%C3%A9%C3%A9%20par-hackers__tchad-00ff00?style=for-the-badge&logoColor=black" alt="hackers_tchad">
</p>

**hackers_tchad** est une communauté dédiée à la cybersécurité, au hacking éthique, au développement logiciel et aux technologies émergentes au Tchad et en Afrique.

- **GitHub** : https://github.com/hackers_tchad
- **Contact** : hackers_tchad@protonmail.com

---

<div align="center">

```
╔══════════════════════════════════════════════════════════════════╗
║                                                                  ║
║     MERCI D'AVOIR LU CE GUIDE COMPLET SUR LES PROTOCOLES         ║
║           MQTT • CoAP • AMQP • DDS • XMPP                        ║
║                                                                  ║
║              Créé avec passion par hackers_tchad                 ║
║                                                                  ║
╚══════════════════════════════════════════════════════════════════╝
```

</div>
