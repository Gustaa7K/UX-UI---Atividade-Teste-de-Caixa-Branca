# UX-UI---Atividade-Teste-de-Caixa-Branca

# Teste Caixa Branca - Sistema de Login e Autenticação em Java

Este projeto é uma implementação básica de um sistema de autenticação utilizando Java e conexão com banco de dados. O objetivo é validar as credenciais de um usuário e retornar o resultado da autenticação.

---

## Etapa 1: Erros Encontrados no Código (Teste de Caixa Branca)

1. **Ausência de logs para falhas críticas:**  
   Exceções capturadas não são registradas, dificultando a depuração e rastreamento de problemas.

   - **Correção proposta:** Utilizar bibliotecas como Log4j ou SLF4J para registrar falhas.

2. **Conexões abertas mesmo após falha:**  
   Conexões não são fechadas adequadamente, mesmo em casos de erro, podendo causar vazamentos de recursos.

   - **Correção proposta:** Implementar o uso de `try-with-resources`.

3. **Uso de variáveis globais inseguras:**  
   Atributos como `public String nome` são expostos diretamente, representando riscos à segurança e encapsulamento.

   - **Correção proposta:** Utilizar encapsulamento com modificadores de acesso adequados.

4. **Falta de validação dos parâmetros de entrada:**  
   Dados de entrada não são validados, abrindo espaço para entradas malformadas.

   - **Correção proposta:** Implementar rotinas de validação antes de executar consultas SQL.

5. **Dependência de driver JDBC desatualizado:**  
   O código utiliza `com.mysql.Driver`, que está obsoleto em versões mais recentes do MySQL JDBC.

   - **Correção proposta:** Atualizar para `com.mysql.cj.jdbc.Driver` e garantir compatibilidade com versões modernas.


---

## Instruções para Compilar e Executar

### Compilação
Use o terminal para compilar o código Java. Execute o seguinte comando no diretório raiz do projeto:

```bash
javac -d bin src/login/User.java
