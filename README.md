# Sudoku CLI - Java 21 🧩
## 🎮 Bootcamp DIO em parceria com AlmavivA - JAVA & QA

Um jogo de Sudoku interativo para terminal desenvolvido em **Java 21** desenvolvido durante o aprendizado dentro do Bootcamp.
O projeto utiliza conceitos modernos da linguagem como *Switch Expressions*, *Pattern Matching*, *Stream API* e *Local Variable Type Inference (var)*.

---

## 🚀 Funcionalidades

- **Menu Interativo**: Navegação simples via console para gerenciar todas as etapas do jogo.
- **Validação de Entrada Robusta**: Sistema que impede o fechamento do programa caso o usuário digite letras ou caracteres inválidos onde se esperam números.
- **Lógica de Jogo Completa**:
    - Iniciar novo jogo.
    - Colocar/Remover números (respeitando células fixas).
    - Visualizar o tabuleiro formatado.
    - Verificar status (Se há erros, se está incompleto ou se foi finalizado).
    - Limpar todo o progresso do tabuleiro atual.

## 🛠️ Tecnologias e Conceitos Utilizados

- **Java 21 (LTS)**: Uso de `var`, `Stream API` (flatMap, anyMatch, noneMatch) e as novas `Switch Expressions`.
- **Programação Orientada a Objetos**: Separação clara entre modelos (`Board`, `Space`), enums de estado e utilitários.
- **Scanner & Input Handling**: Tratamento de buffer do teclado para uma experiência de usuário sem travamentos.

---

## 🏗️ Estrutura do Código

O projeto está dividido nos seguintes pacotes principais:

1. **`br.com.dio.model`**:
    - `Board`: O "cérebro" do jogo. Controla a matriz de `Space` e valida as regras do Sudoku.
    - `Space`: Representa cada quadrado do tabuleiro, armazenando o valor atual, o esperado e se a célula é imutável (fixa).
    - `GameStatusEnum`: Gerencia os estados `NON_STARTED`, `INCOMPLETE` e `COMPLETE`.

2. **`br.com.dio.util`**:
    - `BoardTemplate`: Contém a estrutura visual em String para renderização do tabuleiro no console.

3. **`Main`**:
    - Ponto de entrada da aplicação, contendo o loop principal e os métodos de validação de entrada do usuário.

---

## 🎮 Exemplo de Uso

Ao executar o projeto no **IntelliJ**, o sistema apresentará um menu numerado. Graças à validação implementada no método `runUntilGetValidNumber`, o programa é resiliente a erros de digitação:

1. **Entrada de Dados**: O usuário escolhe uma opção de 1 a 8.
2. **Tratamento de Erros**: Se o usuário digitar uma letra (ex: `abc`) ou apenas der `Enter` (vazio), o sistema exibirá:
   > `Entrada inválida! Informe um número inteiro entre 1 e 8`
3. **Fluxo de Jogo**:
    - Selecione `1` para carregar o tabuleiro inicial.
    - Selecione `4` para visualizar o mapa do Sudoku formatado.
    - Selecione `2` para inserir um número, informando a **Coluna**, a **Linha** e o **Valor** desejado.

---

## 🤝 Contribuição

Este é um projeto de código aberto para fins de estudo. Para contribuir:

1. Faça um **Fork** do projeto.
2. Crie uma **Branch** para sua modificação (`git checkout -b feature/NovaFuncionalidade`).
3. Comite suas alterações (`git commit -m 'Adicionando nova funcionalidade'`).
4. Dê um **Push** na Branch (`git push origin feature/NovaFuncionalidade`).
5. Abra um **Pull Request**.

**Sugestões para futuras versões:**
- Implementar a lógica de carregar diferentes níveis de dificuldade via `args` no `main`.
- Adicionar cores no terminal para destacar números fixos de números inseridos pelo usuário.
- Criar testes unitários com **JUnit 5** para validar a lógica de vitória na classe `Board`.


