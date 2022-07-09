## O que é Flexbox?
Uma ferramenta css criada para alinhar e distribuir elementos dentro de uma "caixa" (flex-container) de uma forma dinâmica;

flex-container é o elemento pai, inicializamos a "caixa" com "display: flex";

Por padrão os elementos são distribuidos do canto esquerdo superior (eixo principal) para baixo (eixo secundario); 

## display: flex;
Inicia o flex-container (elemento pai), agrupa e organiza os flex-items (elementos filhos) respeitando o tamanho proporcional de seu conteúdo;

Automaticamente as tags dentro desse container são elementos filhos;

Pode ser usado em qualquer tag html;

## flex-direction:
Define a direção (sentido) do eixo principal;
row - Sentido padrão (default) é em linha (row);
row-reverse - Invertido (Direita pra esquerda);
column - Exibir em coluna de cima pra baixo;
column-reverse - Exibir em coluna de baixo pra cima;

## justify-content:
Alinha os elementos no eixo principal;
flex-start - Agrupa do lado esquerdo;
flex-end - Agrupa do lado direito;
center - Distribui os elementes no centro;
space-between - Distribui elementos no começo, meio e fim;
space-around - Distribui elementos com espaço antes do começo e depois do fim;

## align-items:
Alinha os elementos no eixo perpedincular
flex-start - Agrupa do lado esquerdo;
flex-end - Agrupa do lado direito;
center - Distribui os elementos no centro;
stretch - Distribui os elementos ocupando todo o espaço perpendicular;
baseline - Distribui os elementos alinhando com a tipografia;

## flex-wrap:
Quebra os elementos em linhas
nowrap - Por padrão os elementos sempre buscam caber em uma única linha;
wrap - Desce os elementos quebrando linhas para baixo;
wrap-reverse - Sobe os elementos quebrando linhas para cima;

## flex-flow:
Define o flex-direction e o flex-wrap em uma mesma linha;

## align-content:
Alinha as linhas do flex-wrap no eixo perpendicular;
flex-start - Agrupa os elementos para o topo;
flex-end - Agrupa os elementos para a base;
center - Centraliza os elementos;
space-between - Distribui elementos no topo, meio e base;
space-around - Distribui elementos com espaço depois do top e antes da base;

## gap
Define tamanho (px) entre elementos para separá-los;
Com um único valor define o espaço entre linhas e colunas iguais;
Com dois valores define o espaço entre linhas e colunas diferentes;

## row-gap
Define a distância entre as linhas dos elementos;

## column-gap
Define a distância entre as colunas dos elementos;







## padding
É a distância entre o elemento e borda;

