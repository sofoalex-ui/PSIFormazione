# PsiFormazione

Corsi, workshop e master per psicologi e psicoterapeuti in Italia, divisi per argomento, regione, costo, crediti ECM e modalità.
In collaborazione con ASIPP – Associazione Scientifica Italiana di Psicologia Perinatale.

## File del progetto

| File | A cosa serve |
|---|---|
| `index.html` | L'app (pagina unica, nessuna installazione) |
| `formazioni.json` | L'elenco delle formazioni: è l'unico file da aggiornare |
| `asipp.png` | Logo ASIPP (usato anche come icona del sito) |
| `vercel.json` | Impostazioni per Vercel (l'elenco non resta in cache, così gli aggiornamenti si vedono subito) |

## Pubblicare la prima volta

### 1. GitHub
1. Vai su github.com → **New repository** → nome `psiformazione` → Public → **Create repository**.
2. Clicca **uploading an existing file** e trascina tutti i file di questa cartella (`index.html`, `formazioni.json`, `asipp.png`, `vercel.json`, `README.md`).
3. **Commit changes**.

### 2. Vercel
1. Vai su vercel.com → **Add New… → Project**.
2. Scegli il repository `psiformazione` → **Import**.
3. Framework Preset: **Other**. Non serve altro → **Deploy**.
4. Il sito sarà su un indirizzo tipo `psiformazione.vercel.app` (si può cambiare in Settings → Domains).

## Aggiornare le formazioni

L'archivio "vero" resta l'app PsiFormazione su claude.ai (dove ogni lunedì arrivano in automatico le nuove formazioni e dove approvi le proposte dei colleghi). Per portare gli aggiornamenti sul sito:

1. Apri PsiFormazione su claude.ai e tocca **Esporta per il sito**: salvi il file `formazioni.json`.
2. Su GitHub apri il repository → **Add file → Upload files** → trascina il nuovo `formazioni.json` (sostituisce il vecchio) → **Commit changes**.
3. Vercel ripubblica da solo in circa un minuto.

Le formazioni con data già passata spariscono da sole, anche senza aggiornare il file.

## Proposte dei colleghi (sul sito)

Sul sito chiunque può toccare **+ Proponi formazione**: l'app prepara un messaggio con un codice `PF1:` da copiare o condividere (WhatsApp, email…).
Quando lo ricevi, incollalo in PsiFormazione su claude.ai → **Da approvare** → "Hai ricevuto una proposta per messaggio?" → **Approva**.

Per mostrare anche il pulsante **Invia per email**, apri `index.html` e scrivi l'indirizzo in questa riga (vicino all'inizio dello script):

```js
const EMAIL_PROPOSTE="";
```

## Note
- Nessun dato personale viene raccolto: il sito legge solo `formazioni.json`.
- Prezzi e date sono quelli pubblicati dagli enti; sul sito c'è l'invito a verificarli sulla pagina del corso.
