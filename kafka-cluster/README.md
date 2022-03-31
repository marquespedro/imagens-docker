
Acessa a maquina para criacao do topico
    docker exec -it kafka-cluster_kafka-1_1 bash

Cria o topico 
    kafka-topics --create --bootstrap-server localhost:29092 --replication-factor 3 --partitions 3 --topic meutopico 

Listar topico criado 
    kafka-topics --list --bootstrap-server localhost:29092