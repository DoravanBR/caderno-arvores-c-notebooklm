# caderno-arvores-c-notebooklm

# 🌳 Caderno Temático: Árvores em C

> **Desafio de Projeto DIO** — Explorando Inteligência Artificial como ferramenta ativa de aprendizagem com NotebookLM.

---

## 📌 Contexto e Objetivos

### Por que Árvores em C?

Estruturas de dados em árvore estão no coração de sistemas de alto desempenho: bancos de dados, sistemas operacionais, compiladores e mecanismos de busca dependem delas para funcionar com eficiência. Em C, onde o programador controla diretamente a memória, entender como implementar e balancear árvores é um diferencial técnico significativo.

Este caderno temático, construído com o auxílio do **NotebookLM**, cobre três das estruturas mais importantes da Ciência da Computação:

| Estrutura | Complexidade de Busca | Principal Aplicação |
|---|---|---|
| Árvore Binária de Busca (BST) | O(log n) médio / O(n) pior caso | Base conceitual para todas as outras |
| Árvore AVL | O(log n) garantido | Quando o desempenho previsível é crítico |
| Árvore B | O(log n) em disco | Bancos de dados e sistemas de arquivos |

### 🎯 Objetivos de Estudo

1. **Compreender** a estrutura e as propriedades de cada tipo de árvore.
2. **Implementar** as operações fundamentais (inserção, busca, remoção) em C.
3. **Dominar** o mecanismo de rotações (simples e duplas) nas Árvores AVL.
4. **Entender** por que as Árvores B são superiores para armazenamento em disco.
5. **Relacionar** cada estrutura ao seu caso de uso prático no mercado.
6. **Consolidar** o aprendizado com um guia de revisão próprio, reutilizável em entrevistas técnicas.

---

## 📚 Curadoria de Fontes

As cinco fontes abaixo foram selecionadas e carregadas no NotebookLM. Todas são de **acesso aberto** — disponibilizadas por universidades, pela GNU Free Software Foundation ou publicadas sob licenças Creative Commons.

### Fonte 1 — Livro GNU: An Introduction to Binary Search Trees and Balanced Trees
- **Autor:** Ben Pfaff (GNU Project / Free Software Foundation)
- **Licença:** GNU Free Documentation License (totalmente aberta)
- **URL:** https://adtinfo.org/libavl.html/index.html
- **Cobertura:** BST, AVL, Red-Black Trees — implementações completas em C com análise de eficiência de memória e código produção-grade.
- **Por que escolhi:** Uma das referências mais rigorosas e gratuitas sobre implementação real de árvores em C. O código é de nível profissional, a licença é completamente aberta e o site é super estável.

### Fonte 2 — Projeto de Algoritmos (IME-USP): Árvores Binárias de Busca
- **Autor:** Prof. Paulo Feofiloff — Universidade de São Paulo (IME-USP)
- **Licença:** Material didático público (acesso aberto)
- **URL:** https://www.ime.usp.br/~pf/algoritmos/aulas/binst.html
- **Cobertura:** Conceitos de árvore binária, buscas e implementações essenciais na linguagem C.
- **Por que escolhi:** É indiscutivelmente o material de algoritmos em C mais famoso e confiável do Brasil. Sempre online e extremamente didático para iniciantes.

### Fonte 3 — GeeksforGeeks: AVL Tree Data Structure
- **Autor:** Comunidade GeeksforGeeks
- **Licença:** Acesso aberto gratuito
- **URL:** https://www.geeksforgeeks.org/introduction-to-avl-tree/
- **Cobertura:** Fator de balanceamento, visualização das 4 rotações (LL, RR, LR, RL) e implementação passo a passo em C.
- **Por que escolhi:** Material muito visual e prático, ideal para alimentar o NotebookLM com o raciocínio por trás de cada rotação da árvore AVL.

