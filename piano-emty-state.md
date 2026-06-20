# Piano Breve

**Task**: Quando non ci sono ticket aperti, mostrare un messaggio semplice centrato nella griglia vuota, senza card stilizzata, con badge conteggio visibile.

### Bozza piano (5 punti operativi)

1. **Modificare `src/components/TicketList.jsx`**: aggiungere condizionale `tickets.length === 0` che renderizza un `<p>` con testo "Non ci sono ticket aperti." (senza classi CSS aggiuntive) al posto della griglia `.ticket-list`.

2. **Centrare il messaggio**: avvolgere il `<p>` in un wrapper `<div className="empty-state">` con stili flexbox per centrarlo orizzontalmente e verticalmente nello spazio della griglia vuota.

3. **Mantenere badge conteggio**: il `<span className="ticket-count">` nell'intestazione resta visibile (mostra "0").

4. **Non modificare altri file**: `App.jsx`, API, routing, componenti esistenti. Eventuali stili di centratura aggiunti in `src/styles.css` solo se necessario.

5. **Verifica**: eseguire `pnpm dev`, visitare `?empty=true`, controllare messaggio centrato senza card; poi con ticket normali, controllare che la lista funzioni.

### Fuori scope
- Routing, nuove feature, refactor, redesign.
- Modifiche a API o backend.
- Riutilizzo della classe `.state-message` (rimossa su richiesta).

### Verifica
- `pnpm dev` e test manuale con `?empty=true` e senza.
- Controllare che il badge mostri "0".
- Controllare che il messaggio sia centrato e senza bordo/sfondo/padding.

### Rischio
**Basso**: modifica singola, reversibile, nessuna dipendenza esterna.

### Permesso massimo
Modificare `src/components/TicketList.jsx` e, se necessario, aggiungere stili di centratura in `src/styles.css`.

### Strategia prompt
**Zero-shot**: task chiaro, codebase piccola, modifica condizionale semplice.

### Evidenze da controllare prima della patch
- **Assunzioni principali**: il testo semplice è sufficiente; centratura gestita con wrapper flexbox.
- **Criterio usato**: minimalità (un file, un condizionale), rimozione stile card.
- **Verifica proposta**: test manuale con e senza ticket.