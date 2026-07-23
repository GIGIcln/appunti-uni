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
| **Fisiologia dell'esercizio fisico** 🚧 *in corso* | 2 | 18 | 3 | [📄 PDF](anno%202/Fisiologia%20dell%27esercizio%20fisico/main.pdf) | [`.tex`](anno%202/Fisiologia%20dell%27esercizio%20fisico/) |

> Le altre materie del piano di studi hanno la cartella già pronta in repo, ma la dispensa
> non è ancora scritta: compariranno in questa tabella quando ci sarà qualcosa da leggere.

<details>
<summary><b>Anatomia umana</b> — indice dei 23 capitoli</summary>

1. Cenni di storia dell'anatomia
2. Generalità dell'anatomia
3. Il tessuto epiteliale
4. Il tessuto connettivo
5. Il tessuto connettivo specializzato
6. Il tessuto muscolare
7. Il tessuto nervoso
8. L'apparato scheletrico
9. L'apparato muscolo-scheletrico
10. Le articolazioni dell'arto superiore
11. Le articolazioni dell'arto inferiore
12. L'apparato digerente
13. L'apparato respiratorio
14. L'apparato urinario
15. L'apparato genitale maschile
16. L'apparato genitale femminile
17. L'apparato cardiovascolare
18. L'apparato circolatorio
19. Il sistema nervoso periferico
20. Il sistema nervoso centrale
21. Il sistema endocrino
22. Il sistema nervoso autonomo
23. Le vie sensitive e motorie

</details>

<details>
<summary><b>Funzionamento dei sistemi biologici</b> — indice dei 4 capitoli</summary>

1. **Organismi viventi** — biologia, la materia vivente, gli organismi viventi, citologia, biotecnologie
2. **Biologia cellulare** — membrana plasmatica (struttura e funzioni), citoscheletro, giunzioni cellulari, endomembrane, mitocondri e cloroplasti
3. **Ciclo cellulare e genetica** — nucleo e DNA, ciclo cellulare, sintesi proteica, genetica mendeliana, cariotipo
4. **Istologia** — tessuto epiteliale, connettivo (generalità e propriamente detto), cartilagineo, osseo, emolinfopoietico, muscolare, nervoso, potenziale d'azione, contrazione muscolare

</details>

<details>
<summary><b>Fondamenti di biochimica applicata al calcio</b> — indice dei 22 capitoli</summary>

1. Organizzazione della materia
2. La cellula eucariotica
3. Amminoacidi
4. Le proteine
5. Trasporto e utilizzo dell'ossigeno
6. Enzimi
7. Carboidrati
8. Lipidi
9. Nucleotidi
10. Introduzione al metabolismo energetico
11. Metabolismo degli zuccheri
12. Ciclo di Krebs e fosforilazione ossidativa
13. Metabolismo dei lipidi
14. Metabolismo degli amminoacidi
15. Principi di regolazione del metabolismo
16. Il muscolo scheletrico e la contrazione muscolare
17. Biochimica dell'esercizio fisico ad alta intensità
18. Biochimica dell'esercizio fisico di endurance
19. Biochimica del gioco del calcio
20. Adattamenti metabolici all'allenamento
21. Esercizio fisico e stress ossidativo
22. Basi biochimiche della fatica

</details>

<details>
<summary><b>Fisiologia dell'esercizio fisico</b> — capitoli scritti finora</summary>

1. L'omeostasi
2. L'eccitabilità cellulare
3. La trasmissione sinaptica

</details>

---

## 🛠 Come sono fatte

Ogni dispensa nasce dalle lezioni del corso e viene riscritta in LaTeX seguendo un insieme
di convenzioni fisse, raccolte in [`CONVENZIONI.md`](CONVENZIONI.md):

- **fedeltà al contenuto**: si trascrive quello che è stato spiegato a lezione, senza
  aggiungere nozioni prese da altre fonti;
- **forma schematica**: `Termine: spiegazione;` — liste annidate come struttura portante,
  catene di processo con `→`, formule in *math mode*;
- **niente immagini**: le figure delle lezioni sono descritte a parole, così il PDF resta
  leggero e interamente testuale (quindi ricercabile);
- **due template comuni**: [`template-schematico.tex`](template-schematico.tex), usato di
  default, e [`template.tex`](template.tex) per la prosa discorsiva.

## 📁 Struttura

```
appunti-uni/
├── anno 1/<materia>/          # una cartella per materia
│   ├── main.tex               #   preambolo, metadati e \input dei capitoli
│   ├── main.pdf               #   dispensa compilata (il prodotto finale)
│   └── capitoli/NN_nome.tex   #   un file per capitolo, ordinato dal prefisso
├── anno 2/<materia>/
├── template-schematico.tex    # template di default (classe book)
├── template.tex               # variante a prosa discorsiva
├── CONVENZIONI.md             # regole di trascrizione e di stile
└── docs/                      # setup e workflow di lavoro
```

## ⚙️ Compilare in locale

Serve una distribuzione LaTeX (MacTeX, TeX Live o MiKTeX). Dalla cartella della materia:

```bash
pdflatex main.tex && pdflatex main.tex
```

Due passate: la seconda risolve indice e riferimenti incrociati. Setup completo e workflow
di sincronizzazione in [`docs/setup-e-workflow.md`](docs/setup-e-workflow.md).

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
