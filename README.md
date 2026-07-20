# Reolink MQTT Bridge App für Home Assistant

Diese App integriert KI‑Events (Person, Fahrzeug, Tier, Paket) der Reolink RLC‑520A 
und anderer kompatibler Kameras direkt in Home Assistant über MQTT.

Sie nutzt die neue Reolink‑API (Token‑Login + Event‑Stream) und erzeugt echte 
Home Assistant Binary Sensoren über MQTT Auto‑Discovery.

Die App ist vollständig kompatibel mit dem neuen Home Assistant App‑System 
(ohne Supervisor / ohne Add-on Store).

---

## Funktionen

- Token-basierter Login in die Kamera  
- Abonnieren des KI‑Eventstreams  
- Erkennen von:
  - Person  
  - Fahrzeug  
  - Tier  
  - Paket  
- MQTT‑Publishing der Events  
- Auto‑Discovery für Home Assistant  
- Läuft als native Home Assistant App (kein Docker, kein Supervisor)

---

## Installation

### 1. Repository in Home Assistant hinzufügen

**Einstellungen → Apps → App‑Store → Repositories → Repository hinzufügen**

URL:https://github.com/bloodybeginner-spec/reolink-mqtt-app


### 2. App installieren

Nach dem Hinzufügen erscheint die App im App‑Store unter:

**Reolink MQTT Bridge**

### 3. Konfiguration eintragen

- Kamera-IP  
- Benutzername  
- Passwort  
- MQTT‑Host  
- MQTT‑Benutzer  
- MQTT‑Passwort  

### 4. App starten

Die App verbindet sich automatisch mit der Kamera und sendet KI‑Events an MQTT.

---

## Konfiguration

| Option        | Beschreibung                         |
|---------------|--------------------------------------|
| camera_host   | IP der Kamera                        |
| camera_user   | Benutzername (z. B. admin)           |
| camera_pass   | Passwort der Kamera                  |
| mqtt_host     | MQTT‑Server (z. B. 127.0.0.1)        |
| mqtt_user     | MQTT‑Benutzer                        |
| mqtt_pass     | MQTT‑Passwort                        |

---

## MQTT Topics

- `reolink/person`  
- `reolink/vehicle`  
- `reolink/pet`  
- `reolink/package`  

---

## Home Assistant Entitäten

- `binary_sensor.reolink_person`  
- `binary_sensor.reolink_vehicle`  
- `binary_sensor.reolink_pet`  
- `binary_sensor.reolink_package`  

---

## Kompatibilität

Getestet mit:

- Reolink RLC‑520A  
- Firmware v3.2.0.5180_2507241369  
- Home Assistant OS (App‑System)  
- Mosquitto MQTT  

---

## Lizenz

MIT License


