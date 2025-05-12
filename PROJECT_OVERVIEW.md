# GMToolkit – Informační zpráva pro vývoj

Tvořím **webovou aplikaci GMToolkit** pro vedení TTRPG kampaně, zaměřenou na pomoc Pánovi jeskyně. Projekt je modulární, rozdělený na **nezávislé podprojekty**, které lze nejprve testovat jako samostatné konzolové nástroje. Následně je plánováno jejich propojení pomocí **REST API** a zobrazení přes webové rozhraní (**React**).

---

## 📁 Struktura projektu

gmtoolkit/
├── core/ # Herní logika: postavy, iniciativy, generátory, deník
├── backend/ # REST API: FastAPI nebo Django REST Framework
├── frontend/ # Webové UI: React (v další fázi)
├── data/ # Vzorky, YAML/CSV/JSON soubory
└── tests/ # Testy jednotlivých modulů

---

## 🧩 Modulární podprojekty

1. **Správa postav a NPC**
   - `dataclass` nebo `pydantic`
   - CRUD operace v CLI
   - JSON ukládání

2. **Iniciativní tracker**
   - Výpočet iniciativy, fronta postav
   - Stav postav: HP, statusy
   - CLI ovládání a výpis (`rich`, `tabulate`)

3. **Náhodné generátory**
   - Generování jmen (`faker`, vlastní seznamy)
   - Poklady, NPC, události z CSV/YAML

4. **Deník kampaně**
   - Záznamy s tagy, datem a poznámkami
   - Fulltextové vyhledávání

5. **Správa lokací a map**
   - Textový popis lokací, ASCII mapy
   - Interaktivní zobrazení a úpravy

6. **REST API**
   - FastAPI nebo Django REST Framework
   - Endpointy pro CRUD operace postav, iniciativy, deníku

7. **Datová vrstva**
   - Práce se soubory: JSON, YAML, SQLite
   - Import/export, validace

8. **Frontend (volitelný později)**
   - React komponenty pro zobrazení dat z REST API
   - Formuláře a interaktivní tabulky

---

## 🚀 Vývojový postup

1. **Fáze 1 – Lokální logika v `core/`**
   - Vývoj modulů jako CLI nástrojů (nezávislých)
   - Testování základních funkcí

2. **Fáze 2 – REST API v `backend/`**
   - Zpřístupnění dat přes HTTP rozhraní

3. **Fáze 3 – Frontend v `frontend/`**
   - Vytvoření uživatelského rozhraní v Reactu
   - Napojení na API

---

_Tento dokument slouží jako referenční přehled pro udržení směru vývoje projektu GMToolkit._
