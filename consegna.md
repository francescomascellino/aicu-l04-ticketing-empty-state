# Consegna - Lab 04

## Obiettivo

Aggiungere un empty state semplice alla lista dei ticket aperti.

Il valore del lab non e' fare una UI bellissima. Il valore e' rendere il lavoro controllabile:

```txt
kit -> richiesta -> piano -> gate -> modifica -> diff -> verify -> handoff -> commit/push
```

## Repository Di Lavoro

Lavora nel tuo fork della repo:

```txt
aicu-l04-ticketing-empty-state
```

Prima di chiedere modifiche al codice, copia o adatta dal tuo kit L03:

```txt
AGENTS.md
prompt-kit/
  02-piano-breve.md
  03-modifica-controllata.md
  04-controllo-diff.md
  05-handoff.md
handoff-note.md
```

Il kit L03 e' un punto di partenza: in questa repo devi adattarlo al task empty state.

## Richiesta Del Lab

Titolo:

```txt
Aggiungere un messaggio per lista vuota
```

Descrizione:

```txt
Quando non ci sono ticket aperti, la pagina deve mostrare un empty state semplice: un messaggio chiaro che spiega che non ci sono ticket da visualizzare.
```

Copy baseline:

```txt
Non ci sono ticket aperti.
Quando verra' creato un nuovo ticket, lo vedrai qui.
```

Puoi modificare il testo a tuo piacimento.

## Flusso Con Output

| Step | Cosa apri | Cosa fai | Output |
| --- | --- | --- | --- |
| Kit | kit L03 | adatti alla repo L04 | `AGENTS.md`, `prompt-kit/`, `handoff-note.md` |
| Richiesta | questa consegna | riscrivi il task in 1 frase | task e criteri chiari |
| Piano | `prompt-kit/02-piano-breve.md` | chiedi piano senza patch | file probabili, scope, verifica |
| Gate | piano ricevuto | approvi o restringi | permesso massimo alla patch |
| Modifica | `prompt-kit/03-modifica-controllata.md` | chiedi patch minima | codice modificato |
| Diff | `git diff` o Source Control | leggi cosa e' cambiato | diff controllato |
| Verify | README repo | provi zero ticket e ticket presenti | evidenze di verifica |
| Handoff | `prompt-kit/05-handoff.md` | compili nota | `handoff-note.md` |
| Salvataggio | Git | commit e push | traccia nel fork |

## Prima Di Modificare

Usa il prompt adattato:

```txt
prompt-kit/02-piano-breve.md
```

Il piano deve dire:

- file probabili;
- modifica minima;
- cosa non tocchera';
- prova di controllo;
- strategia prompt: zero-shot o few-shot;
- evidenze richieste: assunzioni principali, criterio usato, verifica proposta.

## Gate Umano

Piano accettato significa che puoi rispondere a queste domande:

| Punto | Domanda |
| --- | --- |
| Task | Sai dirlo in una frase? |
| Scope | Sai cosa resta fuori scope? |
| Prompt | Basta zero-shot o servono 1-2 esempi few-shot? |
| Diff | Ti aspetti una modifica piccola e leggibile? |
| Verify | Sai controllare stato vuoto e stato con ticket? |

Se una risposta manca, non autorizzare ancora la patch. Chiedi all'agente di restringere o chiarire il piano.

Non chiedere chain-of-thought estesa. Ti servono evidenze brevi per decidere, non un ragionamento lungo.

## Modifica

Solo dopo il gate umano, usa:

```txt
prompt-kit/03-modifica-controllata.md
```

La patch deve essere minima:

- niente redesign;
- niente filtri;
- niente routing;
- niente creazione ticket;
- niente refactor generale.

Se il tuo tool non modifica file direttamente, usa fallback chat/manuale:

- fatti indicare il blocco da cambiare;
- applicalo tu in VS Code;
- controlla il `diff`.

## Diff

Leggi il diff prima di considerare chiusa la modifica.

Puoi usare terminale:

```bash
git diff
```

Oppure Source Control in VS Code.

Controlla:

- quali file sono cambiati;
- se il diff risponde solo al ticket;
- se c'e' codice non richiesto;
- se la verifica proposta copre i file davvero modificati.

## Verifica

Devi controllare:

- stato con zero ticket aperti;
- stato con ticket presenti.

Usa i comandi o le istruzioni indicate nel README di `aicu-l04-ticketing-empty-state`.

Se la repo prevede un modo rapido per simulare zero ticket, ad esempio query param `?empty=true`, toggle dev o fixture locale, usa quello. Se non lo trovi entro pochi minuti, chiedi al docente.

Non basta scrivere:

```txt
L'AI dice che funziona.
```

## Handoff

Compila:

```txt
handoff-note.md
```

Deve contenere:

- scope;
- changes;
- validation;
- review notes;
- controlli non eseguiti, se ci sono;
- rischi o dubbi residui, se ci sono.

## Git

Percorso standard nel tuo fork:

```bash
git status
git diff
git add .
git commit -m "Add empty state for open tickets"
git push
```

Se stai usando un fallback senza Git funzionante, compila comunque `handoff-note.md` e annota il blocco tecnico.

## Output Obbligatorio

- `AGENTS.md` e `prompt-kit/` adattati al lab;
- modifica piccola;
- `diff` leggibile o evidenza equivalente;
- verifica stato vuoto e stato con ticket;
- `handoff-note.md`;
- commit & push nel tuo fork, se usi il percorso standard;
- blocco tecnico annotato, se Git/tool non funzionano.

## Fuori Scope (Per il primo task)

- Redesign.
- Filtri.
- Routing.
- Creazione ticket.
- Refactor.
- Test automatici.
- Richiesta di review per chiudere il lab.

## Bonus

Solo dopo l'output obbligatorio:

1. migliora il copy;
2. migliora spaziatura o gerarchia usando stili esistenti;
3. aggiungi screenshot o verifica piu' precisa;
4. apri una Pull Request, senza spendere piu' di 10 minuti su setup o UI GitHub.

Una Pull Request e' una richiesta di review su modifiche gia' salvate. Non serve per chiudere il lab.

## Pronto Quando

- L'empty state e' visibile con zero ticket.
- La lista funziona ancora con ticket presenti.
- Hai controllato il `diff`.
- Hai compilato `handoff-note.md`.
- Hai annotato strategia prompt ed evidenze principali.
- Hai fatto commit & push nel tuo fork, oppure hai annotato il blocco tecnico.
- Sai spiegare modifica e verifica in 60 secondi.

> **Team Mode**
> In un team, questa Handoff Note puo' diventare la base della descrizione di una Pull Request: scope, changes, validation e review notes. Non serve aprire una Pull Request per completare il lab; serve capire come rendere revisionabile il lavoro.
