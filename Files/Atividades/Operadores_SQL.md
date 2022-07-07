 # Exercícios de Fixação
~~~
CREATE TABLE tbProdutos(id int PRIMARY KEY, descricao
varchar(80) not null, preco float, quantidadeEstoque int, unidade
varchar(10), fornecedor varchar(100));
~~~

***1. Crie sentenças SQL para inserir 6 produtos na tabela acima.***
~~~
INSERT INTO tbProdutos
VALUES
(35, "Ração alcon, pára curió.",  29.90,  500, "Kg", "Bruno da ração"),
(89, "Pizzas de ótima qualidade.",  39.90,  -30, "UN", "Nobrus pizzaria"),
(12, "Garotinho muito bonitinho, chamado Bruno.",  50.00,  1, "UN", "Shopee"),
(10, "Tênis Air Jordan",  1000.00,  400, "UN", "Vandin Shopee"),
(55, "Celular NOKIA",  300.00,  50, "UN", null),
(65, "Tênis Jordan Adidas", 210.00, -50, "UN", "Estevão Sapatos");
~~~
##

***2. Crie sentenças SQLs para responder as seguintes questões.***

- a) Quais produtos custam entre R$ 200 e R$ 500?
~~~
SELECT * FROM tbProdutos
WHERE preco BETWEEN 200 and 500;
~~~

- b) Mostre o nome e o preço dos produtos que não têm fornecedor cadastrado.
~~~
SELECT descricao, preco FROM tbProdutos
WHERE fornecedor IS NULL;
~~~

- c) Mostre os produtos com quantidade em estoques acima de 300 ou negativas.
~~~
SELECT * FROM tbProdutos
WHERE quantidadeEstoque > 300 OR quantidadeEstoque < 0;
~~~

- d) Mostre todos os dados dos sapatos(todos os tipos de sapatos)
~~~
SELECT * FROM tbProdutos
WHERE descricao LIKE 'tênis%';
~~~

- e) Quais o preço, unidade e quantidade em estoque dos produtos com IDs 35, 89, 23, 10, 50, 65.
~~~
SELECT preco, unidade, quantidadeEstoque FROM tbProdutos
WHERE id IN(35, 89, 23, 10, 50, 65);
~~~
##



