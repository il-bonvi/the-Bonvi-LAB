# Sezione 11 — Algoritmi decisionali

*Le flow chart di questa sezione sintetizzano i ragionamenti sviluppati nelle Sezioni 2-9 e non sostituiscono la lettura dei capitoli dedicati, richiamati in ciascun algoritmo. Sono strumenti di supporto rapido alla decisione, non protocolli diagnostici autosufficienti.*

---

### Ferritina bassa: cosa controllare?

#### Ragionamento alla base dell'algoritmo

Una ferritina bassa isolata richiede sempre di essere contestualizzata con lo stato infiammatorio (PCR) e con gli altri indicatori del quadro marziale, prima di essere considerata conclusiva. Vedi [[sezione-3-biomarcatori-metabolismo-del-ferro]] per il dettaglio completo.

```mermaid
flowchart TD
    A[Ferritina bassa] --> B{PCR normale?}
    B -- No, PCR elevata --> C[Ripetere ferritina dopo risoluzione infiammazione, considerare sTfR se disponibile]
    B -- Si, PCR normale --> D{TSAT ridotto e MCV ai limiti bassi?}
    D -- Si --> E[Quadro coerente di sideropenia: valutare supplementazione e indagare causa - dieta, perdite ematiche]
    D -- No --> F[Sideropenia iniziale isolata: monitorare trend, valutare dieta e fattori di rischio]
    E --> G[Ricontrollo dopo alcune settimane di intervento]
    F --> G
```

---

### PCR alta: come interpretare la ferritina?

#### Ragionamento alla base dell'algoritmo

La PCR elevata è il primo elemento da valutare prima di interpretare una ferritina normale o elevata, poiché la ferritina è una proteina di fase acuta positiva. Vedi [[sezione-4-biomarcatori-infiammazione-e-danno-muscolare]] e [[sezione-3-biomarcatori-metabolismo-del-ferro]].

```mermaid
flowchart TD
    A[PCR elevata] --> B{Coerente con timing di esercizio recente 24-72h?}
    B -- Si --> C[Verosimile risposta infiammatoria attesa da esercizio, non richiede azione se asintomatico]
    B -- No --> D{Sintomi clinici presenti?}
    D -- Si --> E[Valutazione medica: possibile infezione o altra causa infiammatoria]
    D -- No --> F[Ripetere PCR a distanza, valutare pattern cronico di carico/recupero]
    C --> G{Ferritina concomitante normale o elevata?}
    F --> G
    G -- Si --> H[Non escludere sideropenia mascherata: considerare TSAT e sTfR]
    G -- No, ferritina bassa --> I[Sideropenia probabile anche in presenza di infiammazione]
```

---

### CK elevata: danno muscolare atteso o problema?

#### Ragionamento alla base dell'algoritmo

L'elemento chiave è sempre il confronto con il baseline individuale e la coerenza con il tipo di allenamento svolto nelle 24-72 ore precedenti. Vedi [[sezione-4-biomarcatori-infiammazione-e-danno-muscolare]].

```mermaid
flowchart TD
    A[CK elevata] --> B{Coerente con carico eccentrico recente e baseline individuale?}
    B -- Si --> C{Atleta sintomatico? Dolore severo, urine scure, calo prestativo marcato?}
    C -- No --> D[Risposta attesa: monitorare normalizzazione nei giorni successivi]
    C -- Si --> E[Valutare rischio rabdomiolisi: funzione renale, idratazione, valutazione medica]
    B -- No, non giustificata dal carico --> F{Trend in aumento su piu controlli successivi?}
    F -- Si --> G[Possibile carico eccessivo rispetto al recupero: rivedere programmazione]
    F -- No, isolato --> H[Monitorare, verificare eventuali fattori confondenti pre-analitici]
```

---

### Hb bassa: quali passi successivi?

#### Ragionamento alla base dell'algoritmo

La distinzione principale è tra pseudo-anemia da espansione volemica (adattamento atteso nell'endurance) e anemia vera, da caratterizzare poi per tipo (rigenerativa vs non rigenerativa, microcitica vs normo/macrocitica). Vedi [[sezione-2-biomarcatori-emocromo]] e [[sezione-3-biomarcatori-metabolismo-del-ferro]].

```mermaid
flowchart TD
    A[Hb bassa] --> B{Atleta di endurance asintomatico con MCV normale?}
    B -- Si --> C{Ferritina e TSAT normali?}
    C -- Si --> D[Verosimile pseudo-anemia da espansione volemica: nessuna azione, confrontare con baseline]
    C -- No --> E[Sideropenia sovrapposta a possibile pseudo-anemia: gestire come sideropenia]
    B -- No --> F{MCV ridotto?}
    F -- Si --> G[Verosimile anemia sideropenica: pannello marziale completo e ricerca della causa]
    F -- No --> H{Reticolociti elevati?}
    H -- Si --> I[Anemia rigenerativa: valutare emolisi o sanguinamento acuto]
    H -- No --> J[Anemia non rigenerativa: valutare B12/folati, infiammazione cronica, altre cause midollari]
```

---

### Atleta pronto per l'altura?

#### Ragionamento alla base dell'algoritmo

Prima di un blocco di allenamento in altitudine, lo stato marziale e infiammatorio dell'atleta condiziona l'efficacia dell'adattamento eritropoietico atteso. Vedi [[sezione-8-preparazione-e-risposta-all-altura]] per il dettaglio completo.

```mermaid
flowchart TD
    A[Screening pre-altura 4-6 settimane prima] --> B{Ferritina superiore alla soglia target e PCR normale?}
    B -- Si --> C[Procedere con la partenza come da programma]
    B -- No, ferritina insufficiente --> D[Avviare supplementazione marziale mirata]
    B -- No, PCR elevata --> E[Ripetere pannello dopo risoluzione dello stato infiammatorio]
    D --> F[Ricontrollo pannello marziale prima della partenza]
    E --> F
    F --> G{Ferritina ora adeguata?}
    G -- Si --> C
    G -- No --> H[Valutare con staff medico se rimandare o ridurre intensita del blocco di quota]
```

---

### Come usare questi algoritmi nella pratica

- Ogni algoritmo è un punto di partenza per orientare il ragionamento, non un sostituto della valutazione clinica completa né della consultazione con il medico dello sport nei casi dubbi o sintomatici.
- Il criterio del trend nel tempo e della coerenza tra parametri, discusso in [[sezione-1-fondamenti-di-interpretazione]], resta sempre prioritario rispetto alla lettura isolata di un singolo nodo decisionale.
- La presenza di sintomi clinici significativi deve sempre portare a una valutazione medica, indipendentemente dal percorso indicato dall'algoritmo.

---

*Prosegui con [[sezione-12-casi-pratici-emocromo-e-metabolismo-del-ferro]] per i casi pratici commentati, che applicano questi algoritmi a scenari realistici.*
