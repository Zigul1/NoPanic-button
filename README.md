<h1>NoPanic button</h1>

Eseguendo lo *script* *__NoPanic__* come **admin**, compare nello schermo un'immagine con pulsante rosso; cliccandoci:
- verrano salvati nella cartella "Panic", creata in automatico in Documenti, il *file* "Screen.png" con lo __*screenshot* del *desktop*__, il *file* "connessioni.txt" con le **connessioni attive** e il *file* "processi.txt" con i **processi attivi** (così che siano disponibili per un'indagine tramite sistema operativo *live*)
- verrà disconnesso il PC dalle **reti**, sia Internet che locale
- verranno disconnesi i **dischi** (non quello di *boot*) e i *drive* USB
- verrà riavviato il PC direttamente al **BIOS** (così da poter intervenire con sistemi *live*).

La **posizone** di *default* del "bottone" è relativa alla risuluzione 1920x1080 ed è la seguente (per modificarla, cambiare le coordinate alla riga 21 dello *script*):
![BoB](https://github.com/user-attachments/assets/90c8b1f1-abc2-4c79-91e0-6919d0564251)

Alzando la finestra del "bottone" è disponibile una casella di testo per mostrare istruzioni e promemoria.

![full](https://github.com/user-attachments/assets/d56500f6-4054-48b8-bb70-404e4fe2c63d)


Ovviamente, **personalizzando** lo *script* è possibile aggiungere altri comandi, modificare la scritta "Panic!" o la casella di testo o le dimensioni dell'immagine, forzare la finestra sempre in primo piano, etc.
Per distinguerlo da altri *script* o collegamenti PowerShell è disponibile, fra i *file* sopra, un'**icona** personalizzata ("panic-icon.ico"), assegnabile manualmente allo *script* quando viene creato un collegamento.


**[Articolo su TurboLab](https://turbolab.it/4320)**

**[Video tutorial su YouTube](https://www.youtube.com/watch?v=JEnhV_dIxQQ)**

<h2>FAQ</h2>

**Q - Non si potrebbe semplicemente riavviare al BIOS, senza "perdere tempo" a disattivare dischi, periferiche e a disconnettersi dalla rete?** 

**A -** In teoria sì, in pratica il processo di riavvio potrebbe riscontrare rallentamenti, concedendo suo malgrado ulteriore tempo al *malware* (o all'eventuale, meno probabile, attaccante). Disconnettere dischi e periferiche dà la priorità a tutelare eventali *file* di *backup* (o di "*versioning*") allocati su altri *drive*, così come il disconettersi dalla rete (senza aspettare la disconnessione pre-riavvio) dà la priorità a bloccare eventuali connessioni malevole, esfiltrazioni di dati e contaminazione di altri dispositivi o *host* di rete. Inoltre, qualora si debba poi riavviare il sistema senza la certezza di averlo bonificato, conviene ritrovarlo già *offline* e senza le altre unità connesse, in modo da prevenire che il malaugurato riattivarsi del *malware* possa dilagare troppo.

**Q - Come inserire altri comandi e/o rimuovere quelli già presenti?**

**A -** Dalla riga 72 alla 119 dello *script*, c'è l'elenco dei comandi inseriti, che possono essere cancellati e/o modificati; per aggiungerne altri è sufficiente scriverli prima della riga 119, che serve a chiudere la finestra con l'immagine del pulsante dopo che sono stati eseguiti i comandi.
