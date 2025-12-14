
## Smart Energy Monitoring System (SEMS)

---

## 1. Produktbezeichnung

**SEMS (Smart Energy Monitoring System)**

---

## 2. Abstrakt zum Produkt und Projekt

### Produkt

SEMS ist eine zentrale Software-Applikation zur Aggregation und Verarbeitung von  
Smart-Home-Gerätedaten. Das System verwendet eine **geschichtete Architektur**.

Die Anbindung der Hardwarekomponenten erfolgt über das Kommunikationsprotokoll  
**CoAP (Constrained Application Protocol)** zur Erfassung von Gerätedaten.  
Diese Daten werden anschließend in einem dedizierten Systembereich prozessiert  
und zur schnellen Verfügbarkeit **persistent gespeichert**.

Die Applikation stellt die gesammelten Informationen sowie den Systemstatus  
für den Nutzer visuell dar. Das System unterstützt die Betriebssysteme  
**iOS** und **Android**.

### Projekt

Ziel des Projekts ist die **Entwicklung und Implementierung eines funktionsfähigen  
SEMS-Prototyps**.

Das Ergebnis muss die vollständige Verarbeitungskette demonstrieren:
- Erfassung von Gerätedaten über **CoAP**
- Unterstützung von **mindestens zwei unterschiedlichen Gerätetypen**
- Persistente Speicherung der Daten
- Visuelle Darstellung der Daten in der mobilen Applikation

---

## 3. Zu erzielendes Ergebnis (Produkt) und zentrale Eigenschaften

Das Projektergebnis ist eine **lauffähige und dokumentierte SEMS-Applikation**,  
bestehend aus:
- einem **Backend-Service**
- einer **mobilen Client-Anwendung (iOS & Android)**

### Zentrale Eigenschaften (hierarchische Übersicht)

#### I. Systemkern & Datenfluss

- **A. CoAP-Schnittstelle**  
  Implementierung eines CoAP-Servers zum Empfang von Gerätezuständen  
  (GET / PUT) auf der Backend-Seite.

- **B. Datenverarbeitung**  
  Modul zur Validierung und Normierung der empfangenen Rohdaten zur  
  Sicherstellung der Datenqualität.

- **C. Persistenz**  
  Dedizierte Datenbank zur effizienten Speicherung von Zeitreihendaten  
  (z. B. Energieverbrauch, Temperatur).

#### II. Mobile Applikation (iOS & Android)

- **A. Geräte-Verwaltung**  
  Funktionalität zur Registrierung und Konfiguration neuer CoAP-fähiger Geräte.

- **B. Visualisierung**
  - Darstellung aktueller Messwerte  
  - Grafische Darstellung historischer Verlaufsdaten  
    (Tages-, Wochen- und Monatsbasis)

#### III. Non-funktionale Anforderungen

- **A. Sicherheit**  
  Token-basierte Authentifizierung für den App-Zugriff sowie Einsatz von  
  **CoAPs (CoAP Secure)** oder einer verschlüsselten Übertragungsschicht.

- **B. Skalierbarkeit**  
  Architekturdesign zur späteren Erweiterung der Geräteanzahl und  
  des Datenvolumens.

---

## 4. Meilenstein-Planung (phasenbasiert)

Das Projekt ist auf eine Dauer von **3 Monaten (ca. 11 Wochen)** ausgelegt.

| Meilenstein | Dauer | Beschreibung / Ergebnis |
|------------|-------|-------------------------|
| **M1: Definition & Team-Setup** | 1 Wochen | Erstellung Lasten- und Pflichtenheft, Teamaufbau, Aufgabenverteilung, Definition des CoAP-Datenmodells |
| **M2: Design & Architektur-Basis** | 2 Wochen | Finalisierung der Architektur, Setup Backend & Datenbank, Basis-CoAP-Schnittstelle |
| **M3: Umsetzung Kernfunktionalität** | 3 Wochen | Backend-Core: Datenverarbeitung, Persistenz, API, zentrale Systemlogik |
| **M4: Mobile App & Visualisierung** | 3 Wochen | Umsetzung Mobile App (iOS/Android), Benutzerverwaltung, Visualisierung, Backend-Integration |
| **M5: Testphase** | 1 Wochen | System-, Integrations- und UAT-Tests, Fehlerbehebung, Dokumentation |
| **M6: Projektabnahme** | 1 Wochen | Formale Abnahme, Übergabe von Quellcode und Dokumentation |

