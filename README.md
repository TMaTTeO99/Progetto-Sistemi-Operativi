# Progetto-Sistemi-Operativi

L’applicazione è costituita da due programmi, un file storage server e un programma client.
Il file storage è strutturato in modo da servire le diverse richieste provenienti dal programma client, fra
queste ad esempio la possibilità di caricare, eliminare e leggere, diversi tipi di file. I file provenienti
dal programma client vengono mantenuti in memoria centrale dal file storage, il client però ha la
possibilità di salvare sul disco i file precedentemente caricarti nello storage tramite le opzioni messe a
disposizione (inserendo –h nell’input che il client riceve è possibile leggere quali sono). All’avvio, il
file storage utilizza un file di configurazione per settare tutti i parametri necessari per eseguire il
lavoro, mentre le operazioni interne vengono opportunamente memorizzate su un file testuale di log. Lo storage
ha una capacità limitata sia in termini di numero massimo di file memorizzabili che in termini di
numero di byte che i file possono occupare. Quando tale capacità si esaurisce, se arrivano ulteriori
richieste di memorizzazione di file, quest’ultimi contenuti all’interno dello storage verranno espulsi
finché non sarà disponibile abbastanza spazio per memorizzare il nuovo file. Tali file espulsi saranno
inviati al client che ne ha causato l’espulsione. Client e server utilizzano il protocollo <richiesta-
risposta> per comunicare, per ogni richiesta ricevuta il server comunica al client se tale richiesta è
stata soddisfatta o meno, inoltre nel caso in cui un client dovesse ricevere uno o più file a causa di una
espulsione o per una semplice lettura, manderà un messaggio di notifica al server per comunicare di
aver ricevuto il file. Ogni richiesta che il server deve soddisfare viene effettuata tramite delle
opportune API che il client utilizza per ricevere o spedire messaggi e file.

# Si tratta di un'applicazione "giocattolo", presenta molti bug, imperfezioni e non è ottimizzata al meglio, può essere considerata però come un buon esempio per vedere i meccanismi principali che vengono implementati all'interno del kernel linux. 
