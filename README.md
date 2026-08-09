\# 📊 Automated KPI Reporting Dashboard



\## 📌 Projektübersicht



Automated KPI Reporting ist ein End-to-End Business-Intelligence-Projekt zur automatisierten Analyse von Verkaufsdaten und Visualisierung wichtiger Unternehmenskennzahlen (KPIs) in einem interaktiven Power BI-Dashboard.



Das Projekt kombiniert PostgreSQL, SQL, n8n und Power BI, um Verkaufsdaten automatisiert auszuwerten und entscheidungsrelevante Kennzahlen bereitzustellen.



Der komplette Prozess umfasst:



\- Speicherung der Verkaufsdaten in PostgreSQL

\- Automatisierte SQL-Abfragen über n8n

\- Berechnung wichtiger KPIs

\- Visualisierung der Ergebnisse in einem interaktiven Power BI-Dashboard



\---



\## 🎯 Projektziel



Ziel dieses Projekts ist die Entwicklung einer automatisierten KPI-Lösung, mit der Unternehmen ihre Verkaufsleistung schneller analysieren können.



Das Projekt demonstriert den vollständigen Business-Intelligence-Prozess – von der Datenspeicherung über SQL-Abfragen bis hin zur interaktiven Visualisierung.



Das Dashboard bietet unter anderem folgende Analysefunktionen:



\- Analyse des Gesamtumsatzes

\- Anzahl der Bestellungen

\- Durchschnittlicher Bestellwert

\- Umsatz nach Produktkategorie

\- Umsatzentwicklung über die Zeit

\- Regionale Umsatzanalyse

\- Interaktive Tooltip-Seite für Produktdetails



\---



\## ⭐ Projekt-Highlights



\- End-to-End Business-Intelligence-Projekt

\- PostgreSQL als relationale Datenbank

\- SQL-basierte KPI-Berechnungen

\- Workflow-Automatisierung mit n8n

\- Interaktives Power BI-Dashboard

\- Star-Schema-Datenmodell

\- Deutsche Dashboard-Oberfläche

\- Vollständige Projektdokumentation



\---



\## 🛠 Verwendete Technologien



| Technologie | Zweck |

|-------------|-------|

| PostgreSQL | Datenbank |

| SQL | Datenanalyse |

| Power BI Desktop | Dashboard \& Visualisierung |

| DAX | KPI-Berechnungen |

| n8n | Workflow-Automatisierung |

| Excel | Ursprünglicher Datensatz |

| Markdown | Projektdokumentation |

| Git \& GitHub | Versionsverwaltung |



\---



\## 📂 Projektstruktur



```text

Automated\_KPI\_Reporting

│

├── Documentation

│   ├── Architecture.md

│   ├── SQL\_Queries.md

│   └── Workflow\_Explanation.md

│

├── Data

│   ├── Sales\_Dataset.xlsx

│   └── Sample\_Sales\_Dataset.csv

│

├── Workflow

│   └── Automated\_KPI\_Reporting.json

│

├── Screenshots

│   ├── Dashboard\_Overview.jpg

│   └── Dashboard\_Tooltip.jpg

│

├── Sales\_Performance\_Dashboard.pbix

├── Sales\_Performance\_Dashboard.pdf

└── README.md
```



\---



\## 📈 Dashboard-Komponenten



\### KPI-Karten



Das Dashboard zeigt drei zentrale Kennzahlen:



\- Gesamtumsatz

\- Anzahl der Bestellungen

\- Durchschnittlicher Bestellwert



\---



\### Balkendiagramm



\#### Umsatz nach Kategorie



Visualisierung des Gesamtumsatzes nach Produktkategorien:



\- Technologie

\- Möbel

\- Bürobedarf



\---



\### Liniendiagramm



\#### Umsatz im Zeitverlauf



Darstellung der monatlichen Umsatzentwicklung.



\---



\### Regionsfilter



Interaktive Filterung nach Regionen:



\- Osten

\- Süden

\- Westen

\- Zentrum



\---



\### Tooltip-Seite



