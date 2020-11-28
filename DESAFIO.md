# CSS Flexbox

FlexBox é uma forma eficiente de estruturar, alinhar e ordenar itens em container's. Junto da Grade e outras especificações, temos um módulo de layout mais completo como resposta para as flutuações, tabelas e outros hacks que designers web tem usado pelos anos.

Com Flexbox, itens podem ser posicionados em qualquer direção e ajustar seus tamanhos, seja crescendo para preencher o espaço ou diminuindo para não estourar o elemento pai.

## O que vamos aprender?

Você vai aprender sobre CSS Flexbox e layouts responsivos

O desenvolvimento de páginas responsivas tem sido cada vez mais presente e nescessária devido aos vários dispositivos e telas divergentes, então em meados de 2008 havia somente quatro formas de posicionar e ajustar os elementos: _block_, _inline_, _table_, _Position_. Eis que chegou em 2009 o Flexbox.

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

O container "pai" dá aos Filhos Direção, Justificação, Alinhamento. Elementos filhos podem sozinho se ordenar, e se alinhar individualmente.


##### Importante aprender sobre Os *Eixos* do Flexbox

Compreender a diferença entre os eixos principal e perpendicular é o que importa quando começamos a observar o alinhamento ou justificação dos itens flexíveis (flex items); o flexbox possui propriedades que alinham e justificam o conteúdo ao longo de um eixo ou de outro.

#### Display: Flex

vamos começar pelo pai, primeiramente você precisa definir o pai com a propriedade display: flex; que torna o elemento(pai) um flex container automaticamente transformando todos os seus filhos diretos em flex itens porém caso não seja filho direto estes não serão flex itens.

#### Flex Direction

Uma propriedade importante é o flex-direction que define a direção dos flex itens. Por padrão ele é row (linha), por isso quando o display: flex; é adicionado, os elementos ficam em linha, um do lado do outro.

A mudança de row para column geralmente acontece quando estamos definindo os estilos em media queries para o mobile. Assim você garantir que o conteúdo seja apresentado em coluna única.

* flex-direction: row;
// Os itens ficam em linha

* flex-direction: row-reverse;
// Os itens ficam em linha reversa, ou seja 3, 2, 1.

* flex-direction: column;
// Os itens ficam em uma única coluna, um embaixo do outro.

* flex-direction: column-reverse;
// Os itens ficam em uma única coluna, um embaixo do outro, porém em ordem reversa: 3, 2 e 1.

#### justify-contentrdena

justify-content alinha os flex itens no container de acordo com a direção(flex-direction). A propriedade só funciona se os itens atuais não ocuparem todo o container. Isso significa que ao definir flex: 1; ou algo similar nos itens, a propriedade não terá mais função.

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

* justify-content: space-evenly;
// Cria um espaçamento entre os elementos. Distribue os items uniformemente/igualmente no espaço ao seu redor tanto inicial, final e meio.

* justify-content: stretch;       
// Estende/Estica Qualquer item de tamanho automático, onde terá seu tamanho aumentado igualmente (não proporcionalmente), embora ainda respeite as restrições impostas por max-height / max-width (ou funcionalidade equivalente), de modo que o tamanho combinado preenche exatamente o contêiner de alinhamento ao longo do eixo principal.

#### align-items

align-items controla o alinhamento de todos os itens filhos diretos como um grupo no eixo transversal. Lembre - se que:
O eixo transversal é perpendicular ao eixo principal, logo, se a propriedade flex-direction estiver definida nas linhas, como row ou row-reverse, o eixo transversal estará na direção das colunas, como column ou column-reverse.

Se o eixo principal for definido nas colunas, como column ou column-reverse, então o eixo transversal estará na direção das linhas, como row ou row-reverse.

* align-items: center;
// Itens posicionados ao redor do centro

* align-items: flex-start;
// Posiciona itens-flex a partir do início

* align-items: flex-end;
// Posiciona itens-flex a partir do fim


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


## Exercícios


Antes de fazer os nosso exerícios sugiro fazer também os exercícios com o 'Flexbox Froggy', um jogo onde você pode ajudar Froggy e seus amigos ao escrever código CSS. 
Em recursos adicionais também está disponivel um Playgroud para que você tenha uma 
idéia de como se comporta os elementos.

