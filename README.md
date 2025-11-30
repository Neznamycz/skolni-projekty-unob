# 🌱 **Greenhouse Management System (GMS)**

**Greenhouse Management System (GMS)** je moderní, modulární a snadno rozšiřitelný nástroj pro automatizované řízení skleníku.  
Cílem projektu je vytvořit jednoduché, ale plně funkční **MVP**, které dokáže monitorovat prostředí, řídit zařízení a poskytuje vzdálenou správu přes webové rozhraní.

---

## ✨ **Funkce**

### 🔍 **Monitoring prostředí**
Systém v reálném čase sleduje klíčové parametry uvnitř skleníku:

- 🌡️ **Teplota**
- 💧 **Vlhkost vzduchu**
- 🟫 **Vlhkost půdy**
- ☀️ **Intenzita světla**
- 🫁 **Koncentrace CO₂** *(pokud je v systému používána)*

Všechna data se **ukládají do databáze** a lze je zobrazit v přehledných grafech.

---

### ⚙️ **Automatizované řízení**
GMS umožňuje **automatické i manuální ovládání**:

- 🌀 **Ventilace** (zap/vyp)  
- 🪟 **Otevírání oken / klapek**  
- 💦 **Zavlažování**  
- 💡 **LED/UV osvětlení**  

Automatické režimy se řídí **nastavitelnými prahovými hodnotami**.

---

### 📊 **Webová aplikace**
Webové rozhraní nabízí:

- 🖥️ **Dashboard** s daty v reálném čase  
- 📈 **Grafy** posledních hodin/dnů  
- 🕹️ **Manuální ovládání** aktuátorů  
- 🔔 **Notifikace při překročení limitů**  

---

### 🧠 **Backend & API**
Backend poskytuje:

- **REST API** pro čtení dat a ovládání  
- **MQTT nebo HTTP** komunikaci s mikrokontrolérem  
- Ukládání dat do **SQLite / PostgreSQL / jiných DB**

---

### 🔌 **Hardware**
Systém je navržen pro levný a dostupný hardware:

- **ESP32** nebo **Raspberry Pi**  
- Senzory:  
  - 🌡️ *DHT22*  
  - 🌡️ *DS18B20*  
  - ☀️ *BH1750*  
  - 🌱 *Soil Moisture Sensor*  
  - 🫁 *CO₂ senzor*  
- **Relé / SSR** pro ovládání zařízení  

---

## 🏗️ **Architektura**

       ┌───────────────────────┐
       │      Web UI           │
       └───────────▲───────────┘
                   │ REST API
       ┌───────────┴───────────┐
       │       Backend          │
       │  (Node.js / Python)    │
       └───────────▲───────────┘
                   │ MQTT/HTTP
       ┌───────────┴───────────┐
       │    ESP32 / RPi         │
       │  (Senzory + aktuátory) │
       └───────────▲───────────┘
                   │
           Fyzický skleník


---

## 📌 **Hlavní cíle projektu (MVP)**

- **Minimalistický**, ale funkční systém  
- **Snadná instalace a konfigurace**  
- **Nízké náklady** na hardware  
- **Otevřený kód**, snadno rozšiřitelný  

---



