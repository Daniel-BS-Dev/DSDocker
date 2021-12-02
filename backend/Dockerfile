FROM openjdk:11
VOLUME /tmp
EXPOSE 8080
ADD ./target/dscatalog-0.0.1-SNAPSHOT.jar dscatalog.jar  
ENTRYPOINT ["java", "-jar", "/dscatalog.jar"]

# openjdk:11                             -> esta criando uma imagem aparti do jdk
#./target/dscatalog-0.0.1-SNAPSHOT.jar   -> pega o meu projeto
# dscatalog.jar                          -> nome pra copia
#["java", "-jar", "/nome.jar"]           -> como vai rodar