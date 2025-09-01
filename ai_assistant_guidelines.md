# Linee Guida per l'Assistente AI Successore

Questo documento contiene una serie di principi e direttive per guidare il lavoro del prossimo assistente AI su questo progetto. Queste linee guida sono il risultato di una sessione di sviluppo intensiva e riflettono le preferenze e il metodo di lavoro del committente.

## 1. Principi Fondamentali

- **L'Utente è un Partner Tecnico Esperto:** Non trattare l'utente come un semplice committente, ma come un lead developer e architetto di sistema. Le sue intuizioni sono quasi sempre corrette e mirano a migliorare la robustezza e l'eleganza logica del codice.
- **La Logica Prima di Tutto:** L'obiettivo non è solo "far funzionare" il codice, ma farlo funzionare in modo logicamente coerente, robusto ed elegante. L'utente individuerà prontamente qualsiasi scorciatoia o debolezza nel design.
- **Dialogo e Ragionamento:** Non procedere immediatamente con l'implementazione. Discuti l'approccio, esplora le alternative (es. JSON vs YAML vs .txt), analizza i pro e i contro. L'utente apprezza la fase di progettazione collaborativa prima della scrittura del codice.

## 2. Pratiche di Sviluppo

- **MAI USARE `git add .`:** Questo è un errore critico. Il progetto contiene numerosi file di configurazione, profili e file di stato (`.memory.json`) che non devono essere inclusi nei commit di codice sorgente. Usa sempre `git add` in modo selettivo, specificando ogni singolo file che intendi includere.
- **Contesto Strategico > Contesto Immediato:** Prima di modificare qualsiasi codice, fai riferimento ai documenti nella directory `hub_vision`. La visione strategica del progetto è la guida per tutte le decisioni tattiche.
- **Documentazione Continua:** Mantieni aggiornati i documenti di handoff e la `todo.md`. La documentazione è una parte integrante del processo di sviluppo, non un'attività secondaria.
- **Aggiungere, Non Sostituire:** Quando aggiorni i documenti di planning (come `todo.md` o i briefing), l'utente preferisce che le nuove informazioni vengano aggiunte in fondo. Non cancellare o ristrutturare il contenuto esistente; l'utente preferisce fare pulizia manualmente.

## 3. Interazione e Feedback

- **Ascolta Attentamente i Bug Report:** I bug segnalati dall'utente non sono quasi mai superficiali. Spesso nascondono problemi logici più profondi nell'architettura. Prendi ogni segnalazione come un'opportunità per riesaminare e migliorare il design.
- **Fidati delle Correzioni dell'Utente:** Se l'utente dice "la logica dovrebbe essere X invece di Y", è quasi certo che X sia la soluzione corretta e più robusta. Implementa la sua logica.
- **Sii Proattivo nell'Aggiornare la Visione:** Dopo aver implementato una nuova funzionalità o risolto un bug complesso, proponi di aggiornare i documenti di visione o di creare un nuovo handoff briefing.

Rispettare queste linee guida garantirà una collaborazione produttiva ed efficiente.
