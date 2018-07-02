---

copyright:

  years:  2016, 2018

lastupdated: "2018-06-11"

---

# Ordine, visualizzazione e rimozione dei servizi per le istanze vCenter Server

Puoi ordinare servizi per le tue istanze VMware vCenter Server, ad esempio una soluzione di ripristino di emergenza. Quando non hai più bisogno di questi servizi, puoi rimuoverli dalle tue istanze.

## Servizi disponibili per le istanze vCenter Server

La seguente tabella mostra i servizi disponibili per le istanze vCenter Server.

Tabella 1. Servizi disponibili per le istanze vCenter Server

| Nome servizio                                                                           | Disponibilità |
|----------------------------------------------------------------------------------------|------------------|
| [F5 on IBM Cloud](../services/f5_considerations.html)                                 | Sì              |
| [FortiGate Security Appliance on IBM Cloud](../services/fsa_considerations.html)       | Sì              |
| [FortiGate Virtual Appliance on IBM Cloud](../services/fortinetvm_considerations.html) | Sì              |
| [HyTrust CloudControl on IBM Cloud](../services/htcc_considerations.html)              | Sì              |
| [HyTrust DataControl on IBM Cloud](../services/htdc_considerations.html)              | Sì              |
| [IBM Spectrum Protect Plus on IBM Cloud](../services/spp_considerations.html)         | Sì              |
| [KMIP for VMware on IBM Cloud](../services/kmip_considerations.html)                  | Sì              |
| [Veeam on IBM Cloud](../ services/veeam_considerations.html)                           | Sì              |
| [VMware HCX on IBM Cloud](../services/hcx_considerations.html)                         | No              |
| [Zerto on IBM Cloud](../services/addingzertodr.html)                                 | Sì              |


## Aggiunta di servizi alle istanze vCenter Server

Per aggiungere un servizio alla tua istanza vCenter Server, fai clic sul link del servizio appropriato nella tabella precedente per esaminare le considerazioni relative al servizio e controllare i componenti distribuiti. Quindi, segui le istruzioni nell'argomento su come ordinare i servizi per aggiungere il servizio alla tua istanza.

### Risultati dell'installazione del servizio

Una volta completata correttamente l'installazione del servizio, riceverai una notifica via e-mail e il servizio verrà visualizzato nella pagina **Servizi** dell'istanza con lo stato **Installato**.

## Visualizzazione dei servizi per le istanze vCenter Server

1. Dalla console {{site.data.keyword.vmwaresolutions_short}}, fai clic su **Istanze distribuite** nel riquadro di navigazione a sinistra.
2. Nella tabella **Istanze vCenter Server**, fai clic sull'istanza per la quale vuoi visualizzare i servizi.
3. Fai clic su **Servizi** nel riquadro di navigazione a sinistra.
4. Nella pagina **Servizi**, fai clic su un servizio per esaminare le relative informazioni, come lo stato del servizio e altri dettagli.
5. A seconda del servizio visualizzato, puoi accedere alle relative console utilizzando le credenziali fornite nei dettagli del servizio e gestire quindi il servizio da qui.

## Rimozione dei servizi per le istanze vCenter Server

1. Dalla console {{site.data.keyword.vmwaresolutions_short}}, fai clic su **Istanze distribuite** nel riquadro di navigazione a sinistra.
2. Nella tabella **Istanze vCenter Server**, fai clic sull'istanza per la quale vuoi rimuovere i servizi.
3. Fai clic su **Servizi** nel riquadro di navigazione a sinistra.
4. Nella pagina **Servizi**, individua l'istanza del servizio che vuoi rimuovere e fai clic sull'icona **Elimina**.
5. Nella pagina **Elimina servizio**, esamina le eventuali considerazioni o avvertenze. Seleziona **Accetto** e fai clic su **Elimina**.

### Risultati della rimozione del servizio

Dopo che la tua richiesta di rimozione del servizio viene accettata, lo stato del servizio viene modificato in  **In fase di rimozione**.

Una volta completata correttamente la rimozione del servizio, riceverai una notifica via e-mail e il servizio verrà rimosso dalla pagina **Servizi** dell'istanza.

**Attenzione**: per i servizi rimossi ti vengono addebitati costi fino alla fine del ciclo di fatturazione dell'infrastruttura {{site.data.keyword.cloud_notm}}.

## Link correlati

* [Domande frequenti](../vmonic/faq.html)