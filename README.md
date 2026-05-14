# Sistema-de-controle
📦 Sistema de Controle de Estoque em Python

Sobre o Projeto

Este projeto é um **Sistema de Controle de Estoque** desenvolvido em **Python** utilizando:

* **SQLite** → armazenamento dos dados
* **Pandas** → visualização e manipulação de tabelas
* **NumPy** → cálculos matemáticos
* **JSON** → exportação de dados
* **Datetime** → registro de data e hora das movimentações

O sistema foi criado com o objetivo de auxiliar no gerenciamento de produtos em estoque, permitindo cadastrar produtos, controlar entradas e saídas, acompanhar movimentações e gerar relatórios simples.
Além disso, o projeto demonstra na prática conceitos importantes de programação, banco de dados e análise de dados.


Funcionalidades

O sistema possui as seguintes funcionalidades:

Cadastro de Produtos

Permite adicionar novos produtos ao estoque contendo:

* Nome do produto
* Quantidade inicial
* Preço
* Estoque mínimo

Exemplo:

```python
adicionar_produto("Mouse Gamer", 10, 120.50, 3)
```

Entrada de Produtos

Realiza o aumento da quantidade em estoque quando novos produtos chegam.

Exemplo:

```python
entrada_produto(1, 5)
```

Saída de Produtos

Realiza a retirada de produtos do estoque.

O sistema verifica automaticamente se existe quantidade suficiente disponível.

Exemplo:

```python
saida_produto(1, 2)
```

Controle de Estoque Baixo

Ao listar os produtos, o sistema verifica automaticamente quais itens estão abaixo do estoque mínimo.

Exemplo de alerta:

```bash
⚠️ ALERTA: Estoque baixo!
```

Histórico de Movimentações

Todas as entradas e saídas ficam registradas no banco de dados com:

* ID do produto
* Tipo da movimentação
* Quantidade
* Data e horário

Isso permite acompanhar toda a movimentação do estoque.

Cálculo do Valor Total em Estoque

O sistema calcula automaticamente o valor total armazenado no estoque utilizando:

```python
quantidade × preço
```

Média de Preços

Calcula a média de preços dos produtos cadastrados.


Exportação para JSON

Permite exportar os dados do estoque para um arquivo `.json`.

Exemplo do arquivo gerado:

```json
[
    {
        "id": 1,
        "nome": "Teclado",
        "quantidade": 15,
        "preco": 99.9,
        "estoque_min": 5
    }
]
```

🛠️ Tecnologias Utilizadas

| Tecnologia | Função                |
| ---------- | --------------------- |
| Python     | Linguagem principal   |
| SQLite     | Banco de dados local  |
| Pandas     | Manipulação de dados  |
| NumPy      | Operações matemáticas |
| JSON       | Exportação de dados   |
| Datetime   | Registro de horários  |


Estrutura do Banco de Dados

O sistema utiliza duas tabelas:

Tabela produtos

Armazena os produtos cadastrados.

| Campo       | Tipo    |
| ----------- | ------- |
| id          | INTEGER |
| nome        | TEXT    |
| quantidade  | INTEGER |
| preco       | REAL    |
| estoque_min | INTEGER |

---

Tabela movimentações

Armazena o histórico de entradas e saídas.

| Campo      | Tipo    |
| ---------- | ------- |
| id         | INTEGER |
| produto_id | INTEGER |
| tipo       | TEXT    |
| quantidade | INTEGER |
| data       | TEXT    |


Como Executar o Projeto

1️⃣ Instalar as bibliotecas

Caso necessário, instale:

```bash
pip install pandas numpy
```

2️⃣ Executar o arquivo

```bash
python nome_do_arquivo.py
```

Menu do Sistema
Ao executar o programa, o seguinte menu será exibido:

```bash
1 - Cadastrar Produto
2 - Entrada
3 - Saída
4 - Listar Estoque
5 - Valor Total
6 - Média de Preços
7 - Histórico
8 - Exportar JSON
0 - Sair
```

Exemplo de Uso:
Cadastro de Produto

```bash
Nome: Notebook
Quantidade: 10
Preço: 3500
Estoque mínimo: 2
```
Entrada de Produto

```bash
ID: 1
Quantidade: 5
```

Saída de Produto

```bash
ID: 1
Quantidade: 3
```


Conceitos Aplicados

Este projeto utiliza diversos conceitos importantes da programação:

* Programação estruturada
* Funções em Python
* Banco de dados SQLite
* CRUD (Create, Read, Update, Delete)
* Manipulação de DataFrames
* Operações matemáticas
* Tratamento de estoque
* Exportação de arquivos
* Estruturas condicionais
* Laços de repetição

Possíveis Melhorias Futuras

Algumas melhorias que podem ser adicionadas futuramente:

* Interface gráfica
* Login de usuários
* Relatórios avançados
* Dashboard com gráficos
* Integração com API
* Controle de fornecedores
* Sistema de vendas
* Leitura de código de barras
* Backup automático

Este projeto foi desenvolvido com foco educacional para praticar:

* Python
* Banco de dados
* Organização de código
* Manipulação de dados
* Lógica de programação

Além disso, o sistema simula um cenário real de controle de estoque utilizado em empresas e comércios.

👩‍💻 Autores

Projeto desenvolvido por **Jullia, Karen, Thainá e João Pedro** como prática de programação e gerenciamento de estoque em Python.