### Fonte 4 — GeeksforGeeks: Introduction of B-Tree
- **Autor:** Comunidade GeeksforGeeks
- **Licença:** Acesso aberto gratuito
- **URL:** https://www.geeksforgeeks.org/introduction-of-b-tree-2/
- **Cobertura:** Propriedades da Árvore B, diferenças para a BST/AVL e motivação do seu uso para minimizar acessos a disco.
- **Por que escolhi:** É um dos poucos materiais focados exclusivamente na Árvore B de forma simplificada, perfeito para criar resumos com IA.

### Fonte 5 — Wikipedia (PT): Árvore B
- **Licença:** Creative Commons CC-BY-SA 4.0
- **URL:** https://pt.wikipedia.org/wiki/%C3%81rvore_B
- **Cobertura:** Teoria completa das Árvores B, casos de uso em bancos de dados (como PostgreSQL e SQLite) e sistemas de arquivos.
- **Por que escolhi:** A Wikipédia em português possui um excelente artigo sobre Árvores B, muito bem estruturado e com licença 100% aberta, o que garante que sempre estará disponível.

---

## 📖 Referências Complementares

> ⚠️ **Nota sobre licença:** Os materiais abaixo são obras **protegidas por direitos autorais** (copyright comercial) e **não se enquadram como fontes abertas**. Por isso, não foram listados na curadoria oficial nem carregados no NotebookLM. São incluídos aqui apenas como referências bibliográficas de estudo pessoal, da forma como qualquer estudante citaria uma obra consultada.

- **TENENBAUM, Aaron M.; LANGSAM, Yedidyah; AUGENSTEIN, Moshe J.** *Estruturas de Dados Usando C.* São Paulo: Pearson / Makron Books, 1995.
  - Capítulos relevantes: 7 (Árvores), 8 (BST e balanceamento), 9 (Árvores B)
  - Referência clássica adotada em inúmeras universidades brasileiras. Excelente para aprofundar os conceitos estudados nas fontes abertas acima.

---

## 🧪 Engenharia de Prompts e Cicatrizes

Esta seção documenta as perguntas estratégicas elaboradas no NotebookLM, as variações testadas e as lições aprendidas no processo.

---

### 🔁 Prompt 1 — Ponto de Partida Conceitual

**Objetivo:** Construir uma visão geral antes de mergulhar nos detalhes.

**Prompt inicial:**
> "Explique a diferença fundamental entre uma Árvore Binária, uma Árvore Binária de Busca (BST), uma Árvore AVL e uma Árvore B."

**Resultado:** Boa resposta geral, mas sem contexto prático.

**Refinamento:**
> "Explique a diferença entre BST, AVL e Árvore B, e dê um exemplo prático de sistema real onde cada uma seria usada."

**Resposta obtida (síntese):**
- **BST:** usada em autocomplete de editores de texto (pesquisa por prefixo rápida)
- **AVL:** usada em dicionários em memória RAM onde a altura máxima previsível importa
- **B-Tree:** usada em índices de banco de dados (PostgreSQL, SQLite) porque minimiza acessos a disco com nós grandes

**💡 Cicatriz:** A primeira versão do prompt era vaga. Adicionar "sistema real" transformou uma resposta teórica em algo memorável e aplicável.

---

### 🔁 Prompt 2 — Aprofundando as Rotações AVL

**Objetivo:** Entender as 4 rotações da AVL de forma visual e sequencial.

**Prompt inicial:**
> "Como funcionam as rotações de uma Árvore AVL?"

**Resultado:** Explicação correta mas abstrata. Difícil de visualizar.

**Refinamento 1:**
> "Explique as 4 tipos de rotação da AVL (LL, RR, LR, RL) com um exemplo numérico de inserção para cada caso, mostrando o estado da árvore antes e depois da rotação."

**Resultado:** Muito melhor — o NotebookLM usou os documentos da UFSM para gerar exemplos visuais em texto.

**Refinamento 2 (troubleshooting):**
> "Agora mostre o código C da função de rotação simples à esquerda (`rotacionar_esquerda`) e explique linha por linha."

