### DOCKER
## Containerizzazione applicativi JAVA

In questo esercizio è richiesta la creazione di due immagini DOCKER per due applicativi JAVA (immagine di partenza suggerita su dockerhub: maven:3-jdk-12).

I due applicativi sono contenuti nella due cartelle (2.1-shop-catalog e 2.2-shop-purchase), entrambi espongono tramite protocollo HTTP sulla porta 8080 e si aspettano di trovare un db mongo all'hostname mongo.

Istruzioni:
  - Creare il Dockerfile per entrambi le APP
  - Creare un Compose file che comprende:
    - I due applicativi
    - Il server MongoDB
    - che faccia il bind delle porte degli applicativi sull'host

Migliorativi:
  - Ridurre al minimo le dimensioni dell'immagine Docker
  - Configurare la cache per le dipendenze Maven in fase di build
  - Ottimizzare l'utilizzo della RAM da parte della JVM
  - aggiungere al docker compose Un server proxy in ascolto sulla porta 80 che inoltri il traffico in base all'url.
      /api/products per il container 2.1-shop-catalog
      /api/acquisti per il container 2.2-shop-purchase

Requisiti per la creazione dell'immagine:
  - Java JDK 12
  - Maven 3

Requisiti per l'esecuzione del container:
  - Java JDK 12
  - MongoDB 4
