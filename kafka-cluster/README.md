
## Acessa a maquina para criacao do topico
    # docker exec -it kafka-cluster_kafka-1_1 bash
    
## Cria o topico 
    # kafka-topics --create --bootstrap-server localhost:29092 --replication-factor 3 --partitions 3 --topic meutopico 

## Listar topico criado 
    # kafka-topics --list --bootstrap-server localhost:29092
    
## se conecta ao topico criado (meutopico) como um PRODUCER no broker localhost:29092 afim de enviar as mensagens via console
    # kafka-console-producer --broker-list localhost:29092 --topic meutopico
 
## se conecta ao topico criado (meutopico) como um CONSUMER no broker localhost:29092 afim de visualizar via console as mensagens enviadas via console
    # kafka-console-consumer --bootstrap-server localhost:29092 --topic meutopico
    
## o mesmo do comando anterior porém obtendo todas as mensagens enviadas no topico desde o inicio
    # kafka-console-consumer --bootstrap-server localhost:29092 --topic meutopico --from-beginning
    
## o mesmo do comando anterior porém consumindo de um grupo o que paraleliza o consumo das mensagens tornando mais performatico
    # kafka-console-consumer --bootstrap-server localhost:29092 --topic meutopico --from-beginning --group a

## exibe as informacoes sobre o topico
    # kafka-topics --describe --bootstrap-server localhost:29092 --topic meutopico
 
 ## exibe as informacoes sobre o grupo de consumers
    # kafka-consumer-groups --group a --bootstrap-server localhost:29092 --describe
    
     
 
