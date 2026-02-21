
FLEX BOX: APRENDENDO COM  FLEX BOX ADVENTURE

Para ativar ele, deve ser feito o display: flex

Nele, nós temos: justify-content – Justificar conteúdo. Nele pode ser usado esses elementos:
Ela serve para distribuir o espaço extra no eixo principal (que, por padrão, é a horizontal) quando os itens não ocupam todo o espaço do container.

1. Alinhamento por Posição
Esses valores movem o bloco de itens como um todo:
•	flex-start (Padrão): Agrupa todos os itens no início do container. Se o texto for da esquerda para a direita, eles ficam na esquerda.
•	center: Coloca todos os itens exatamente no centro do container. É o "queridinho" para criar layouts centralizados.
•	flex-end: Agrupa todos os itens no final do container (geralmente à direita).

2. Distribuição de Espaço

Esses valores são mágicos para criar espaçamentos automáticos e responsivos:
•	space-between: O primeiro item gruda no início, o último item gruda no final, e o espaço restante é dividido igualmente apenas entre os itens. Ótimo para barras de navegação (Logo de um lado, Menu do outro).
•	space-around: Os itens recebem um espaço igual em ambos os lados. Na prática, o espaço entre dois itens é o dobro do espaço nas bordas externas.
•	space-evenly: Distribui o espaço de forma que a distância entre qualquer par de itens (e entre os itens e a borda) seja exatamente a mesma.

Além do justify Content, tem o align items que:Se o justify-content cuida do eixo principal, o align-items é o responsável por controlar o comportamento dos itens no eixo transversal (cross-axis). Se o seu container for uma linha (horizontal), esta propriedade vai dizer como os itens se alinham verticalmente.

Os Modos de Alinhamento
•	stretch (Padrão): Os itens são esticados para preencher todo o tamanho do container no eixo transversal (desde que não tenham uma altura ou largura fixa definida).
•	center: Os itens são centralizados verticalmente (em um layout de linha). É a forma mais fácil de alinhar elementos de alturas diferentes de modo que fiquem alinhados pelo meio.
•	flex-start: Alinha todos os itens no início do eixo transversal (no topo, se for uma linha).
•	flex-end: Alinha todos os itens no final do eixo transversal (na base, se for uma linha).
•	baseline: Alinha os itens de acordo com a linha de base do texto. Se você tiver itens com tamanhos de fonte diferentes, eles serão ajustados para que o texto de todos "pouse" na mesma linha invisível.

Também, a propriedade flex-direction é o "maestro" do Flexbox. Ela define a direção do eixo principal (main axis), determinando se os itens serão empilhados como uma linha ou como uma coluna.
1. Orientação Horizontal (Linha)
•	row (Padrão): Os itens são dispostos horizontalmente, da esquerda para a direita (em sistemas de escrita ocidentais). O início do container é à esquerda.
•	row-reverse: Os itens também ficam na horizontal, mas a ordem é invertida. O primeiro item da lista aparece na extremidade direita e o fluxo segue para a esquerda.
2. Orientação Vertical (Coluna)
•	column: Os itens são empilhados verticalmente, de cima para baixo. O "eixo principal" agora corre de cima para baixo, o que significa que o justify-content passará a controlar o alinhamento vertical.
•	column-reverse: Os itens são empilhados verticalmente, mas de baixo para cima. O primeiro item da sua lista HTML aparecerá no fundo do container.

Além disso,tem a order, a propriedade order é uma das ferramentas mais poderosas do Flexbox para controle de layout, pois ela permite que você altere a ordem visual dos elementos sem precisar mexer no código HTML original.
Como a Ordem é Definida

•	Valor Padrão (0): Por padrão, todos os itens flexíveis têm o valor order: 0 e aparecem na ordem exata em que foram escritos no HTML.
•	Inteiros Positivos e Negativos: Você pode atribuir qualquer número inteiro, como -2, -1, 0, 1, 2, para reposicionar o item.
•	Regra de Posicionamento: O navegador organiza os itens do menor valor para o maior.
•	Um item com order: -1 aparecerá antes de todos os itens que estão com o padrão 0.
•	Um item com order: 1 aparecerá depois de todos os itens com valor 0.

Exemplo de Comportamento

Imagine três caixas no seu HTML: A, B e C.
1.	Se todas forem order: 0, a sequência será A -> B -> C.
2.	Se você der order: 2 para a caixa A, a sequência visual mudará para B -> C -> A.
3.	Se você der order: -1 para a caixa C, a sequência visual será C -> A -> B.

Ainda, enquanto o align-items define o comportamento de todos os itens de uma vez, a propriedade align-self permite que um item individual "se rebele" e adote um alinhamento diferente do resto do grupo.

Ela é aplicada diretamente no item filho (o elemento dentro do flex container) e trabalha no eixo transversal.
Valores Comuns

Aqui estão os comportamentos que você pode aplicar a um elemento específico:
•	stretch: O item estica para preencher toda a altura (ou largura, dependendo do eixo) do container.
•	center: O item se posiciona no centro do eixo transversal, independentemente de onde os seus "irmãos" estejam.
•	flex-start: Alinha o item individual ao início do container.
•	flex-end: Alinha o item individual ao final do container.

Ademais, a propriedade flex-wrap é a solução para quando você tem mais itens do que o espaço do container permite carregar em uma única linha. Ela decide se os itens devem ser "esmagados" ou se devem pular para uma nova linha.
Os Modos de Quebra de Linha
•	nowrap (Padrão): Tenta manter todos os itens em uma única linha, não importa quantos sejam. Se houver muitos itens, eles podem transbordar o container ou encolher até o limite mínimo para caber.
•	wrap: Permite que os itens que não cabem na primeira linha pulem para a linha de baixo. Isso cria um layout multi-linhas que se ajusta conforme o tamanho da tela diminui.
•	wrap-reverse: Funciona como o wrap, mas a ordem das linhas é invertida. Em vez de pular para baixo, os novos itens aparecerão em uma linha acima da anterior.
