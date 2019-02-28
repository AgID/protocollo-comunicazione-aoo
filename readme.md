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


## Changelog

Modifiche apportate a segnatura di protocollo emanata con circolare AgID 60/2013.

In quanto segue si assume: 

* il prefisso *xsd* per il namespace http://www.w3.org/2001/XMLSchema
* il prefisso *prot* per il namespace http://www.agid.gov.it/protocollo/

### File segnatura_protocollo.xsd

* Aggiornato namespace a http://www.agid.gov.it/protocollo/
* Consolidamento naming dei type utilizzando CamelCase ed aggiungendo suffisso type
* Definito root element *prot:SegnaturaInformatica*
* Eliminato element prot:Segnatura
* Aggiornato type *prot:SegnaturaInformaticaType*, nel dettaglio:
	1. Aggiornato attributo versione a 3.0.0 
* Aggiunto *prot:ImprontaType*
* Eliminato element *prot:Intestazione*
* Aggiornato type *prot:IntestazioneType*, nel dettaglio
	1. Tipizzato element *Oggetto* a *xsd:string*
	2. Tipizzato element *Riservato* a *xsd:string*
	3. Tipizzato element *InterventoOperatore* a *xsd:string*
	4. Tipizzato element *RiferimentoDocumentiCartacei* a *xsd:boolean*
	5. Tipizzato element *RiferimentiTelematici* a *xsd:boolean*
	6. Tipizzato element *Note* a *xsd:string*
	7. Eliminato element *PrimaRegistrazione*
* Eliminato element *prot:Identificatore*
* Aggiornato type *prot:IdentificatoreType*, nel dettaglio:
	1. Tipizzato element *DataRegistrazione* a *xsd:date*
* Eliminato element *prot:Origine*
* Eliminato element *prot:Destinazione*
* Aggiornato type *prot:DestinazioneType*, nel dettaglio:
	1. Tipizzato attribute *confermaRicezione* a *xsd:boolean*
* Eliminato element *prot:OraRegistrazione*
* Aggiornato type *prot:OraRegistrazioneType*, nel dettaglio:
	1. Tipizzato a *xsd:time*
	2. Eliminato il valore dell'enumeration *NMTOKEN*
* Eliminato element *prot:PerConoscenza*
* Eliminato type *prot:PerConoscenzaType* equivalente a *DestinazioneType*
* Eliminato element *prot:Risposta*
* Eliminato element *prot:InterventoOperatore*
* Eliminato element *prot:RiferimentoDocumentiCartacei*
* Eliminato element *prot:Riservato*
* Eliminato element *prot:RiferimentiTelematici*
* Eliminato element *prot:Denominazione*
* Eliminato element *prot:Classifica*
* Aggiornato type *prot:ClassificaType*, nel dettaglio:
	1. Tipizzato element *Denominazione* a *xsd:string*
* Aggiornato type *prot:LivelloType*, nel dettaglio:
	1. Tipizzato a *xsd:string*
* Eliminato element *prot:Mittente*
* Eliminato element *prot:Telefono*
* Eliminato element *prot:Fax*
* Eliminato element *prot:Indirizzo*
* Eliminato element *prot:IndirizzoPostale*
* Aggiornato type *prot:IndirizzoPostaleType,* nel dettaglio:
	1. Eliminato element *Indirizzo*
	2. Aggiunto element *Toponimo*
	3. Aggiunto element *Civico*, tipizzato a *xsd:string*
	4. Aggiunto element *CAP*
	5. Aggiunto element *Comune*
	6. Aggiunto element *Provincia*, tipizzato a *xsd:string*
	7. Aggiunto element *Nazione*, tipizzato a *xsd:string*
	8. Tipizzato element *Denominazione* a *xsd:string*
* Eliminato element *prot:Civico*
* Eliminato element *prot:Provincia*
* Eliminato element *prot:Nazione*
* Eliminato element *prot:Toponimo*
* Aggiornato type *prot:ToponimoType*, nel dettaglio:
	1. Tipizzato a *xsd:string*
* Eliminato element *prot:CAP*
* Aggiornato type *prot:CAPType*, nel dettaglio
	1. Tipizzato a *xsd:string* e pattern *[0-9]{6}*
* Eliminato element *prot:Comune*
* Aggiornato type *prot:ComuneType*, nel dettaglio:
	1. Tipizzato a *xsd:string*
* Aggiunto type *prot:CodiceISTATType*
* Aggiornato type *prot:AmministrazioneType*, nel dettaglio:
	1. Tipizzato element *Definito* a *xsd:string*
* Eliminato element *prot:UnitaOrganizzativa*
* Eliminato element *prot:Ruolo*
* Aggiornato type *prot:RuoloType*, nel dettaglio:
	1. Tipizzato element *Denominazione* a *xsd:string*
* Eliminato element *prot:Identificativo*
* Aggiornato type *prot:IdentificativoType*, nel dettaglio:
	1. Tipizzato a *xsd:string* e pattern *[A-Za-z0-9_\.\-]{1,16}*
* Eliminato element *prot:AOO*
* Aggiornato type *prot:AOOType*, nel dettaglio:
	1. Tipizzato element *Denominazione* a *xsd:string*
* Eliminato element *prot:Descrizione*
* Aggiornato type *prot:DescrizioneType*, nel dettaglio:
	1. Tipizzato element *Note* a *xsd:string*
* Eliminato element *prot:Messaggio*
* Aggiornato type *prot:MessaggioType*, nel dettaglio:
	1. Tipizzato element *DescrizioneMessaggio* a *xsd:type*
