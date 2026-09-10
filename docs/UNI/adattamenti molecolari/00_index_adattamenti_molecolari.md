---
title: indice
hide:
  - footer
---

# Indice

## Capitolo 1.1 — Membrane cellulari e organelli

```mermaid
graph LR
    classDef default fill:#f9f9f9,stroke:#333,stroke-width:1px,color:#000;
    
    %% NODO CENTRALE (Fucsia/Rosso Intenso)
    classDef root fill:#FF4757,stroke:#FF0000,stroke-width:3px,font-weight:bold,color:#fff;
    
    %% RAMO PROPRIETÀ (Giallo/Arancio -> Giallo Chiaro -> Giallo Chiarissimo)
    classDef propL1 fill:#FFA502,stroke:#FF7F50,stroke-width:2px,font-weight:bold,color:#000;
    classDef propL2 fill:#FFEAA7,stroke:#FDCB6E,stroke-width:1px,color:#000;

    %% RAMO NUCLEO (Viola -> Lilla -> Lilla Chiarissimo)
    classDef nucL1 fill:#9B5DE5,stroke:#6C5CE7,stroke-width:2px,font-weight:bold,color:#fff;
    classDef nucL2 fill:#E0C3FC,stroke:#B388FF,stroke-width:1px,color:#000;

    %% RAMO MITOCONDRI (Arancione Intenso -> Arancione Chiaro -> Arancione Chiarissimo)
    classDef mitL1 fill:#FF6B1A,stroke:#E65100,stroke-width:2px,font-weight:bold,color:#fff;
    classDef mitL2 fill:#FFCC80,stroke:#FFE0B2,stroke-width:1px,color:#000;

    %% RAMO RETICOLO/GOLGI (Azzurro/Blu -> Turchese -> Celeste Chiarissimo)
    classDef retL1 fill:#1E90FF,stroke:#0984E3,stroke-width:2px,font-weight:bold,color:#fff;
    classDef retL2 fill:#81ECEC,stroke:#00CEC9,stroke-width:1.5px,color:#000;
    classDef retL3 fill:#E0F7FA,stroke:#B2EBF2,stroke-width:1px,color:#000;

    %% RAMO ORGANELLI (Verde Smeraldo -> Verde Menta -> Verde Chiarissimo)
    classDef orgL1 fill:#2ED573,stroke:#26AF58,stroke-width:2px,font-weight:bold,color:#fff;
    classDef orgL2 fill:#55E6C1,stroke:#58B19F,stroke-width:1px,color:#000;

    %% RAMO TRASPORTO (Rosa Acceso -> Rosa Pastello -> Rosa Chiarissimo)
    classDef traL1 fill:#FF1493,stroke:#D81B60,stroke-width:2px,font-weight:bold,color:#fff;
    classDef traL2 fill:#FF85A2,stroke:#FFB7C5,stroke-width:1px,color:#000;

    MC((Membrane Cellulari)):::root

    %% Proprietà (Sfuma verso il giallo chiaro)
    MC --> Prop([Proprietà]):::propL1
    Prop --> P1([Doppio strato lipidico]):::propL2
    Prop --> P2([Contengono proteine]):::propL2
    Prop --> P3([Dividono in compartimenti]):::propL2

    %% Nucleo & Citosol (Sfuma verso il lilla)
    MC --> N([Nucleo]):::nucL1
    MC --> Cit([Citosol]):::nucL1
    Cit --> CitD([Reazioni metaboliche]):::nucL2

    %% Mitocondri (Sfuma verso l'arancione chiarissimo)
    MC --> Mit([Mitocondri]):::mitL1
    Mit --> Mit1([Metabolismo energetico]):::mitL2

    %% Reticolo ed Apparato di Golgi (Sfumatura a 3 livelli: Blu -> Turchese -> Celeste)
    MC --> RE([Reticolo Endoplasmatico]):::retL1
    RE --> RER([RER Ruvido]):::retL2
    RE --> REL([REL Liscio]):::retL2
    RER --> RER1([Sintesi Proteine]):::retL3
    REL --> REL1([Sintesi Lipidi]):::retL3
    
    MC --> G([Apparato di Golgi]):::retL1
    G --> G1([Modifica e smistamento]):::retL2

    %% Altri Organelli (Sfuma verso il verde menta chiaro)
    MC --> Org([Altri Organelli]):::orgL1
    Org --> O1([Lisosomi]):::orgL2
    Org --> O2([Perossisomi]):::orgL2
    Org --> O3([Endosomi]):::orgL2
    Org --> O4([Esosomi]):::orgL2

    %% Meccanismi di Trasporto (Sfuma verso il rosa chiarissimo)
    MC --> T([Trasporto Proteine]):::traL1
    T --> T1([Avviene negli organelli]):::traL2
    T --> T2([Meccanismi differenti]):::traL2
```

