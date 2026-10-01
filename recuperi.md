### Esercizio 6

#### Situazione n. 1
Comandi usati: 
```
touch nota.txt
git add nota.txt
git status
git restore --staged nota.txt
git status
```

Effetto osservato: Inanzitutto siamo andati a creare il file con il comando touch e lo abbiamo aggiunto nell'area di stage con il comando git add. Successivamente, con il comando git status, possiamo vedere che effettivamente il file nota.txt si trovava nell'area pronto per essere salvato in un commit. Ora usiamo il comando "git restore --staged nota.txt". Lanciando il comando gi status di nuovo, notiamo che il file è stato rimosso dall'area di stage e che non abbiamo perso alcune modifiche.

#### Situazione n. 2
Comandi usati:
```
git status
git restore README.md
git status
```

Effetto osservato: Per questo esercizio ho scritto una riga in più nel file README.md. 
Successivamente, ho eseguito il comando git status per controllare se la modifica sia stata rilevata e che sia pronta per essere salvata in un commit. Con l'esecuzione comando "git restore README.md", la riga è stata cancellata. Eseguendo un altro git status alla fine, possiamo anche vedere che le modifiche che prima erano pronte per essere salvate, ora non ci sono più all'interno dell'area di stage.

#### Situazione n. 3
Comandi usati:
```
git add nota.txt
git commit -m "Aggiunta di un file con un errore di batitura"
git commit --amend -m "Aggiunta di un file senza errore di battitura"
git log --oneline
```

Effetto osservato: Abbiamo aggiunto il file all'area di stage, per poi eseguire un commit alla quale scriveremo un messaggio con un errore di battitura. Successivamente, per riuscire a modificare il messaggio senza creare un commit, andremo ad eseguire il comando "git commit --amend -m "Aggiunta di un file senza errore di battitura". Per controllare che tutto sia andato a buon fine, possiamo eseguire il comando git log, che si scrivererà la cronologia di tutti i commit fatti fino ad ora. Così possiamo controllare se il messaggio è stato effetivamente corretto.