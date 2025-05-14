# 💰 Sistema Bancário — Programação Orientada a Objetos (POO)

Este projeto é um **sistema bancário simples** desenvolvido em **Java**, com foco nos princípios da Programação Orientada a Objetos (POO). Ele foi criado como parte de um estudo dirigido na disciplina de POO no curso de Análise e Desenvolvimento de Sistemas.

---

## Objetivo

Simular operações bancárias básicas — como depósito, saque, transferência, aplicação de juros diários e emissão de extrato — utilizando classes Java com encapsulamento e organização modular.

---

## Estrutura e Lógica do Projeto

O projeto está dividido em cinco arquivos principais:

| Arquivo/Classe        | Função                                                                 |
|------------------------|------------------------------------------------------------------------|
| `Conta.java`           | Classe genérica que encapsula saldo, cliente e operações básicas.     |
| `ContaCorrente.java`   | Conta com aplicação de juros de 0.1% ao dia.                           |
| `ContaPoupanca.java`   | Conta com aplicação de juros de 0.08% ao dia.                          |
| `ContaSalario.java`    | Conta que não aplica juros.                                            |
| `Main.java`            | Classe principal que instancia as contas e realiza todas as operações.|

---

### 1. `Conta.java`

Classe base utilizada internamente por todas as contas. Contém:

- Atributos privados:
  - `String cliente`
  - `double saldo`
- Métodos públicos:
  - `depositar(double valor)`
  - `sacar(double valor)`
  - `transferir(Conta destino, double valor)`
  - `aplicarJuros(double percentual)`
  - `imprimirExtrato(String tipoConta)`
  - `getSaldo()`

---

### 2. `ContaCorrente.java`

- Representa contas correntes
- Juros: 0.1% ao dia
- Usa internamente um objeto da classe `Conta`
- Exibe extrato identificando o tipo de conta

---

### 3. `ContaPoupanca.java`

- Representa contas poupança
- Juros: 0.08% ao dia
- Usa internamente um objeto `Conta`
- Permite saque, depósito, transferência e aplicação de juros

---

### 4. `ContaSalario.java`

- Representa contas salário
- **Não aplica juros**
- Permite transferência para contas correntes, depósito e saque

---

### 5. `Main.java`

Classe que **executa o sistema** e realiza as seguintes ações:

- Criação de contas (`ContaCorrente`, `ContaPoupanca`, `ContaSalario`)
- Realiza operações de depósito, saque e transferência
- Aplica juros conforme o tipo de conta
- Exibe extratos finais com os saldos atualizados

---

## Como executar o projeto

### Pré-requisitos

Você precisa ter instalado:

- [Java JDK 17+](https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html)
- [IntelliJ IDEA](https://www.jetbrains.com/idea/) ou outra IDE
- Git (opcional, para clonar o repositório)

### Usando o IntelliJ IDEA (recomendado)

1. **Clone o repositório:**
```bash
git clone https://github.com/SchusterAluizio/programacao-oo.git

2. **Abra o IntelliJ IDEA:**

Vá em File > Open...

Selecione a pasta programacao-oo

3. **Abra o diretório ed02**

4. **Execute o programa:**

Clique com o botão direito sobre Main.java

Escolha Run 'Main.main()'
