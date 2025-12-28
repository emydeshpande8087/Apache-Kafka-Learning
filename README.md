# learning_apache_kafka
My learning for apache kafka

#For starting the kafka server and kafka UI 
docker compose up -d 

#Scripts are located at 
cd /opt/kafka/bin


#create a topic 
/opt/kafka/bin/kafka-topics.sh --create --topic <topicname> --bootstrap-server localhost:9092

#create producer 
/opt/kafka/kafka-console-producer.sh --topic expense_data --bootstrap-server localhost:9092
#then put whatever message you wanted here in this.


#create consumer  
/opt/kafka/kafka-console-consume.sh --topic expense_data --bootstrap-server localhost:9092

#start a producer with multiple partitions 
/opt/kafka/kafka-console-producer.sh --topic expense_data --bootstrap-server localhost:9092 --partitions 3 

#start a consumer within a group 
./kafka-console-consumer.sh --topic expense-data-partitioned --from-beginning --bootstrap-server localhost:9092 --group my-app