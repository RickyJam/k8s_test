# __SmartCity__

## Requisiti:
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
    - (sembrerebbe un passaggio di troppo, ma serve a prepararsi già per deploy su server remoti)
  * creare un deployments con tutte le specifiche necessarie e non di più.
    - usare l'immagine appena creata
  * vedere se serve creare anche un service correlato
  * questo service corriesponde effettivamente al nostro servizio api che andiamo a sviluppare
  
  
  
* accortezze: utilizzare immagini alpine così da velocizzare il processo di download.



## Esecuzione e comandi utili
* posizionarsi nella folder k8s_test/SmartCity/k8s
* eseguire il comando: ```kubectl apply -f .```
  * se dovessero esserci problemi con il namespace, eseguire prima in modo isolato il comando: ```kubectl apply -f smart_city_namespace.yaml```
* verificare che i sia tutto su con: ```kubectl get pods``` (e poi ```deploy```, ```service```)
* una volta che i servizi sono tutti, ecco i comandi possibili:
  * aprire server node: ```minikube service --url node-service -n smart-city```
  * aprire verifa che sia online: ```minikube service --url mongo-service -n smart-city``` 
  * sia da CLI che dalla console compass inserire questi dati:
    * host: <ip> ritornato dal comando sopra
    * porta: <porta> ritornata dal comando sopra
    * password: <Password123>
    * username: <Admin>