## Capitolo 1.2 — Il codice della vita: dal gene alla proteina

```mermaid
%%{init: {
  'theme': 'base',
  'themeVariables': {
    'fontSize': '15px',
    'fontFamily': 'arial'
  },
  'flowchart': {
    'nodeSpacing': 20,
    'rankSpacing': 35,
    'padding': 12
  }
}}%%
graph TD
    %% =========================================================================
    %% DEFINIZIONE STILI (Coerenza cromatica per ogni macro-fase biologica)
    %% =========================================================================
    classDef dna fill:#ff7675,stroke:#d63031,stroke-width:3px,font-weight:bold;
    classDef rna fill:#74b9ff,stroke:#0984e3,stroke-width:2px,font-weight:bold;
    classDef rnaL2 fill:#e0f2fe,stroke:#74b9ff,stroke-width:1.5px;
    
    classDef trad fill:#ffeaa7,stroke:#fdcb6e,stroke-width:2px,font-weight:bold;
    classDef tradL2 fill:#fff9db,stroke:#ffeaa7,stroke-width:1.5px;

    classDef prot fill:#a55edd,stroke:#8854d0,stroke-width:3px,font-weight:bold;
    classDef protL2 fill:#f3e8ff,stroke:#a55edd,stroke-width:1.5px;

    classDef deg fill:#ff7f50,stroke:#ff6348,stroke-width:2px,font-weight:bold;
    classDef degL2 fill:#ffeadb,stroke:#ff7f50,stroke-width:1.5px;

    classDef endG fill:#2ed573,stroke:#26af58,stroke-width:3px,font-weight:bold;

    %% =========================================================================
    %% FLUSSO CONTINUO DAL GENE ALLA DEGRADAZIONE
    %% =========================================================================

    A(["DNA: Gene"]):::dna
    
    %% Regolazione del Gene (Compattata in un unico blocco per non allargare)
    A --> B(["Regolazione dell'espressione<br/>• Promotori e Enhancer<br/>• Fattori di trascrizione"]):::dna

    %% Trascrizione
    A --> C(["Trascrizione: RNA Polimerasi II"]):::rna
    C --> D(["pre-mRNA"]):::rna

    %% Maturazione mRNA (Flusso standard e alternativo)
    D --> E(["Maturazione dell'mRNA"]):::rna
    E --> E_Std(["Modificazioni Co-trascrizionali:<br/>• 5' Cap<br/>• Splicing Standard<br/>• Coda Poli-A"]):::rnaL2
    E --> E_Alt(["Splicing Alternativo:<br/>Seleziona combinazioni<br/>diverse di esoni"]):::rnaL2

    E_Std --> F(["mRNA Maturo"]):::rna
    E_Alt --> F_Alt(["mRNA Maturo Alternativo"]):::rna

    %% Traduzione
    F --> G(["Traduzione"]):::trad
    F_Alt --> G

    G --> G_Comp(["Requisiti:<br/>• Ribosomi e tRNA con Amminoacidi<br/>• Energia: ATP e GTP<br/>• Fattori proteici"]):::tradL2
    
    G --> G_Cod(["Codice Genetico:<br/>• Codoni a triplette<br/>• Start: AUG<br/>• Stop: UAA, UAG, UGA"]):::tradL2

    G --> G_Fasi(["Fasi della Traduzione:<br/>Iniziazione → Allungamento → Terminazione"]):::tradL2

    %% Proteina
    G_Fasi --> H(["Proteina"]):::prot
    
    %% Modificazioni Post-Traduzionali
    H --> I(["Modificazioni post-traduzionali:<br/>• Fosforilazione e Glicosilazione<br/>• Acetilazione e Metilazione<br/>• Ubiquitinazione"]):::protL2

    %% Destino Finale: Degradazione
    H --> J(["Degradazione Proteica"]):::deg

    %% Perché e Come (Ispirato al tuo schema perfetto)
    J --> J_Perche(["Perché?<br/>• Riciclo amminoacidi<br/>• Eliminazione proteine danneggiate<br/>• Regolazione funzione"]):::degL2
    
    J --> J_Come(["Come?"]):::deg
    
    J_Come --> K(["Via Lisosomiale"]):::degL2
    J_Come --> L(["Via Proteasomiale"]):::prot

    %% Sotto-flusso 1: Lisosoma
    K --> K1(["Proteine a lunga emivita"]):::degL2
    K1 --> O(["Amminoacidi"]):::endG

    %% Sotto-flusso 2: Proteasoma (La cascata lineare e corretta)
    L --> L1(["Ubiquitinazione:<br/>E1 → E2 → E3"]):::protL2
    L1 --> L2(["Poliubiquitinazione"]):::protL2
    L2 --> M(["Proteasoma 26S"]):::prot
    M --> M1(["19S: Riconoscimento e unfolding"]):::protL2
    M1 --> M2(["20S: Degradazione"]):::protL2
    M2 --> N(["Peptidi"]):::protL2
    N --> O
```

