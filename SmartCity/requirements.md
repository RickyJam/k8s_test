# Cosa deve avere _SmartCity__
* Database:
  * il db non sarà replicato, sarà in un pod a se stante 
  * idelamente useremo un db noSql, abbiamo già tutto fatto nel progetto
  * va usato il modello statefulSet perchè richiede lo stato essendo un DB. Vedere la questione volumi

* per iniziare ci mettiamo un semplice server node.
  * strutturiamo come service? 
  
  
  
  
* accortezze: utilizzare immagini alpine così da velocizzare il processo di download.

