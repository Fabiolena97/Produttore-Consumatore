# thread-scuola
##Autore
    Lena Fabio

##Data creazione
     28/03/2015

                              VERSIONI DEL PROGRAMMA PRODUTTORE E CONSUMATORE
##Descrizione delle varie versioni
Versione 1 - Prima versione Produttore-Consumatore.
Non abbiamo ALTERNANZA STRETTA come si vede dall'esecuzione i programmi hanno velocità diverse e quindi l'output non è corretto.


Versione 2 - Produttore e Consumatore.
Introduco delle variabili BOOLEAN che mi permettono di capire se il dato è stato letto o scritto: buffer empty (letto) e buffer full (scritto); ora ottengo la stretta alternanza: P/C/P/C...
In questo esempio la variabile condivisa full non è protetta da una sezionecritica!


Versione 3 - Produttore e Consumatore.
Introduce la sezione critica per garantire che la modifica delle variabili condivise avvenga in mutua esclusione.
NB. La cs (critical section) deve essere inizializzata altrimenti non funziona!


Versione 4 - Produttore e Consumatore.
Superamento dell'attesa attivao busy waiting mediante la CONDITION_VARIABLE che sospende il processo che non può avanzare. 


Versione 5 - Produttore e Consumatore.
L'alternanza stretta fra P e C limita di molto la velocità di esecuzione. Usiamo ora un buffer circolare che permette per brevi periodi velocità diverse fra P e C. Vedi caso tipico del buffer di un HD oppure la stampa.
NB. Ora sono anche necessarie due variabili diverse per segnalare pienoe vuoto così come per le variabili condition!