## Capitolo 1.3 — Cell Signaling

```mermaid
%%{init: {
  'theme': 'base',
  'themeVariables': {
    'fontSize': '16px',
    'fontFamily': 'arial'
  },
  'flowchart': {
    'nodeSpacing': 25,
    'rankSpacing': 35,
    'padding': 15
  }
}}%%
graph LR
    %% =========================================================================
    %% DEFINIZIONE STILI (Sfumature coerenti, bordi e testi ad alto contrasto)
    %% =========================================================================
    classDef root fill:#ff7675,stroke:#d63031,stroke-width:3px,font-weight:bold;
    
    classDef endo fill:#ffeaa7,stroke:#fdcb6e,stroke-width:2px,font-weight:bold;
    classDef endoL2 fill:#fff9db,stroke:#ffeaa7,stroke-width:1.5px;

    classDef para fill:#74b9ff,stroke:#0984e3,stroke-width:2px,font-weight:bold;
    classDef paraL2 fill:#e0f2fe,stroke:#74b9ff,stroke-width:1.5px;

    classDef auto fill:#ff7f50,stroke:#ff6348,stroke-width:2px,font-weight:bold;
    classDef autoL2 fill:#ffeadb,stroke:#ff7f50,stroke-width:1.5px;

    classDef neuro fill:#a55edd,stroke:#8854d0,stroke-width:2px,font-weight:bold;
    classDef neuroL2 fill:#f3e8ff,stroke:#a55edd,stroke-width:1.5px;

    classDef cont fill:#2ed573,stroke:#26af58,stroke-width:2px,font-weight:bold;
    classDef contL2 fill:#e3fcef,stroke:#a3e9c9,stroke-width:1.5px;

    %% =========================================================================
    %% STRUTTURA LINEARE E GEOMETRICAMENTE ORDINATA
    %% =========================================================================

    A(["Comunicazione Cellulare"]):::root

    %% BIVIO DELLE MODALITÀ
    A --> B(["Endocrina"]):::endo
    A --> C(["Paracrina"]):::para
    A --> D(["Autocrina"]):::auto
    A --> E(["Neuronale"]):::neuro
    A --> F(["Contatto-dipendente"]):::cont

    %% RAMO ENDOCRINA (Giallo)
    B --> B1(["Portata: Lungo raggio"]):::endoL2
    B1 --> B2(["Meccanismo: Ormoni secreti nel flusso<br/>sanguigno per raggiungere cellule target distanti"]):::endoL2

    %% RAMO PARACRINA (Azzurro)
    C --> C1(["Portata: Corto raggio"]):::paraL2
    C1 --> C2(["Meccanismo: Mediatori locali rilasciati<br/>nello spazio extracellulare verso cellule limitrofe"]):::paraL2

    %% RAMO AUTOCRINA (Arancione)
    D --> D1(["Portata: Corto raggio"]):::autoL2
    D1 --> D2(["Meccanismo: La cellula segnalante<br/>risponde essa stessa al segnale inviato"]):::autoL2

    %% RAMO NEURONALE (Viola)
    E --> E1(["Portata: Lungo / Corto raggio"]):::neuroL2
    E1 --> E2(["Meccanismo: Messaggi elettrici convertiti in<br/>segnali chimici (neurotrasmettitori) nelle sinapsi"]):::neuroL2

    %% RAMO CONTATTO-DIPENDENTE (Verde)
    F --> F1(["Portata: Corto raggio"]):::contL2
    F1 --> F2(["Meccanismo: Richiede il contatto fisico tra<br/>molecole legate alla membrana delle due cellule"]):::contL2
```

