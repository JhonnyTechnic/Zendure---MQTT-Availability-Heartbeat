# Zendure---MQTT-Availability-Heartbeat
Diese Automation markiert Zendure-MQTT-Entitäten automatisch als online, indem sie bei jedem empfangenen Datenpunkt die passenden Availability-Topics mit dem Status online aktualisiert.

Grund:
Die Zendure Solarflow 2400 unterstützt zwar MQTT, allerdings sendet sie nicht stabil die availability message.
das kann dazu führen,dass Home Assistant die Entitäten als "Nicht Verfügbar" anzeigt obwohl via MQTT daten ankommen. 

[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2FJhonnyTechnic%2FZendure---MQTT-Availability-Heartbeat%2Fblob%2Fmain%2FBlueprint_Zendure-MQTT-Availability-Heartbeat.yaml)

Anwendungsfall:
Benutzung der MQTT funktion ohne Zendure integration aus HACS.
Besonders wenn MQTT Broker (z.B.:Mosquitto) extern (also nicht als HA APP) betrieben wird.

Getestet mit:
Solarflow 2400AC+ 
Firmware V2.0.2
