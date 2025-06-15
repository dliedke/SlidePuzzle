# 🎉 Slide Puzzle Divertido

[Jogue agora! Acesse aqui](https://dliedke.github.io/SlidePuzzle/slidepuzzle.html)

Um quebra-cabeça deslizante (slide puzzle) em JavaScript, HTML e CSS, com dicas otimizadas por IDA\* incremental e fallback guloso para garantir performance em dispositivos móveis e desktop.

## 📦 Estrutura do Projeto

```
├── slidepuzzle.html  # Arquivo principal do jogo
└── README.md         # Este arquivo de documentação
```

## 🚀 Como Usar

1. **Abra** o arquivo `slidepuzzle.html` em um navegador moderno (Chrome, Firefox, Edge, Safari).
2. O jogo carregará automaticamente um tabuleiro 3×3 embaralhado.
3. Use os botões de controle para:

   * Selecionar tamanho: `3×3` ou `4×4`
   * Iniciar um **Novo Jogo**
   * **Ativar/Desativar Dicas**
4. Clique nas peças adjacentes ao espaço vazio para movê-las.
5. Veja o **contador de tempo** e o número de **movimentos** no canto.
6. Ao resolver, um diálogo exibirá seu desempenho.

## 🕹️ Controles

* **3×3 / 4×4**: Redefine o tabuleiro para o tamanho escolhido.
* **Novo Jogo**: Embaralha novamente o tabuleiro do tamanho atual.
* **Ativar Dicas**: Mostra a próxima jogada ideal. Otimizado:

  * Para tabuleiro 3×3: usa IDA\* incremental.
  * Para tabuleiro 4×4: heurística gulosa instantânea.
* **Peças**: Clique em uma peça vizinha ao espaço vazio para movê-la.

## ⚙️ Algoritmo de Dicas

* **IDA**\*: pré-calcula posições meta, swap in-place e heurística Manhattan incremental.
* **Timeout**: se a busca ultrapassar 80 ms, cai no fallback guloso.
* **Fallback Guloso**: escolhe o movimento que minimiza a distância Manhattan.

## 📐 Layout e Estilo

* **Grid CSS** para dimensionar dinamicamente o tabuleiro.
* **Responsive**: ocupa até 80% da menor dimensão da janela.
* **UI**: botões com animações simples e feedback visual.
* **Tema**: gradientes de fundo e cores contrastantes para peças.

## 🛠️ Tecnologias

* **Vanilla JS** (ES6+)
* **HTML5** & **CSS3**
* **Sem dependências externas**
