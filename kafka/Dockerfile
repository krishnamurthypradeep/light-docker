FROM openjdk:8-jdk
RUN wget -q -O - http://www.us.apache.org/dist/kafka/2.0.0/kafka_2.12-2.0.0.tgz |  tar -xzf - -C /usr/local
WORKDIR /usr/local/kafka_2.12-2.0.0
EXPOSE 9092
VOLUME /usr/local/kafka-config
ADD ./config/server.properties /usr/local/kafka-config/server.properties
ADD run-kafka.sh /usr/local/kafka_2.12-2.0.0/run-kafka.sh
CMD ./run-kafka.sh
