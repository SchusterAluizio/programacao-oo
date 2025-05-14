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

---

### Usando o IntelliJ IDEA (recomendado)

1. **Clone o repositório:**
```bash
git clone https://github.com/SchusterAluizio/programacao-oo.git
```bash

---

2. **Abra o IntelliJ IDEA:**

---

3. Vá no menu: File > Open...

**Selecione a pasta raiz do projeto:**

programaca-oo

---

4. **Espere o IntelliJ carregar o projeto**

No painel lateral esquerdo, abra o diretório ed02

Localize e abra o arquivo Main.java

Clique com o botão direito no método main

Escolha:

Run 'Main.main()'

---

## O que o projeto executa

Ao rodar a classe Main, o seguinte fluxo ocorre:

1. **Cria três contas bancárias:**

Corrente (Alice)

Poupança (Bob)

Salário (Carlos)

2. **Realiza:**

Depósito de R$200 na conta corrente

Saque de R$100 da conta poupança

Transferência de R$300 da conta salário para a corrente

3. **Aplica juros diários conforme o tipo da conta:**

0.1% na corrente

0.08% na poupança

0% na salário

4. **Exibe extratos com cliente, tipo da conta e saldo atualizado**

---

## Exemplo de saída no console:

========== INÍCIO DAS OPERAÇÕES ==========

[Depósito] Alice deposita R$200,00
Saldo atual de Alice: R$1200.00

[Saque] Bob realiza saque de R$100,00
Saldo atual de Bob: R$1400.00

[Transferência] Carlos transfere R$300,00 para Alice
Saldo atual de Carlos: R$900.00
Saldo atual de Alice após receber: R$1500.00

[Juros] Aplicando juros diários:
Juros 0.1% aplicados à conta de Alice. Novo saldo: R$1501.50
Juros 0.08% aplicados à conta de Bob. Novo saldo: R$1401.12
Conta salário de Carlos não recebe juros. Saldo permanece: R$900.00

========== EXTRATOS FINAIS ==========

[Conta Corrente] Cliente: Alice | Saldo: R$1501.50
[Conta Poupança] Cliente: Bob | Saldo: R$1401.12
[Conta Salário] Cliente: Carlos | Saldo: R$900.00






