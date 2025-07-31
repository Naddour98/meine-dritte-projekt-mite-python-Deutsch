# Automatidata Taxi-Datenanalyse

### Nutzung des Codes
Um den Code auszuführen und eigene Analysen durchzuführen, gehe wie folgt vor:
1. Repository klonen
2. Virtuelle Umgebung erstellen und aktivieren
3. Abhängigkeiten installieren **pip install -r requirements.txt**
4. Notebook starten: **jupyter notebook main_file.ipynb**


### Übersicht
Dieses Projekt wurde im Rahmen meines Datenanalysekurses erstellt und zusätzlich eigeninitiativ umgesetzt, um meine Fähigkeiten zu vertiefen. Ziel war es, Taxifahrtdaten eines fiktiven Kunden, TLC (Taxi and Limousine Company), zu analysieren und prädiktive Modelle zu entwickeln, um Muster in Fahrpreisen und anderen fahrtenbezogenen Kennzahlen zu erkennen. Der Datensatz enthielt detaillierte Informationen wie Abhol- und Abgabezeiten, Entfernungen, Passagieranzahl und Zahlungsmethoden.

Im Projekt wurden verschiedene Machine-Learning-Modelle erstellt, darunter lineare Regression, Entscheidungsbaum, Random Forest und XGBoost. Nach Hyperparameter-Tuning erzielte das XGBoost-Modell die beste Gesamtleistung mit hoher Genauigkeit und guter Generalisierungsfähigkeit auf unbekannten Daten.

Die wichtigsten Faktoren, die die Fahrpreise und Gesamtkosten beeinflussten, waren Fahrstrecke, Abhol- und Abgabeort, Zahlungsmethode sowie Passagieranzahl. Diese Erkenntnisse können dem Unternehmen helfen, Preisstrategien zu optimieren und die betriebliche Planung zu verbessern.


### Datenverständnis
Die verwendeten Fahrtdaten stammen aus einem fiktiven Projekt der Firma TLC (Taxi and Limousine Company) und basieren auf synthetischen Daten. Der Datensatz umfasst mehrere zehntausend Fahrten und enthält Informationen zu Abhol- und Abgabezeitpunkten, Fahrstrecke, Anzahl der Passagiere, Zahlungsmethode sowie Fahrpreisdetails.

Die abhängige Variable variiert je nach Modellierung:
Für Regressionsmodelle wurde der Fahrpreis (total_amount) als Zielgröße genutzt.

Für Klassifikationsmodelle (z. B. Entscheidungsbaum, Random Forest, XGBoost) wurde geprüft, ob Fahrten bestimmte Merkmale erfüllen (z. B. hoher/niedriger Fahrpreisbereich).

Diese Datenstruktur ermöglicht sowohl explorative Analysen als auch den Aufbau von Vorhersagemodellen, um Muster im Fahrverhalten und in der Preisgestaltung zu identifizieren.


### Variablen definieren / Datenwörterbuch

Variable  | Beschreibung |
---------|--------------|
Unnamed: 0 | Index der Zeile im Datensatz |
VendorID | ID des Taxiunternehmens (z. B. 1 oder 2) |
tpep_pickup_datetime | Datum und Uhrzeit des Fahrtbeginns |
tpep_dropoff_datetime | Datum und Uhrzeit des Fahrtendes |
passenger_count | Anzahl der Fahrgäste im Taxi |
trip_distance | Fahrtstrecke in Meilen |
RatecodeID | Tarifcode der Fahrt (z. B. Standardtarif, JFK, Newark) |
store_and_fwd_flag | Ob die Fahrt zwischengespeichert und später übertragen wurde („Y“ oder „N“) |
PULocationID | Standort-ID des Einstiegsorts |
DOLocationID | Standort-ID des Ausstiegsorts |
payment_type | Verwendete Zahlungsmethode (z. B. Bar, Kreditkarte) |
fare_amount | Grundfahrpreis der Fahrt |
extra | Zusätzliche Gebühren (z. B. für Stoßzeiten oder Nachtfahrten) |
mta_tax | Obligatorische MTA-Steuer für die Fahrt |
tip_amount | Trinkgeld, das vom Fahrgast gegeben wurde |
tolls_amount | Mautgebühren, die während der Fahrt angefallen sind |
improvement_surcharge | Zuschlag zur Unterstützung von Fahrerleistungen |
total_amount | Gesamtbetrag, der für die Fahrt berechnet wurde (inkl. aller Gebühren) |


### Fazit
Die erstellten Modelle können dem Unternehmen dabei helfen, wichtige Einflussfaktoren auf Fahrpreise und Fahrtmuster zu erkennen und diese Informationen für betriebliche Entscheidungen zu nutzen, wie z. B. optimierte Preisgestaltung, Routenplanung oder Ressourcenzuteilung.
