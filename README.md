# DSDocker

## Ferramentas utilizadas

   * JDK 11
   * STS
   * Postman
   * Git
   * Postgres
   * pgMyAdmin
   * Docker
   * PowerShell
   * Versão do maven 2.4.4

## Sobre o projeto

Neste projeto eu aprendi. Criar projeto Spring Boot, criar monorepositório Git, organizar projeto em camadas, criar entidades, perfis de projeto, seeding da base de dados, criar web services REST, padrão DTO, CRUD completo, tratamento de exceções, dados de auditoria e paginação de dados, trabalhar com Postman para testar as requisições, validação de dados com Bean Validation, autenticação e autorização com OAuth2 e JWT
   
  
## Arquivos de configuração:

   ### application.properties
   
         spring.profiles.active=${APP_PROFILE:test}

         spring.jpa.open-in-view=false

         security.oauth2.client.client-id=${CLIENT_ID:dscatalog}
         security.oauth2.client.client-secret=${CLIENT_SECRET:dscatalog123}

         jwt.secret=${JWT_SECRET:MY-JWT-SECRET}
         jwt.duration=${JWT_DURATION:86400}

   
   ### application-prod.properties
   
         spring.datasource.url={DB_URL}
         spring.datasource.username={DB_USERNAME}
         spring.datasource.password={DB_PASSWORD}

         spring.jpa.database-platform=org.hibernate.dialect.PostgreSQLDialect
         spring.jpa.properties.hibernate.jdbc.lob.non_contextual_creation=true
         spring.jpa.hibernate.ddl-auto=none
	 
	 
### Arquivo File criado na raiz no meu projeto

```java
     FROM openjdk:11
     VOLUME /tmp
     EXPOSE 8080
     ADD ./target/dscatalog-0.0.1-SNAPSHOT.jar dscatalog.jar  
     ENTRYPOINT ["java", "-jar", "/dscatalog.jar"]
  
 ````
 
 ## Comandos git
 
 ```java
    - ./mvnw -v 
    - ./mvnw clean package
    

 
 ```
 
 ## No PowerShell
 ```java
   - colar o caminho do meu arquivo. Lembra que esse comando é sempre onde esta minha pasta target
   - docker build -t nomeImagem:v1 .
	}
}

 ````
 
 
 
