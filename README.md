# Modelagem Cenário E-Commerce
# Bootcamp Database Experience <https://web.dio.me/track/database-experience>

Após várias aulas foi proposto o desafio de fazer a modelagem do mini-mundo de um e-commerce, dentro da pasta está o arquivo gerado no MySQL e a exportação em PDF.

## Desafio

O esquema deverá ser adicionado a um repositório do Github para futura avaliação do desafio de projeto. Adicione ao Readme a descrição do projeto conceitual para fornecer o contexto sobre seu esquema.

## Objetivo

Refine o modelo apresentado acrescentando os seguintes pontos:
* Cliente PJ e PF – Uma conta pode ser PJ ou PF, mas não pode ter as duas informações;
* Pagamento – Pode ter cadastrado mais de uma forma de pagamento;
* Entrega – Possui status e código de rastreio;

#### O que foi feito

##### Cliente PJ e PF – Uma conta pode ser PJ ou PF, mas não pode ter as duas informações;
Na entidade cliente alterei o atributo identificação para CPF/CNPJ e coloquei como UNIQUE, dessa forma o idCliente terá que ser um ou outro, não poderá ser os dois.

##### Pagamento – Pode ter cadastrado mais de uma forma de pagamento;
Criei uma entidade Condições de Pagamento e fiz o relacionamento N pra N com a entidade Pedido, dessa forma poderá ser usado várias condições de pagamento no pedido.

Criei uma entidade Forma de pagamento e fiz o relacionamento dela com a entidade cliente de 1 pra N.

Fiz o relacionamento da entidade Formas de pagamento com a pedido de N pra N gerando assim uma nova tabela.

##### Entrega – Possui status e código de rastreio;
Como já possui o atributo Status do Pedido na entidade pedido, adicionei o atributo código do rastreiro.
