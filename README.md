# Exercicios_SQL_CRUD
Exercícios realizados no curso "Curso de SQL com MYSQL: Manipule e Consulte Dado" da Alura.

### Segue códigos aprendidos no curso:
    CREATE DATABASE LOJA2;

    DROP DATABASE LOJA2;

    CREATE DATABASE LOJA;

    USE loja;

    CREATE TABLE tbvendedores2 (
    MATRICULA VARCHAR(5),
    NOME VARCHAR(100),
    COMISSAO FLOAT
    );

    DROP TABLE tbvendedores2;

    CREATE TABLE tbvendedores (
    MATRICULA VARCHAR(5),
    NOME VARCHAR(100),
    COMISSAO FLOAT
    );

    INSERT INTO tbvendedores (
    MATRICULA, NOME, COMISSAO) VALUES (
    00233, 'João Geraldo da Fonseca', 0.10);

    INSERT INTO tbvendedores (
    MATRICULA, NOME, COMISSAO) VALUES (
    00235, 'Márcio Almeida Silva', 0.08);

    INSERT INTO tbvendedores (
    MATRICULA, NOME, COMISSAO) VALUES (
    00236, 'Cláudia Morais', 0.08);

    UPDATE tbvendedores SET COMISSAO = 0.11
    WHERE MATRICULA = 00236;

    UPDATE tbvendedores SET NOME = 'José Geraldo da Fonseca Junior'
    WHERE MATRICULA = 00233;

    DELETE FROM tbvendedores WHERE MATRICULA = 00233;

    ALTER TABLE tbvendedores ADD PRIMARY KEY (MATRICULA);

    ALTER TABLE tbvendedores ADD COLUMN (DATA_ADMISSAO DATE);

    ALTER TABLE tbvendedores ADD COLUMN (DE_FERIAS VARCHAR(3));

    UPDATE tbvendedores SET DATA_ADMISSAO = '2014-08-15'
    WHERE MATRICULA = 00235;

    UPDATE tbvendedores SET DE_FERIAS = 'Não'
    WHERE MATRICULA = 00235;

    UPDATE tbvendedores SET DATA_ADMISSAO = '2013-09-17'
    WHERE MATRICULA = 00236;

    UPDATE tbvendedores SET DE_FERIAS = 'Sim'
    WHERE MATRICULA = 00236;

    INSERT INTO tbvendedores (
    MATRICULA, NOME, COMISSAO, DATA_ADMISSAO, DE_FERIAS) VALUES (
    00237, 'Roberta Martins', 0.11, '2017-03-18', 'Sim');

    INSERT INTO tbvendedores (
    MATRICULA, NOME, COMISSAO, DATA_ADMISSAO, DE_FERIAS) VALUES (
    00238, 'Péricles Alves', 0.11, '2016-08-21', 'Não');

    SELECT * FROM tbvendedores;

    SELECT NOME, MATRICULA FROM tbvendedores;

    SELECT * FROM tbvendedores WHERE NOME = 'Cláudia Morais';

    SELECT * FROM tbvendedores WHERE COMISSAO > 0.10;

    SELECT * FROM tbvendedores WHERE YEAR(DATA_ADMISSAO) >= 2016;

    SELECT * FROM tbvendedores WHERE DE_FERIAS = 'Sim' AND YEAR(DATA_ADMISSAO) < 2016;