Beim Überfahren eines Balkens im Diagramm \*\*„Umsatz nach Kategorie“\*\* erscheint eine interaktive Tooltip-Seite mit zusätzlichen Informationen.



Angezeigt werden:



\- Gesamtumsatz

\- Anzahl der Bestellungen

\- Durchschnittlicher Bestellwert

\- Umsatztrend

\- Top 3 Produkte nach Umsatz



\---



\## 🗄 Datenmodell



Das Projekt basiert auf einem klassischen \*\*Star-Schema\*\*.



\### Faktentabelle



\- `fact\_sales`



\### Dimensionstabellen



\- `dim\_customer`

\- `dim\_product`

\- `dim\_date`



\### Beziehungen



```text

fact\_sales



├── customer\_key → dim\_customer

├── product\_key  → dim\_product

└── date\_key     → dim\_date

```



\---



\## ⚙ Workflow



Die Daten werden automatisiert über einen n8n-Workflow verarbeitet.



Nach dem manuellen Start werden mehrere PostgreSQL-Abfragen parallel ausgeführt, um die benötigten Kennzahlen für das Dashboard bereitzustellen.



Der Workflow umfasst folgende Verarbeitungsschritte:



1\. KPI-Zusammenfassung

2\. Umsatz nach Kategorie

3\. Umsatz nach Region

4\. Monatliche Umsatzentwicklung

5\. Top-Produkte nach Umsatz



Die Ergebnisse werden anschließend von Power BI geladen und in einem interaktiven Dashboard visualisiert.



\---



\## 📊 Berechnete KPIs



Folgende Kennzahlen werden berechnet:



\- Gesamtumsatz

\- Anzahl der Bestellungen

\- Durchschnittlicher Bestellwert

\- Umsatz pro Kategorie

\- Umsatz pro Region

\- Monatlicher Umsatz

\- Top-Produkte nach Umsatz



\---



\## 🌍 Dashboard-Sprache



Das Dashboard wurde vollständig auf Deutsch umgesetzt.



Beispiele:



\- Gesamtumsatz

\- Anzahl der Bestellungen

\- Durchschnittlicher Bestellwert

\- Umsatz nach Kategorie

\- Umsatz im Zeitverlauf

\- Regionen

\- Möbel

\- Bürobedarf



Auch die Monatsnamen wurden lokalisiert.



Beispiele:



\- Mär

\- Mai

\- Okt

\- Dez



\---



\## 📷 Screenshots



\### Dashboardübersicht



!\[Dashboard Overview](Screenshots/Dashboard\_Overview.jpg)



\---



\### Tooltip-Seite



!\[Dashboard Tooltip](Screenshots/Dashboard\_Tooltip.jpg)


---



\## 🚀 Erweiterungsmöglichkeiten



Mögliche zukünftige Erweiterungen:



\- Automatische Datenaktualisierung

\- Geplanter n8n-Workflow

\- Automatischer E-Mail-Versand von KPI-Berichten

\- PDF-Export

\- Veröffentlichung im Power BI Service

\- Mobile Dashboard-Ansicht

\- Drillthrough-Seiten

\- Echtzeit-Datenanbindung



\---



\## 📚 Dokumentation



Weitere technische Informationen befinden sich in folgenden Dokumenten:



\- `Documentation/Architecture.md`

\- `Documentation/Workflow\_Explanation.md`

\- `Documentation/SQL\_Queries.md`



\---



\## 👨‍💻 Autor



\*\*Vaibhav Sachdeva\*\*



M.Sc. Digital Business Management



Portfolio-Projekt mit Schwerpunkt auf:



\- Business Intelligence

\- Power BI

\- SQL

\- PostgreSQL

\- DAX

\- n8n Workflow Automation

\- Datenvisualisierung



\---



\## 📄 Lizenz



Dieses Projekt wurde zu Lern-, Portfolio- und Demonstrationszwecken entwickelt.



Die verwendeten Beispieldaten dienen ausschließlich der Demonstration von Business-Intelligence-Konzepten und besitzen keinen produktiven Charakter.

