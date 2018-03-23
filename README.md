docker-prediction-maki
======================

Ejecuta MAKI PredictionIO en Docker

1. Clona este repositorio

2. Construye la imagen del dockerfile 
    
    ```Bash
    $ docker build -t bigdatamx/predictionmaki .
    ```
    
3. Ejecuta el contenedor

    ```Bash
    $ docker run -p 9000:9000 -p 8000:8000 -p 7070:7070 --name predictionmaki_instance -it bigdatamx/predictionmaki /bin/bash
    ```

4. Dentro del contenedor ejecuta el siguiente comando para levantar los servicios

    ```Bash
    $ pio-start-all
    ```
   
   Verifica que los servicios esten arriba

    ```Bash
    $ jps -l
    ```

5. La consola esta disponible en el puertos 9000

### Referencias:

 * Nos basamos en este Dockerfile [docker-predictionio](https://github.com/steveny2k/docker-predictionio)


=========================

### Pendientes:

Ya que este estable hacer push al docker hub
