# DB
Um framework PHP simples e leve para trabalhar com bancos de dados.

## Sobre o projeto
Este projeto é um framework PHP que facilita a conexão e a manipulação de bancos de dados relacionais. Ele usa uma classe SQL para executar consultas SQL e retornar os resultados como objetos PHP. Ele também possui um arquivo de depuração que permite testar as consultas SQL e ver os erros.

## Como usar
Para usar este framework, você precisa seguir estes passos:

- Clone este repositório na sua máquina local.
- Inclua o arquivo DBFramework.php no seu script PHP.
- Crie uma instância da classe DBFramework e passe os parâmetros de conexão do seu banco de dados (host, usuário, senha e nome do banco de dados).
- Use os métodos da classe DBFramework para executar consultas SQL e obter os resultados como objetos PHP.
- Use o arquivo debug.php para testar as suas consultas SQL e ver os erros.

## Exemplo
Aqui está um exemplo de como usar este framework para inserir um registro em uma tabela chamada users:

```php
<?php
// Inclui o arquivo DBFramework.php
include 'DBFramework.php';

// Cria uma instância da classe DBFramework
$db = new DBFramework('localhost', 'root', '', 'test');

// Define uma consulta SQL para inserir um usuário
$sql = "INSERT INTO users (name, email) VALUES ('Samuel', 'samuel@gmail.com')";

// Executa a consulta SQL e verifica se houve sucesso
if ($db->execute($sql)) {
  echo "Usuário inserido com sucesso!";
} else {
  echo "Erro ao inserir usuário: " . $db->error;
}
?>
```