```mermaid
%%{init: {
  'theme': 'base',
  'themeVariables': {
    'fontSize': '16px',
    'fontFamily': 'arial'
  },
  'flowchart': {
    'nodeSpacing': 12,
    'rankSpacing': 35,
    'padding': 15
  }
}}%%
graph LR
    %% =========================================================================
    %% DEFINIZIONE STILI (Coerenza cromatica con i rami precedenti)
    %% =========================================================================
    classDef root fill:#ff7675,stroke:#d63031,stroke-width:3px,font-weight:bold;
    
    classDef ion fill:#74b9ff,stroke:#0984e3,stroke-width:2px,font-weight:bold;
    classDef ionL2 fill:#e0f2fe,stroke:#74b9ff,stroke-width:1.5px;

    classDef gpc fill:#a55edd,stroke:#8854d0,stroke-width:2px,font-weight:bold;
    classDef gpcL2 fill:#f3e8ff,stroke:#a55edd,stroke-width:1.5px;

    classDef rtk fill:#2ed573,stroke:#26af58,stroke-width:2px,font-weight:bold;
    classDef rtkL2 fill:#e3fcef,stroke:#a3e9c9,stroke-width:1.5px;

    classDef intra fill:#ff7f50,stroke:#ff6348,stroke-width:2px,font-weight:bold;
    classDef intraL2 fill:#ffeadb,stroke:#ff7f50,stroke-width:1.5px;

    %% =========================================================================
    %% STRUTTURA AD ALBERO ASCIUTTA (SOLO PAROLE CHIAVE)
    %% =========================================================================
    
    ROOT(["Recettori Cellulari"]):::root

    %% -------------------------------------------------------------------------
    %% RAMO 1: CANALI IONICI (Azzurro)
    %% -------------------------------------------------------------------------
    ROOT --> ION(["Canali Ionici"]):::ion
    ION --> ION1(["Chimico → Elettrico"]):::ionL2
    ION --> ION2(["Flusso ioni gradiente:<br/>Na+, K+, Ca2+, Cl-"]):::ionL2
    ION --> ION3(["Contrazione muscolare"]):::ionL2

    %% -------------------------------------------------------------------------
    %% RAMO 2: GPCR (Viola)
    %% -------------------------------------------------------------------------
    ROOT --> GPCR(["GPCR"]):::gpc
    GPCR --> GPCR1(["Subunità α, β, γ"]):::gpcL2
    GPCR --> GPCR2(["Via cAMP → PKA"]):::gpcL2
    GPCR2 --> GPCR3(["Amplificazione:<br/>Adrenalina 10^8 Glucosio"]):::gpcL2

    %% -------------------------------------------------------------------------
    %% RAMO 3: RTK / ENZIMI (Verde)
    %% -------------------------------------------------------------------------
    ROOT --> RTK(["RTK / Enzimi"]):::rtk
    RTK --> RTK1(["Dimerizzazione"]):::rtkL2
    RTK --> RTK2(["Autofosforilazione"]):::rtkL2
    RTK2 --> RTK3(["Siti SH2 / PTB"]):::rtkL2

    %% -------------------------------------------------------------------------
    %% RAMO 4: RECETTORI INTRACELLULARI (Arancione)
    %% -------------------------------------------------------------------------
    ROOT --> INTRA(["Intracellulari"]):::intra
    INTRA --> IN1(["Ormoni steroidei / tiroidei"]):::intraL2
    INTRA --> IN2(["Diffusione membrana"]):::intraL2
    IN2 --> IN3(["Complesso + DNA (HRE)"]):::intraL2
    IN3 --> IN4(["Trascrizione genica"]):::intra
```

## Capitolo 2 — Omeostasi durante l'esercizio fisico

```mermaid
%%{init: {
  'theme': 'base',
  'themeVariables': { 'fontSize': '15px', 'fontFamily': 'arial' },
  'flowchart': { 'nodeSpacing': 25, 'rankSpacing': 32, 'padding': 12 }
}}%%
graph LR
    classDef root fill:#ff7675,stroke:#d63031,stroke-width:3px,font-weight:bold;

    classDef ventL1 fill:#74b9ff,stroke:#0984e3,stroke-width:2px,font-weight:bold;
    classDef ventL2 fill:#e0f2fe,stroke:#74b9ff,stroke-width:1.5px;

    classDef cardL1 fill:#a55edd,stroke:#8854d0,stroke-width:2px,font-weight:bold;
    classDef cardL2 fill:#f3e8ff,stroke:#a55edd,stroke-width:1.5px;

    classDef paL1 fill:#ff7f50,stroke:#ff6348,stroke-width:2px,font-weight:bold;
    classDef paL2 fill:#ffeaa7,stroke:#fdcb6e,stroke-width:1.5px;

    classDef flussoL1 fill:#2ed573,stroke:#26af58,stroke-width:2px,font-weight:bold;
    classDef flussoL2 fill:#e3fcef,stroke:#a3e9c9,stroke-width:1.5px;

    classDef ridL1 fill:#ff6b81,stroke:#ff4757,stroke-width:2px,font-weight:bold;
    classDef ridL2 fill:#ffe4e6,stroke:#ff85a2,stroke-width:1.5px;

    Ex((Omeostasi durante<br/>l'esercizio fisico)):::root

    Ex --> Vent([Ventilazione]):::ventL1
    Vent --> V1([Chemocettori carotidei/aortici<br/>rilevano PO2, PCO2, pH]):::ventL2
    Vent --> V2([Via afferente/efferente:<br/>nervo frenico, intercostali]):::ventL2

    Ex --> Card([Cardiac output]):::cardL1
    Card --> C1([Comando centrale + EPR<br/>+ barocettori]):::cardL2
    Card --> C2([↑Simpatico, ↓Parasimpatico<br/>→ ↑HR, ↑SV]):::cardL2

    Ex --> PA([Pressione arteriosa]):::paL1
    PA --> P1([Barocettori si riadattano<br/>a livelli più alti]):::paL2
    PA --> P2([Inibizione GABAergica<br/>a livello dell'NTS]):::paL2

    Ex --> Flusso([Flusso sanguigno muscolare]):::flussoL1
    Flusso --> F1([Vasodilatazione locale:<br/>asse ACh-NO, ATP/adenosina]):::flussoL2
    Flusso --> F2([Simpatolisi funzionale<br/>nel muscolo attivo]):::flussoL2
    Flusso --> F3([Vasocostrizione simpatica<br/>nei distretti non attivi]):::flussoL2

    Ex --> Rid([Ridondanza ed eterogeneità]):::ridL1
    Rid --> R1([Meccanismi multipli<br/>e sovrapposti]):::ridL2
    Rid --> R2([Risposta dipende da massa,<br/>durata, intensità, tipo di esercizio]):::ridL2
```

