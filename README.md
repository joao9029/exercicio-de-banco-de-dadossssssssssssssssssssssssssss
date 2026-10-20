

CREATE DATABASE Exercicio;
USE Exercicio;

DELIMITER $$

CREATE FUNCTION Aluno (nome_aluno VARCHAR(100)) 
RETURNS VARCHAR(100)
DETERMINISTIC
BEGIN 
    SET nome_aluno = 'João lucas'; 
    RETURN CONCAT(nome_aluno); 
END $$

DELIMITER ;
select concat('Ola, me chamo ');

-- Forma correta de chamar a função:
SELECT Aluno('Qualquer Texto');
