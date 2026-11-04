Il materiale ZF001, classificato come FERT (Finished Product), rappresenta il prodotto finito destinato alla vendita.

Nella vista MRP 1 dell'anagrafica materiale è stato impostato il tipo di pianificazione VB (Manual Reorder Point Planning), con l'obiettivo di garantire il mantenimento di un livello minimo di scorte.

Questa configurazione consente a SAP S/4HANA di monitorare le disponibilità del materiale e generare automaticamente proposte di riapprovvigionamento quando il livello delle scorte scende al di sotto del punto di riordino definito manualmente, favorendo la continuità delle vendite e la disponibilità del prodotto finito.
<img width="1914" height="1074" alt="ZL_F001 Fertigerzeugnis LUNA" src="https://github.com/user-attachments/assets/7d53f5ee-3f51-4c30-bd31-c49160720a9f" />

Successivamente, si è proceduto alla creazione delle anagrafiche dei semilavorati (HALB), utilizzando come riferimento la struttura precedentemente definita per il prodotto finito ZF001 (FERT).
La configurazione è stata adattata modificando il tipo di materiale e i parametri pertinenti, con particolare attenzione ai dati di valorizzazione e ai costi, nonché alle impostazioni MRP necessarie per garantire una corretta pianificazione dei fabbisogni e l'integrazione dei semilavorati nel flusso produttivo.
<img width="1912" height="1048" alt="ZL_H001 HALB Testa bambola Luna" src="https://github.com/user-attachments/assets/b7967932-7645-43b2-b828-1b032d39128a" />

Nella vista MRP 2 del semilavorato ZL_H001 – Testa della bambola LUNA, è stato impostato il Procurement Type E (In-house Production), poiché questo componente sarà sempre realizzato internamente e non acquistato da fornitori esterni.

Per quanto riguarda il Backflush, ho selezionato il valore 2 (Work Center Decides), delegando al centro di lavoro la gestione del consumo automatico dei materiali.

Il Backflush è stato impostato sul valore 2 (Work Center Decides), delegando al centro di lavoro la decisione sull'attivazione del prelievo automatico dei componenti dal magazzino al momento della conferma delle operazioni produttive, evitando così la registrazione manuale dei singoli movimenti di uscita.


