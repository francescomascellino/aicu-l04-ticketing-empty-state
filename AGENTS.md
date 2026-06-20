# AGENTS.template.md

## Contesto Del Progetto

Piattaforma di ticketing basilare a scopo didattico.

## Obiettivo Corrente

Quando non ci sono ticket aperti, la pagina deve mostrare un empty state semplice: un messaggio chiaro che spiega che non ci sono ticket da visualizzare.

## Ambito Delle Istruzioni

Queste istruzioni valgono per la repo target dopo adattamento.

- Regole stabili: diventano `AGENTS.md` nella repo target.
- Prompt riusabili: restano in `prompt-kit/`.
- Task del momento: va scritto nel prompt o nel ticket, non reso permanente qui.

## Regole Di Lavoro

- Prima di modificare file, riscrivi il task in una frase.
- Prima di modificare file, proponi un piano breve seguendo le direttive in "prompt-kit\02-piano-breve.md".
- Se la richiesta e' ambigua, fai una sola domanda.
- Se il task diventa troppo largo, fermati e proponi una versione piu' piccola.
- Non simulare modifiche non eseguite.
- Non mostrare chain-of-thought estesa: riporta solo assunzioni principali, criterio usato e verifica proposta.
- Usa esempi few-shot solo se chiariscono formato o criterio; non usarli per anticipare la soluzione.
- Chiedi sempre prima di modificare o creare files e solo dopo l'approvazione del piano.
- Accedi ai contenuti della cartella  "prompt-kit\" solo quando richiesto.

## Confini

Durante il lavoro:

- non cambiare layout globale;
- non aggiungere nuove feature non richieste;
- non modificare routing o configurazione;
- non fare refactor non richiesti;
- non cambiare file fuori dallo scope del task.

## Comandi Utili

Compila solo se li conosci o se sono nel README della repo target.

- install: pnpm install
- dev: pnpm dev
- test:
- lint:

## Prova Di Controllo

Per ogni modifica, indica:

- come controllare il caso modificato;
- come controllare che il caso normale funzioni ancora;
- quali controlli non sono stati eseguiti.
- quali assunzioni principali e quale criterio hanno guidato la scelta.

## Output Finale

Alla fine rispondi con:

- file modificati, compresi di percorso relativo;
- mostra il diff;
- cosa e' cambiato;
- prova di controllo eseguita o da eseguire;
- strategia prompt usata se rilevante: zero-shot o few-shot;
- rischi o dubbi rimasti.