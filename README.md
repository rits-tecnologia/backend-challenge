# Backend Challenge - Rits Tecnologia
Desafio para desenvolvedor backend para Rits Tecnologia.

Por esse desafio, o desenvolvedor deverá mostrar ser capaz de desenvolver uma API RESTFul para criar pedidos de uma lanchonete, e um painel administrativo para cadastrar os produtos e gerenciar os pedidos.

## Instruções para entrega
- Seu código deverá ser versionado com Git e hospedado no GitHub;
- Crie um README.md explicando como solucionou o problema, como poderemos executar e outros pontos que achar necessário;
- Envie um e-mail para daniellopes@rits.com.br como o assunto "Desafio desenvolvedor Backend" seguido da senioridade que desejará ser avaliado (Júnior, Pleno ou Sênior).

## Sobre o problema
O Sistema deverá contemplar os módulos: Cliente, Produto e Pedido. Um Pedido pertence a um Cliente, e contém vários produtos.

A API será utilizada para o _client_ que irá realizar os pedidos. Nesse sentido, ela deverá conter _endpoints_ para que um __Cliente__ possa se cadastrar. Além de `criar`, `listar`, `ver` e `excluir` __Pedidos__ de um __Cliente__ específico. Obs.: Para evitar autenticação, o id do __Cliente__ pode ser usado como parâmetro para realizar essas ações.

O painel administrativo deve conter uma autenticação básica. E através dele deverá ser possível `listar` __Clientes__ e `listar` __Pedidos__, além de poder gerenciar os __Produtos__ da lanchonete, com as ações `CRUDL`.

Os campos para cada entidade serão:
- Cliente: `nome`, `email`, `telefone` e `endereço`;
- Produto: `nome` e `preço`;
- Pedido: `código do cliente`, `código do produto`, `data de criação` e `status do pedido`.

O __Pedido__ poderá conter os `status`: `Pendente`, `Em preparo`, `Em entrega`, `Entregue` e `Cancelado`.

## Requisitos para Desenvolvedor Júnior
- Não poderá existir mais de um __Cliente__ com o mesmo `email` ou `telefone`;
- Todos os dados deverão ser validados.

## Requisitos para Desenvolvedor Pleno
- Todos os requisitos do programador Júnior;
- A cada troca de `status` do __Pedido__, o __Cliente__ deverá ser notificado por e-mail do `status` do seu __Pedido__;
- Quando um __Pedido__ for criado, um e-mail deverá ser disparado para um e-mail pré-configurado no `.env` da aplicação;
- Os disparos de e-mail deverão ser processados por uma _queue_ à parte.

## Diferenciais
- Testes unitários;
- Estrutura pra subir a aplicação com `DockerFile` ou `docker-compose`;
- Um _bot_ no Telegram, que recebe quando um __Pedido__ é criado ou cancelado;
- Aplicação de padrões de projeto como `Repository`, `Service Layer` ou `Command Pattern`.

## Critérios de avaliação
- Profundidade de conhecimento do framework;
- Organização do código;
- Fidelidade aos requisitos;
