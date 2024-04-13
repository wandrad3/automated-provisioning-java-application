📘 **Tutorial de Aprovisionamento de Aplicação Java com Vagrant (Curso Devops com Imran Teli)**

ℹ️ **Arquitetura da Aplicação:**

A aplicação Java a ser aprovisionada possui os seguintes componentes e configurações:
- **Repositório da Aplicação:**
  - https://github.com/devopshydclub/vprofile-project.git 
- **Banco de Dados MySQL:**
  - Driver: `com.mysql.jdbc.Driver`
  - URL: `jdbc:mysql://db01:3306/accounts?useUnicode=true&characterEncoding=UTF-8&zeroDateTimeBehavior=convertToNull`
  - Usuário: `admin`
  - Senha: `admin123`

- **Memcached:**
  - Host Ativo:
    - Host: `mc01`
    - Porta: `11211`
  - Host StandBy:
    - Host: `127.0.0.2`
    - Porta: `11211`

- **RabbitMQ:**
  - Endereço: `rmq01`
  - Porta: `5672`
  - Usuário: `test`
  - Senha: `test`

- **Elasticsearch:**
  - Host: `192.168.1.85`
  - Porta: `9300`
  - Cluster: `vprofile`
  - Node: `vprofilenode`

🛠️ **Passos para Aprovisionamento:**

1. **Configuração do Ambiente:**
   - Instale o Vagrant em sua máquina.
   - Crie um arquivo `Vagrantfile` com as configurações necessárias para a máquina virtual.

2. **Provisionamento do Banco de Dados MySQL:**
   - Utilize o script `mysql.sh` para instalar e configurar o MariaDB.
   - Restaure o banco de dados da aplicação com o arquivo `db_backup.sql`.

3. **Provisionamento do Memcached:**
   - Execute as etapas do script `backend.sh` para instalar e configurar o Memcached.

4. **Provisionamento do RabbitMQ:**
   - Siga as instruções do script `backend.sh` para instalar e configurar o RabbitMQ.

5. **Provisionamento do Tomcat:**
   - Utilize o script `tomcat.sh` para instalar o Apache Tomcat e configurar o serviço.
   - Clone o repositório `vprofile-project` e compile o projeto com Maven.
   - Configure o Tomcat para executar a aplicação Java.

6. **Configuração da Aplicação:**
   - Atualize os arquivos de configuração da aplicação com as informações do banco de dados, Memcached, RabbitMQ e Elasticsearch.

7. **Inicialização da Aplicação:**
   - Inicie o Tomcat e verifique se a aplicação está funcionando corretamente.


