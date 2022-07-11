# Exercícios Práticos de fixação

***1. Crie as seguintes Tabelas: 
<br>tbProfessor(<u>siape</u> int, nome, rua, numero, bairro, cidade, cep, salarioBasico); 
<br>tbDisciplina(<u>id</u> int, nome, nomeCurso, cargahoraria).***
~~~
create table tbProfessor (
siape int primary key, 
nome varchar(50), 
rua varchar(20),
numero int,
bairro varchar(20),
cidade varchar(20),
cep int,
salarioBasico real
);

create table tbDisciplina (
id int primary key,
nome varchar(50),
nomeCurso varchar(20),
cargahoraria int
);
~~~
##

***2. Inserir 5 linhas para cada uma das tabelas criadas no item 1.***
~~~
insert into tbProfessor values
(111, 'Carlos', 'Rua 2', 23, 'Village', 'Montes CLaros', 39397888, 6000),
(222, 'Jão', 'Rua Brasil', 445, 'Centro', 'Itumbiara', 67679888, 5000),
(333, 'José', 'Rua dos bobos', 0, 'Esmero', 'Ibiracatu', 37378999, 2000),
(444, 'Bruno', 'Rua Felicidade', 328, 'Edgar Pereira', 'Mirabela', 17289000, 2500),
(555, 'Davi', 'Rua Santinho Amorim', 109, 'Vila Mauriceia', 'Montes Claros', 39491101, 20000);

insert into tbDisciplina values
(101, 'Português', 'Informática', 120),
(202, 'Programação Visual', 'Informática', 200),
(303, 'Química Analítica', 'Química', 150),
(404, 'Matemática', 'Edificações', 120),
(505, 'Banco de Dados', 'Química', 12);
~~~
##

***3. Inserir o campo formação profissional com 60 caracteres na tabela tbProfessor.***
~~~
alter table tbProfessor add formacaoProfissional varchar(60);
~~~
##

***4. Alterar o nome do professor cujo siape é 3420 para Rodrigo Carneiro Brandão.***
~~~
update tbProfessor set nome = 'Rodrigo  Carneiro Brandão'
where siape = 3420;
~~~
##

***5. Modifique o nome do professor Silvio Santos para Laércio Ives Santos.***
~~~
update tbProfessor set nome = 'Laércio Ives Santos'
where nome = 'Silvio Santos';
~~~
##

***6. Modifique o salário da professora Ana Maria Braga para R$3500,12.***
~~~
update tbProfessor set salarioBasico = 3500.12
where nome = 'Ana Maria Braga'; 
~~~
##

***7. Acrescente 30 reais para todos os professores que ganham entre R$1000,00 e R$2000,00.***
~~~
update tbProfessor set salarioBasico = salarioBasico + 30
where salarioBasico in (1000, 2000);
~~~
##

***8. Dê um aumento de 70% para os professores que ganham menos de 1000 reais.***
~~~
update tbProfessor set salarioBasico = salarioBasico + (salarioBasico * 0.7)
where salarioBasico < 1000;
~~~
##

***9. Modifique o siape de Roberto Carlos para '5234'***
~~~
update tbProfessor set siape = 5234
where nome = 'Roberto Carlos';
~~~
