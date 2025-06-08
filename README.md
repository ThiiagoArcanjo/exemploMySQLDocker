# Docker básico de MySQL.

## Como usar? 

* 1 - Crie uma rede da sua preferencia com o comando docker network create, usei o exemplo thiago_network(<b>docker network create</b> thiago_network).

* 2 - Adicione essa rede nas linhas 8, 30 e 42 do arquivo docker-compose.yml(que encontra-se na raiz da pasta)

* 3 - Crie uma pasta na raiz da pasta chamada mysql, pois na linha 14 ela é mapeada para o container;

* 3.1 -(Se houver erros de permissão)Torne o usuário mysql dono dessa pasta chown -R 999:999

* 4 - Copie o arquivo da pasta config dbcopy.env, cole-o na pasta  raiz do projeto como .env

* 5 - Abra o arquivo recém renomeado .env e mude as variaveis de ambiente de acordo com a sua preferência, obs: o caminho da pasta é a pasta mysql que você criou.

* 6 - Inicie o container com docker compose up

## Como acessar esse servidor? O.O
* Para acessar no workbanch basta usar o seu localhost(127.0.0.1) na porta 3307, mas somente fora do container(do seu host para o container). Se for acessar o BD por outra aplicação, caso esteja na rede que você criou, basta usar a porta 3306(propria do mysql).
* Se precisar acessar o phpmyadmin, basta colocar localhost:8080(por que mapeamos) o servidor é mysql, usuario pode ser root ou oque você criou e as senhas são as definidas por você mesmo no env.