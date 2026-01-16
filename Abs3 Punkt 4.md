# Abs. 3: Projektstruktur & Resourscenplannung, Punkt 4

## 1. Business Model Canvas
![Business Model Canvas]("C:\Users\Iman Chemlali\Documents\Sem3\SWE\LASTENHEFT\bmc.png")

## 2. Grobschätzung des Aufwands (Material, Personal, Finanzmittel)
### Personalaufwand
- Projektlaufzeit: ca. 3 Monate (11 Wochen)
- Teamgröße: 4 Personen
- Durchschnittliche Auslastung: 4-5 Personentage pro Woche
- Gesamtaufwand: ca. 180 Mann-Tage (MT)

**Verteilung nach Tätigkeitsbereichen**
| Tätigkeitsbereich | Aufwand (MT) | Zuordnung zu Meilensteinen / Fokus |
|------------------|-------------|------------------------------------|
| Konzeption & Spezifikation | 20 MT | M1: Lasten- & Pflichtenheft, Datenmodell, Aufgabenverteilung |
| Architektur & Design | 25 MT | M2: Systemarchitektur, Backend- & DB-Setup |
| Backend / CoAP-Implementierung | 45 MT | M2–M3: CoAP-Server, Datenverarbeitung, API |
| Datenbank & Persistenz | 25 MT | M3: Persistenzlogik, Zeitreihendaten |
| Mobile App (Frontend & Logik) | 40 MT | M4: Mobile Client, Visualisierung, Backend-Anbindung |
| Testing & Qualitätssicherung | 15 MT | M5: System-, Integrations- und UAT-Tests |
| Dokumentation & Abnahme | 10 MT | M5–M6: technische Doku, Abnahmeunterlagen |
| **Gesamt** | **180 MT** | |

#### Personalkosten

### Materialaufwand
#### Hardware
- Raspberry Pi 5: ca. 120 €
- CoAP-fähige Sensorgeräte (Temperatur, Energieverbrauch...): 150-250 €
**Summe: ca. 270-370 €**

#### Software / Tools
- Entwicklung: meist kostenlos (VS Code...)
- Backend: kostenlos (Spring Boot, Node.js...)
- Datenbank: kostenlos (MySQL...)
**Summe: kostenlos**

#### Finanzmittel
Die Gesamtkosten ergeben sich aus:
- **Personal:** ...
- **Material:** 270 - 370 €
- **Sonstiges (Reisekosten, Meetings, Infrastruktur**: 500 - 1.000 €

**Gesamtkostenrahmen**:
ca. x - x

## 3. Risiken
- Nutzung von CoAP kann zu Paketverlusten führen, wodurch Messwerte
unvollständig im Backend ankommen.
- Fällt das Gateway auf dem Raspberry Pi 5 aus, steht die gesamte Datenverarbeitung still.
- Mit wachsender Anzahl an Sensoren besteht das risiko, dass die Datenbank zum Engpass
wird und Antwortzeiten steigen.
- Sicherheitsrisiken ergeben sich durch unverschlüsselte CoAP-Kommunikation, weshalb
CoAPs oder alternative Schutzmechanismen notwendig sind. 
- Projektspezifisch kann die Unterstützung unterschiedlicher Gerätetypen zu kmplexeren
Validierungs- und Normalisierungsprozessen führen, und die Visualisierung historischer
Daten erfordert effiziente Aggregationslogik

## 4. Vergleich mit bestehenden Lösungen
- **Herstellerspezifische Ökosysteme**  
  Proprietäre Protokolle oder Cloud-Plattformen, eingeschränkte  
  Drittanbieter-Integration (z. B. große Smart-Home-Anbieter).

- **Open-Source-Automatisierungsplattformen**  
  Systeme wie *Home Assistant* oder *OpenHAB* mit hoher Flexibilität,  
  jedoch höherem Konfigurationsaufwand und geringerem Fokus auf  
  ein einzelnes leichtgewichtiges Protokoll.