## Capitolo 3 — Risposta mitocondriale all'esercizio di endurance

```mermaid
%%{init: {
  'theme': 'base',
  'themeVariables': { 'fontSize': '14px', 'fontFamily': 'arial' },
  'flowchart': { 'nodeSpacing': 22, 'rankSpacing': 30, 'padding': 10 }
}}%%
graph LR
    classDef root fill:#ff7675,stroke:#d63031,stroke-width:3px,font-weight:bold;

    classDef p1L1 fill:#74b9ff,stroke:#0984e3,stroke-width:2px,font-weight:bold;
    classDef p1L2 fill:#e0f2fe,stroke:#74b9ff,stroke-width:1.5px;

    classDef p2L1 fill:#a55edd,stroke:#8854d0,stroke-width:2px,font-weight:bold;
    classDef p2L2 fill:#f3e8ff,stroke:#a55edd,stroke-width:1.5px;

    classDef p3L1 fill:#2ed573,stroke:#26af58,stroke-width:2px,font-weight:bold;
    classDef p3L2 fill:#e3fcef,stroke:#a3e9c9,stroke-width:1.5px;

    classDef p4L1 fill:#ff6b81,stroke:#ff4757,stroke-width:2px,font-weight:bold;
    classDef p4L2 fill:#ffe4e6,stroke:#ff85a2,stroke-width:1.5px;

    Cap((Allenamento e<br/>biogenesi<br/>mitocondriale)):::root

    Cap --> P1([Parte 1: Metabolismo<br/>energetico acuto]):::p1L1
    P1 --> P1a([3 vie ATP:<br/>aerobica, PCr, lattacida]):::p1L2
    P1 --> P1b([Endurance → ↑proteine<br/>mitocondriali, Holloszy]):::p1L2

    Cap --> P2([Parte 2: Regolazione<br/>molecolare]):::p2L1
    P2 --> P2a([TFAM, asse<br/>PGC-1/NRF]):::p2L2
    P2 --> P2b([Sensori: AMPK,<br/>Ca2+, p53]):::p2L2

    Cap --> P3([Parte 3: Substrati<br/>e fibre]):::p3L1
    P3 --> P3a([Ossidazione FA:<br/>trasportatori, PPAR]):::p3L2
    P3 --> P3b([Glucosio: GLUT4,<br/>NURR1, Mediator]):::p3L2

    Cap --> P4([Parte 4: Mimetici<br/>e doping]):::p4L1
    P4 --> P4a([AICAR: mima AMPK]):::p4L2
    P4 --> P4b([GW501516: agonista<br/>PPARδ]):::p4L2
```

## Capitolo 4 — Risposta ipertrofica all'esercizio

