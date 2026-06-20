# Modifica Controllata

Applica solo la modifica minima approvata nel piano.

Prima di modificare, conferma in una frase:

- task;
- eventuali files da toccare indicandone il percorso relativo (ES: src/components/component.xxx);
- eventuali files da creare indicandone il percorso relativo (ES: src/components/component.xxx);
- prova di controllo;
- cosa resta fuori scope;
- strategia prompt usata: zero-shot o few-shot.

Confini:

- non cambiare layout globale;
- non aggiungere nuove feature;
- non fare refactor non richiesti;
- non modificare routing o configurazione;
- fermati se devi toccare file fuori scope.

Dopo la patch:

- mostra il diff;
- spiega cosa e' cambiato;
- indica la prova di controllo.
- riporta solo evidenze brevi: assunzioni principali, criterio usato, verifica proposta.
- non effettuare commit, push o pr se non richiesto.

Se non puoi modificare file direttamente:

- non simulare di averli modificati;
- indicami il blocco di codice da cambiare;
- dimmi dove inserirlo;
- spiega perche' la modifica e' minima;
- indicami come controllarla in VS Code.

Non mostrare chain-of-thought estesa e non aggiungere esempi o alternative fuori scope.
