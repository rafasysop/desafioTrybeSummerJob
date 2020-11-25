# CSS Flexbox



## O que vamos aprender?

Você vai aprender sobre CSS Flexbox e layouts responsivos

O desenvolvimento de páginas responsivas tem sido cada vez mais presente e nescessária devido aos vários dispositivos e telas divergentes, então em meados de 2008 havia somente quatro formas de posicionar e ajustar os elementos: block, inline, table, Position. Eis que chegou em 2009 o Flexbox.

## Você será capaz de:

Desenvolver layouts responsivos, entender sobre as propriedades do Flexbox.

Com Flexbox você será capaz de alinhar os elementos filho de um container através
de regras aplicadas no container, mas também pode aplicar regras independentes para cada
elemento filho.

## Porque isso é importante?

Era comum que se pensasse CSS em eixos X e Y, onde os elementos eram posicionados em tabelas. Eram criadas seções nas quais os elementos eram jogados para esquerda e para a direita com float. Quando a necessidade de atender múltiplas telas entrou no jogo, isso precisou mudar. Então o Flexbox com uma forma de escrever CSS que configura o alinhamento, posicionamento e distribuição dos elementos através de regras especificadas pelo container pai, passa a ser responsável por organizar o conteúdo dentro do espaço que ele possui. ao invés de cada elemento ter que cuidar de si. Muito mais amigável à realidade de múltiplas dimensões de tela.

## Conteúdos

O CSS se baseia em Box Models(caixas dentro de caixas), esses boxes são "pedaçõs" da tela, onde serão aplicados os estilos: preenchimento, borda e etc. dentro desses pedaços, entram os elementos: textos, imagens e etc.

Caixas podem ter outras caixas e elementos dentro delas, quando isso acontece temos que dizer como a caixa externa posiciona o conteúdo que abriga, ai entra o Flexbox.

O container "pai" dá aos Filhos Direção, Justificação, Alinhamento. Elementos filhos podem sozinho se ordenar, e se alinha individualmente.

#### Display: Flex
vamos começar pelo pai, primeiramente você precisa definir o pai com a propriedade display: flex; que torna o elemento(pai) um flex container automaticamente transformando todos os seus filhos diretos em flex itens porém caso não seja filho direto estes não serão flex itens.

#### Flex Direction
uma outra propriedade importante é o flex-direction que define a direção dos flex itens. Por padrão ele é row (linha), por isso quando o display: flex; é adicionado, os elementos ficam em linha, um do lado do outro.

A mudança de row para column geralmente acontece quando estamos definindo os estilos em media queries para o mobile. Assim você garante que o conteúdo seja apresentado em coluna única.

* flex-direction: row;
// Os itens ficam em linha

* flex-direction: row-reverse;
// Os itens ficam em linha reversa, ou seja 3, 2, 1.

* flex-direction: column;
// Os itens ficam em uma única coluna, um embaixo do outro.

* flex-direction: column-reverse;
// Os itens ficam em uma única coluna, um embaixo do outro, porém em ordem reversa: 3, 2 e 1.

#### flex-wrap

flex-wrap define se os itens devem quebrar ou não a linha. Por padrão eles não quebram linha, isso faz com que os flex itens sejam compactados além do limite do conteúdo.

Essa é geralmente uma propriedade que é quase sempre definida como flex-wrap: wrap; Pois assim quando um dos flex itens atinge o limite do conteúdo, o último item passa para a coluna debaixo e assim por diante.

* flex-wrap: nowrap;
// Valor padrão, não permite a quebra de linha.

* flex-wrap: wrap;
// Quebra a linha assim que um dos flex itens não puder mais ser compactado.

* flex-wrap: wrap-reverse;
// Quebra a linha assim que um dos flex itens não puder mais ser compactado. A quebra é na direção contrária, ou seja para a linha acima.

#### Flex-flow

O flex-flow é um atalho para as propriedades flex-direction e flex-wrap. Você não verá muito o seu uso, pois geralmente quando mudamos o flex-direction para column, mantemos o padrão do flex-wrap que é nowrap.

E quando mudamos o flex-wrap para wrap, mantemos o padrão do flex-direction que é row.

* flex-flow: row nowrap;
// Coloca o conteúdo em linha e não permite a quebra de linha.

* flex-flow: row wrap;
// Coloca o conteúdo em linha e permite a quebra de linha.

* flex-flow: column nowrap;
// Coloca o conteúdo em coluna e não permite a quebra de linha

#### justify-content

justify-content alinha os itens flex no container de acordo com a direção(flex-direction). A propriedade só funciona se os itens atuais não ocuparem todo o container. Isso significa que ao definir flex: 1; ou algo similar nos itens, a propriedade não terá mais função.

Excelente propriedade para ser usada em casos que você deseja alinhar um item na ponta esquerda e outro na direita, como em um simples header com marca e navegação.

* justify-content: flex-start;
// Alinha os itens ao início do container.

* justify-content: flex-end;
// Alinha os itens ao final do container.

* justify-content: center;
// Alinha os itens ao centro do container.

* justify-content: space-between;
// Cria um espaçamento igual entre os elementos. Mantendo o primeiro grudado no início e o último no final.

* justify-content: space-around;
// Cria um espaçamento entre os elementos. Os espaçamentos do meio são duas vezes maiores que o inicial e final.

## Exercícios



## Recursos Adicionais