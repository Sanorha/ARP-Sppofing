# ARP Spoofing (Python)

Ce projet implémente un script de **spoofing ARP** en Python. Le but de ce projet est d'apprendre à manipuler des paquets réseau et de tester des concepts de sécurité informatique, notamment l'attaque par spoofing ARP.

## 🎯 **Objectif du projet**  
- Comprendre le fonctionnement de l'ARP (Address Resolution Protocol).  
- Manipuler les paquets réseau à l'aide de la bibliothèque **Scapy**.  
- Apprendre à effectuer un **spoofing ARP** pour rediriger le trafic réseau entre une machine cible et un routeur.

Ce projet est destiné à des fins éducatives et peut être utilisé dans des environnements contrôlés pour apprendre les principes de base des attaques de type Man-in-the-Middle.

## 📜 **Description du script**  
Le script fonctionne de la manière suivante :  
1. Il demande l'adresse IP de la machine cible (cible du spoofing ARP).  
2. Il demande l'adresse IP du routeur ou point d'accès (la passerelle).  
3. Ensuite, il envoie des paquets ARP falsifiés pour rediriger le trafic entre la cible et le routeur.  
4. Lorsque le script est interrompu, il restaure les paquets ARP d'origine pour rétablir la connexion.

### Fonctionnalités
- **Récupération des adresses MAC** des machines cibles et du routeur à l'aide de requêtes ARP.
- **Spoofing ARP** pour intercepter le trafic réseau entre les deux appareils.
- **Restauration des adresses ARP** lorsque le processus est arrêté.

## ▶️ **Exemple d'utilisation**  
```bash
$ python3 arp_spoof.py
```
Adresse IP cible : 192.168.1.10
Adresse IP point d'accès : 192.168.1.1

Le script commence à envoyer des paquets ARP pour intercepter le trafic réseau entre la cible et la passerelle. Pour l'arrêter, utilisez Ctrl + C. Le script rétablira alors les adresses MAC d'origine.

## 🧠 Pourquoi ce projet ?
Ce projet m'a permis de me familiariser avec la manipulation des paquets réseau en Python, en utilisant Scapy. J'ai appris à comprendre le protocole ARP et comment il peut être manipulé dans un contexte de test de sécurité.

Quelques pistes d'amélioration possibles :

Ajouter des options pour exécuter le script de manière plus flexible (choix d'interface réseau, etc.).

Intégrer une interface utilisateur pour rendre l'expérience plus interactive.

Tester d'autres types d'attaques sur des réseaux privés.

## ⚠️ Avertissement

> Ce script est **strictement éducatif**. Il ne doit en aucun cas être utilisé pour tenter de déchiffrer des mots de passe réels ou accéder à des systèmes sans autorisation.

---

📁 Projet réalisé dans le cadre de ma candidature à une formation en cybersécurité.  
