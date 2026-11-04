### Configurazione delle varianti di prodotto (Variant Configuration)

Per la gestione della bambola LUNA è stato adottato un approccio basato sulla **Variant Configuration di SAP S/4HANA**, in considerazione della natura personalizzabile del prodotto. Tale scelta è stata motivata dalla necessità di offrire al cliente diverse combinazioni di caratteristiche estetiche, in particolare il **colore degli occhi, il colore dei capelli e la tipologia di abbigliamento**, mantenendo una struttura di prodotto comune.

A tale scopo, sono state definite le caratteristiche configurabili mediante la transazione **CT04** e organizzate all'interno di una classe di tipo **300**, destinata alla gestione delle varianti di prodotto. La configurazione è stata strutturata per consentire la selezione delle caratteristiche desiderate in fase di acquisizione dell'ordine cliente, associando a ciascuna combinazione i componenti pertinenti della distinta base.

Questa soluzione permette di gestire differenti modelli della bambola LUNA senza dover creare un'anagrafica materiale indipendente per ogni possibile combinazione, riducendo la ridondanza dei dati anagrafici e migliorando la flessibilità della pianificazione produttiva.

L'integrazione della **Variant Configuration con la strategia di pianificazione 20 (Make-to-Order)** consente inoltre di orientare la produzione alle specifiche richieste del cliente, evitando la realizzazione anticipata di prodotti finiti con caratteristiche non ancora definite.
