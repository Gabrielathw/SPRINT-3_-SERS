# Referências e Explicações Técnicas

Este documento reúne as referências bibliográficas, técnicas e de inteligência artificial utilizadas no desenvolvimento do projeto **ChargeVolt**, além de explicações detalhadas sobre conceitos e funções aplicados no código.

---

## Referências Utilizadas

### Disciplinas e Aulas
*   **Aulas de Data Structures and Algorithms (DSA):** Utilizadas para a lógica de programação, estruturas e a organização do código Python.
*   **Aulas de Python:** Base para toda a sintaxe, funções e bibliotecas utilizadas no projeto (datetime, time).
*   **Aulas de Computer Organization and Architecture:** Fundamentaram a compreensão de como o software se comunica com o hardware simulado (sensor do eletroposto).
*   **Aulas de Prompt and Artificial Intelligence:** Essenciais para a estruturação dos comandos e uso de IAs como ferramentas de auxílio.
*   **Aulas de Modelagem Linear para Aprendizado de Máquina:** Forneceram a base para a análise de dados e métricas de desempenho que podem ser aplicadas ao dashboard.

### Inteligência Artificial como Ferramenta de Auxílio
*   **IA (DeepSeek e Claude):** Utilizadas como ferramentas de auxílio em técnicas não desenvolvidas ou ainda não conhecidas pelo grupo, além de apoio na estruturação e revisão de partes do código.

### Documentação Oficiais
*   **Mermaid.js Documentation:** Para criação de diagramas diretamente no README do GitHub.

---

## Explicações de Conceitos do Código

### O que é ".strip().lower()'?

Essa combinação é usada para limpar e padronizar o que o usuário digita.

*   **`.strip()`**: Remove espaços em branco do início e do fim de uma string. Isso evita erros causados por espaços acidentais.
*   **`.lower()`**: Transforma todas as letras **maiúsculas em minúsculas**. Se o usuário digitar `"Admin"`, o resultado será `"admin"`.

**Exemplo no código:**

email = input("Email: ").strip().lower()
Se o usuário digitar: "  LAURA@EMAIL.COM  "
O Python transforma para: "laura@email.com"

---

### O que é "usuário demo"?
O "usuário demo" é uma conta de teste pré-cadastrada no código, criada para facilitar a vida de quem vai testar o sistema (ex: professores).
Se alguém digitar o usuário demo e a senha 123456, o sistema não vai dar erro de "usuário não encontrado". Ele vai criar automaticamente esse usuário na hora e já vai dar a ele um saldo
inicial de R$ 100,00. Isso permite testar o fluxo de recarga e pagamento sem precisar perder tempo criando um cadastro do zero toda vez que rodarem o programa.

---

### Biblioteca uuid em Python

A biblioteca uuid (Universally Unique Identifier) é utilizada para gerar identificadores únicos universais. Em vez de usar números sequenciais (como 1, 2, 3), usamos o uuid para criar códigos aleatórios e únicos.
No nosso backend, o uuid é usado para gerar o id de usuários, recargas e agendamentos. Então, mesmo que o sistema cresça e tenha milhares de registros, cada um terá um código único e rastreável.
