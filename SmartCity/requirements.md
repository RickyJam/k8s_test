# Cosa deve avere _SmartCity__
* Database:
  * il db non sarà replicato, sarà in un pod a se stante 
  * idelamente useremo un db noSql, abbiamo già tutto fatto nel progetto
  * va usato il modello statefulSet perchè richiede lo stato essendo un DB. Vedere la questione volumi

* per iniziare ci mettiamo un semplice server node.
  * creare server node in JS
  * creare Dockerfile
  * buildare il DockerFile
  * metterlo in un container e vedere che parte! ok!
  * a questo punto spararle su dockerhub e k8s la ripesca da li 
    - (sembrerebbe un passaggio di troppo, maserve a prepararsi già per deploy su server remoti)
  * creare un deployments con tutte le specifiche necessarie e non di più.
    - usare l'immagine appena creata
  * vedere se serve creare anche un service correlato
  
  
  
* accortezze: utilizzare immagini alpine così da velocizzare il processo di download.