**Resposta obtida (trecho):**
```c
No *rotacionar_esquerda(No *x) {
    No *y = x->dir;        // y é o filho direito de x
    No *T2 = y->esq;       // salva o filho esquerdo de y

    y->esq = x;            // x passa a ser filho esquerdo de y
    x->dir = T2;           // o antigo filho esquerdo de y vai para x

    // Atualiza alturas (x primeiro, pois agora está abaixo de y)
    x->altura = 1 + max(altura(x->esq), altura(x->dir));
    y->altura = 1 + max(altura(y->esq), altura(y->dir));

    return y;              // y é a nova raiz
}
```

**💡 Cicatriz:** Pedir "linha por linha" é ouro. A IA justifica cada decisão de implementação, o que ajuda a fixar a lógica na memória em vez de apenas copiar código.

---

### 🔁 Prompt 3 — Comparando Complexidades

**Objetivo:** Entender em que cenários cada árvore vence.

**Prompt:**
> "Com base nos documentos, crie uma tabela comparativa entre BST, AVL e B-Tree mostrando: complexidade de busca (melhor, médio, pior caso), uso de memória e cenário ideal de aplicação."

**Resultado:** Excelente. O NotebookLM sintetizou múltiplas fontes em uma tabela única.

**💡 Cicatriz:** Pedir explicitamente "com base nos documentos" faz o NotebookLM ancorar as respostas nas fontes carregadas, reduzindo alucinações e citando trechos específicos.

---

### 🔁 Prompt 4 — Dificuldade: Remoção em Árvore AVL

**Objetivo:** Entender a operação de remoção, que é a mais complexa.

**Prompt inicial:**
> "Como funciona a remoção em uma Árvore AVL?"

**Problema encontrado:** A resposta foi longa demais e misturou conceitos de remoção em BST com AVL sem separar claramente os passos.

**Refinamento (decompondo o problema):**
> "Divida a remoção em AVL em 3 etapas separadas: 1) remoção como numa BST comum, 2) atualização das alturas, 3) verificação e correção do fator de balanceamento. Explique cada etapa separadamente."

**Resultado:** Muito mais claro. A decomposição em etapas forçou a IA a organizar o raciocínio.

**💡 Cicatriz:** Quando a resposta sai confusa, numere as etapas no próprio prompt. Você está essencialmente pedindo para a IA seguir um roteiro — e ela obedece bem quando o roteiro é explícito.

---

### 🔁 Prompt 5 — Por que B-Tree existe?

**Objetivo:** Entender a motivação da Árvore B, não apenas seu funcionamento.

**Prompt:**
> "Por que as Árvores B foram inventadas se as AVL já garantem O(log n)? Qual limitação das AVL elas resolvem no contexto de banco de dados?"

**Resposta obtida (síntese):**
> A AVL é eficiente em RAM, mas em disco, cada acesso a um ponteiro pode significar uma operação de I/O. Como cada nó AVL tem apenas 2 filhos, uma árvore com 1 milhão de chaves pode ter altura ~20, exigindo 20 acessos ao disco. A B-Tree resolve isso permitindo centenas de chaves por nó: uma árvore com ordem 100 e 1 milhão de chaves tem altura ~3 — apenas 3 acessos ao disco.

**💡 Cicatriz:** Perguntar "por que X foi inventado" é um dos melhores prompts de aprendizado. Revela a motivação histórica e o problema real que a estrutura resolve — muito mais memorável do que só aprender o funcionamento.

---

### 🔁 Prompt 6 — Geração de Quiz para Revisão

**Objetivo:** Criar material de revisão ativo.

**Prompt:**
> "Crie 10 perguntas de revisão (com gabarito) sobre Árvores Binárias, AVL e B-Trees, misturando questões conceituais e de implementação em C. O nível deve ser adequado para uma entrevista técnica de estágio."

