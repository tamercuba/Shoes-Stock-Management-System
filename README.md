# Shoe Stock Inventory Management System

> Uma aplicação de controle de estoque de calçados construida sob arquitetura REST.

## Descrição

Escrito em Python + Django e utilizando o Django Rest Framework para a implementação da arquitetura REST, o SSIMS visa fornecer uma CRUD para gerenciar um sistema de estoque de calçados.


## Features

A aplicação retorna valores JSON a partir dos seguintes endpoints:

Método HTTP | URL | Comportamento
------------|-----|---------------
`GET` | `api/resources/` | Retorna lista paginada de calçados
`POST`| `api/resources/` | Adiciona um novo calçado
`GET` | `api/resources/id` | Retorna um calçado existente
`PUT` | `api/resources/id` | Altera as informações de um calçado existente
`PATCH` | `api/resources/id` | Altera parcialmente as informações de um calçado existente
`DELETE` | `api/resources/id` | Remove um calçado existente

## Depêndencias

Pacote | Versão
------ | -------
Django | 2.2.1  
djangorestframework | 3.9.4  
pip | 19.1.1
psycopg2 | 2.8.2  
python-decouple | 3.1    
pytz | 2019.1
setuptools | 41.0.1
sqlparse | 0.3.0  
wheel | 0.33.4

## Tutorial de Instalação

1. Primeiramente crie um diretório raiz para o SSIMS no seu computador executando `mkdir SSIMS_ROOT` no seu terminal e entre no diretório com `cd SSIMS_ROOT`.
2. Caso não tenha, instale o `VirtualEnv` utilizando `pip install virtualenv` (lembre-se que o projeto utiliza Python 3, se o seu Sistema Operacional utilizar o 2 como padrão talvez você tenha que usar `pip3`)
3. Localize o diretório raiz do Python 3.7 na sua máquina executando `which python3.7`
4. Agora execute `virtualenv --python=/path/to/your/python3.7 .venv` (lembre-se de substituir /path/to/your/python3.7 pelo caminho descoberto na etapa anterior, note que você pode substituir o nome `.venv` para o nome que desejar) e ative o ambiente virtual rodando `source .venv/bin/activate` (para desativá-lo basta substituir o `source` por `deactivate`).
5. Execute agora `git clone https://github.com/tamercuba/Shoes-Stock-Inventory-Management-System.git` para clonar o repositório que ficará num diretório chamado `SSIMS` dentro do diretório raiz. Entre no diretório utilizando o comando `cd SSIMS`.
6. Para baixar as depêndencias execute `pip install -r requirements.txt`.
7. Execute `touch .env`, edite esse arquivo com seu editor e texto preferido colocando as seguintes informações:
```
NAME_DB= "NOME DO BANCO"
USER_DB= "NOME DO USUÁRIO"
PW_DB= "SENHA"
HOST_DB= "ENDEREÇO"
PORT_DB= "PORTA"
```
Substitua os valores entre parenteses com as informações necessárias de um banco de dados PostgreSQL.

8. Execute `./manage.py makemigrations` em seguida execute `./manage.py migrate`.
9. Agora você ja está pronto para rodar a aplicação com o comando `./manage runserver`

## Versões

* v0.1 - ATUAL

## Contato

* [LinkedIn](https://linkedin.com/in/tamercuba)
* [Facebook](https://www.fb.com/tamercuba)
* E-mail: `tamercuba@gmail.com`
