# Interfaccia JSON

Due editor HTML per caricare, modificare e scaricare file JSON. Ogni file è autonomo (HTML + CSS + JS inline), senza dipendenze esterne.

---

## 1. `editor-json.html` — Editor a form

**Titolo:** Editor JSON Interattivo  
**Uso:** Vista a form, adatta a qualsiasi dispositivo; layout compatto su PC con etichetta e campo sulla stessa riga.

### Funzionalità

- **Caricamento:** Seleziona un file `.json` oppure usa **Carica esempio** per un JSON di prova.
- **Modifica:** I campi vengono generati automaticamente dal JSON:
  - **Stringhe, numeri, boolean** → campi di input (testo, number, checkbox).
  - **Oggetti** → blocchi espandibili/comprimibili con i campi annidati.
  - **Array** → array di oggetti con righe aggiungibili/rimovibili; array di valori primitivi con ricerca e selezione da menu.
- **Comprimi / Espandi:**  
  - **Comprimi tutto** e **Espandi tutto** in testa all’editor.  
  - Su ogni oggetto/array (e su ogni elemento di array di oggetti) è possibile comprimere/espandere singolarmente cliccando sulla riga del titolo (triangolo ▼/▶).
- **Aggiungi / Rimuovi (solo primo livello):**
  - **+** (verde): in fondo al form, nella riga “Nuovo campo”. Aggiunge un nuovo campo a livello root con la **stessa struttura** del primo campo esistente (oggetto, array o valore semplice). Opzionale: inserire il nome della chiave nel campo di testo.
  - **−** (rosso): su ogni riga di **primo livello** rimuove quel campo dall’oggetto (dati aggiornati e form ridisegnato).
- **Anteprima:** Aggiornamento in tempo reale del JSON sotto il form.
- **Scarica JSON:** Pulsante **Scarica JSON** per scaricare il JSON modificato.

### Utilizzo

Apri `editor-json.html` in un browser (anche da file). Non serve un server.  
Esiste anche una copia in `json/editor-json.html` (stesse funzionalità).

---

## 2. `editor-json-tabella.html` — Editor a tabella (PC)

**Titolo:** Editor JSON – Vista tabellare (PC)  
**Uso:** Visualizzazione a tabelle orizzontali, pensata per schermi grandi.

### Funzionalità

- **Caricamento:** Come l’editor a form: file JSON o **Carica esempio**.
- **Modifica a tabella:**  
  - Gli **oggetti** sono mostrati come tabelle (chiavi in colonna, valori in celle modificabili).  
  - Gli **array** come elenchi puntati o tabelle; pulsanti **+** / **−** per aggiungere o rimuovere righe/elementi.  
  - Celle con `textarea` e a capo; altezza minima e anteprima quando la riga è compressa.
- **Comprimi / Espandi:** Comprimi/espandi globale e per singola riga.
- **Anteprima e download:** Anteprima JSON e pulsante **Scarica JSON** per scaricare il file modificato.

### Utilizzo

Apri `editor-json-tabella.html` in un browser. Consigliato su PC per sfruttare il layout a tabella.

---

## Riepilogo

| File                    | Vista     | Ideale per        | Note                                      |
|-------------------------|-----------|-------------------|-------------------------------------------|
| `editor-json.html`       | Form      | Tutti i dispositivi | Label e campo sulla stessa riga, +/− solo primo livello |
| `editor-json-tabella.html` | Tabella   | PC                | Oggetti in tabelle, array in righe/elenchi |

Entrambi i file sono in italiano e non richiedono installazione: basta aprirli dal filesystem.
