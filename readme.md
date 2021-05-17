# Segnatura di protocollo informatico

Il file *segnatura_protocollo.xsd* riporta l'aggiornamento della *segnatura informatica* di protocollo realizzata da AgID nell'ambito delle linee guida per il *documento amministrativo elettronico* prodotte in attuazione dell'articolo 71 del decreto legislativo 7 marzo 2005, n. 82 e s.m.i.

Lo scambio di *documenti amministrativi elettronici protocollati* tra AOO vede coinvolti:

* *AOO mittente*, l’AOO che invia i *documenti amministrativi elettronici protocollati* e **DEVE** utilizzare uno dei canali di comunicazione indicati al capitolo “4. Modalità tecniche di trasmissione”;
* *AOO destinataria*, l’AOO che riceve i *documenti amministrativi elttronici protocollati*.

Un *messaggio di protocollo*, l’elemento atomico di interesse per dare seguito allo scambio di *documenti amministrativi elettronici protocollati* tra AOO, è una struttura logica che:

* **DEVE** contenere il *documento amministrativo elettronico primario* (di seguito *documento primario*);
* **PUÒ** contenere un numero qualsiasi di *documenti amministrativi elettronici allegati* (di seguito *allegati*);
* **DEVE** contenere la *segnatura informatica* di protocollato (di seguito *segnatura informatica*).

Il *documento primario* e gli eventuali *allegati* **DEVONO** essere formati nel rispetto delle regole di formazione dei documenti amministrativi informatici.

La *segnatura informatica* **DEVE** essere formata nel rispetto del root element *SegnaturaInformatica* riportato in *segnatura_protocollo.xsd*.

La *segnatura informatica* **DEVE** essere associata in forma permanente al documento primario e agli allegati che con esso formano il messaggio di protocollo. A tal fine l’AOO mittente:

* **DEVE** riportare nella segnatura informatica l'impronta (digest) del *documento primario* e, se presenti, degli *allegati*;
* **DEVE** assicurare l’autenticità, integrità e il non ripudio della *segnatura informatica* attuando le regole tecniche in materia di firma elettronica dei documenti informatici emanate dall’AgID.

La AOO mittente **DEVE** assicurare il controllo della *validità amministrativa* del *documento primario*, degli eventuali *allegati* e dei dati riportati nella *segnatura informatica* prima della composizione del *messaggio di protocollo*.

Le informazioni contenute nella *segnatura informatica* **DEVONO** essere memorizzate nel sistema di gestione dei documenti della *AOO mittente* e in quello delle *AOO destinatarie*.

Per completezza sono riportati i file:

* previous_schemas/segnatura_protocollo_circolare 28_2001.dtd, in cui è riportato il Document Type Definition relativo alla segnatura di protocollo emanato con Circolare AIPA del 7 maggio 2001, n. 28
* previous_schemas/segnatura_protocollo_circolare 60_2013.xsd, in cui è riportato il XML Schema relativo alla segnatura di protocollo emanato con Circolare AgID del 23 gennaio 2013, n. 60



## IMPORTANTE: il contenuto del presente repo è allineato con la DETERMINAZIONE N. 371 /2021 AgID che ha per oggetto "Modifiche testo Linee Guida sulla formazione, gestione e conservazione dei documenti informatici, allegato 5 - Metadati, allegato 6 - Comunicazione tra AOO di Documenti Amministrativi Protocollati ed estensione dei termini di entrata in vigore".
