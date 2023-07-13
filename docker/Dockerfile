FROM openjdk:17-oracle
LABEL maintainer rita.nordtug@mastercard.com
RUN apt-get -y install git
RUN git clone -q https://github.com/rita-nordtug/helloworld.git
WORKDIR helloworld
RUN ./gradlew build
EXPOSE 8080
RUN java -jar build/libs/helloworld-0.0.1-SNAPSHOT.jar com.example.helloworld.HelloworldApplication

CMD ["gradlew", "build"]

