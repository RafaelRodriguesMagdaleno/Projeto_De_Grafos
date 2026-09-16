# Projeto de Grafos

Projeto acadêmico desenvolvido em **Python** para demonstrar diferentes formas de representar grafos e aplicar algoritmos clássicos de busca.

O material apresenta exemplos de **lista de adjacência**, **matriz de adjacência** e **lista de arestas**, além de implementar buscas em largura e profundidade em grafos direcionados e não direcionados.

## Objetivos

- Demonstrar diferentes estruturas de representação de grafos;
- Criar e remover vértices e arestas;
- Consultar vizinhos e verificar a existência de arestas;
- Calcular graus de entrada, saída e grau total dos vértices;
- Validar percursos em um grafo;
- Realizar busca em largura, ou BFS;
- Encontrar o menor caminho usando busca em largura;
- Realizar busca em profundidade, ou DFS;
- Detectar ciclos com busca em profundidade.

## Representações de grafos

### Lista de adjacência

A lista de adjacência armazena, para cada vértice, os vértices que podem ser alcançados por meio de uma aresta. Essa representação costuma ser adequada para grafos esparsos, pois armazena apenas as conexões existentes.

Está implementada no arquivo `GrafoNaoImplementado.py`.

### Matriz de adjacência

A matriz de adjacência utiliza uma matriz quadrada para indicar as conexões entre os vértices. Quando existe uma aresta entre dois vértices, a posição correspondente recebe o valor `1`; caso contrário, permanece com o valor `0`.

Está implementada no arquivo `GrafoMatrizNaoImplementado.py`.

### Lista de arestas

A lista de arestas representa cada conexão como um par formado pelo vértice de origem e pelo vértice de destino. Essa abordagem é utilizada no arquivo que reúne os algoritmos de busca e as operações gerais do grafo.

## Algoritmos implementados

O arquivo `GrafoListaArestaNaoImplementado.py` contém as seguintes operações e algoritmos:

| Função | Descrição |
|---|---|
| `criar_grafo` | Inicializa as listas de vértices e arestas. |
| `inserir_vertice` | Adiciona um vértice caso ele ainda não exista. |
| `inserir_aresta` | Insere uma aresta direcionada ou não direcionada. |
| `remover_aresta` | Remove uma aresta do grafo. |
| `remover_vertice` | Remove um vértice e as arestas ligadas a ele. |
| `existe_aresta` | Verifica se uma conexão entre dois vértices existe. |
| `vizinhos` | Retorna os vértices alcançáveis a partir de um vértice. |
| `grau_vertices` | Calcula os graus de entrada, saída e total. |
| `percurso_valido` | Verifica se uma sequência representa um percurso válido. |
| `bfs` | Realiza uma busca em largura a partir de um vértice inicial. |
| `bfs_menor_caminho` | Encontra o menor caminho entre dois vértices. |
| `dfs` | Realiza uma busca em profundidade. |
| `dfs_detectar_ciclo` | Verifica a existência de ciclos no grafo. |

## Estrutura do projeto

```text
Projeto_De_Grafos-main/
├── README.md
└── grafos/
    ├── GrafoListaArestaNaoImplementado.py
    ├── GrafoMatrizNaoImplementado.py
    └── GrafoNaoImplementado.py
```

### Descrição dos arquivos

- `grafos/GrafoNaoImplementado.py`: demonstra a criação de um grafo utilizando lista de adjacência;
- `grafos/GrafoMatrizNaoImplementado.py`: demonstra a criação de um grafo utilizando matriz de adjacência;
- `grafos/GrafoListaArestaNaoImplementado.py`: implementa a lista de arestas, operações do grafo, BFS, BFS para menor caminho, DFS e detecção de ciclos.

## Como executar

### Pré-requisito

É necessário ter o **Python 3** instalado. Para verificar a instalação, execute:

```bash
python3 --version
```

No Windows, o comando também pode ser:

```powershell
python --version
```

### Executando os exemplos

Na raiz do projeto, execute os arquivos individualmente:

```bash
python3 grafos/GrafoNaoImplementado.py
python3 grafos/GrafoMatrizNaoImplementado.py
python3 grafos/GrafoListaArestaNaoImplementado.py
```

No Windows, se necessário, substitua `python3` por `python`.

O terceiro arquivo executa um grafo de exemplo com os vértices `A`, `B`, `C`, `D` e `E`, exibindo suas arestas, vizinhos, graus, percursos e resultados das buscas.

## Grafos direcionados e não direcionados

Por padrão, a função `inserir_aresta` adiciona uma conexão no sentido `origem -> destino`. Para representar uma aresta não direcionada, utilize o parâmetro `nao_direcionado=True`. Nesse caso, o programa adiciona as duas direções:

```python
inserir_aresta(vertices, arestas, "A", "B", nao_direcionado=True)
```

Na implementação da matriz e da lista de adjacência, as linhas comentadas mostram como adicionar também a conexão inversa para representar um grafo não direcionado.

## Exemplo de resultado

O programa principal do arquivo `GrafoListaArestaNaoImplementado.py` demonstra, entre outras operações:

```text
--- Busca de Largura Padrão ---
Visitados a partir de A: [...]

--- Busca de Largura por menor Caminho ---
Menor caminho de A até C: [...]

--- Busca em Profundidade (DFS) ---
Visitados a partir de A: [...]

--- DFS para Detecção de Ciclos ---
Ciclo detectado? Não
```