**Resultado:** 10 perguntas bem formuladas, citando as fontes para cada resposta.

**💡 Cicatriz:** Especificar o nível ("entrevista técnica de estágio") e o tipo ("conceituais e de implementação") produziu um quiz muito mais útil do que simplesmente pedir "perguntas de revisão".

---

## 📖 Miniguia de Estudo

### 1. Resumos Estruturados

---

#### 🌳 Árvore Binária de Busca (BST — Binary Search Tree)

**Conceito:** Cada nó tem no máximo dois filhos. Para qualquer nó N:
- Todos os valores à **esquerda** são **menores** que N
- Todos os valores à **direita** são **maiores** que N

**Estrutura em C:**
```c
typedef struct No {
    int chave;
    struct No *esq;
    struct No *dir;
} No;
```

**Operações fundamentais:**

| Operação | Complexidade Média | Complexidade Pior Caso |
|---|---|---|
| Busca | O(log n) | O(n) — árvore degenerada |
| Inserção | O(log n) | O(n) |
| Remoção | O(log n) | O(n) |

**Problema crítico:** Inserções em ordem crescente criam uma lista encadeada (pior caso O(n)).

```
Inserir: 1, 2, 3, 4, 5 → árvore degenerada:
1
 \
  2
   \
    3
     \
      4
       \
        5
```

**Percursos (Traversals):**
- **In-order (E-N-D):** Visita na ordem crescente — útil para listar elementos ordenados
- **Pre-order (N-E-D):** Útil para serializar/copiar a árvore
- **Post-order (E-D-N):** Útil para deletar a árvore da memória

---

#### ⚖️ Árvore AVL (Adelson-Velsky e Landis, 1962)

**Conceito:** Uma BST com a garantia de balanceamento: a diferença de altura entre as subárvores esquerda e direita de qualquer nó (o **fator de balanceamento**) é sempre -1, 0 ou +1.

**Estrutura em C:**
```c
typedef struct No {
    int chave;
    struct No *esq;
    struct No *dir;
    int altura;   // campo adicional em relação à BST
} No;
```

**Fator de balanceamento:**
```
FB(nó) = altura(esq) - altura(dir)
```

**As 4 Rotações:**

| Caso | Quando ocorre | Solução |
|---|---|---|
| LL (Left-Left) | FB > 1 e inserção à esquerda-esquerda | Rotação simples à direita |
| RR (Right-Right) | FB < -1 e inserção à direita-direita | Rotação simples à esquerda |
| LR (Left-Right) | FB > 1 e inserção à esquerda-direita | Rotação dupla: esq + dir |
| RL (Right-Left) | FB < -1 e inserção à direita-esquerda | Rotação dupla: dir + esq |

**Complexidades (garantidas):**

| Operação | Complexidade |
|---|---|
| Busca | O(log n) — **garantido** |
| Inserção | O(log n) — **garantido** |
| Remoção | O(log n) — **garantido** |

**Custo adicional:** Maior complexidade de implementação e overhead das rotações.

---

#### 🗄️ Árvore B (B-Tree)

**Conceito:** Uma árvore de busca **multi-way** (múltiplos filhos por nó), otimizada para minimizar operações de I/O em disco. Desenvolvida por Bayer e McCreight (1972) para sistemas de banco de dados.

**Propriedades de uma B-Tree de ordem m:**
- Cada nó tem no máximo **m filhos**
- Cada nó não-raiz tem no mínimo **⌈m/2⌉ filhos**
- Todos os nós folha estão no **mesmo nível**
- Um nó com k filhos contém exatamente **k-1 chaves**

**Por que é superior para disco?**

```
AVL com 1.000.000 de elementos: altura ≈ 20 → 20 acessos ao disco
B-Tree ordem 1000, 1.000.000 de elementos: altura ≈ 2 → 2-3 acessos ao disco
```