```mermaid
%%{init: {
  'theme': 'base',
  'themeVariables': { 'fontSize': '14px', 'fontFamily': 'arial' },
  'flowchart': { 'nodeSpacing': 22, 'rankSpacing': 30, 'padding': 10 }
}}%%
graph LR
    classDef root fill:#ff7675,stroke:#d63031,stroke-width:3px,font-weight:bold;

    classDef p1L1 fill:#74b9ff,stroke:#0984e3,stroke-width:2px,font-weight:bold;
    classDef p1L2 fill:#e0f2fe,stroke:#74b9ff,stroke-width:1.5px;

    classDef p2L1 fill:#a55edd,stroke:#8854d0,stroke-width:2px,font-weight:bold;
    classDef p2L2 fill:#f3e8ff,stroke:#a55edd,stroke-width:1.5px;

    classDef p3L1 fill:#2ed573,stroke:#26af58,stroke-width:2px,font-weight:bold;
    classDef p3L2 fill:#e3fcef,stroke:#a3e9c9,stroke-width:1.5px;

    Cap((Ipertrofia<br/>muscolare)):::root

    Cap --> P1([Parte 1: Equilibrio<br/>e miochine]):::p1L1
    P1 --> P1a([Bilancia anabolismo<br/>vs catabolismo]):::p1L2
    P1 --> P1b([IGF-1 vs Miostatina:<br/>effetti sinergici]):::p1L2

    Cap --> P2([Parte 2: Segnalazione<br/>e mTOR]):::p2L1
    P2 --> P2a([AKT-mTOR →<br/>biogenesi ribosomiale]):::p2L2
    P2 --> P2b([Contrazione blocca<br/>la traduzione; atrofia]):::p2L2

    Cap --> P3([Parte 3: Meccanotrasduzione<br/>e cellule satellite]):::p3L1
    P3 --> P3a([Dominio mionucleare:<br/>soffitto e cellule satellite]):::p3L2
    P3 --> P3b([Doping e<br/>allenamento concorrente]):::p3L2
```

## Capitolo 5 — Ipossia: adattamenti fisiologici e sistema respiratorio

```mermaid
%%{init: {
  'theme': 'base',
  'themeVariables': { 'fontSize': '15px', 'fontFamily': 'arial' },
  'flowchart': { 'nodeSpacing': 25, 'rankSpacing': 32, 'padding': 12 }
}}%%
graph LR
    classDef root fill:#ff7675,stroke:#d63031,stroke-width:3px,font-weight:bold;

    classDef allL1 fill:#74b9ff,stroke:#0984e3,stroke-width:2px,font-weight:bold;
    classDef allL2 fill:#e0f2fe,stroke:#74b9ff,stroke-width:1.5px;

    classDef hifL1 fill:#a55edd,stroke:#8854d0,stroke-width:2px,font-weight:bold;
    classDef hifL2 fill:#f3e8ff,stroke:#a55edd,stroke-width:1.5px;

    classDef respL1 fill:#ff7f50,stroke:#ff6348,stroke-width:2px,font-weight:bold;
    classDef respL2 fill:#ffeaa7,stroke:#fdcb6e,stroke-width:1.5px;

    classDef trasL1 fill:#2ed573,stroke:#26af58,stroke-width:2px,font-weight:bold;
    classDef trasL2 fill:#e3fcef,stroke:#a3e9c9,stroke-width:1.5px;

    Ip((Ipossia)):::root

    Ip --> All([Allenamento in ipossia]):::allL1
    All --> AllStrat([LHTH, LHTL,<br/>intermittente, ipoventilazione]):::allL2
    All --> AllAda([Adattamenti cardio-respiratori<br/>e muscolari]):::allL2

    Ip --> Hif([HIF]):::hifL1
    Hif --> HifEpo([Trascrizione EPO]):::hifL2
    Hif --> HifGlic([Metabolismo glicolitico,<br/>angiogenesi]):::hifL2

    Ip --> Resp([Meccanica respiratoria]):::respL1
    Resp --> RespInsp([Inspirazione: pressione<br/>negativa]):::respL2
    Resp --> RespControllo([Controllo bulbo-pontino,<br/>chemocettori CO2/O2]):::respL2

    Ip --> Tras([Trasporto dei gas]):::trasL1
    Tras --> TrasO2([O2: curva sigmoide<br/>emoglobina, BPG, pH]):::trasL2
    Tras --> TrasCo2([CO2: 65% come<br/>bicarbonato]):::trasL2
```

## Capitolo 6 — Esercizio fisico e cervello: BDNF

