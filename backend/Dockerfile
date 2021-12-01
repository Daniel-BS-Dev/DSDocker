FROM openjdk:11
VOLUME /tmp
EXPOSE 8080
ADD ./target/dscatalog-0.0.1-SNAPSHOT.jar dscatalog.jar  
ENTRYPOINT ["java", "-jar", "/dscatalog.jar"]

# esta criando uma imagem aparti do jdk
#./target/nome.jar nome.jar    -> é um arquivo gerado na pasta build
#["java", "-jar", "/nome.jar"] -> como vai rodar