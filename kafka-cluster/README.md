
## Acessa a maquina para criacao do topico
    # docker exec -it kafka-cluster_kafka-1_1 bash

## Cria o topico 
    # kafka-topics --create --bootstrap-server localhost:29092 --replication-factor 3 --partitions 3 --topic meutopico 

## Listar topico criado 
    # kafka-topics --list --bootstrap-server localhost:29092
    
## se conecta ao topico criado (meutopico) como um PRODUCER no broker localhost:29092 afim de enviar as mensagens via console
    # kafka-console-producer --broker-list localhost:29092 --topic meutopico
 
## se conecta ao topico criado (meutopico) como um CONSUMER no broker localhost:29092 afim de enviar as mensagens via console
    # kafka-console-consumer --bootstrap-server localhost:29092 --topic meutopico
