# Docker básico de MySQL.

## Como usar? 

* 1 - Crie uma rede da sua preferencia com o comando docker network create,  usei o exemplo thiago_network(<b>docker network create</b> thiago_network).

* 2 - Adicione essa rede nas linhas 10 e 21 do arquivo docker-compose.yml(que encontra-se na raiz da pasta)

* 3 - Crie uma pasta na raiz da pasta chamada mysql, pois na linha 12 ela é mapeada para o container;

* 4 - Copie e cole o arquivo dbcopy.env na mesma pasta e renomeio para db.env

* 5 - abra o arquivo recém renomeado db.env e mude as variaveis de ambiente de acordo com a sua preferencia.

* 7 - Na pasta do projeto use docker compose up -d para subir o servidor e docker compose down para para-lo.