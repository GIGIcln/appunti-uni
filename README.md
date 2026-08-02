# 📚 Appunti universitari — Scienze motorie, curriculum calcio

Dispense LaTeX scritte a partire dalle lezioni del corso di laurea, pubblicate qui in
versione **leggibile** (il PDF compilato) e **modificabile** (i sorgenti `.tex`).

Lo stile è volutamente **schematico**: definizioni con i due punti, liste annidate,
niente prosa lunga e niente immagini — tutto il contenuto della lezione, in forma
telegrafica e ripassabile.

[![Licenza: CC BY-NC-SA 4.0](https://img.shields.io/badge/Licenza-CC%20BY--NC--SA%204.0-lightgrey.svg)](LICENSE)

---

## 📖 Dispense disponibili

| Materia | Anno | Pagine | Capitoli | | |
|---|:--:|:--:|:--:|:--:|:--:|
| **Anatomia umana** *(curriculum calcio)* | 1 | 152 | 23 | [📄 PDF](anno%201/Anatomia%20umana%20%28curriculum%20calcio%29/anatomia.pdf) | [`.tex`](anno%201/Anatomia%20umana%20%28curriculum%20calcio%29/) |
| **Funzionamento dei sistemi biologici** | 1 | 103 | 4 | [📄 PDF](anno%201/Funzionamento%20dei%20sistemi%20biologici/main.pdf) | [`.tex`](anno%201/Funzionamento%20dei%20sistemi%20biologici/) |
| **Fondamenti di biochimica applicata al calcio** | 1 | 93 | 22 | [📄 PDF](anno%201/Fondamenti%20di%20biochimica%20applicata%20al%20calcio/main.pdf) | [`.tex`](anno%201/Fondamenti%20di%20biochimica%20applicata%20al%20calcio/) |
| **Fisiologia dell'esercizio fisico** 🚧 *in corso* | 2 | 30 | 5 | [📄 PDF](anno%202/Fisiologia%20dell%27esercizio%20fisico/main.pdf) | [`.tex`](anno%202/Fisiologia%20dell%27esercizio%20fisico/) |
| **Doping - prevenzione e controllo** 🚧 *in corso* | 2 | 13 | 3 | [📄 PDF](anno%202/Doping%20-%20prevenzione%20e%20controllo/main.pdf) | [`.tex`](anno%202/Doping%20-%20prevenzione%20e%20controllo/) |
| **Valutazione funzionale e studio della performance del calciatore** 🚧 *in corso* | 2 | 236 | 22 | [📄 PDF](anno%202/Valutazione%20funzionale%20e%20studio%20della%20performance%20del%20calciatore/main.pdf) | [`.tex`](anno%202/Valutazione%20funzionale%20e%20studio%20della%20performance%20del%20calciatore/) |
| **Impianti sportivi - norme di prevenzione e gestione** 🚧 *in corso* | 2 | 33 | 5 | [📄 PDF](anno%202/Impianti%20sportivi%20-%20norme%20di%20prevenzione%20e%20gestione/main.pdf) | [`.tex`](anno%202/Impianti%20sportivi%20-%20norme%20di%20prevenzione%20e%20gestione/) |

> Le altre materie del piano di studi hanno la cartella già pronta in repo, ma la dispensa
> non è ancora scritta: compariranno in questa tabella quando ci sarà qualcosa da leggere.

---

## 🛠 Come sono fatte

Ogni dispensa nasce dalle lezioni del corso e viene riscritta in LaTeX seguendo un insieme
di convenzioni fisse:

- **fedeltà al contenuto**: si trascrive quello che è stato spiegato a lezione, senza
  aggiungere nozioni prese da altre fonti;
- **forma schematica**: `Termine: spiegazione;` — liste annidate come struttura portante,
  catene di processo con `→`, formule in *math mode*;
- **niente immagini**: le figure delle lezioni sono descritte a parole, così il PDF resta
  leggero e interamente testuale (quindi ricercabile);
- **un template comune** per tutte le materie, così le dispense restano coerenti tra loro.

## 📁 Struttura

```
appunti-uni/
├── anno 1/<materia>/
│   ├── main.tex               # preambolo, metadati e \input dei capitoli
│   ├── main.pdf               # dispensa compilata (il prodotto finale)
│   └── capitoli/NN_nome.tex   # un file per capitolo, ordinato dal prefisso
└── anno 2/<materia>/
```

Una cartella per materia, con il nome per esteso. Le materie ancora senza dispensa hanno la
cartella già pronta ma vuota.

## ⚙️ Compilare in locale

Serve una distribuzione LaTeX (MacTeX, TeX Live o MiKTeX). Dalla cartella della materia:

```bash
pdflatex main.tex && pdflatex main.tex
```

Due passate: la seconda risolve indice e riferimenti incrociati.

---

## ⚠️ Avvertenza

Questi sono **appunti personali**, rielaborati dalle lezioni seguite: non sono materiale
didattico ufficiale, non sono approvati né rivisti dai docenti o dall'ateneo, e possono
contenere errori, omissioni o semplificazioni. Non sostituiscono i libri di testo né il
materiale fornito dal corso — vanno usati come supporto al ripasso, non come fonte primaria.

Le slide e i materiali dei docenti **non sono inclusi** in questa repository: restano di
proprietà dei rispettivi autori.

## 📄 Licenza

I contenuti sono rilasciati sotto licenza
[Creative Commons Attribuzione – Non commerciale – Condividi allo stesso modo 4.0 Internazionale (CC BY-NC-SA 4.0)](LICENSE).

Si possono copiare, ridistribuire e modificare liberamente **per scopi non commerciali**,
citando la fonte e distribuendo le opere derivate con la stessa licenza.
