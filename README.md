# Coleta de dados do banco MYSQL usando o Elasticsearch
Uso do Elasticsearch, Kibana e Logstash, de forma conteinerizada usando Docker.  O plugin JDBC também foi instalado no Logstash e configurado para ler dados do banco de dados MySQL e indexá-los no Elasticsearch. 


## Dependências
    Docker
    Docker Compose

## Instalação e Execução
    1. Clone este repositório em sua máquina local
    2. Na raiz do projeto, execute o comando 'docker-compose up -d' para baixar as imagens e iniciar os containers
    3. Acesse a aplicação através da URL http://172.21.0.15:5601

### Criando um índice no Kibana

Para criar um índice (index) no Kibana, siga os seguintes passos:

    1. Faça login no Kibana;
    2. Na página inicial, clique em "Management" no menu lateral esquerdo;
    3. Em seguida, clique em "Stack Management";
    4. Clique em "Index Patterns" para acessar a tela de criação de padrões de índice;
    5. Na tela de criação de padrões de índice, clique em "Create index pattern";
    6. Digite o nome do índice que deseja criar, no seu caso "logs-carol", e clique em "Next step";
    7. Na próxima tela, selecione o campo de data como "Time Filter field name", selecione o formato correto e clique em "Create index pattern";
    8. Pronto, agora você tem um novo índice criado no Kibana.
   
    Lembrando que é necessário ter pelo menos um índice criado no Elasticsearch para que ele apareça na lista de índices disponíveis para criação no Kibana.
