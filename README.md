# Docker básico de MySQL.

## Como usar? 

* 1 - Crie uma rede da sua preferencia com o comando docker network create, usei o exemplo thiago_network(<b>docker network create</b> thiago_network).

* 2 - Adicione essa rede nas linhas 10, 23 e 32 do arquivo docker-compose.yml(que encontra-se na raiz da pasta)

* 3 - Crie uma pasta na raiz da pasta chamada mysql, pois na linha 12 ela é mapeada para o container;

* 4 - Copie e cole o arquivo dbcopy.env na mesma pasta e renomeio para db.env

* 5 - Abra o arquivo recém renomeado db.env e mude as variaveis de ambiente de acordo com a sua preferencia.

* 7 - Na pasta do projeto use docker compose up -d para subir o servidor e docker compose down para para-lo.

## Como acessar esse servidor? O.O
* Para acessar no workbanch basta usar o seu localhost(127.0.0.1) na porta 3307, mas somente fora do container(do seu host para o container). Se for acessar o BD por outra aplicação, caso esteja na rede que você criou, basta usar a porta 3306(propria do mysql).
* Se precisar acessar o phpmyadmin, basta colocar localhost:8080(por que mapeamos) o servidor é mysql, usuario pode ser root ou oque você criou e as senhas são as definidas por você mesmo no env.