```mermaid
%%{init: {
  'theme': 'base',
  'themeVariables': { 'fontSize': '15px', 'fontFamily': 'arial' },
  'flowchart': { 'nodeSpacing': 25, 'rankSpacing': 32, 'padding': 12 }
}}%%
graph LR
    classDef root fill:#ff7675,stroke:#d63031,stroke-width:3px,font-weight:bold;

    classDef bdnfL1 fill:#74b9ff,stroke:#0984e3,stroke-width:2px,font-weight:bold;
    classDef bdnfL2 fill:#e0f2fe,stroke:#74b9ff,stroke-width:1.5px;

    classDef mioL1 fill:#a55edd,stroke:#8854d0,stroke-width:2px,font-weight:bold;
    classDef mioL2 fill:#f3e8ff,stroke:#a55edd,stroke-width:1.5px;

    classDef indL1 fill:#ff7f50,stroke:#ff6348,stroke-width:2px,font-weight:bold;
    classDef indL2 fill:#ffeaa7,stroke:#fdcb6e,stroke-width:1.5px;

    Es((Esercizio fisico<br/>e cervello)):::root

    Es --> Bdnf([BDNF]):::bdnfL1
    Bdnf --> BdnfMuscolo([Prodotto anche nel<br/>muscolo: attiva AMPK]):::bdnfL2
    Bdnf --> BdnfCervello([Nel cervello: TrkB →<br/>PI3K/Akt, MAPK, PLC-γ]):::bdnfL2

    Es --> Mio([Miochine che<br/>inducono BDNF]):::mioL1
    Mio --> MioCat([Catepsina B]):::mioL2
    Mio --> MioIri([Irisina: PGC-1α→FNDC5]):::mioL2
    Mio --> MioIl6([IL-6: sensibilità<br/>insulinica, appetito]):::mioL2
    Mio --> MioBohb([β-idrossibutirrato]):::mioL2

    Es --> Ind([Vie indirette]):::indL1
    Ind --> IndKyn([Chinurenina → KYNA<br/>via PGC-1α]):::indL2
    Ind --> IndOrg([Tessuto adiposo<br/>e fegato]):::indL2
```

## Capitolo 7 — Ipossia molecolare: HIF-1α

```mermaid
%%{init: {
  'theme': 'base',
  'themeVariables': { 'fontSize': '15px', 'fontFamily': 'arial' },
  'flowchart': { 'nodeSpacing': 25, 'rankSpacing': 32, 'padding': 12 }
}}%%
graph LR
    classDef root fill:#ff7675,stroke:#d63031,stroke-width:3px,font-weight:bold;

    classDef rosL1 fill:#74b9ff,stroke:#0984e3,stroke-width:2px,font-weight:bold;
    classDef rosL2 fill:#e0f2fe,stroke:#74b9ff,stroke-width:1.5px;

    classDef hifL1 fill:#a55edd,stroke:#8854d0,stroke-width:2px,font-weight:bold;
    classDef hifL2 fill:#f3e8ff,stroke:#a55edd,stroke-width:1.5px;

    classDef metL1 fill:#ff7f50,stroke:#ff6348,stroke-width:2px,font-weight:bold;
    classDef metL2 fill:#ffeaa7,stroke:#fdcb6e,stroke-width:1.5px;

    classDef protL1 fill:#2ed573,stroke:#26af58,stroke-width:2px,font-weight:bold;
    classDef protL2 fill:#e3fcef,stroke:#a3e9c9,stroke-width:1.5px;

    Ip((Ipossia<br/>molecolare)):::root

    Ip --> Ros([O2 e ROS]):::rosL1
    Ros --> RosMod([Ipossia moderata:<br/>↑ROS transitorio]):::rosL2
    Ros --> RosGrave([Ipossia grave:<br/>↓ROS, risparmio energetico]):::rosL2

    Ip --> Hif([HIF-1α]):::hifL1
    Hif --> HifNorm([Normossia: PHD/pVHL<br/>degradano HIF-1α]):::hifL2
    Hif --> HifIpo([Ipossia: HIF-1α stabile<br/>→ trascrizione via HRE]):::hifL2

    Ip --> Met([Riprogrammazione<br/>metabolica]):::metL1
    Met --> MetGlic([↑Glicolisi, ↓Krebs<br/>via PDK1]):::metL2
    Met --> MetMito([Mitofagia,<br/>↓ROS mitocondriali]):::metL2

    Ip --> Prot([Proteostasi]):::protL1
    Prot --> ProtUpr([UPR: PERK,<br/>IRE1, ATF6]):::protL2
    Prot --> ProtMtor([Inibizione mTOR]):::protL2
```

## Capitolo 8 — Ipossia e attività fisica nel muscolo scheletrico

