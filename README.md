# Fenster schließen – Hitzeschutz-Benachrichtigung

[![Import Blueprint](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2FTschaegged%2Ffensterschliessen-hitzeschutz-blueprint%2Fblob%2Fmain%2Fblueprints%2Fautomation%2Ffensterschliessen_hitzeschutz.yaml)

## Beschreibung

Sendet eine Benachrichtigung wenn:
1. Die **Außentemperatur** einen konfigurierbaren Schwellenwert überschreitet, **und**
2. Die Außentemperatur **wärmer** ist als der Durchschnitt der gewählten Innenraum-Sensoren, **und**
3. Fenster oder Türen **geöffnet** sind

So wird nur benachrichtigt wenn das Schließen der Fenster tatsächlich hilft – nämlich wenn draußen wärmer als drinnen ist.

## Konfiguration

| Eingabe | Beschreibung |
|---|---|
| Außentemperatursensor | Sensor für die aktuelle Außentemperatur |
| Mindest-Außentemperatur | Schwellenwert ab dem die Automation prüft (Standard: 22 °C) |
| Innenraum-Temperatursensoren | Räume für den Durchschnitt – Mehrfachauswahl |
| Fenster-/Türen-Sensor | Binärsensor für offene Fenster/Türen |
| Personen | Nur benachrichtigen wenn eine Person zu Hause ist (optional) |
| Benachrichtigungsaktionen | Beliebige HA-Aktionen (notify.mobile_app_..., etc.) |

## Anforderungen

- Home Assistant 2024.10.0 oder neuer
- Temperatursensoren für Außen- und gewünschte Innenräume
- Binärsensor für Fenster/Türen (z.B. Gruppe offener Fenster)
