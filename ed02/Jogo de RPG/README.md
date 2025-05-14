# 🛡️ Jogo de RPG — Programação Orientada a Objetos (POO)

Este projeto é um **jogo de RPG simples** desenvolvido em **Java**, com foco nos princípios da Programação Orientada a Objetos (POO). Ele foi criado como parte de um estudo dirigido na disciplina de POO no curso de Análise e Desenvolvimento de Sistemas.

---

## Objetivo

Simular o comportamento de diferentes personagens em um jogo de RPG. Cada personagem possui **HP (vida)**, **poder de ataque** e um comportamento específico para **atacar**, **defender** e **usar uma habilidade especial**.

---

## Estrutura e Lógica do Projeto

O projeto está dividido em cinco arquivos principais:

| Arquivo/Classe       | Função                                                                 |
|----------------------|------------------------------------------------------------------------|
| `Personagem.java`    | Classe base com atributos e métodos comuns a todos os personagens.     |
| `Guerreiro.java`      | Personagem com ataque físico forte e defesa com escudo.                |
| `Mago.java`           | Personagem com ataque mágico e habilidade em área.                    |
| `Arqueiro.java`       | Personagem com ataque médio e chance de crítico.                      |
| `Main.java`          | Classe principal que executa o combate entre os personagens.           |

---

## Descrição das Classes

### 1. `Personagem.java`
Classe utilizada internamente por todas as subclasses para armazenar:
- Nome
- HP (vida)
- Poder de ataque

Métodos:
- `getNome()`
- `getHp()`
- `getAtaqueBase()`
- `setHp(int novoHp)`
- `status()` — exibe o nome, HP e ataque atual do personagem

---

### 2. `Guerreiro.java`
- **Ataque:** físico forte
- **Defesa:** reduz o dano recebido pela metade
- **Habilidade especial:** `Golpe Duplo` — causa o dobro de dano em um único ataque

---

### 3. `Mago.java`
- **Ataque:** mágico, forte
- **Defesa:** normal (sem redução)
- **Habilidade especial:** `Bola de Fogo` — causa dano mágico em todos os inimigos

---

### 4. `Arqueiro.java`
- **Ataque:** médio, com chance de **acerto crítico** (20%)
- **Defesa:** normal
- **Habilidade especial:** `Chuva de Flechas` — realiza 3 ataques consecutivos

---

### 5. `Main.java`
Classe que simula o combate:

- Instancia um `Guerreiro`, um `Mago` e um `Arqueiro`
- Executa ataques e defesas entre os personagens
- Chama todas as habilidades especiais
- Exibe o status final de cada personagem

---

## Como executar o projeto

### Pré-requisitos

Você precisa ter instalado:

- [Java JDK 17+](https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html)
- [IntelliJ IDEA](https://www.jetbrains.com/idea/) ou outra IDE
- Git (opcional, para clonar o repositório)

---

### Usando o IntelliJ IDEA (recomendado)

**1. Clone o repositório:**

```bash
git clone https://github.com/SchusterAluizio/programacao-oo.git
```

**2. Abra o IntelliJ IDEA**

Va em:

File > Open

Selecione a pasta raiz do projeto:

**programacao-oo**

**Abra a pasta** `ed03`

**Abra o arquivo** `Main.java`

Execute

---

**Clique com o botão direito sobre o método `main`**

**Selecione: `Run 'Main.main()'`**

---

## O que o projeto executa

**1. Ao rodar a classe Main, o seguinte acontece:**

Cria 3 personagens:

`Thorgal` (Guerreiro)

`Merlino` (Mago)

`Legolis` (Arqueiro)

**2. Simula:**

Ataques físicos e mágicos

Defesas (com ou sem redução)

Uso de habilidades especiais

Golpe Duplo

  Bola de Fogo

  Chuva de Flechas

**3. Mostra o status final com o HP atualizado após o combate**


## Exemplo de saída no console:

```bash
=== STATUS INICIAL ===
Thorgal - HP: 150 | Ataque: 20
Merlino - HP: 100 | Ataque: 25
Legolis - HP: 120 | Ataque: 18

=== COMBATE ===
Thorgal ataca com espada causando 20 de dano.
Merlino sofre 20 de dano. HP atual: 80
Merlino lança Bola de Fogo! Causa 25 de dano em todos os inimigos.
Legolis sofre 25 de dano. HP atual: 95
Thorgal sofre 25 de dano. HP atual: 125
Legolis usa Chuva de Flechas! Ataca 3 vezes.
→ Ataque 1: causa 18 de dano.
→ Ataque 2: causa 18 de dano.
→ Ataque 3: causa 18 de dano.
Dano total causado: 54
Thorgal usa Golpe Duplo! Causa 40 de dano em Merlino.

=== STATUS FINAL ===
Thorgal - HP: 125 | Ataque: 20
Merlino - HP: 40 | Ataque: 25
Legolis - HP: 95 | Ataque: 18
