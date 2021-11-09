# Backend Challenge - Rits Tecnologia
Desafio para desenvolvedor backend para Rits Tecnologia.

Por esse desafio, o desenvolvedor deverá mostrar ser capaz de desenvolver uma API RESTFul, para criar pedidos de uma lanchonete, e um painel administrativo para cadastrar os produtos e gerenciar os pedidos.

## Instruções para entrega
- Seu código deverá ser versionado com Git e hospedado no GitHub;
- Crie um README.md explicando como solucionou o problema, como poderemos executar e outros pontos que achar necessário;
- Envie um e-mail para lucassoares@rits.com.br com o assunto "Desafio desenvolvedor Rits".

## Sobre o problema
O Sistema deverá contemplar os módulos: __Cliente__, __Produto__ e __Pedido__. Um __Pedido__ pertence a um __Cliente__ e um __Pedido__ contém vários __Produtos__.

A API será utilizada para o _client_ que irá realizar os pedidos. Nesse sentido, ela deverá conter _endpoints_ para que um __Cliente__ possa se cadastrar. Além de `criar`, `listar`, `ver` e `excluir` __Pedidos__ de um __Cliente__ específico. Obs.: Para evitar autenticação, o id do __Cliente__ pode ser usado como parâmetro para realizar essas ações.

O painel administrativo deve conter uma autenticação básica. E através dele deverá ser possível `listar` __Clientes__ e `listar` __Pedidos__, além de poder gerenciar os __Produtos__ da lanchonete, com as ações `CRUD`.

Os campos para cada entidade serão:
- Cliente: `nome`, `email`, `telefone` e `endereço`;
- Produto: `nome` e `preço`;
- Pedido: `código do cliente`, `código do produto`, `data de criação` e `status do pedido`.

O __Pedido__ poderá conter os `status`: `Pendente`, `Em preparo`, `Em entrega`, `Entregue` e `Cancelado`.

## Requisitos
- Não poderá existir mais de um __Cliente__ com o mesmo `email` ou `telefone`;
- Todos os dados deverão ser validados;
- Um __Cliente__ não pode excluir um __Pedido__ criado por outro __Cliente__.

## Diferenciais
- Testes unitários;
- Estrutura pra subir a aplicação com `DockerFile` ou `docker-compose`;
- Um _bot_ no Telegram, que recebe quando um __Pedido__ é criado ou cancelado;
- Aplicação de padrões de projeto como `Repository`, `Service Layer` ou `Command Pattern`;
- Uma notificação em tempo real de quando um __Pedido__ for criado ou cancelado.

## Critérios de avaliação
- Profundidade de conhecimento do framework escolhido;
- Organização do código;
- Fidelidade aos requisitos;