* Eliminato element *prot:DescrizioneMessaggio*
* Eliminato element *prot:Riferimenti*
* Eliminato element *prot:ContestoProcedurale*
* Aggiornato type *prot:ContestoProceduraleType*, nel dettaglio:
	1. Tipizzato element *Tipo* a *xsd:string*
	2. Tipizzato element *Oggetto* a *xsd:string*
	3. Tipizzato element *DataAvvio* a *xsd:date*
	4. Tipizzato element *Note* a *xsd:string*
	5. Eliminato attribute *id*	
	6. Eliminato attribute *rife*
* Eliminato element *prot:DataAvvio*
* Eliminato element *prot:TipoContestoProcedurale*
* Eliminato element *prot:Responsabile*
* Eliminato element *prot:Procedimento*
* Aggiornato type *prot:ProcedimentoType*, nel dettaglio:
	1. Creato come estensione di *prot:ContestoProceduraleType*
	2. Tipizzato element a *Responsabile* a *prot:Persona* eliminando il livello Responsabile
	3. Tipizzato element *DataTermine* a *xsd:date*
* Eliminato element *prot:DataTermine*
* Eliminato element *prot:Nome*
* Eliminato element *prot:Cognome*
* Eliminato element *prot:Titolo*
* Eliminato element *prot:CodiceFiscale*
* Eliminato element *prot:Allegati*
* Eliminato type *prot:AllegatiType*
* Eliminato element *prot:Fascicolo*
* Eliminato type *prot:FascicoloType*
* Eliminato element *prot:TestoDelMessaggio*
* Elimianto type prot:TestoDelMessaggioType
* Eliminato element *prot:Documento*
* Aggiornato type *prot:DocumentoType*, nel dettaglio:
	1. Tipizzato element *CollocazioneTelematica* a *xsd:string*
	2. Tipizzato element *TitoloDocumento* a *xsd:string*
	3. Tipizzato element *TipoDocumento* a *xsd:string*
	4. Tipizzato element *Oggetto* a *xsd:string*
	5. Tipizzato element *NumeroPagine* a *xsd:int*
	6. Tipizzato element *Note* a *xsd:string*
	7. Reso obbligatorio element *Impronta*
	8. Eliminati attributi
* Eliminato element *prot:CollocazioneTelematica*
* Eliminato element *prot:TitoloDocumento*
* Eliminato element *prot:TipoDocumento*
* Eliminato element *prot:Oggetto*
* Eliminato element *prot:Note*
* Eliminato element *prot:MetadatiEsterni*
* Aggiornato type *prot:MetadatiEsterniType*, nel dettaglio:
	1. Tipizzato element *NomeFile* a *xsd:string*
* Eliminato element *prot:PiuInfo*
* Aggiornato type *prot:PiuInfoType*, nel dettaglio:
	1. Tipizzato element *MetadatiInterni* a *xsd:string*
* Eliminato element *prot:Persona*
* Aggiornato type *prot:PersonaType*, nel dettaglio:
	1. Tipizzato element *Denominazione a xsd:string
	2. Tipizzato element *Nome* a *xsd:string*
	3. Tipizzato element *Cognome* a *xsd:string*
	4. Tipizzato element *Titolo* a *xsd:string*
	5. Tipizzato element *CodiceFiscale* a *prot:CodiceFiscaleType*
	6. Eliminato attribute *id*	
	7. Eliminato attribute *rife*
* Aggiunto type *prot:CodiceFiscaleType*
* Eliminato element *prot:CodiceAmministrazione*
* Aggiornato type *prot:CodiceAmministrazioneType*, nel dettaglio:
	1. Tipizzato a *xsd:string*
* Eliminato element *prot:CodiceAOO*
* Aggiornato type *prot:CodiceAOOType*, nel dettaglio:
	1. Tipizzato a *xsd:string* e pattern *[A-Za-z0-9_\.\-]{1,16}*
* Eliminato element *prot:CodiceRegistroType*
* Aggiornato type *prot:CodiceRegistroType*, nel dettaglio:
	1. Tipizzato a *xsd:string* e pattern *[A-Za-z0-9_\.\-]{1,16}*
* Eliminato element *prot:NumeroRegistrazione*
* Aggiornato type *prot:NumeroRegistrazioneType*, nel dettaglio:
	1. Tipizzato a *xsd:string* e pattern *[0-9]{7,}*
* Eliminato element *prot:DataRegistrazione*
* Eliminato element *prot:IndirizzoTelematico*
* Aggiornato type *prot:IndirizzoTelematicoType*, nel dettaglio:
	1. Tipizzato a *xsd:string*
	2. Tipizzato attribute *Note* a *xsd:string*
	3. Modificato valore enumeration da *NMTOKEN* a *other*
* Eliminato il type *prot:ConfermaRicezione*
* Eliminato il element *prot:ConfermaRicezione*
* Eliminato il type *prot:MessaggioRicevuto*
* Eliminato il element *prot:MessaggioRicevuto*
* Eliminato il type *prot:AggiornamentoConferma*
* Eliminato il element *prot:AggiornamentoConferma*
* Eliminato il type *prot:NotificaEccezione*
* Eliminato il element *prot:NotificaEccezione*
* Eliminato il type *prot:Motivo*
* Eliminato il element *prot:Motivo*
* Eliminato il type *prot:AnnullamentoProtocollazione*
* Eliminato il element *prot:AnnullamentoProtocollazione*
* Eliminato il type *prot:Provvedimento*
* Eliminato il element *prot:Provvedimento*