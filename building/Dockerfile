FROM bitnami:java:latest
RUN apt-get update -y && apt-get upgrade -y

RUN apt-get install git -y
RUN apt-get install default-jdk -y
RUN apt-get install gradle -y

RUN git clone https://github.com/Patuuuska/java-todo-jenkins
WORKDIR /ToDo

RUN gradle build