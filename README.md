# hierarquiadedados
<dependencies>
    <!-- Dependência do JUnit Jupiter (JUnit 5) -->
    <dependency>
        <groupId>org.junit.jupiter</groupId>
        <artifactId>junit-jupiter</artifactId>
        <version>5.10.0</version>
        <scope>test</scope>
    </dependency>
</dependencies>
-- Criação da tabela com auto-relacionamento
CREATE TABLE Funcionarios (
    id INT PRIMARY KEY,
    nome VARCHAR(100),
    cargo VARCHAR(50),
    id_supervisor INT,
    FOREIGN KEY (id_supervisor) REFERENCES Funcionarios(id)
);

-- Inserção de dados
INSERT INTO Funcionarios (id, nome, cargo, id_supervisor) VALUES (1, 'Ana', 'Diretora', NULL);
INSERT INTO Funcionarios (id, nome, cargo, id_supervisor) VALUES (2, 'Bruno', 'Gerente', 1);
INSERT INTO Funcionarios (id, nome, cargo, id_supervisor) VALUES (3, 'Carlos', 'Analista', 2);
INSERT INTO Funcionarios (id, nome, cargo, id_supervisor) VALUES (4, 'Diana', 'Estagiária', 3);
