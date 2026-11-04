## Progetto LUNA — Processo End-to-End in SAP S/4HANA

**Moduli:** PP / MM / SD  
**Strategia produttiva:** Make-to-Order (MTO) – Strategia 20  
**Elementi distintivi:** Variant Configuration e Production Versions

### 1. Configurazione iniziale (Customizing)

- **SPRO:** accesso all'Implementation Guide (IMG) per la configurazione dei processi produttivi.
- **OX10 / OX18:** verifica della divisione produttiva e della relativa assegnazione alla società.
- **OPPQ:** configurazione dei parametri di pianificazione MRP a livello di divisione.
- **OPL8:** definizione dei parametri dipendenti dal tipo di ordine di produzione.
- **OPK4:** configurazione dei parametri per la conferma delle operazioni.

### 2. Creazione delle anagrafiche materiali

- **MM01:** creazione di 25 materiali: 1 FERT, 9 HALB e 15 ROH.
- **MM02:** impostazione dei dati MRP, approvvigionamento, pianificazione e valorizzazione.
- **Strategia 20:** assegnazione al prodotto finito LUNA per la produzione su commessa.

### 3. Configurazione delle varianti di prodotto

- **CT04:** definizione delle caratteristiche configurabili (colore degli occhi, capelli e abbigliamento).
- **CL01 / CL02:** creazione e gestione della classe di tipo 300.
- **MM01 / MM02:** gestione dell'anagrafica del materiale configurabile.
- **CU01:** definizione delle dipendenze per la selezione dei componenti.
- **CU41:** creazione del profilo di configurazione.
- **CU50:** simulazione delle diverse configurazioni della bambola.

### 4. Definizione delle risorse produttive

- **CR01:** creazione dei 14 centri di lavoro.
- **CR02:** configurazione di capacità, tempi e risorse disponibili.
- **CR03:** verifica dei dati dei centri di lavoro.

### 5. Creazione delle distinte base (BOM)

- **CS01:** creazione delle distinte base multilivello per FERT e HALB.
- **CS02:** assegnazione e modifica dei componenti.
- **CS12:** verifica della struttura completa del prodotto mediante esplosione multilivello.

### 6. Definizione dei cicli di lavorazione (Routing)

- **CA01:** creazione dei 10 cicli produttivi.
- **CA02:** definizione delle operazioni e assegnazione ai centri di lavoro.
- **CA03:** verifica delle sequenze operative e dei tempi di lavorazione.

### 7. Gestione delle versioni di produzione

- **C223:** creazione di versioni di produzione alternative, associando differenti Routing alla BOM del medesimo materiale.
- Definizione delle alternative produttive in funzione della disponibilità delle macchine e della distribuzione del carico di lavoro.

### 8. Acquisizione dell'ordine cliente (SD)

- **VA01:** creazione dell'ordine di vendita e definizione della configurazione personalizzata della bambola LUNA.
- **VA03:** verifica dell'ordine e delle caratteristiche selezionate dal cliente.

### 9. Pianificazione dei fabbisogni (MRP)

- **MD02 / MD01N:** esecuzione della pianificazione dei fabbisogni.
- **MD04:** analisi della situazione stock/fabbisogni.
- Generazione degli ordini pianificati per i materiali prodotti internamente e delle proposte di approvvigionamento per le materie prime.

### 10. Approvvigionamento delle materie prime (MM)

- **ME21N:** creazione degli ordini di acquisto.
- **ME23N:** verifica degli ordini.
- **MIGO – Movimento 101:** registrazione dell'entrata merci in magazzino.
- **MMBE:** verifica delle giacenze disponibili.

### 11. Esecuzione della produzione (PP)

- **MD04 / CO40:** conversione degli ordini pianificati in ordini di produzione.
- **CO01 / CO02:** creazione, modifica e rilascio degli ordini.
- **CO11N / CO15:** registrazione delle conferme delle operazioni e delle quantità prodotte.
- **MIGO – Movimento 261:** registrazione del consumo dei componenti, se non gestito automaticamente tramite Backflush.
- **MIGO – Movimento 101:** registrazione dell'entrata a magazzino dei prodotti realizzati.
- **COGI:** verifica e correzione degli eventuali errori nei movimenti automatici.

### 12. Controllo e monitoraggio della produzione

- **COOIS:** monitoraggio degli ordini di produzione.
- **COHV:** elaborazione collettiva degli ordini.
- **MD04:** verifica dell'aggiornamento dei fabbisogni e delle disponibilità.

### 13. Consegna del prodotto finito (SD)

- **VL01N:** creazione della consegna in riferimento all'ordine cliente.
- **VL02N:** gestione della consegna e registrazione dell'uscita merci.
- **VF01:** creazione della fattura di vendita, a completamento del ciclo commerciale.

### Risultato

Il processo End-to-End integra **configurazione del prodotto, gestione dei dati anagrafici, pianificazione MRP, approvvigionamento, produzione e consegna al cliente**, valorizzando la personalizzazione della bambola LUNA attraverso la *Variant Configuration* e la flessibilità delle risorse produttive mediante le *Production Versions*.
