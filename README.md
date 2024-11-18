# Sistema Bancário em Python - Descrição do Projeto

Este sistema bancário é uma aplicação desenvolvida para simular funcionalidades comuns de um banco, como gerenciamento de clientes, contas e transações financeiras. O código implementa conceitos avançados de **Programação Orientada a Objetos (POO)**, utilização de **decorators** e **abstração de classes**.

---

## 🚀 Funcionalidades Principais

### 1. **Gerenciamento de Clientes**
- **Cadastro de Clientes:** Permite registrar clientes com CPF, nome, data de nascimento e endereço.
- **Relacionamento de Contas:** Cada cliente pode ter múltiplas contas associadas.

### 2. **Operações Bancárias**
- **Depósitos:** Adiciona valores ao saldo de uma conta.
- **Saques:** Realiza retiradas com controle de limite por valor e número máximo de saques diários.
- **Extratos:** Exibe todas as transações realizadas e o saldo atual.

### 3. **Contas Bancárias**
- **Conta Corrente:** Implementa características como limite de saque e limite diário de transações.
- **Histórico de Transações:** Registra todas as operações realizadas por conta.

### 4. **Interface do Usuário**
- Menu interativo que permite navegar entre as funcionalidades, como criar contas, listar contas, realizar transações e consultar extratos.

---

## 🛠 Estrutura do Código

### **1. Classes Principais**
#### - `Cliente`
Representa os clientes do banco e gerencia suas contas.

#### - `PessoaFisica` *(herda de `Cliente`)*
Adiciona informações específicas, como CPF e data de nascimento.

#### - `Conta`
Modelo base para contas bancárias, contendo saldo, número, agência e histórico de transações.

#### - `ContaCorrente` *(herda de `Conta`)*
Adiciona regras específicas como limite de saque e controle de saques diários.

#### - `Historico`
Armazena e organiza as transações realizadas em uma conta.

#### - `Transacao` *(abstrata)*
Classe base para transações financeiras, como depósitos e saques.

### **2. Operações Bancárias**
- **Saque:** Classe específica que herda de `Transacao` e implementa a lógica de retirada de valores.
- **Depósito:** Classe específica que herda de `Transacao` e implementa a lógica de adicionar valores.

### **3. Decorators**
- **`log_transacao`:** Permite monitorar o fluxo de transações para fins de auditoria ou logging (a ser implementado).

### **4. Interface**
- Função `menu()`: Cria um menu interativo para usuários realizarem operações como depósitos, saques, consultas e criação de contas.

---

## 📋 Fluxo de Operações

1. **Menu Principal:** O programa inicia com um menu que apresenta as opções disponíveis.
2. **Cadastro de Usuários e Contas:**
   - Registrar clientes com CPF e dados pessoais.
   - Criar contas correntes associadas a clientes existentes.
3. **Transações:**
   - Realizar depósitos e saques em contas específicas.
   - Consultar extratos e saldo atualizado.
4. **Listagem de Contas:**
   - Exibe todas as contas cadastradas no sistema.

---

## 🔧 Recursos Técnicos

- **POO:** Utilização de herança, encapsulamento, abstração e polimorfismo.
- **Classes Abstratas:** Garantem que todas as transações sigam uma estrutura padrão.
- **Iteradores:** Planejado para manipulação de contas em listas (implementação inicial presente).
- **Menus e Validações:** Interação com o usuário por meio de entradas controladas.

---

## 💻 Como Utilizar

1. Execute o programa:
   ```bash
   python main.py