---

## 5. Aufwandsabschätzung und benötigte Ressourcen

### Aufwandsabschätzung (Mann-Tage, MT)

Die Aufwandsabschätzung basiert auf:
- einer **Projektlaufzeit von ca. 3 Monaten (11 Wochen)**  
- einer **Teamgröße von 4 Personen**

Bei einer durchschnittlichen Auslastung von ca. **4–5 Personentagen pro Woche**  
ergibt sich ein **Gesamtaufwand von ca. 180 Mann-Tagen (MT)**.

Die Aufwände orientieren sich an der in Kapitel 4 definierten  
**Meilenstein-Planung**.

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

---

### Personelle Zuordnung (4 Personen)

- **Person 1 – Backend & CoAP**  
  Architektur, CoAP-Schnittstelle, Datenverarbeitung

- **Person 2 – Datenbank & Persistenz**  
  Datenmodell, Speicherung, Performance

- **Person 3 – Mobile App / Frontend**  
  App-Entwicklung, UI, Visualisierung

- **Person 4 – Projektkoordination & Testing**  
  Aufgabenkoordination, Tests, Dokumentation

---

### Benötigte Ressourcen

#### Testumgebung
- CoAP-fähige Hardware oder simulierte Sensoren/Aktoren  
  (z. B. Temperatur- und Energieverbrauchsdaten)

#### Infrastruktur
- Entwicklungsumgebung für Backend und Mobile App  
- Lokale oder cloudbasierte Datenbank für Testzwecke

#### Software & Tools
- GitHub (Versionsverwaltung, Issues, Dokumentation)  
- Entwicklungsframeworks für Backend und Mobile Clients  
- Modellierungs- und Dokumentationstools


#### Testumgebung
- **CoAP-fähige Hardware (Sensoren/Aktoren)**  
  Simulation der Geräteebene zur funktionalen Prüfung

#### Infrastruktur
- **Cloud-Hosting für Backend & Datenbank**  
  Stabile Test- und spätere Produktionsumgebung

---

## 6. Verwertbarkeitsstudie und Konkurrenzprodukte

### Verwertbarkeitsstudie (technischer Fokus)

Die technische Verwertbarkeit von SEMS basiert auf der Schaffung einer  
**einheitlichen, protokollzentrierten Software-Schicht** über verschiedene  
Hardware-Ökosysteme.

Durch die ausschließliche Nutzung des offenen **CoAP-Standards** eignet sich  
SEMS als leichtgewichtige und ressourcenschonende Monitoring-Lösung.

**Wertbeitrag:**  
SEMS bietet eine technisch fokussierte Alternative zu proprietären Systemen,  
indem die Interoperabilität auf **Protokoll-Ebene standardisiert** wird.  
Messwerte unterschiedlichster CoAP-Geräte werden in einem zentralen,  
verarbeitbaren Datenpool aggregiert.

### Konkurrenzprodukte / Mitbewerber

- **Herstellerspezifische Ökosysteme**  
  Proprietäre Protokolle oder Cloud-Plattformen, eingeschränkte  
  Drittanbieter-Integration (z. B. große Smart-Home-Anbieter).

- **Open-Source-Automatisierungsplattformen**  
  Systeme wie *Home Assistant* oder *OpenHAB* mit hoher Flexibilität,  
  jedoch höherem Konfigurationsaufwand und geringerem Fokus auf  
  ein einzelnes leichtgewichtiges Protokoll.

### SEMS – Alleinstellungsmerkmal

- Offene, **standardbasierte Lösung (CoAP)**  
- Fokus auf **Energy Monitoring**
- Schlanke Architektur für **batteriebetriebene, ressourcenbeschränkte Geräte**
- Hohe Interoperabilität ohne proprietäre Abhängigkeiten
