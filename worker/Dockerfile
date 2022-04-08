FROM  maven:3.8.4-jdk-11-slim

COPY . /worker

WORKDIR /worker

RUN mvn dependency:resolve

RUN mvn package

RUN cp /worker/target/worker-jar-with-dependencies.jar .

CMD ["java", "-jar", "worker-jar-with-dependencies.jar"]