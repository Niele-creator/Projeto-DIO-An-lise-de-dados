E-commerce - Modelo de Banco de Dados

Descrição do Projeto

Este projeto consiste na modelagem conceitual de um banco de dados para um sistema de E-commerce. O esquema foi refinado para incluir os seguintes requisitos adicionais:

Cliente PJ: O sistema permite que uma conta seja cadastrada como Pessoa Jurídica (PJ);

Pagamento: Os clientes podem cadastrar múltiplas formas de pagamento;

Entrega: Cada pedido possui status de entrega e código de rastreamento.


Modelo Conceitual

O banco de dados foi estruturado para suportar operações essenciais de um e-commerce, garantindo eficiência no armazenamento e recuperação de dados. O modelo contém as seguintes entidades principais:

Tabelas Principais

1. Clientes

id_cliente (PK)

nome

email

telefone

tipo_cliente (PJ ou PF)

cnpj (nullable para PF)



2. Endereços

id_endereco (PK)

id_cliente (FK)

logradouro

cidade

estado

cep



3. Pagamentos

id_pagamento (PK)

id_cliente (FK)

tipo_pagamento (Cartão, Boleto, Pix, etc.)

detalhes



4. Produtos

id_produto (PK)

nome

descricao

preco

estoque



5. Pedidos

id_pedido (PK)

id_cliente (FK)

data_pedido

valor_total

status_pedido



6. Itens do Pedido

id_item (PK)

id_pedido (FK)

id_produto (FK)

quantidade

preco_unitario



7. Entrega

id_entrega (PK)

id_pedido (FK)

status_entrega

codigo_rastreamento

data_envio

data_entrega_prevista