**Estrutura simplificada em C:**
```c
#define ORDEM 5

typedef struct NoBTree {
    int chaves[2 * ORDEM - 1];
    struct NoBTree *filhos[2 * ORDEM];
    int num_chaves;
    int folha;
} NoBTree;
```

**Aplicações reais:**
- **PostgreSQL, MySQL, SQLite:** índices de tabelas
- **Sistemas de arquivos:** NTFS (Windows), ext4 (Linux), APFS (macOS)
- **Sistemas de arquivos modernos:** Btrfs usa B-Trees como estrutura central

---

### 2. Glossário

| Termo | Definição |
|---|---|
| **Nó (Node)** | Unidade básica de uma árvore. Contém um dado (chave) e ponteiros para seus filhos |
| **Raiz (Root)** | O nó no topo da hierarquia, sem nó pai |
| **Folha (Leaf)** | Nó sem filhos. Representa o fim de um ramo da árvore |
| **Altura (Height)** | Número de arestas no caminho mais longo da raiz até uma folha |
| **Fator de Balanceamento (FB)** | `altura(subárvore_esq) - altura(subárvore_dir)`. Na AVL, deve ser sempre -1, 0 ou +1 |
| **BST (Binary Search Tree)** | Árvore binária onde esq < nó < dir para qualquer nó |
| **AVL** | BST auto-balanceada (Adelson-Velsky e Landis). Garante O(log n) em todas as operações |
| **Árvore B (B-Tree)** | Árvore de busca multi-way otimizada para I/O em disco |
| **Rotação** | Reestruturação local de nós para restaurar o balanceamento sem alterar a propriedade de busca |
| **Rotação Simples** | Envolve 3 nós. Resolve casos LL e RR na AVL |
| **Rotação Dupla** | Envolve 3 nós em 2 operações. Resolve casos LR e RL na AVL |
| **In-order Traversal** | Percurso Esquerda → Nó → Direita. Produz elementos em ordem crescente numa BST |
| **Degeneração** | Quando uma BST se torna uma lista linear. Ocorre com inserções ordenadas |
| **Predecessor** | Na BST, o maior valor menor que o nó atual. Usado na remoção de nós com 2 filhos |
| **Sucessor** | Na BST, o menor valor maior que o nó atual. Alternativa ao predecessor na remoção |
| **Ordem (B-Tree)** | Parâmetro `m` que define o número máximo de filhos de cada nó numa B-Tree |
| **Underflow** | Condição em B-Trees onde um nó tem menos que o mínimo de chaves após uma remoção |
| **Split (Divisão)** | Operação em B-Trees onde um nó cheio é dividido em dois durante uma inserção |
| **Merge (Fusão)** | Operação em B-Trees onde dois nós são unidos para resolver underflow |
| **malloc/free** | Funções da stdlib.h em C para alocação e desalocação dinâmica de memória |
| **Ponteiro nulo (NULL)** | Em C, representa a ausência de filho. Toda folha tem `esq = NULL` e `dir = NULL` |
| **Complexidade O(log n)** | O tempo cresce logaritmicamente com o tamanho. Para n=1.000.000, log₂(n) ≈ 20 passos |

---

### 3. Prompts Reutilizáveis para Revisão

Copie e cole estes prompts no NotebookLM (ou em qualquer IA) para revisões futuras:

---

**🔍 Revisão conceitual rápida:**
```
Com base nos documentos, explique [BST | AVL | B-Tree] em 3 parágrafos:
1. O que é e qual problema resolve
2. Suas propriedades fundamentais
3. Um caso de uso real onde ela seria a melhor escolha
```

---

**💻 Foco em implementação:**
```
Mostre o código C completo da função [inserir | buscar | remover] em uma [BST | AVL | B-Tree].
Após o código, explique cada bloco em linguagem simples, como se eu nunca tivesse visto antes.
```

---

