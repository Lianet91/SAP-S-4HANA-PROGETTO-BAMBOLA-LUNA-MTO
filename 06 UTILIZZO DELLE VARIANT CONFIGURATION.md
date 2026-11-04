### Implementazione della Variant Configuration – Bambola LUNA

Per la gestione della bambola LUNA è stato adottato un approccio basato sulla **Variant Configuration di SAP S/4HANA**, in considerazione della natura personalizzabile del prodotto. Tale scelta è stata motivata dalla necessità di offrire al cliente diverse combinazioni di caratteristiche estetiche, in particolare il **colore degli occhi, il colore dei capelli e la tipologia di abbigliamento**, mantenendo una struttura di prodotto comune.

A tale scopo, è stata definita la seguente sequenza di configurazione:

1. **CT04 – Creazione delle caratteristiche:** definizione delle caratteristiche configurabili e dei relativi valori ammessi.
2. **CL01 / CL02 – Gestione della classe di tipo 300:** creazione della classe di configurazione e associazione delle caratteristiche precedentemente definite.
3. **MM02 – Configurazione dell'anagrafica materiale:** abilitazione del materiale alla configurazione delle varianti e assegnazione della classe di tipo 300.
4. **CU41 – Creazione del Configuration Profile:** definizione del profilo di configurazione del prodotto e delle modalità di gestione delle varianti.
5. **CS01 – Creazione della Super BOM:** strutturazione di una distinta base comune, comprendente i componenti condivisi e quelli alternativi in funzione delle caratteristiche selezionate.
6. **CU01 – Definizione delle dipendenze:** creazione delle regole di selezione che collegano le caratteristiche configurabili ai componenti pertinenti della distinta base, con successiva assegnazione delle dipendenze agli oggetti interessati.

Questa configurazione consente di selezionare le caratteristiche desiderate durante l'acquisizione dell'ordine cliente, determinando i componenti necessari alla realizzazione della variante richiesta.

La soluzione permette di gestire differenti modelli della bambola LUNA senza dover creare un'anagrafica materiale indipendente per ogni possibile combinazione, riducendo la ridondanza dei dati anagrafici e migliorando la flessibilità della pianificazione produttiva.

L'integrazione della **Variant Configuration con la strategia di pianificazione 20 (Make-to-Order)** consente inoltre di orientare la produzione alle specifiche richieste del cliente, evitando la realizzazione anticipata di prodotti finiti con caratteristiche non ancora definite.
