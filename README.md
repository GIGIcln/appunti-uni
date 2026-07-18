# 📚 Appunti Universitari - LaTeX Sync Repository

Repository sincronizzata per gestire appunti universitari in LaTeX tra Windows e Mac, con workflow ottimizzato per Visual Studio Code.

##  Struttura del Repository
```
appunti-uni/
├── .gitignore
├── README.md
├── template-schematico.tex   ← template preferito (classe book), da copiare come main.tex
├── template.tex              ← template a prosa discorsiva
├── backup.sh
├── anno 1/
│ ├── Anatomia umana (curriculum calcio)/
│ ├── Elementi di fisica e biomeccanica applicata al calcio/
│ ├── Fondamenti di biochimica applicata al calcio/
│ ├── Funzionamento dei sistemi biologici/
│ ├── Inglese tecnico/
│ ├── Psicologia applicata al calcio/
│ ├── Statistica - scouting, match analysis ed elaborazione dati/
│ └── Teoria e metodologia dell'allenamento applicata al calcio/
└── anno 2/
  ├── Doping - prevenzione e controllo/
  ├── Fisiologia dell'esercizio fisico/
  ├── Impianti sportivi - norme di prevenzione e gestione/
  ├── Nutrizione umana e controllo ormonale/
  ├── Principi di medicina dello sport/
  ├── Teoria, tecnica e didattica del calcio/
  └── Valutazione funzionale e studio della performance del calciatore/
```
> I nomi delle cartelle materia sono **identici** a quelli del vault Obsidian, così il flusso slide → `.tex` → nota resta allineato tra i due sistemi.
- Esiste **un unico template master** (`template.tex`, classe `book`): copialo nella cartella del corso quando inizi a scrivere.
- Ogni cartella corso contiene un `.gitkeep` per essere tracciata da Git anche se vuota.
- I file di compilazione LaTeX (`.pdf`, `.aux`, `.log`, `.synctex.gz`, ecc.) sono automaticamente ignorati.

## 🚀 Setup Rapido (Nuovo dispositivo o reinstallazione)
### 1. Prerequisiti
- Git installato
- Account GitHub
- Visual Studio Code con estensione `LaTeX Workshop`

### 2. Configura SSH (una sola volta per device)
Apri il terminale e genera la chiave:
`ssh-keygen -t ed25519 -C "tua@email.com"` (Premi Invio 3 volte)
Copia il contenuto di: `~/.ssh/id_ed25519.pub` (Mac) o `%USERPROFILE%\.ssh\id_ed25519.pub` (Windows)
Incollalo in GitHub: Settings → SSH and GPG keys → New SSH key
Verifica: `ssh -T git@github.com`

### 3. Clona e Configura VS Code
`git clone git@github.com:GIGIcln/appunti-uni.git`
`cd appunti-uni`
Apri la cartella in VS Code e accetta `git fetch` automatico quando richiesto.

## 📝 Workflow Giornaliero
1. **Apri** VS Code sulla cartella `appunti-uni`
2. **Sync iniziale**: Clicca 🔄 in basso a destra per scaricare aggiornamenti dall'altro PC
3. **Studia & Scrivi**: Salva spesso (`Cmd+S` / `Ctrl+S`)
4. **Commit & Push**: 
   - Vai su `Cmd+Shift+G` / `Ctrl+Shift+G`
   - Scrivi un messaggio chiaro (es. `add: anatomia - sistema nervoso`)
   - Clicca ✅ `Commit & Sync`
5. **Chiudi**: Verifica che la scheda Source Control sia vuota

## 🛡️ Regole Anti-Conflitto
- ✅ **Un device alla volta**: lavora su Windows o Mac, non contemporaneamente sullo stesso file
-  **Sync prima e dopo**: scarica sempre le modifiche prima di iniziare, e pusha prima di cambiare PC
- 📝 **Commit frequenti**: messaggi chiari ti permettono di tornare indietro a qualsiasi versione
- 🚫 **No modifiche parallele**: se devi studiare su entrambi, usa file diversi o sincronizza subito
- 🧹 **File temporanei**: sono gestiti da `.gitignore`, non committarli mai manualmente

## 🔧 Troubleshooting Rapido
| Problema | Soluzione |
|----------|-----------|
| `fatal: bad object HEAD` | Cancella la cartella locale e rifai `git clone` |
| VS Code non mostra le modifiche | `Cmd+Shift+P` → `Developer: Reload Window` |
| Conflitti di merge | Risolvi manualmente in VS Code o chiedi supporto |
| SSH rifiutata / Permission denied | Verifica con `ssh -T git@github.com` o rigenera la chiave |
| PDF non si compila | Controlla il pannello `LaTeX Workshop` → `View Log` |

---
🎓 *Creato per studio universitario. Sync sicuro, zero conflitti, massima produttività.*