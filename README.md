# mongodb-introducao

Atividade proposta na aula de Banco de dados não relacional
As ferramentas utilizadas foram MongoDB Compass e Shell

Resolução exercícios MongoDB

4- db.livros.find().count() = 431 => comando find para encontrar todos os registros, com count para mostrar a quantidade de registros

5 - db.livros.find({pageCount:{$lte: 100}}).pretty().count() = 166 => comando com condição de nº de páginas <= 100
6 - db.livros.find({isbn:{$lte: "1617200000"}}).pretty().count() = 22 => comando com condição de campo isbn <= 1617200000

6.1 - db.livros.find({isbn:{$gt: "1933988746"}}).pretty().count() = 85 => comando com condição de campo isbn > 1933988746


9 - db.livros.find({isbn:{$lte:"10"}}).count() = 4 => comando com condição de campo isbn <= 10
9.1 - db.livros.find({isbn:{$lte:"100"}}).count() = 5 => comando com condição de campo isbn <= 100

10 - db.livros.find({isbn:{$lte:"10"}}).pretty().limit(2).count() = 2 => comando com condição de campo isbn <= 10 limitando a mostrar 2 registros

11- db.livros.find({isbn:{$lte: "100"}}).pretty().skip(2) = Multimedia Computing, Implementing SAP R/3, Second Edition e Saci Pererê. => comando com condição de campo isbn <= 100 pulando os 2 primeiros registros encontrados

12 - db.livros.find({title: /Windows/}).count() = 11
O \Windows\  funciona como o LIKE no mundo SQL

13 – db.livros.find( { }, {“pageCount”: 1}).sort({“pageCount”: -1}).limit(2) = 1101 e 1096. => Utilização de ordenação decrescente e mostrando apenas id por padrão e quantidade de paginas no resultado
