# Campo Minado

Este é um jogo de Campo Minado desenvolvido em C que roda no terminal do windows. O jogo consiste em um campo 9x9 onde o objetivo é revelar todas as posições que não contenham minas. O jogo é controlado através do teclado, utilizando as teclas direcionais `W`, `A`, `S`, `D` e a barra de espaço para selecionar uma célula.

## Funcionalidades

- **Movimentação**: Use as teclas `W`, `A`, `S`, `D` para mover o cursor pelo campo.
- **Seleção de Célula**: Pressione a barra de espaço para revelar a célula selecionada.
- **Níveis de Dificuldade**: Escolha entre três níveis de dificuldade:
  - **Iniciante**: 8 bombas
  - **Intermediário**: 9 bombas
  - **Avançado**: 10 bombas
- **Contagem de Jogadas**: O jogo conta e exibe o número de jogadas realizadas.
- **Tempo de Jogo**: O tempo total da partida é mostrado ao final do jogo.

### Estrutura do Código

- **campo**: Estrutura que define uma célula do campo, contendo o valor da célula e seu status (aberta ou fechada).
- **coord**: Estrutura para armazenar as coordenadas x e y do cursor.
- **info**: Estrutura para armazenar informações do jogo como número de jogadas e quantidade total de movimentos.

### Funções Principais

- **mostra_matriz**: Exibe o campo na tela, mostrando as células abertas ou fechadas.
- **marca_matriz**: Marca as adjacências das bombas, atribuindo números às células.
- **jogada**: Executa a jogada na célula selecionada.
- **varredura**: Verifica as bombas ao redor de uma célula.

## Como Jogar

1. Ao iniciar o jogo, escolha o nível de dificuldade digitando o número correspondente (1, 2 ou 3).
2. Movimente o cursor usando as teclas `W` (para cima), `A` (para esquerda), `S` (para baixo) e `D` (para direita).
3. Pressione a barra de espaço para revelar a célula onde o cursor está localizado.
4. O objetivo é revelar todas as células que não contenham bombas. Se você revelar uma célula com uma bomba, o jogo termina.
5. O jogo também pode ser encerrado pressionando a tecla `ESC`.

## Cores

O jogo utiliza cores diferentes para mostrar o estado das células:
- **Verde**: Números adjacentes
- **Vermelho**: Indicativo de erro ou bomba
- **Cores**: Para mostrar diferentes números de bombas adjacentes

## Compilação e Execução

Para compilar e executar o jogo, siga os passos abaixo:

1. Compile o código usando o GCC ou qualquer outro compilador C:
   ```bash
   gcc -o CampoMinado CampoMinado.c -lconio
## Execute o jogo:

  ```bash
  ./CampoMinado
  ```
  
### Resultado

Ao final do jogo, uma mensagem informará se você ganhou ou perdeu, junto com o tempo total e o número de jogadas.
