# UX-UI---Atividade-Teste-de-Caixa-Branca

# Teste Caixa Branca - Sistema de Login e Autenticação em Java

Este projeto é uma implementação básica de um sistema de autenticação utilizando Java e conexão com banco de dados. O objetivo é validar as credenciais de um usuário e retornar o resultado da autenticação.

---

## Estrutura do Projeto

O projeto está dividido em:

- **src/login/User.java**: Classe principal que contém os métodos para conectar ao banco de dados e verificar o login do usuário.
- **docs/**: Documentação Javadoc gerada a partir do código.
- **bin/**: Arquivos gerados pela compilação do código.

---

## Documentação do Projeto

A documentação foi gerada com a ferramenta Javadoc e descreve as classes, métodos e atributos utilizados no projeto. Para acessá-la:

1. Baixe o repositório.
2. Abra a pasta `docs`.
3. Clique no arquivo `index.html` e visualize no navegador.

---

## Funcionalidades Implementadas

1. **Conexão ao Banco de Dados**:
   - Estabelece conexão com um banco MySQL utilizando `DriverManager`.
   - Detalhes de autenticação estão configurados diretamente na string de conexão.

2. **Validação de Credenciais**:
   - Verifica o login e a senha fornecidos.
   - Retorna `true` se as credenciais forem válidas, junto com o nome do usuário.

---

## Instruções para Compilar e Executar

### Compilação
Use o terminal para compilar o código Java. Execute o seguinte comando no diretório raiz do projeto:

```bash
javac -d bin src/login/User.java
