# SistemaEscolar
Scripts SQL para a criação e manipulação de um banco de dados de sistema escola simples.
sistema_escolar.sql

CREATE SCHEMA IF NOT EXISTS SistemaEscolar DEFAULT CHARACTER SET utf8;
use SistemaEscolar;

CREATE TABLE IF NOT EXISTS Estudante (
    nome VARCHAR(255) ,
    email VARCHAR(255) ,
    telefone VARCHAR(255),
    altura DECIMAL(3,2),
   aprovado tinyint (1)
    ) ENGINE = InnoDB;
    
    select * from Estudante;
		INSERT INTO Estudante VALUES ('Felicia Tomaz', 'felicia@gmail.com', '6199542144', 1.70, 1);
        INSERT INTO Estudante VALUES ( 'Lais Marciel', 'luisalgusto@gmail.com', '61995465164', 1.80, 1);
        INSERT INTO Estudante VALUES ( 'Sarah Gomes', 'Gomes@gmail.com', '61995542414', 1.68, 0);
        INSERT INTO Estudante VALUES ( 'Lucas Marques', 'lucasmarques@gmail.com', '6199752345', 1.76, 1);
        INSERT INTO Estudante VALUES ( 'Clara Reis', 'clara@gmail.com', '6196435253', 1.80, 0);
        
        select avg(altura) from Estudante where aprovado = 0;
        select count(altura) from Estudante where altura>= 1.70;
        select sum(altura) from Estudante;
        select sum(altura) from Estudante where aprovado = 1;
        select max(altura) from Estudante;
        select min(altura) from Estudante;