```mermaid
%%{init: {
  'theme': 'base',
  'themeVariables': { 'fontSize': '15px', 'fontFamily': 'arial' },
  'flowchart': { 'nodeSpacing': 25, 'rankSpacing': 32, 'padding': 12 }
}}%%
graph LR
    classDef root fill:#ff7675,stroke:#d63031,stroke-width:3px,font-weight:bold;

    classDef acuL1 fill:#74b9ff,stroke:#0984e3,stroke-width:2px,font-weight:bold;
    classDef acuL2 fill:#e0f2fe,stroke:#74b9ff,stroke-width:1.5px;

    classDef croL1 fill:#a55edd,stroke:#8854d0,stroke-width:2px,font-weight:bold;
    classDef croL2 fill:#f3e8ff,stroke:#a55edd,stroke-width:1.5px;

    classDef fibL1 fill:#ff7f50,stroke:#ff6348,stroke-width:2px,font-weight:bold;
    classDef fibL2 fill:#ffeaa7,stroke:#fdcb6e,stroke-width:1.5px;

    classDef regL1 fill:#2ed573,stroke:#26af58,stroke-width:2px,font-weight:bold;
    classDef regL2 fill:#e3fcef,stroke:#a3e9c9,stroke-width:1.5px;

    Ip((Ipossia e<br/>attività fisica)):::root

    Ip --> Acu([Ipossia acuta/esercizio]):::acuL1
    Acu --> AcuHif([HIF-1α transitorio<br/>→ VEGF, glicolisi]):::acuL2
    Acu --> AcuAll([Allenamento →<br/>↑PHD/FIH, risposta attenuata]):::acuL2

    Ip --> Cro([Ipossia cronica]):::croL1
    Cro --> CroAtro([↓Akt/mTOR, ↑miostatina<br/>→ atrofia]):::croL2
    Cro --> CroFibra([Rimodellamento tipo<br/>di fibra: dipende dal contesto]):::croL2

    Ip --> Reg([Lesione e rigenerazione]):::regL1
    Reg --> RegHif([HIF-1α/VEGF transitorio<br/>→ pro-rigenerativo]):::regL2
    Reg --> RegHif2([HIF-2α: staminalità<br/>cellule satellite]):::regL2

    Ip --> Fib([Fibrosi]):::fibL1
    Fib --> FibCronico([HIF persistente + TGFβ/SMAD<br/>→ CTGF/CCN2 → ECM]):::fibL2
```

## Capitolo 9 — Adattamento sistemico all'alta quota

```mermaid
%%{init: {
  'theme': 'base',
  'themeVariables': { 'fontSize': '15px', 'fontFamily': 'arial' },
  'flowchart': { 'nodeSpacing': 25, 'rankSpacing': 32, 'padding': 12 }
}}%%
graph LR
    classDef root fill:#ff7675,stroke:#d63031,stroke-width:3px,font-weight:bold;

    classDef fisL1 fill:#74b9ff,stroke:#0984e3,stroke-width:2px,font-weight:bold;
    classDef fisL2 fill:#e0f2fe,stroke:#74b9ff,stroke-width:1.5px;

    classDef patL1 fill:#a55edd,stroke:#8854d0,stroke-width:2px,font-weight:bold;
    classDef patL2 fill:#f3e8ff,stroke:#a55edd,stroke-width:1.5px;

    classDef popL1 fill:#ff7f50,stroke:#ff6348,stroke-width:2px,font-weight:bold;
    classDef popL2 fill:#ffeaa7,stroke:#fdcb6e,stroke-width:1.5px;

    classDef genL1 fill:#2ed573,stroke:#26af58,stroke-width:2px,font-weight:bold;
    classDef genL2 fill:#e3fcef,stroke:#a3e9c9,stroke-width:1.5px;

    Alt((Adattamento<br/>sistemico<br/>all'alta quota)):::root

    Alt --> Fis([Risposte acute]):::fisL1
    Fis --> FisVent([↑Ventilazione,<br/>alcalosi respiratoria]):::fisL2
    Fis --> FisCard([↑Gittata cardiaca,<br/>vasocostrizione polmonare]):::fisL2
    Fis --> FisSangue([Emoconcentrazione<br/>→ EPO → eritrocitosi]):::fisL2

    Alt --> Pat([Patologie da<br/>acclimatazione insufficiente]):::patL1
    Pat --> PatAms([AMS: mal di testa,<br/>nausea]):::patL2
    Pat --> PatHape([HAPE: edema<br/>polmonare]):::patL2
    Pat --> PatHace([HACE: edema<br/>cerebrale, fatale]):::patL2

    Alt --> Pop([Popolazioni<br/>di alta quota]):::popL1
    Pop --> PopAndini([Andini: ↑↑Hb]):::popL2
    Pop --> PopTibet([Tibetani: ↑NO,<br/>↑ventilazione, ↓Hb]):::popL2
    Pop --> PopEtio([Etiopi: Hb<br/>quasi normale]):::popL2

    Alt --> Gen([Basi genetiche<br/>via HIF]):::genL1
    Gen --> GenEpas([EPAS1/HIF-2α]):::genL2
    Gen --> GenEgln([EGLN1/PHD2]):::genL2
    Gen --> GenPpar([PPARA/PPARα]):::genL2
```