[flexboxfroggy.com](http://flexboxfroggy.com/#pt-br)


##### Exercicio 01:

Dado uma div com a classe .container como sendo 'pai' e outras 3 div's com classe .square sendo 'filhas' de container, copie o código html abaixo e crie o arquivo ex01.html(com o codigo copiado) na raiz da sua branch. Na classe pai defina como *flex*.

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exercios CSS Flexbox</title>
    <style type="text/css">
        .aula {
            text-align: center;
        }

        .container {
            background-color: #333;
            min-width: 100vh;
            min-height: 70vh;
            padding: 20px 5px;
        }

        .square {
            align-items: center;
            background-color: aqua;
            display: flex;
            height: 100px;
            font-size: larger;
            font-weight: 700;
            margin: 10px;
            justify-content: center;
            width: 100px;
        }
    </style>
</head>
<body>
    <h1 class="aula">CSS Flexbox</h1>
    <div class="container">
        <div class="square">1</div>
        <div class="square">2</div>
        <div class="square">3</div>
    </div>
    <footer><h2 class="aula">Exercicio desenvolvido e praticado na <a href="https://www.betrybe.com/" target="_blank"><img src="https://uploads-ssl.webflow.com/5dbd9ce75ad64f24b67f0932/5dbdd9165ad64f5e29811c52_BRAND3.png" height="20" sizes="(max-width: 479px) 46vw, 110px" srcset="https://uploads-ssl.webflow.com/5dbd9ce75ad64f24b67f0932/5dbdd9165ad64f5e29811c52_BRAND3-p-500.png 500w, https://uploads-ssl.webflow.com/5dbd9ce75ad64f24b67f0932/5dbdd9165ad64f5e29811c52_BRAND3.png 522w" alt="Logo Trybe"></a></h2></footer>
</body>
</html>

```

##### Exercicio 02:

Utilizando css alinhe os Quadrados(.square) de acordo com a imagem abixo:
Dica: utilize *justify-content*.

Salve o resultado como ex02.html

![](/imagens-ex/exercicio02.png)

##### Exercicio 03:

Utilizando css alinhe os Quadrados(.square) de acordo com a imagem abixo:
Dica: utilize *justify-content*.

Salve o resultado como ex03.html

![](/imagens-ex/exercicio03.png)

##### Exercicio 04:

Utilizando css alinhe os Quadrados(.square) de acordo com a imagem abixo:
Dica: utilize *justify-content*, *align-items*.

Salve o resultado como ex04.html

![](/imagens-ex/exercicio04.png)

##### Exercicio 05:

Utilizando css alinhe os Quadrados(.square) de acordo com a imagem abixo:
Dica: utilize *justify-content*, *align-items*, *flex-direction*.

Salve o resultado como ex05.html

![](/imagens-ex/exercicio05.png)

##### Exercicio 06:

Utilizando css alinhe os Quadrados(.square) de acordo com a imagem abixo:
Dica: utilize *justify-content*, *align-items*, *flex-direction*.

Salve o resultado como ex06.html

![](/imagens-ex/exercicio06.png)

##### Exercicio 07:

Utilizando css alinhe os Quadrados(.square) de acordo com a imagem abixo:
Dica: utilize *justify-content*, *align-items*, *flex-direction*.

Salve o resultado como ex07.html

![](/imagens-ex/exercicio07.png)

##### Exercicio 08:

Utilizando css alinhe os Quadrados(.square) de acordo com a imagem abixo:
Dica: utilize *justify-content*, *align-items*, *flex-direction*.

Salve o resultado como ex08.html

![](/imagens-ex/exercicio08.png)




## Recursos Adicionais

Como recursos adicionais você pode estudar mais profundamente sobre: [Flexbox na documentação MDN web docs](https://developer.mozilla.org/pt-BR/docs/Web/CSS/CSS_Flexible_Box_Layout/Conceitos_Basicos_do_Flexbox).

Baixe esse Playground para CSS Flexbox desenvolvido por rmanguinho.
[PlayGround-Flexbox-css](https://github.com/rmanguinho/flexbox-playground/archive/master.zip)

> Para usar o playground você deve primeiramente baixar o arquivo .zip e extrair, depois acessar a pasta onde você extraiu os arquivos navegar ate a pasta **_dist_** e abrir o arquivo **_index.html_** com seu navegador, então você poderá adicionar novos elementos ou retirar e usar as propriedades do flexbox dinamicamente com javascript.