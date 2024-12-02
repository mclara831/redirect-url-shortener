# URL Shortener & Redirector
Este é um projeto de encurtador e redirecionador de URLs desenvolvido como parte de um curso sobre tecnologias AWS e Java.
A aplicação é projetada para criar URLs encurtadas que redirecionam para destinos específicos, utilizando serviços
serverless da AWS para garantir escalabilidade e alta disponibilidade.

Este projeto foi desenvolvido no Curso Gratuito de Java + AWS da Rocketseat, ministrado pela Fernanda Kipper.

## 📜 Descrição
A aplicação permite encurtar URLs longas, armazená-las de forma eficiente e redirecionar os usuários ao destino
original ao acessar o link encurtado. A arquitetura serverless foi implementada para reduzir custos operacionais
e aumentar a flexibilidade.

## 🛠️ Tecnologias Utilizadas
* **Java 17**: Linguagem principal para desenvolvimento da lógica da aplicação.
* **AWS Lambda**: Para processamento serverless e execução de código em resposta a eventos.
* **Amazon S3**: Armazenamento de dados, incluindo gerenciamento de buckets para persistência das URLs.
* **Amazon API Gateway**: Exposição de endpoints HTTP para acesso à aplicação.
* **Jackson**: Biblioteca para manipulação de dados em JSON.

## 📦 Estrutura do Projeto
O projeto está dividido em duas Lambdas:
* **Create Shortener URL**: Responsável por gerar o código encurtado e armazenar os dados no S3.
* **Redirect Shortener URL**: Responsável por redirecionar o usuário para o URL original.

## API's endpoints
#### Create Shortener URL
```bash
POST /create - cria e retorna o id da URL encurtada dado a URL original e o tempo de expiração passadaos no body da requisição.
```

#### Redirect Shortener URL
```bash
 GET /{shortURL} - redireciona o usuário para URL original por meio id da URL encurtada passada como parâmetro.
```