# Aquasentinel-IOT Télésurveillance LoRaWAN d'infrastructures hydrauliques
Télésurveillance LoRaWAN d’infrastructures hydrauliques (ESP32, Node-RED....).

> Projet de Fin d'Études — SUP'PTIC Yaoundé (2023–2026)
> Système IoT de supervision à distance d'un réseau hydraulique, pensé pour les besoins d'un opérateur comme CAMWATER.

![Capture du tableau de bord](docs/images/dashboard.png)

## 1. Problème et objectif
Le soucis étant de resoudre le problème de supervision et gestion des infracstructures hydrauliques étant encore jusque là triviaux il est nés donc l'idées de pouvoir non seulement tout voir(les différents paramètres du fonctionnement de l'infrastructure)  sur un Dashboard mais aussi de relayer ces données des zone reculées(à couverture réseaux réduites) afin d'avoir en tout tant le moindre soucis ou parametres de ces zones quel qu'elle soit en temps réels afin d'améliorer, faciliter et assurer la bonne gestion et continuité de service de ces infrastructures. 


## 2. Architecture
![Schéma d'architecture](docs/images/architecture.png)
| Couche | Technologie |
|---|---|
| Capteurs | À COMPLÉTER (débit, pression, niveau, qualité de l'eau, position GPS, consommation d'énergies, contrôle du dispositifs ) |
| Nœud | ESP32 (plateforme Didalab Did@LoRaWAN) |
| Passerelle / serveur LoRaWAN | matériels expérimental de Did@lab
| Traitement et supervision | Node-RED, MQTT |
| Alertes | Telegram, Gmail

## 3. Fonctionnalités
- Mesure et transmission longue portée des données capteurs
- Supervision en temps réel sur tableau de bord
- Alertes automatiques par Telegram/Gmail en cas de seuil dépassé ou quelquonques soucis

## 4. Structure du dépôt
```
├── firmware/      # Code du nœud ESP32
├── node-red/      # Flux exportés (flows.json, sans identifiants)
├── docs/          # Schémas, captures, rapport
├── config/        # Fichiers
└── README.md
```

## 5. Installation et exécution
1. Cloner le dépôt : `git clone https://github.com/TON-PSEUDO/aquasentinel.git`
2. `config/0-controler-integrite.cmd`
3. Flasher le firmware sur l'ESP32 (préciser l'outil : Arduino IDE / PlatformIO)
4. Importer `node-red/flows.json` dans Node-RED
5.  Importer `influx-db/aquasentinel` dans Influx-Db

## 6. Résultats
Indiquer ce qui a été testé et mesuré : portée, fiabilité de la transmission, délai d'alerte, consommation.

## 7. Limites et perspectives
- ( tests sur site réel, sécurité des communications, passage à l'échelle,coût initial élevé)

## 8. Auteur
**Kos Nathan** — Ingénieur de Travaux en Informatique et Réseaux
Email : kosndolikedanielnathan@email.com
