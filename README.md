<div align="center">

# UnB Academic Graph

[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Neo4j](https://img.shields.io/badge/Neo4j-4581C3?style=for-the-badge&logo=neo4j&logoColor=white)](https://neo4j.com/)
[![NetworkX](https://img.shields.io/badge/NetworkX-013243?style=for-the-badge&logo=python&logoColor=white)](https://networkx.org/)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge&logo=python&logoColor=white)](https://matplotlib.org/)

[![GitHub last commit](https://img.shields.io/github/last-commit/i-JSS/UnB-Academic-Graph?style=flat-square)](https://github.com/i-JSS/UnB-Academic-Graph/commits/main)
[![GitHub repo size](https://img.shields.io/github/repo-size/i-JSS/UnB-Academic-Graph?style=flat-square)](https://github.com/i-JSS/UnB-Academic-Graph)

Grafo de **pré-requisitos, co-requisitos e equivalências** de todas as disciplinas da UnB, com busca em largura (BFS) para encontrar o **menor caminho** até a conclusão de qualquer matéria.

[Ver Apresentação](https://www.youtube.com/watch?v=0t8uElQ3kTg) · [Reportar Bug](https://github.com/i-JSS/UnB-Academic-Graph/issues)

</div>

## Screenshots

<div align="center"><img src= "https://raw.githubusercontent.com/projeto-de-algoritmos-2024/Grafos1_UnB/refs/heads/main/Images/grafoperto.jpg?raw=true"/></div>

<center>
Figura 1 - Grafo no Neo4j
</center>

<div align="center"><img src= "https://raw.githubusercontent.com/projeto-de-algoritmos-2024/Grafos1_UnB/refs/heads/main/Images/busca.png?raw=true"/></div>

<center>
Figura 2 - Realizando a busca
</center>

<div align="center"><img src= "https://raw.githubusercontent.com/projeto-de-algoritmos-2024/Grafos1_UnB/refs/heads/main/Images/grafo.png?raw=true"/></div>

<center>
Figura 3 - Grafo plotado do menor caminho possível
</center>

---

## Sobre o Projeto

O **UnB Academic Graph** modela toda a estrutura curricular da Universidade de Brasília como um **grafo direcionado** armazenado no banco de dados orientado a grafos **Neo4j**. A partir de qualquer disciplina, o sistema realiza uma **Busca em Largura (BFS)** para encontrar o caminho mínimo de pré-requisitos necessários para cursá-la — considerando também co-requisitos e equivalências.

Os dados foram coletados diretamente do [SIGAA UnB](https://sigaa.unb.br/sigaa/public/turmas/listar.jsf) em 23/09/2024.

Este projeto foi desenvolvido na disciplina de **Projeto de Algoritmos** na Universidade de Brasília (UnB), com foco em algoritmos de grafos e estruturas de dados relacionais em grafos.

---

## Funcionalidades

- Modelagem completa do currículo da UnB como grafo direcionado
- Busca em Largura (BFS) para encontrar o menor caminho de pré-requisitos
- Suporte a pré-requisitos, co-requisitos e equivalências
- Armazenamento e consulta em banco de dados de grafos (Neo4j)
- Visualização interativa do grafo com Matplotlib e NetworkX
- Interface gráfica desktop com ttkthemes

---

## Tecnologias Utilizadas

| Camada                  | Tecnologia             |
|-------------------------|------------------------|
| Linguagem               | Python                 |
| Banco de Dados de Grafo | Neo4j                  |
| Algoritmo de Grafos     | BFS — Busca em Largura |
| Visualização            | Matplotlib + NetworkX  |
| Interface Desktop       | Tkinter + ttkthemes    |
| Parser                  | Lark                   |

---

## Como Executar

### Pré-requisitos

- Python 3.8+
- [Neo4j Desktop](https://neo4j.com/download/) instalado e em execução

### Instalação das dependências

```bash
pip install lark-parser
pip install neo4j
pip install networkx
pip install ttkthemes
pip install matplotlib
```

### Configuração do banco de dados

Crie um banco de dados no Neo4j com as seguintes credenciais:

| Campo   | Valor         |
|---------|---------------|
| Usuário | `JSS`         |
| Senha   | `Grafos1-UnB` |

### Executando

**1. Popule o grafo no Neo4j**

```bash
python src/popula.py
```

**2. Execute a busca**

```bash
python src/busca.py
```

---

## Algoritmo

A lógica central do projeto utiliza **Busca em Largura (BFS)** sobre um grafo carregado em memória a partir do Neo4j:

- Cada **disciplina** é um nó no grafo
- Cada **pré-requisito, co-requisito ou equivalência** é uma aresta direcionada
- A BFS percorre o grafo a partir da disciplina-alvo e retorna o **menor caminho** de dependências a serem cumpridas

> O grafo é subido em memória via NetworkX para garantir performance nas consultas de menor caminho.
---

## Autores

| Matrícula  | Aluno                         |
|------------|-------------------------------|
| 22/1031149 | Danilo César Tertuliano Melo  |
| 22/1008150 | João Antonio Ginuino Carvalho |


---

<div align="center">
Feito com <3 na <strong>Universidade de Brasília</strong>
</div>