**⚖️ Comparação entre estruturas:**
```
Compare [BST vs AVL | AVL vs B-Tree | BST vs B-Tree] respondendo:
- Em que situação eu escolheria uma sobre a outra?
- Qual tem menor overhead de memória e por quê?
- Qual tem desempenho garantido vs médio?
Cite trechos específicos dos documentos carregados.
```

---

**🎯 Geração de quiz para revisão:**
```
Crie um quiz de 5 perguntas de múltipla escolha sobre [tema] no nível [iniciante | intermediário | entrevista técnica].
Para cada pergunta: 4 opções, gabarito e uma explicação de 2 linhas da resposta correta.
```

---

**🐛 Debugging conceitual:**
```
Analise este código C de uma [BST | AVL] e identifique possíveis bugs ou problemas:
[cole o código aqui]
Foque especialmente em: gerenciamento de memória (malloc/free), casos de ponteiro nulo e atualização de altura.
```

---

**🔁 Revisão das rotações AVL:**
```
Para cada uma das 4 rotações AVL (LL, RR, LR, RL):
1. Descreva a situação que a dispara (inserção que causa o desequilíbrio)
2. Mostre um exemplo numérico com a árvore antes e depois
3. Mostre o código C da rotação
Apresente uma rotação por vez e pergunte se posso continuar.
```

---

**📊 Análise de complexidade:**
```
Crie uma tabela comparativa com as complexidades de tempo (melhor, médio, pior caso) e espaço para:
Busca, Inserção, Remoção e Percurso (traversal)
Das estruturas: BST, AVL e B-Tree (ordem m).
Explique em qual cenário cada pior caso ocorre.
```

---

## 🗺️ Roteiro de Estudos Sugerido

```
Semana 1: Fundamentos
├── Dia 1-2: Revisão de ponteiros e structs em C
├── Dia 3-4: Árvore Binária de Busca — teoria e inserção
└── Dia 5-7: BST — busca, percursos e remoção (implementar do zero)

Semana 2: AVL
├── Dia 1-2: Fator de balanceamento e detecção de desequilíbrio
├── Dia 3-4: Rotações simples (LL e RR) — implementar e testar
└── Dia 5-7: Rotações duplas (LR e RL) + remoção com rebalanceamento

Semana 3: B-Tree e Revisão
├── Dia 1-2: Motivação e propriedades da B-Tree
├── Dia 3-4: Inserção com split em B-Tree
└── Dia 5-7: Revisão geral + simulado de entrevista técnica
```

---

## 🔗 Links Úteis

- [NotebookLM](https://notebooklm.google.com/) — Ferramenta utilizada para criar este caderno
- [Visualgo — Visualização de BST e AVL](https://visualgo.net/en/bst) — Animações interativas das operações
- [B-Tree Visualization](https://www.cs.usfca.edu/~galles/visualization/BTree.html) — Visualizador de B-Trees
- [Compiler Explorer (godbolt.org)](https://godbolt.org/) — Teste código C no navegador
- [DIO](https://dio.me) — Plataforma com cursos, bootcamps e desafios de programação

---

## 📝 Reflexão Final

O uso do NotebookLM transformou o estudo destas estruturas. Em vez de consumir passivamente vídeos ou livros, o processo de **engenharia de prompts** forçou a articulação ativa das dúvidas — o que por si só já é aprendizagem.

As maiores lições do processo:

1. **Prompts vagos geram respostas vagas.** Sempre especifique nível, formato e contexto.
2. **Decompor é poder.** Dividir uma pergunta complexa (ex: "como funciona a remoção AVL") em etapas menores produz explicações muito mais claras.
3. **Pedir "por quê" antes de "como".** Entender a motivação histórica de uma estrutura (por que a B-Tree foi inventada?) ancora o conhecimento em problemas reais.
4. **A IA cita fontes, mas você valida.** Sempre verifique as informações nas fontes originais carregadas no NotebookLM.

---

*Projeto desenvolvido como parte do Desafio de Projeto da [DIO](https://dio.me) — Explorando IA como Ferramenta de Aprendizagem com NotebookLM.*
