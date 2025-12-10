# Dashboard Premier League – Power BI

Questo progetto nasce con l’obiettivo di esercitarmi su un caso reale utilizzando Power BI, lavorando su un flusso completo: dal database alla dashboard, con particolare attenzione anche alla qualità del dato.

## Contenuto del progetto
La dashboard fornisce una **overview sulla Premier League a livello di team**, con una visione generale delle performance delle squadre.

In particolare sono presenti:
- panoramica delle **statistiche principali per ogni squadra**
- **classifica dei top marcatori**
- **indicatori sintetici** su risultati e andamento delle squadre

Il modello è stato pensato per poter essere **esteso su più stagioni**, con l’aggiunta di ulteriori pagine di dettaglio e confronti temporali.

## Tecnologie utilizzate
- SQL Server come database di appoggio
- Power BI per la visualizzazione
- Script ETL per la preparazione dei dati

## Attività svolte
- Caricamento dati su SQL Server  
- Preparazione e trasformazione dei dati tramite ETL  
- Creazione del modello dati con tabelle di fatti e dimensioni  
- Sviluppo della dashboard di overview in Power BI  

---

## Processo di Data Profiling e Data Quality

### STEP 1 – Profilazione base
**Obiettivo:** ottenere una visione sintetica del volume dati per ogni tabella di staging.  

---

### STEP 2 – Profilazione per colonne
**Obiettivo:** analizzare ogni colonna per capire la qualità dei dati.

Per ogni colonna di ogni tabella vengono calcolati:
- numero totale di righe  
- numero di righe non valorizzate (NULL o vuote)  
- numero di valori distinti  
- percentuale di nullità e di univocità  

Questo step permette di capire subito se una colonna è:
- poco popolata  
- poco significativa  
- potenzialmente problematica  

---

### STEP 3 – Profilazione numerica
Analisi di:
- MIN  
- MAX  
- AVG  
- STDDEV  
- individuazione outlier  

Serve per verificare se i valori numerici hanno un range credibile, ad esempio:
- goal negativi  
- minuti giocati > 6000  
- età giocatore non realistica  

Questo permette di individuare valori sballati che falsano medie e KPI.

---

### STEP 4 – Regole di business
Verifica delle **logiche di dominio (calcio)**, ad esempio:
- Starts <= Matches  
- Goals <= Shots  
- Minutes >= 0  

Queste regole permettono di controllare che il dato rispetti la logica del contesto applicativo.

---

## Nota
Il progetto ha uno scopo prevalentemente didattico ed è stato realizzato per consolidare le competenze su:
- modellazione dati  
- integrazione  
- qualità del dato  
- visualizzazione in Power BI  
