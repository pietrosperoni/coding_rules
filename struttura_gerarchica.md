# Struttura delleo sviluppo

Lo sviluppo del programma segue una struttura ben definita. Oltre all'utente usa queste AI: AI_Vision, AI_project_manager, AI_coder

L'utente umano sviluppa la visione la descrive scompostamente a una AI (AI_Vision) che la scrive nei dettagli. Poi dopo aver ricevuto l'approvazione dell'utente umano, la visione viene caricata su un progetto. 

Poi viene generata una AI per quel progetto, AI_project_manager che legge la visione, il codice, e qualsiasi altro documento che sia stato passato. Ha accesso al codice che è stato registrato su github, ma potrebbe non essere l'ultima versione. Sulla base di questo, e parlando con l'utente, decide quali sono i prossimi obiettivi. E divide i prossimi obiettivi in microsteps. 

Non scrive il codice, ma scrive il prompt per far scrivere il codice alla AI_coder che lavora dentro a Cursor. Questi prompt vengono controllati dall'essere umano, che li passa a Cursor. La AI_coder in Cursor sviluppa il codice. L'essere umano lo testa, restituisce il feedback alla AI_project_manager. È importante che il prompt sia scritto dalla AI_project_manager che ha accesso alla visione generale, ma non all'ultima versione del codice. È importante che il codice sia scritto dalla AI_coder che ha accesso all'ultima versione del codice, ma non ha accesso alla visione generale.

## Struttura dei prompt

*Repository*: [in quale repository il codice deve essere scritto, nel caso ce ne sia più di uno]
*Task*: [Scopo  del codice] 
*Instructions*: [istruzioni da eseguire in maniera descrittiva. Non dovrebbe contenere codice ne fare micromanaging. La AI_coding è in grado di scrivere un ottimo codice]

*Requirements*:
[le cose a cui bisogna fare attenzione e soddisfare nello scrivere questo codice]

*Success Criteria*: [cosa dovrebbe succedere se il codice è scritto con successo]

*Test*: [come bisogna fare per testare il codice. Questo spesso è per l'utente. Non per la AI_coder]

