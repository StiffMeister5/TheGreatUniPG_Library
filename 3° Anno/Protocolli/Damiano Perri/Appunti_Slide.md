# Lezioni di Teoria - Comunicazione Dati

---

## Indice Generale

### **Primo Modulo**

- [Comunicazione Dati](#comunicazione-dati)
- [Informazione e Misura](#informazione-e-misura)
- [Flussi Trasmissivi](#flussi-trasmissivi)
- [DTE, DCE, CPE](#dte-dce-cpe)
- [Le Reti ed il Loro Mondo](#le-reti-ed-il-loro-mondo)
- [Valutazione della Rete](#valutazione-della-rete)
- [Tipo di Trasmissione](#tipo-di-trasmissione)
- [Classificazione delle Reti](#classificazione-delle-reti)
- [Reti Wireless](#reti-wireless)
- [Struttura delle Reti](#struttura-delle-reti)
- [Reti Mesh](#reti-mesh)
- [Wi-Fi vs Mesh](#wi-fi-vs-mesh)
- [I Protocolli secondo ISO-OSI](#i-protocolli-secondo-iso-osi)
- [La Trasmissione Dati](#la-trasmissione-dati)
- [Segnali Sinusoidali](#segnali-sinusoidali)
- [Sviluppo in Serie di Fourier](#sviluppo-in-serie-di-fourier)
- [Filtri](#filtri)
- [Modulazione di un Segnale](#modulazione-di-un-segnale)
- [Modulazione ad Onda Continua](#modulazione-ad-onda-continua)
- [Modulazione Impulsiva](#modulazione-impulsiva)
- [PDF_6: PCM](#pdf_6-pcm)
- [PDF_7: EVM](#pdf_7-evm)
- [Codifica Differenziale DPSK](#codifica-differenziale-dpsk)
- [Modulazione QAM](#modulazione-qam)
- [Codifica Trellis](#codifica-trellis)
- [Alterazione del Segnale](#alterazione-del-segnale)
- [Limiti della Velocità nel Trasferimento](#limiti-della-velocità-nel-trasferimento)
- [PDF_8: Altri Limiti della Velocità](#pdf_8-altri-limiti-della-velocità)
- [Schemi di Controllo](#schemi-di-controllo)
- [Codifica di Canale (Encoding)](#codifica-di-canale-encoding)
- [Controllo degli Errori](#controllo-degli-errori)
- [PDF_9](#pdf_9)
- [Multiplazione](#multiplazione)
- [Modem](#modem)
- [ADSL](#adsl)
- [Interfacce](#interfacce)
- [PDF_10](#pdf_10)
- [PDF_11](#pdf_11)

### **Secondo Modulo**

- [PDF_1](#secondo-modulo---pdf_1)
- [PDF_2](#secondo-modulo---pdf_2)
- [PDF_3](#secondo-modulo---pdf_3)
- [PDF_4](#secondo-modulo---pdf_4)
- [PDF_5](#secondo-modulo---pdf_5)
- [PDF_6](#secondo-modulo---pdf_6)
- [PDF_PARTE_FINALE](#secondo-modulo---pdf_parte_finale)

---

## Primo Modulo

### Comunicazione Dati

Per parlare di processo comunicativo, si parla di:

- **Sorgente di informazione**
- **Cammino fisico**
- **Destinatario**

L'**informazione** è l'insieme di dati correlati tra loro. Un esempio è la piramide DIKW.

Il **protocollo** è l'insieme di regole che consentono la comunicazione e definisce **COSA** e **COME**.

Questi protocolli sono definiti da standard stabiliti da organizzazioni come **ISO**, **IEEE**, **ICANN**, **W3C** e senza questi definiti due dispositivi non possono comunicare.

Il **modello TCP/IP ISO** ha 4 layer:

- Network Access
- Internet
- Transport
- Application

---

### Informazione e Misura

L'informazione ha come misura il **bit** e vale:

**Q = log₂M**

dove M è il numero di stati possibili di un sistema e Q i bit necessari per distinguerli.

Un sistema elaborativo deve avere dei **codici** per associare le sequenze di bit ad un carattere come **BCS**, **AIKEN**, **ASCII**, **UNICODE**, ecc.

I più usati sono l'**ASCII** a 7/8 bit, l'**EBCDIC** a 8 bit, l'**UNICODE**.

---

### Flussi Trasmissivi

- **Simplex** → unidirezionale
- **Half duplex** → bidirezionale a turni
- **Full duplex** → bidirezionale diretto

---

### DTE, DCE, CPE

L'applicazione utente risiede nel **Data Terminal Equipment (DTE)** come ad esempio un PC.

Il **Data Circuit Terminating Equipment (DCE)** converte i segnali nella forma migliore per l'invio sul canale.

Il **CPE (Customer Premises Equipment)** si usa in caso sia richiesto un dispositivo di pertinenza dell'utente.

---

### Le Reti ed il Loro Mondo

La **rete** è un insieme di dispositivi connessi. Vi sono uno o più nodi capaci di inviare o ricevere dati.

**Reti ad elaborazione:**

- **Concentrata** → un DTE potente viene messo a disposizione di altri DTE che ne sfruttano la capacità di calcolo
- **Distribuita** → DTE diviso in più punti

Per entrambi i modelli vi sono 3 procedure di colloquio:

- **Inquiry** → forma di interrogazione messa a disposizione da servizi del PC
- **Conversational** → stabilisce delle regole e formati, bloccando quelli diversi
- **Interattivo** → risponde ad applicazioni sensibili. Invia tutte le applicazioni che consentono pieno sfruttamento delle risorse elaborative

---

### Valutazione della Rete

- **Affidabilità** → priva di errori, rimedia ai guasti, gestisce bene le situazioni critiche
- **Sicurezza** → protezione dei dati da accesso, perdite e modifiche indesiderate
- **Prestazioni** →

  - **Ritardo** → misurazione tempo di transito dei dati
  - **Tempo risposta** → tempo tra richiesta e risposta
  - **Throughput** → quantità di dati spediti in unità di tempo

  Queste dipendono da numero di DTE, tipologia dei mezzi e dal software.

  - **Banda** → banda passante di frequenze che può essere usata per la trasmissione dei dati. Massima velocità alla quale è possibile trasmettere informazioni. Per valutare la velocità di banda si usano strumenti come **ping**, **traceroute**, **speedtest**, **pingtest** e **netindex**

---

### Tipo di Trasmissione

- **Point-to-Point** → tra due DTE diretti mediante linea telefonica o dedicata
- **Multi-point** → collegamento condiviso tra più DTE. La condivisione avviene in maniera temporale o condivisione dello spazio del canale

---

### Classificazione delle Reti

- **WAN** → grandi senza limitazione, DTE distanti, arriva fino a Tbits. Sono distribuite, quindi anche se un nodo cade, il routing instrada verso un'altra path.
- **LAN** → 1 o 2 km, uso privato, arriva fino a migliaia Gbits. Possono esserci alcuni DTE che fungono da server.
- **WLAN** → reti locali LAN ma senza fili. Usa lo spettro radio. La velocità dipende dallo standard usato:
  - WiFi 5 (802.11ac) → 3.5 Gbps
  - WiFi 6 (802.11ax) → 9.6 Gbps
  - 2.4 GHz → offre una copertura ampia ma poco potente
  - 5 GHz → copertura meno ampia ma più potente
- **MAN** → livello cittadino, fibra ottica ad alta velocità

> **Docker:** Per sicurezza tutti i software in genere girano come demoni separati all'interno dei software server

---

### Reti Wireless

Usate principalmente per la comunicazione mobile. Abbiamo:

- **WLAN** (802.11)
- **WiMax** (IEEE 802.16x)
- **IEEE 802.20**
- **CDPD** (Cellular Digital Packet Data)

---

### Struttura delle Reti

La **topologia** di una rete è la configurazione geometrica dei collegamenti fra i vari componenti. Sono volte a creare stabilità, a migliorare il rendimento e a diminuire i costi.

- **Rete ad albero** → stazioni a livelli, con un livello centrale. Semplice ma vulnerabile
- **Rete a dorsale** → collegamento multi punto via Ethernet. Questa crea una specie di spina dorsale lungo tutta la rete. Questa rete richiedeva anche una speciale terminazione montata a fine del cavo.
- **Rete a stella** → ogni nodo è connesso ad un dispositivo centrale. È più economica rispetto ad una struttura a maglia completa. Ad esempio un Ethernet con topologia a stella aveva un doppino UTP non schermato, quindi in plastica.
- **Rete ad anello** → molto usata in passato. Ogni nodo ha un punto-a-punto con solo 2 nodi. Ha una trasmissione unidirezionale, ogni nodo rigenera il segnale. Non supporta errori
- **Rete a maglia (MESH)** → tutti i nodi sono collegati tra loro. Il costo totale del percorso è **N(N-1)/2**. Ogni apparato ha un collegamento Duplex.

---

### Reti Mesh

Combinazione di nodi fissi e mobili interconnessi tra loro con link wireless per avere una rete auto-configurante multi-hop.

Offre una grande affidabilità, ha una gestione dinamica dei malfunzionamenti, sia per quanto riguarda il collegamento radio che per quanto riguarda la componente hardware della rete.

Vengono monitorati in tempo reale i percorsi disponibili e selezionati quelli migliori.

Sono soggette ad un alto tasso di errore visto l'utilizzo di onde radio, dunque serve sviluppare protocolli ottimizzati per il wireless.

La maglia usata tra gli access point forma il **wireless backhaul multi-hop**, un sistema di comunicazione che fornisce ad ogni utente servizi a basso costo multi-hop a banda larga.

- **Backhaul network** = rete comprendente nodi intermedi tra dorsale e nodi periferici

La rete Mesh risolve le seguenti esigenze:

- Trasmissione in movimento e simmetrica (uplink-downlink)
- Limiti di banda delle strutture ad albero
- Reti ad-hoc senza infrastruttura
- Configurazione automatica
- Radiolocalizzazione senza GPS
- Resistenza alle interferenze
- 100% degli IP utilizzabili
- Più sicurezza

---

### Wi-Fi vs Mesh

Nelle reti WiFi un guasto blocca tutta la rete mentre nelle reti Mesh si ha maggiore tolleranza ai guasti e flessibilità nella pianificazione.

---

### I Protocolli secondo ISO-OSI

Il compito dei protocolli, ovvero chi gestisce il colloquio tra due DTE o DCE è:

- Gestire il flusso dei dati e gli scambi
- Controllo degli errori
- Sincronizzazione
- Strutturare i dati trasmessi

I protocolli per le relazioni tra due DTE si possono dividere in:

#### **Ambito Primario/Secondario:**

- **Polling/Selecting**
- **BSC**
- **HDLC**
- **SNRM**
- **RTS/CTS** → si basa su interfaccia seriale RS-232. Una stazione che vuole trasmettere manda un segnale alla stazione master attivando il segnale Request To Send. Se il master può ricevere risponde con un segnale Clear To Send. Questa procedura si basa sull'handshake.
- **XON/XOFF** → usato per terminali vicini tra loro. La stazione primaria invia dati, vengono memorizzati e utilizzati. Quando la memoria si riempie viene mandato un carattere XOFF che impedisce l'invio di nuovi blocchi. Appena il DTE si libera manda un messaggio XON
- **Stop and Wait**
- **ARQ** → Automatic Repeat Request o Query. Protocollo Full Duplex che usa il concetto di finestra mobile per essere più efficiente.

#### **Ambito relazioni ibride:**

- **HDLC**
- **PPP**
- **MPLS**

#### **Ambito peer to peer:**

- **TDM**
- **FDM**
- **SDH**

---

### La Trasmissione Dati

Lo strato fisico deve trasportare dati. Questi sono:

- **Digitali** → rappresentazione discreta
- **Analogici** → segnale intenso, continuo

Nei DTE si usa una rappresentazione digitale trascrivendo ogni dato in sequenze di 0 o 1.

I dati vengono sottoposti a:

- Conversione in un differente tipo di segnale digitale, con livello 0 o 1
- Conversione in analogico (modulazione), quindi un segnale con diversi livelli di intensità

---

### Segnali Sinusoidali

È un segnale che varia nel tempo secondo la legge:

**U = U sin(ωt + Φ)**

dove:

- **t** è il tempo trascorso
- **ω** velocità angolare
- **Φ** lo sfasamento di fase

La curva descritta prende il nome di **sinusoide**.

![Segnali Sinusoidali](images/segnali_sinusoidali.png)

Questa curva rappresenta il valore del seno dell'angolo istante per istante che ruota in senso antiorario con velocità **ω**. Quindi **Φ** rappresenta l'angolo che viene formato con l'asse x all'istante 0.

Ruotando tornerà alla posizione di partenza e si ripeterà. Il numero di volte al secondo che il segnale torna allo stato di partenza si chiama **FREQUENZA** e viene calcolata in **Hertz = 1/t**.

Un segnale che ha una frequenza di **1 KHz** vuol dire che percorrerà la circonferenza 1000 volte al secondo. La velocità è data dunque da **2πf**. Il periodo che sta nel mezzo della ripetizione del segnale si chiama periodo.

**ω = 2πf**

Dunque un'onda portante sinusoidale ha forma del tipo:

**s(t) = A cos(2πft + Φ) = A sin(ωt + Φ + π/2)**

con:

- **A** ampiezza della portante
- **f** frequenza
- **Φ** fase

Un **periodo** è dato dall'unità di tempo diviso la frequenza → **T = 1/f**.

Dunque un segnale con **1 KHz** di frequenza ha periodo di **1/1000 = 1 millisecondo**.

La **lunghezza d'onda λ** mette in relazione frequenza e velocità di trasmissione:

**λ = C/f** dove **C = 300.000 km/sec**

Lo **spettro** è l'insieme di frequenze che il segnale contiene.

La **larghezza di banda** è l'intervallo delle frequenze contenute in un segnale composto. Se un segnale ad esempio trasmette da 300 Hz a 3400 Hz la sua larghezza sarà 3100 Hz.

---

### Sviluppo in Serie di Fourier

Il teorema di Fourier ci dice che un segnale periodico può essere considerato come la somma di infinite sinusoidi diverse.

Matematicamente:

**S(t) = A₀ + A₁ sin(ωt + φ₁) + A₂ sin(2ωt + φ₂) + A₃ sin(3ωt + φ₃) + ...**

![Fourier Terza Armonica](images/fourier_terza.png)

![Fourier Nona Armonica](images/fourier_nona.png)

Utilizzando sempre più segnali sinusoidali diversi e opportuni, il segnale ricostruito in giallo è sempre più tendente ad una forma quadrata. Questo si ha passando da un'analisi dalla 3ª alla 9ª armonica. Il numero di armoniche usate per la ricostruzione di un segnale varia in base alla potenza del segnale da rappresentare. In genere si considera l'armonica sino a che la sua ampiezza non sia **1/10** della grandezza originale.

L'analisi di Fourier ci ricorda che un segnale digitale è un segnale analogico composto da banda teoricamente infinita. Nasce il problema di come trasmettere il segnale analogico come digitale tra 2 punti.

---

### Filtri

Sistema che tratta in modo specifico le componenti di un segnale a frequenze diverse. Aiuta a separare le informazioni o eliminare il disturbo.

I **filtri attivi** usano amplificatori operazionali o transistori, quelli **passivi** usano componenti come resistori o condensatori.

#### **Filtro Passa Basso**

Permette il passaggio di frequenze sotto una certa soglia, chiamata frequenza di taglio. In questa sussiste la relazione:

**Vout / Vin = 1/√2**

dove **Vout** è il segnale in uscita e **Vin** quello in entrata. Così è attenuato circa di un 30%.

#### **Filtro Passa Alto**

Permette il passaggio di frequenze al di sopra della frequenza di taglio.

#### **Filtro Passa Banda**

Permette il passaggio di frequenze all'interno di un certo range detto _banda passante_ e attenua quelle fuori da questo range.

#### **Filtro Elimina Banda o Filtro Notch**

Blocca un certo intervallo di frequenze **ωL - ωH**.

---

### Modulazione di un Segnale

Il DTE sorgente immette nel canale un segnale digitale con distribuzione di energia troppo ampia per poter stare dentro un canale telefonico, deve quindi essere convertita.

La **modulazione** è un'operazione secondo la quale un segnale **portante** viene modificato in un parametro essenziale in accordo al segnale informativo d'ingresso, **modulante**.

---

### Modulazione ad Onda Continua

Ha 3 tipi di modulazione analogica:

#### **AM (Amplitude) - Modulazione di Ampiezza**

Sistema per il quale si modula l'ampiezza del segnale che si deve trasmettere **portante** in maniera proporzionale al segnale che si intende trasmettere, **modulante**.

Così il segnale modulato ha la stessa frequenza del segnale portante.

In digitale lo 0 è bassa potenza e l'1 alta potenza.

Trasmettendo un segnale modulante del tipo **vm(t) = vm cos(ωmt + Φ)** ponendo **Φ = 0**.

Sia la portante **vp(t) = vp cos(ωpt)** con frequenza maggiore, il segnale modulato in ampiezza diventa:

**v(t) = [Vp + KaVm cos(ωmt)] cos(ωpt)**

![Modulazioni](images/modulazioni.png)

#### **FM (Frequency) - Modulazione di Frequenza**

Nella AM il rumore che cade nella banda del segnale si somma, degradando così il contenuto informativo. Nella modulazione di frequenza l'ampiezza resta standard, ma cambia la frequenza del segnale. Più l'onda modulante aumenta più l'onda si infittisce. Ha un'efficienza maggiore e risente meno dei disturbi, ma è più complessa da costruire.

La pulsazione della portante varia di frequenza, proporzionalmente al valore della modulante, lasciando l'ampiezza **Vp** inalterata.

**vm(t) = VM sin ωmt**

**vp(t) = Vp sin(ωpt + mf sin ωmt)**

con **mf = (Kf VM)/ωm = (Kf VM)/2πfm = Δf/fm**

#### **PM (Phase) - Modulazione di Fase**

Simile alla modulazione di frequenza, ma la frequenza del segnale portante è più stabile. Viene spesso usato per amplificare il segnale di sistemi di frequenza.

Si fa variare la fase della portante in modo direttamente proporzionale all'ampiezza modulante.

**VPM(t) = VP cos(ωPt + Kp Vm sin ωmt)**

---

### Tabella Riassuntiva AM-FM-PM

| Caratteristica          | AM              | FM        | PM                                |
| ----------------------- | --------------- | --------- | --------------------------------- |
| Parametro modificato    | Ampiezza        | Frequenza | Fase                              |
| Robustezza al rumore    | Bassa           | Alta      | Alta                              |
| Complessità             | Bassa           | Alta      | Alta                              |
| Impiego tipico          | Radio analogica | Radio FM  | Comunicazioni digitali (PSK, QAM) |
| Ampiezza della portante | Variabile       | Costante  | Costante                          |

---

### Modulazione Impulsiva

È un tipo di modulazione dove l'informazione è codificata in una serie di impulsi.

#### **PAM (Pulse Amplitude Modulation)**

Il segnale analogico varia l'ampiezza del treno di impulsi che costituisce la portante.

![PAM](images/pam.png)

#### **PWM (Pulse Width Modulation)**

L'informazione è codificata sotto forma di durata temporale degli impulsi di un segnale. Il modulante varia la larghezza degli impulsi.

![PWM](images/pwm.png)

#### **PPM (Pulse Position Modulation)**

Le ampiezze degli impulsi sono identiche, ma la loro posizione viene modificata in base al segnale della modulante. Più il segnale è positivo più viene ritardata la posizione degli impulsi rispetto a quella di riposo e viceversa.

![PPM](images/ppm.png)

#### **PCM (Pulse Code Modulation)**

Si applica a canali telefonici e permette di fare passare su un solo cavo coassiale fino a 30 telefonate.

---

## PDF_6: PCM

### PCM (Pulse Code Modulation)

Per la sua realizzazione si effettuano 3 operazioni a partire dal microfono di ingresso:

#### **Campionamento**

**Teorema di Shannon:** un segnale a banda limitata compreso tra due frequenze **f₁** e **f₂** | **f₂ > f₁** può essere rappresentato mediante una successione di campioni prelevati con frequenza pari a **2f₂**.

Si assume come frequenza di campionamento il valore **fc = 8 KHz** superiore di **1,2 KHz** al valore minimo di **2f₂ = 6,8 KHz**.

Il periodo sarà dunque **T = 1/fc = 1/8000 = 125 μsec**

Si definisce **frequenza di Nyquist** la minima frequenza necessaria per campionare senza perdere informazione. La minima frequenza è pari al doppio della banda.

Il segnale viene quindi prima campionato poi sostituito dalla frequenza PAM.

#### **Quantizzazione**

Il dato per essere trasmesso deve assumere solo determinati valori discreti e finiti.

Si definisce prima un massimo e un minimo e si divide l'intervallo creato.

Nella **quantizzazione uniforme** ogni sotto-intervallo è uguale ad ogni altro sotto-intervallo.

Dato **n** il numero di bit usati:

- Il numero di livelli sarà **M = 2ⁿ**
- L'ampiezza **q = Vpp/M**
- La varianza **q²/12**

Essendo la quantizzazione irreversibile, occorre tener conto dell'**errore di quantizzazione**, nato dal fatto che il segnale vocale può avere infiniti valori mentre la sua discretizzazione no.

È provato che usando **256 livelli** l'orecchio umano non percepisce differenza.

#### **Codifica**

L'ampiezza degli impulsi viene trasformata in bit.

Ad esempio se l'ampiezza iniziale del primo impulso è di 5V, sarà rappresentata dalla sequenza binaria **101**.

**Esempio:** vengono spediti 96 impulsi. Il n.0, n.32 e n.64 saranno da vedersi consequenziali come il 5, 37, 69. Di questi 32 impulsi il n.0 serve per dettare il sincronismo, il 16 per il controllo della bontà di trasmissione.

In totale di 30 canali vocali, 2 sono di servizio.

Vengono trasmessi 32 canali con 8000 campioni al secondo. Ogni canale contiene 8 bit, quindi al secondo vengono trasmessi:

**Vbit = 32 × 8000 × 8 = 2048 Mbit/s**

Si possono raggruppare più canali.

---

### Modulazioni Digitali

Tecniche che modulano segnali digitali, ossia 0 e 1 o -1 e +1.

#### **Modulazione per Modem di Banda Base**

Per il collegamento tra 2 DTE si parla di codifica volta ad eliminare segnali di bassa frequenza e segnali in componente continua.

Il digitale rimane lo stesso, ma vengono fatte delle modifiche alla portante rispetto al modulante.

#### **ASK (Amplitude Shift Keying)**

La modulazione a spostamento d'ampiezza trasmette i bit modificando l'ampiezza della portante.

**s(t) = { A cos(2πft) se bit=1, 0 se bit=0 }**

Semplice ma sensibile al rumore.

#### **FSK (Frequency Shift Keying)**

Modulazione per spostamento di frequenza. I bit vengono trasmessi variando la frequenza della portante mantenendo ampiezza e fase costanti.

Più robusta di ASK ma richiede banda maggiore.

#### **PSK (Phase Shift Keying)**

Si trasmettono i bit modificando la fase portante, mantenendo ampiezza e frequenza costanti. Molto robusta ma può causare discontinuità.

#### **BPSK (BiPolar Phase Shift Keying)**

La portante mantiene valori costanti per ampiezza e frequenza, ma per garantire massima protezione da rumore, vengono usati due valori opposti di fase in base al valore del bit: **0°** e **180°** per rispettivamente bit 1 e bit 0.

Quindi, l'onda "invertirà" il segnale quando vi sarà un valore 0, mentre per valore 1 rimane uguale.

#### **4-PSK**

Modulazione digitale a 4 fasi. I bit vengono riuniti in coppie usate per modulare in fase la portante sinusoidale (dibit).

![4-PSK](images/4psk.png)

I due bit generano due flussi separati meno veloci di quello originale.

Le due portanti hanno stessa frequenza, ma le loro fasi differiscono di 90°.

La fase del segnale in uscita dal primo modulatore può assumere valori **0°** e **180°**, il secondo **90°** e **270°**.

Infine vengono sommate generando un segnale che può assumere 4 fasi diverse: **45°, 135°, 225°, 315°**.

Il circuito sfasatore sfasa il segnale portante di 90°.

Al blocco di separazione è applicato in ingresso il segnale modulante **Vi** che viene separato in bit pari (P) portati al moltiplicatore 1 e dispari (D) portati al moltiplicatore 2.

Inoltre il separatore associa allo stato logico basso +1, mentre a quello alto -1, così da avere un segnale in fase (livello basso) o sfasato di 180° (livello alto) all'uscita del moltiplicatore.

![Schema 4-PSK](images/4psk_schema.png)

---

### Diagrammi a Costellazione

Rappresentazione teorica del segnale, usata per la comprensione del suo stato.

Il segnale trasmesso in digitale è diviso in 2 segnali modulati in quadratura che non interferiscono denominati **I** e **Q** (In-fase e Quadratura).

Si crea un diagramma su piano con I e Q come assi e in base allo schema di modulazione i punti nel diagramma saranno più o meno fitti.

Il problema è che a causa di interferenze, il vettore del segnale modulato non si trova in uno dei punti previsti, ma leggermente più o meno spostato a seconda dei disturbi.

---

### Vettore Errore

Differenza tra il punto teorico e il punto reale.

Può essere descritto caratterizzato dal suo modulo e dalla sua fase.

![Vettore Errore](images/vettore_errore.png)

I vettori errore descrivono quanto "balla" il segnale ricevuto nei dintorni del punto teorico.

Misurandone tanti e tenendo in considerazione il valore quadratico medio del modulo, si ricava un parametro che descrive la qualità intrinseca della modulazione.

---

## PDF_7: EVM

### EVM (Error Vector Magnitude)

Questo parametro esprime il valore % dell'errore rispetto al segnale.

Può essere calcolato anche come rapporto espresso in dB tra valore quadratico medio della potenza del vettore e il valore quadratico medio della potenza del segnale ideale di riferimento.

**Più grande EVM peggiore la qualità.**

Essendo valori piccoli il rapporto espresso in dB assume valori estremamente piccoli. Tanto più negativi quanto migliore il segnale.

1. [Decibel e EVM](#decibel-e-evm)
2. [Modulazioni Digitali](#modulazioni-digitali)
   - [Codifica Differenziale DPSK](#codifica-differenziale-dpsk)
   - [Modulazione QAM](#modulazione-qam)
   - [Codifica Trellis](#codifica-trellis)
3. [Alterazioni del Segnale](#alterazioni-del-segnale)
4. [Limiti della Velocità](#limiti-della-velocità)
5. [Codifica di Canale](#codifica-di-canale)
6. [Controllo degli Errori](#controllo-degli-errori)
7. [Multiplazione](#multiplazione)
8. [Modem](#modem)
9. [Interfacce](#interfacce)

## Decibel e EVM

### Definizione di Bel e Decibel

Il **Bel** è definito come logaritmo del rapporto tra una grandezza X e il suo valore di riferimento X₀.

**1 Decibel** = 1/10 di Bel

Formula generale: **dBₓ = 10 log(X/X₀)**

**Scala logaritmica:**

- x = 0 ⇒ logaritmo = -∞
- x = 1 ⇒ logaritmo = 0
- x = valore della base ⇒ logaritmo = 1

⚠️ **Importante:** Valori sempre più negativi di EVM indicano prestazioni migliori.

### Misurazione dell'EVM

**Strumenti utilizzati:**

- Analizzatore di segnali
- Analizzatore di modulazione
- Analizzatore vettoriale
- Versione software (su analizzatori di spettro, digitalizzatori, oscilloscopi)

**Processo di misurazione:**

1. Il segnale viene demodulato
2. Dai dati demodulati si ricostruisce il segnale ideale
3. Per differenza si ottiene il segnale errore
4. L'elaborazione del segnale errore porta all'EVM

**Formati di output:**

- Forma sintetica tabellare
- Percentuale
- dB
- Grafico dell'evoluzione nel dominio del tempo
- Analisi della fase del vettore o solo del modulo

---

## Modulazioni Digitali

### Codifica Differenziale DPSK

Per evitare complicazioni si usa una **modulazione differenziale (DPSK)**.

**Caratteristiche:**

- Ai due livelli binari corrisponde:
  - Nessuna variazione, oppure
  - Variazione di 180°
- La prima cifra si individua inviando una sequenza prestabilita a inizio comunicazione
- Ha lo stesso andamento di un PSK (stesse caratteristiche spettrali)

**Codifica avanzata:**

```
01 = 90°
10 = 180°
11 = -90° (o 270°)
```

### Modulazione QAM

**QAM (Quadrature Amplitude Modulation)** = Combinazione di ASK e PSK

Chiamata anche **modulazione di ampiezza in quadratura**.

Si ottiene modulando in ampiezza due portanti della stessa frequenza sommate in quadratura (sfasate di 90°).

✓ **Utile per trasmissioni veloci**

#### Modulazione 16-QAM

**Funzionamento:**

- Dati divisi in gruppi da 4 bit (quadribit)
- La fase della portante varia secondo la regola 8-DPSK in base agli ultimi 3 bit
- Il primo bit opera una modulazione di ampiezza sul segnale già modulato in fase
- Risultato: 2³ = 8 salti di fase, ciascuno con un'ampiezza corrispondente al primo bit (0 o 1)

#### Modulazione 64-QAM

Modulazione **bidimensionale** ottenuta dalla combinazione di due PAM modulate con portanti seno e coseno.

### Codifica Trellis

**Codifica "con memoria"**

Rappresentata da una macchina con due stati associati a:

- **S0** → valore -A
- **S1** → valore +A

(supponendo un segnale PAM dove i simboli sono rappresentati da livelli di ampiezza)

**Regole:**

- Bit **0**: non fa cambiare stato
- Bit **1**: cambia lo stato

---

## Alterazioni del Segnale

Tutti i processi di modifica che differenziano il segnale da quello originale.

### 1. Attenuazione

**Definizione:** Perdita di energia del segnale.

**Soluzione:** Uso di amplificatori.

**Misura in decibel:**

Con **P₁ = potenza di output** e **P₂ = potenza di input**:

```
dB = 10 log₂(P₂/P₁)
```

Con **V₁ = tensione iniziale** e **V₂ = tensione finale**:

```
dB = 20 log₁₀(V₂/V₁)
```

**Valori di riferimento:**

- Fino a 20 dB: ✓ Perfetto
- Da 60 dB in su: ✗ Critico

### 2. Distorsione

**Definizione:** Cambiamento della forma del segnale, tipicamente in un segnale costituito da varie frequenze.

**Causa:** Possibili ritardi tra i vari segnali che creano differenze tra forma del segnale inviato e quello ricevuto.

### 3. Rumore

**Definizione:** Insieme di segnali indesiderati che si sovrappongono a quello utile.

**Causa principale:** Rumore termico causato dai componenti del sistema.

**SNR (Signal-to-Noise Ratio):**

```
SNR = P_segnale / P_rumore
```

**Valori di riferimento:**

- 28 dB: ✓ Ottimo
- 7-10 dB: ✗ Critico

### 4. Interferenza

**Definizione:** Sovrapposizione di informazioni non desiderate. Contaminazione da parte di segnali esterni.

### 5. Interferenza Intersimbolica

**Causa:** Limitazioni della banda che provocano un arrotondamento dei segnali emessi da un DTE.

---

## Limiti della Velocità

Velocità calcolata in **bit/sec** su canali telefonici:

**Tipi di canali:**

- **Canali perfetti:** senza distorsioni o ritardi
- **Canali ideali:** solo ritardo costante
- **Canali reali:** attenuazioni e ritardi in funzione della frequenza

### Teorema di Nyquist

**Formula (canale senza rumore):**

```
MaxDataRate = 2B × log₂(V)
```

- **B** = larghezza di banda
- **V** = numero di livelli di tensione differenti nel segnale

### Teorema di Shannon

**Formula (tenendo conto del rumore):**

```
MaxDataRate = C = B × log₂(1 + S/N)
```

- **B** = larghezza di banda
- **S** = potenza del segnale
- **N** = potenza del rumore

**Utilizzo:**

1. Con la prima formula si ricava il numero opportuno di livelli V
2. Con la seconda si ottiene il Max Data Rate reale

---

## Altri Limiti della Velocità

### Throughput

Quanto velocemente si possono spedire dati attraverso una rete **reale** (la velocità trasmissiva considera quella teorica).

### Latenza

Tempo necessario ad un messaggio per arrivare a destinazione.

**Componenti:**

- Tempo di propagazione
- Tempo di trasmissione
- Tempo di inoltro
- Tempo di attesa

### Jitter

Esprime la **variabilità del ritardo** con cui i pacchetti vengono consegnati.

### Velocità di Modulazione e Trasmissione

**Velocità di modulazione:** numero di simboli trasmessi al secondo, espressa in **baud** (simboli/sec).

⚠️ **Nota:** Un simbolo può rappresentare più bit.

**Relazione:**

```
Velocità_modulazione = Velocità_trasmissione / log₂(n)
```

---

## Codifica di Canale (Encoding)

Tecniche di codifica usate per la sincronizzazione.

### NRZ (Not Return to Zero)

**Caratteristiche:**

- Stato digitale **1** → segnale alto
- Stato digitale **0** → segnale basso
- ✓ Facile, non richiede circuiti complicati
- Dati passati direttamente in uscita
- ✗ Lunghe stringhe potrebbero causare perdita di sincronismo

### RZ (Return to Zero)

**Caratteristiche:**

- Stessa rappresentazione degli stati digitali
- A metà dell'impulso torna sempre a 0
- Clock a frequenza doppia (riduce al 50% la durata dell'impulso)
- Il ricevitore distingue tra 3 livelli
- ✓ Lunghe stringhe non causano perdita di sincronismo
- ✗ Maggior rischio di errore

### Manchester

**Caratteristiche:**

- Divide in 2 parti uguali il periodo di cifratura
- **0 logico** → transizione dal basso verso l'alto a metà bit
- **1 logico** → transizione dall'alto verso il basso a metà bit
- ✗ Raddoppia la banda necessaria
- ✓ Usata nelle LAN
- Richiede circuito complicato

### AMI (Alternate Mark Inversion)

**Caratteristiche:**

- Codice a tre livelli: **+V, 0, -V**
- Ottenuto dal codice RZ lasciando inalterato lo zero
- Stato logico **1** alternato tra +V e -V
- ✓ Usato in PCM

### Scrambling

**Scopo:** Superare i problemi di trasmissione su lunga distanza.

**Funzionamento:**

- Cambiano le regole di codifica per mescolare i bit
- Uso di registro a ciclo
- Usato nella codifica **2B1Q** (2 Binary 1 Quaternary)
- Flusso di bit organizzato in gruppi di 2 bit
- Ogni gruppo codificato in uno di 4 possibili livelli
- ✓ Mantiene costante il segnale

---

## Trasmissione dei Dati

### Trasmissione Orientata al Carattere

**Utilizzo:** Principalmente per contenuti testuali

**Caratteristiche:**

- In assenza di start e stop bit: sequenza di caratteri **SYN** per avviare il sincronismo
- **DLE (Data Link Escape):** carattere di controllo per byte stuffing
- **Byte stuffing:** aggiunta di uno 0 ogni cinque 1 consecutivi

### Trasmissione Orientata al Bit

**Caratteristiche:**

- Dati non organizzati in caratteri
- ✓ Riduce l'inefficienza legata ai caratteri di controllo
- ✓ Evita dipendenza dai caratteri
- Usa **idle bytes** o **flag bytes** per indicare inizio/fine trama (non SYN o STX)

---

## Controllo degli Errori

### Tipi di Errore

1. **Errori single bit:** invertono un solo bit (comune)
2. **Errori multiple bit:** invertono più bit non consecutivi
3. **Error burst:** invertono due o più bit consecutivi (molto raro)

### Rilevamento degli Errori

**Tecnica:** Ridondanza

I bit supplementari aggiunti sono **bit ridondanti**, eliminati quando il ricevitore conferma la trasmissione corretta.

#### 1. VRC (Controllo Ridondanza Verticale)

**Funzionamento:**

- Aggiunta di un singolo bit all'unità
- Numero di bit = 1 diventa pari o dispari
- **Parity check:** numero pari
- **Disparity check:** numero dispari

**Limiti:**

- ✓ Facile da implementare
- ✗ Non rileva inversione di bit pari

#### 2. LRC (Controllo Ridondanza Longitudinale)

**Funzionamento:**

- Come VRC: bit di parità per ogni unità
- Aggiunge unità supplementare con bit di parità per sequenze corrispondenti
- ✓ Maggiore affidabilità del VRC
- ✗ Può essere ingannato da trasposizioni di byte

#### 3. CRC (Controllo di Ridondanza Ciclica)

**Funzionamento:**

- Orientato ai bit
- Associa ogni sequenza di k bit ai coefficienti di un polinomio di grado k-1
- Usa un **checksum** per rendere il polinomio divisibile per G(x)
- G(x) è conosciuto a priori da ricevitore e mittente

**Calcolo del checksum:**

1. Aggiungere r bit 0 al segmento → sequenza m+r bit corrispondente a x^r × M(x)

   - r = gradi di G(x)
   - M(x) = polinomio della sequenza iniziale

2. Dividere x^r × M(x) per G(x) con divisione mod 2

   - R(x) = polinomio corrispondente al checksum

3. Sommare R(x) a x^r × M(x) → segmento da trasmettere con checksum

**Suggerimenti per G(x):**

- Con polinomi aventi **x⁰ = 1**: errori di un bit sempre rilevati
- Con **x+1** come fattore: rilevazione errori di numero dispari
- **r** deve essere il più grande possibile

**Classi di errori burst (L = lunghezza errore):**

- **L ≤ r:** tutti gli errori rilevati
- **L ≥ (r+1):** errore non rilevato con probabilità (1/2)^r
- **L = (r+1):** errore non rilevato con probabilità (1/2)^(r-1)

---

## Multiplazione

**Definizione:** Utilizzo dello stesso canale per più comunicazioni separate.

### FDM (Frequency Division Multiplexing)

**Funzionamento:**

- Le comunicazioni vengono shiftate a frequenza superiore con un certo gap
- Ancora ampiamente usata nella rete telefonica

**Caratteristiche:**

- Banda fonica: **B = 4 kHz**
- Ogni canale multiplato occupa 4 kHz
- Numero di canali: **N = BT / 4 kHz**
- Traslazione realizzata mediante modulazione di ampiezza di N portanti (**frequenze vertici**)
- In ricezione: filtraggio delle bande e demodulazione per estrarre segnale in banda base
- Da 12 a 10.800 canali multiplabili
- ✗ Sensibile al rumore (segnale analogico)

**Esempio:**

- 12 canali multiplati traslati con portanti distanti 4 kHz (64-68-...-108 kHz)
- Banda totale: **BT = 12 × 4 kHz = 48 kHz**

### WDM (Wavelength Division Multiplexing)

**Utilizzo:** Segnali ottici

**Caratteristiche:**

- Ottimizza l'utilizzo della fibra ottica
- Modula la lunghezza d'onda del raggio luminoso
- ✓ Invio di diversi raggi in contemporanea

### D-WDM (Dense Wavelength Division Multiplexing)

**Caratteristiche:**

- Modula fino a **16 lunghezze d'onda** alla distanza di 0.08 nm
- Lunghezze d'onda modulate con flussi TDM
- Velocità: fino a **1 Tb/s**

#### EDFA (Amplificatori in fibra ottica drogata)

Usano un tratto di fibra drogata di lunghezza L come mezzo per l'amplificazione del segnale ottico. Il segnale ottico e uno di pompa vengono multiplati in una fibra drogata e il segnale risulta amplificato per effetto dell'emissione di fotoni grazie all'interazione del segnale ottico di pompa con gli ioni del drogante.

### C-WDM (Coarse Wavelength Division Multiplexing)

**Utilizzo:** Reti metropolitane a basso costo

**Caratteristiche:**

- Maggiori spaziature tra i canali
- ✓ Risparmio economico
- Spaziatura: circa **20 nm**
- Frequenze: da 1310 nm a 1610 nm

### TDM (Time Division Multiplexing)

**Funzionamento:** Usa la temporizzazione per i differenti segnali

**Tipi:**

1. **TDM Sincrono:**

   - Intervalli scelti indipendentemente dalla presenza di dati
   - Corrispondenza tra dato e canale

2. **TDM Statistico:**
   - Intervalli allocati solo quando ci sono dati da spedire
   - Nessuna corrispondenza fissa tra dato e canale

Un segmento di dati è diviso in base al numero di canali logici disponibili.

---

## Modem

**Modem** = Contrazione di **Modulatore/Demodulatore**

### Funzioni Principali

- Converte segnali dal DTE in segnali adatti per la trasmissione (tipicamente linea telefonica)
- Trasforma segnale numerico dal DTE in segnale analogico e viceversa
- Gestisce circuiti di comando e controlla l'interfaccia
- Corregge errori e analizza i dati ricevuti

### Modem Fonici

**Range di frequenze:** 300-3400 Hz

### Altri Tipi di Modem

- **Modem ISDN:** 128 kbps
- **Modem xDSL:** da 640 kbps a 100 Mbps
- **Modem PLC** (Power Line Communications): su linea elettrica (640 kbps – 200 Mbps)
- **Modem GPRS/UMTS/HSDPA/LTE:** integrati in cellulari o PC card (56 kbps – 7.2 Mbps - 100 Mbps)
- **Modem in banda base:** collega direttamente due utenti su doppino telefonico

### Configurazioni

**Modem esterni:**

- Seriali (cavo COM1/2)
- Paralleli (cavo LPT1/2)
- USB

**Modem interni:**

- PCI (lavorano sul BUS PCI)
- PCMCIA o PC card (solo PC portatili)

### Modulazione per Velocità

- **Bassa velocità** (fino a 1200 bit/s): modulazione **FSK**
- **Velocità media** (fino a 4800 bit/s): modulazione **PSK** o **DPSK**
- **Alta velocità** (oltre 9600 bit/s): modulazione **QAM**

### Standard ITU

Lo standard delle tecniche di interfacciamento è deciso dall'**ITU**.

#### V.21 - FSK

#### V.29 - QAM

- Codifica multilivello su 4 bit
- Spettro: circa 2400 Hz
- Portante: 1700 (±1) Hz

#### V.32 - QAM

- Modalità sincrona point-to-point
- Modulazione QAM
- 2400 baud, quadribit su 16 livelli
- Velocità: 9600 bit/s
- **Codifica Trellis:** maggiore immunità al rumore
  - Aumenta la ridondanza (ogni 4 bit, uno ridondante)
  - Costellazione di 32 livelli
- **Soppressione dell'eco:** invio full-duplex del segnale e sua replica invertita

#### V.34

- Collegamenti con due terminazioni analogiche
- Velocità: 28.880 bit/s
- Codifica non lineare, multidimensionale
- Sfrutta tutta la banda disponibile

#### V.90

- Migliora le prestazioni del V.34
- Flusso verso la rete minore
- Segnale verso l'utente tipo dati

#### V.92

- Upstream: 48 kbps
- **Quick connect**
- Mantiene connessioni attive fino a 16 minuti
- Codifica adattiva

---

## ADSL

(Asymmetrical Digital Subscriber Line)
Il doppino telefonico possiede una discreta banda, limitata però a soli 4 kHz.

### Tecniche di Modulazione

1. **CAP (Carrierless Amplitude Phase)**

   - Versione sofisticata di QAM

2. **DMT (Discrete Multi-Tone)**
   - Modula un insieme di **256 sottoportanti** distanti 4.3125 kHz
   - Banda totale: 26 kHz - 1.1 MHz

### Suddivisione della Banda

1. **Banda bassa:** fino a 4 kHz
2. **Banda media:** per upstream
3. **Banda alta:** per downstream

### Velocità Teoriche

- **Downstream:** 8 Mbit/s
- **Upstream:** 800 kbit/s

### Standard ANSI T1.423

- Non ancora completamente standardizzato
- Ogni costruttore ha varianti proprie
- Linee guida dallo standard ANSI T1.423
- Ammette solo modulazione DMT
- Adattamento di rateo
- Connessione a livello di internetworking con reti ATM

---

## Interfacce

### Interfaccia Centronics Parallela

**Caratteristiche:**

- Interfaccia parallela a 8 bit asincrona
- Uso tipico: collegamento PC-stampante
- Originariamente monodirezionale
- Ora supporta anche dispositivi input
- Connettore tipo D a 25 poli Femmina
- Fino a 3 interfacce LPT parallele
- Ogni interfaccia con 3 indirizzi contigui

**Registri:**

- Primo registro: contiene i dati
- Secondo registro: stato della stampante

### Interfaccia RS232

**Connettori:**

- **DTE:** spina
- **DCE:** presa
- Connettore standard: 25 poli
- Altre applicazioni: connettore a 9 poli

**Linee (Circuiti) dell'interfaccia V.24:**

| Codice | Nome                               | Direzione | Funzione                                      |
| ------ | ---------------------------------- | --------- | --------------------------------------------- |
| C101   | Massa di protezione                | -         | Collegata alla massa dei segnali C102         |
| C102   | Massa di segnali                   | -         | Riferimento comune per tutti i circuiti       |
| C103   | Dati in trasmissione               | DTE → DCE | Dati binari seriali dal DTE al DCE            |
| C104   | Dati in ricezione                  | DCE → DTE | Dati binari seriali dal DCE al DTE            |
| C105   | Richiesta di trasmissione          | DTE → DCE | Trasmette la portante in linea                |
| C106   | Pronto a trasmettere               | DCE → DTE | DCE pronto a trasmettere (risposta a C105)    |
| C107   | Modem pronto                       | DCE → DTE | Modem collegato                               |
| C108   | DTE pronto                         | DTE → DCE | DTE pronto                                    |
| C109   | Portante in ricezione              | DCE → DTE | Portante sopra soglia di ricezione            |
| C110   | Rilevatore qualità segnale         | DCE → DTE | Tutti i dati sono corretti                    |
| C111   | Selezione di velocità              | DTE → DCE | Obbliga il modem a scegliere velocità elevata |
| C112   | Selezione di velocità              | DCE → DTE | Modem seleziona velocità usata                |
| C113   | Clock trasmissione da DTE          | DTE → DCE | Clock del DTE                                 |
| C114   | Clock trasmissione da DCE          | DCE → DTE | Clock del DCE                                 |
| C115   | Clock in ricezione                 | DCE → DTE | Clock per dati ricevuti su C104               |
| C118   | Trasmissione supervisore           | DTE → DCE | Come C103 per canale supervisore              |
| C119   | Ricezione supervisore              | DCE → DTE | Come C104 per canale supervisore              |
| C120   | Richiesta trasmissione supervisore | DTE → DCE | Per canale supervisore                        |
| C121   | Pronto trasmissione supervisore    | DCE → DTE | Per canale supervisore                        |
| C122   | Rilevatore segnale supervisore     | DCE → DTE | Uguale a C109                                 |
| C123   | Rilevatore qualità supervisore     | DCE → DTE | Come C110                                     |
| C125   | Chiamata in arrivo                 | DCE → DTE | Indica ricezione chiamata (risposta su C108)  |
| C125   | Scelta frequenza trasmissione      | -         | -                                             |

### Interfaccia USB

**Storia:** Inventata nel 1995 per sostituire le porte seriali e parallele.

**Versioni:**

- **USB 1.0:** 12 Mbps
- **USB 2.0:** 480 Mbps
- **USB 3.0:** 5 Gbps

**Connettore:** 4 poli disposti verticalmente

- GND
- DATI +
- DATI -
- +5V

### Interfaccia IEEE 1394 (FireWire)

**Caratteristiche:**

- Seriale e bidirezionale
- Concepita per alte velocità
- Standard evoluto: collegamenti fino a 100 m
- Per PC: schede su bus PCI
- Connettori: 4 pin o 6 pin

---

# Da qui in poi è da far riformattare a claude <3

---

# PDF_10

#### Interfaccia RS422

Nato per la trasmissione di segnali digitali fino a 10Mbits/s fino a 1200m.
Questo standard impone che ogni linea differenziale sia pilotata da un driver
Anche se è più comune l'utilizzo per le connessioni punto a punto , ci possono essere fino a 10 ricevitori.

Gli stati sono rappresentati così:

- quando il terminale A è negativo rispetto a B la linea rappresenta un 1 binario. Tale stato rappresenta anche uno stato di idle
- quando A è positivio rispetto a B la linea rappresenta uno 0 binario
  A>B = 0, A<B = 1
  ![alt text](images/rs422.png)

A e B quindi hanno sempre due valori opposti tra di loro.
La differenza di potenziale tra A e B deve essere almeno di 4V.

### Reti per la trasmissione dati

- PSTN (Public Switching Telephone Network)
- ISDN (Integrated Service Digital Network)
- CATV (Community Antenna Television (negli USA))
- LAN (Local Area Network)
- VPN (Virtual Private Network)
- Wireless Network
  non sono altro che connessioni fisiche ad una seconda rete, quella degi ISP (internet service provider) che fornisce un punto di accesso ad internet

### Strutture di rete

In italia tutt'ora viene usato per la maggiore il doppino telefonico twisted pair. Sono tratti di cavo con centinaia di doppini connessi a punti per la flessibilità usati per il controllo. I tratti di doppino sono distinti in:

- rete di accesso primaria => tra centrale e armadio, formata da cavi con centinaia di coppie
- secondaria => tra armadio e distributore, formata da cavi con decine di coppie
- raccordo cliente o cablaggio verticale => tra distributore e borchia di accesso

#### FTTH, FTTC, FTTB - Fibra ottica

- FTTH => fiber to the home
  - OLT (optical line termination)
  - ONU (optical network unit) => intefaccia con terminale, in genere "vicino all'utente"
  - ONT (optical network termination)
- FTTC => fiber to the cabinet => poi rame fino alla "casa"
- FTTB => fiber to the building => fibra fino ad una centralina condominiale con successivo collegamento in rame.

L'utilizzo d FTTH porta a due approcci distinti all'uso della fibra:

- AON (active optical network) => detet anche p2p
- PON (passive optical network) => assenza di apparati attivi al di fuori delle sedi dove sono collegati OLT ONT o ONU. Usa topologia ad albero

#### Banda larga

##### XDSL

Questo gruppo di sistemi hanno caratteristiche favorevoli per la banda larga come cavi a coppie recenti e circuiti utenti brevi. In italia però come al solito le cose o non le facciamo o le facciamo male, infatti 1/3 della popolazione non ha nel suo comune centrali con termiali DSLAM.
Il DSLAM multipla miglialia di addessi in un'unica interfaccia ad alta densità verso la rete di trasporto.
Opera come uno switch network a livello 2 OSI.

##### Televisione Digitale Terrestre Interattiva

C'è lo standard europeo DVB-H che permette a piccoli apparati di ricevere.
Combina gli standard del video digitale con IP suddividendo i contenuti in paccheti di dati da trasferire su cellulare e leggibile da parte dell'utente.

##### Comunicazioni mobili di 3° e 4° generazione

Tech 3G e 4G
HSPA, high speed packet access è l'anello successivo della catena costituita da

- GSM (global system for mobile communications)
- GPRS (general packet radio service)
- UMTS (uniersal mobile telecommunications system)
  e' gia presente nel mercato.

##### PDH

Plesiochronous Digital Hierarchy, tecnologia che permetti multuplexing e demu dei canali aggregati. Qui due unità sono sincornizzate ma non perefttamente. Infatti ogni volta che si vuole estrarre da un canale si estrae un elemente della gerarchia per volta.
La codifica PCM genera flussi da 64kbit/s e si inviano in trame che si ripetono ogni 125ms.
PDH è il pirmo metodo di multiplazione per trasmettere molti canali isnieme con l'aggiunta di due canali di controllo (32 trame in totale).
Viene usato un multiplexer TDM. Il multiplexer deve inserire slot aggiuntivi per compensare la differenza di bitrate e rendere sincrono il flusso in entrata al multiplexer ricevente.
PDH non controlla le prestazioni della rete.

##### SDH

Synchronous Digital Hierarchy nasce per ovviare a problemi di temporizzazione di PDH. E' un protocollo a livello fisico usato per la trasmissione di fonia e dati su fibra e rete elettrica. Aggrega flussi con bitrate diversi e li spedisci tutti insieme.

Questo protocollo prevede che tutti gli elementi di rete siano sincronizzati sullo stesso clock. Permette di raggiungere elevati livelli di qualità con l'invio di informazioni di servizio.
Viene oggi usata per anelli ottici di accesso con topologia a rete o P2P. Non presenta limiti di distanza e offre una velocita di 140Gb/s.
Unico limite, l'uso di TDM.
Per reti con maggior numero di accessi per anello si preferisce l'uso di tecnologie per la multiplazione statica delle risorse, come Gigabit Ethernet.
SDH oggi si sviluppa in OTN (optical transport network)

# PDF_11

##### SONET

Al livello 3 OSI è responsabile della comunicazione end to end.
Controlla e gestisce lo stato di una connessione.
Lien Layer si occupa di multiplazione di diversi path tra due nodi e della protezione ai guasti.
Section Layer definisce le funzione dei rigeneratori lungo il canale. (Livello 2 OSI)
Photonic Layer definisce il formato di trasmissione su fibra (Livello 1 OSI).

##### Rete CDN

Rete digitale parallela alla PSTN. Prevvede una rete centrale e multiplazione verso gli utenti.
I collegamenti diretti numerici permettono collegamenti punto punto o punto multipunto con tecniche digitali.
Mette a disposizione del cliente un flusso dati della banda desiderata tra due località qualunque del territorio nazionale.
La tecnica di multiplazione è del tutto trasparente.

##### Rete ISDN

Nasce come evoluzione della rete telefonica.
Ha come scopo quello di portare un collegamento digitale a tutte le scrivanie senza l'uso di un modem.
Necessita di apparati specifici installati sia presso la centrale che presso l'utente.
Il vantaggio è quelllo di avere su un unico numero 3 canali: 2 per fonia/dati detti B e 1 di controllo detto canale D.
Ci sono due soluzioni:

- BRI (basic rate interface)
- PRI (primary raet interface). Questa è rivolta ad aziende molto grandi visto che supporta fino a 30 linee multuplate ISDN. L'accesso avviene con un flusso a 2Mbit.

L'accesso usa il protocollo di livello 2 LAPD (link access protocolo channel D)e lavora in ABM (modalità asincrona bilanciata).
Viene installato presso l'utente una borchia ISDN NT1 con i 3 canali.
I due canali B possono essere raggruppati e avere un canale da 128Kbps.
Il segnale in linea è digitale 2B1Q e non necessita di conversioni A/D.
Usa due dispositivi principali come detto prima

- NT1, ha lo scopo di terminare la linea e di convertire il doppino in un bus denominato S. Quest'ultimo è fatto da 8 fili con connettori RJ45 tipico delle reti LAN ETH 10/100base T.
- TA (adapter), usato per interfaciare gli oggetti che non possono essere connesi al bus di tipo S direttamente.
  Il centralino usato per ISDN è denominato ISPBX.

#### Sandard della videocomunicazione

- H.320 => consente la tramissione audio/video su linee digitali ISDN. La trasmissione avviene in digiale indipendentemente dalla velocità di ISDN
- H.323 => standar edlle sessioni di comunicazine audio, video e dati attraverso reti orientate alla connessine. Non è garantita qualità. Diverse applicazioni di diversi produttori possono così operare senza problemi di compatibilità.
- H.324 => standard internazionale per comunicazione multimediale su basso bit rate. (PLMN e 3G ed esempio).
- T.120 => standard delle conferenze dati che fornisce comunicazione in tempo reale tra due o più partecipanti. Comprende funzioni aggiuntive come "una lavagna elettronica", chat, scambio file e condivisione di applicazioni.

## Protocolli del secondo livello ISO-OSI

Il secondo livello, Data Link, si occupa del corretto trasferimento dei dati nella linea trasmissiva strutturando i dati in frames e attuando un controllo di flusso.
Pur avendo definito interfaccia e linea, rimane da indicare tutte le informazioni che il trasmettitore dovrà inviare al ricevitore.
Di questo si occupano i protocolli di trasmissione, in particolare quelli al secondo livello.
Questi rappresentano le regole che DTE, DCE e CPE devono seguire affinchè laa ricezione di dati avvenga correttamente.
Ci sono due principali categorie.

### Protocolli Asinctroni (o start/stop)

Pirma forma di protocolli per la trasmisione dati.
Permettono la trasmissione di caratteri singoli senza stabilire l'intervallo tra due caratteri successivi.
Deve comunque essere definito un bit time di durata.
Ogni char ha un bit di start, uno di partà e uno o due di stop.
Può avvenire un errore di framing in caso il bit di stop non corrisponda.
Tipico pacchetto
![alt text](images/xmodemAsync.png)

- all'inizio il ricevente invia un segnale di NAK ogni 10 secondi segnalando disponibilità
- il trasmettitore invia un pacchetto come quello sopra
  - ASCII 06H ack per ricezione corretta
  - ASCII NAK, ricezione sbagliata
- al termine il mittente invia ASCII 04H, EOT
- il ricevitore riconosce EOT con ACK

### Protocolli Sincroni

Non sono presenti bit di starto o stop, ma caratteri di sincronismo SYN nel particolare per protocolli orientati al carattere oppure sequenze di bit (flags) per protocolli orientati al bit.
La trama è composta da un numero di bit definiti dal protocollo.

#### BSC

BINARY SYNCRONOUS COMMUNICATIONS si divide in 3 tipi

- 1 => rete dedicata p2p
- 2 => rete commutata p2p
- 3 => rete multipunnto
  Usa i seguenti codici
- ASCII
- EBCDIC
- SBT
  Vi sono trame di controllo o informative.
  In caso di p2p il trasmettitore invia caratteri di sincronismo. I DTE possono essere sia trasmettitori che riceventi. In caso vi sia una contesa uno dei due diventa una stazione primaria che ripete l'invio mentre l'altro diventa secondaria.
  Il segnale di ricezione si risponde con ACK oppure NAK e si termina con EOT.

Nel caso di BSC3 multipunto viene fatta un'interrogazione ciclica per individuare il terminale a cui collegarsi.

#### HDLC

High Level Data Link Control, protocollo orientato ai bit per grandi reti.
E' un protocollo standar ISO per trasmissioni sincrone full duplex.
I formati sono fissi definiti in frames o trame.
Si può avere una connessione:

- bilanciata => tra dua stazioone paritetiche
- sbilanciata => una stazion primaria, più secondarie. Half Duplex con un master.
  Si ha in 3 modalità:
- NRM (Normal Response mode) => sbilanciarta half duplex
- ABM (Async Balanced Mode) => unica modalità prevista da LAPB (B channel). Bilanciata full duplex
- ARM (Async Response Mode) => simile a NRM ma limitata a due stazioni

![alt text](images/tramaHDLC.png)

- Flag => 8 bit, stabilisce la sincronizzazione, trasmesso continuamente in linea idle. Si fa bit stuffing.
- Indirizzo => 8 bit estendibile come LLC. Non india protocollo a livello di rete ma altre infor
- Controllo => campo 8 bit estendibile che identifica il tipo di trama.
- Campo informativo => contiene il pacchhetto dati fornito al livello OSI 3. Non esistono limiti per l'ampiezza di questo campo.
- FCSs => frame check sequence, di ridondanza, da almeno 16bit.

I principali valori del campo di controllo in HDLC sono:

- I-frame per dati + numeri di sequenza.
- S-frame per controllo, ack e richieste
- U-frame per setup, gestione link, comandi specialie

Non ho voglia per ora di segnarmi tutti i singoli valori del, campo, bastano queste info qui dai...

# Secondo Modulo

# PDF_1

## TCP/IP

### IP address

Su 32 bit identifica univocamente in rete uno specifico host della rete
Si divide in 2 parti, host e rete.
Ci sono 4 tipi di classi di IP address.

![alt text](images/classiIP.png)

#### Indirizzi riservati

![alt text](images/indirizziRiservati.png)

> !Gli indirizzi vengono assegnati alle intrfacce non agli host!

#### Sottoreti

Un IP addresso può essere localmente modificato usando parzialmente i bit relativi agli host come bit di indirizzo per sottoreti.
Si applica una subnet mask.

- se un bit su una subnet mask è a 1, l'equivalente indirizzo IP è interpretato come un network bit, cioè appartiene ad un indirizzo di rete
- se è a 0, il relativo bit fa parte di un indirizzo di host

![alt text](images/subnetMask.png)

![alt text](images/sottoretiS.png)

### Tabella di routing
I gateway instradano i dati tra diverse reti.
Gil host prendono decisioni di instradamento ne seguente modo:
  - se l'host di destinazione sta sulla rete locale viene mandato direttamente 
  - se l'host è remoto, i dati vengono mandati ad un gateay locale

L'analisi dell'indirizzo ip fatta dall'host
  - determina il tipo di classe
  - controlla la rete di destinazione
  - cerca la rete nella routing table
  - instrada i pacchetti di dati seguendo la tabella di routing

> netstat -nr fa vedere la tabella di routing

![alt text](images/routingTable.png)

![alt text](images/schemaRouting.png)

# PDF_2

# PDF_3

# PDF_4

# PDF_5

# PDF_6

# PDF_PARTE_FINALE
