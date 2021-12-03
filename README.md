# DSDocker

## Ferramentas utilizadas

   * JDK 11
   * STS
   * Postman
   * Git
   * Postgres
   * pgAdmin
   * Docker
   * PowerShell
   * Versão do maven 2.4.4

## Imagens, Containers e Registry

- Imagens: 
    É a difinição estatica de como um container deve ser instânciado, uma imagem é composta por camada, uma imagem tipicamente é difinida de outra imagem existente, 
uma imagem inicial é dfinida a partir de scratch
- Contanier:
  É uma instância de uma imagem pode estar em execução ou parado, container é stateful: mantém estado. Ele possui  uma camada superior de escrito
- Registry:
   É um serviço que armazena imagens, registry padrão para Docker:Docker Hub
 
 ## Comandos Docker
 
 - docker ps :->                                Lista os containers
 - docker ps -a:->                            Lista os container inclusive os parados
 - docker pull image:tag:->                     Baixar uma imagem do docker hub
 - docker imagens:->                           Listar as imagens baixadas
 - docker run options image:tag command args:-> Iniciar um container com base em uma imagem se não estiver baixada baixa do docker hub
 - docker start:-> Reinicia um container
 - docker stop:-> Parar o container
 - docker rm idContainer:-> Deletar um container
 - docker rmi IdConatiner:-> Deleta imagem
 - docker attach:-> Acessar o container
 - docker logs -f idContainer:-> Acompanhar os logs do container
 - docker ps --size:-> Mostar o espaço em bits ocupados pelo container
 - exit:-> Parar sair IdContainer
 - ls:-> Para ver se estar dentro do container


## Instâciando um container Postgres

docker run -p 5433:5432 --name nomeDoContainer -e POSTGRES_PASSWORD=123456 -e POSTGRES_DB=minha_base nomeDaMinhaImagem
 
  
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
	 
	 



 
 
 
