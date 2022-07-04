# CSS Flexbox

## Fundamentos do Flexbox

1 - Conhecer a estrutura básica
2 - Entender a diferença entre Flex Container e FLex Item
3 - Conhecer inicialmente algumas propriedades

## Flex Container

É a tag que envolve os itens, será nela que iremos aplicar a propriedade `display: flex`.
Transforma todos os seus itens filhos em flex itens.

<img src="https://css-tricks.com/wp-content/uploads/2018/10/01-container.svg" alt="Flex Container" width="600" />

##### Propriedades relacionadas:

- `display` -> inicializador do container
- `flex-direction` -> direcionamento em linha ou coluna
- `flex-wrap` -> quebra de linha ou não
- `flex-flow` -> shorthand para `direction` e `wrap`
- `justify-content` -> alinha os itens de acordo com a direção
- `align-items` -> alinha os itens de acordo com seu eixo
- `align-content` -> alinha as linhas do container

### Display: Flex

Torna a tag um elemento do tipo flex container, e assim automaticamente todos os seus filhos diretos tornam-se **flex items**. Conseguimos aplicar em qualquer `<tag HTML>`.

### Flex Direction

É a propriedade que estabelece o eixo principal do container, definindo assim a direção que os flex items são colocados no flex container.

- `row` (padrão) -> direção do texto, esquerda para direita.
- `row-reverse` -> sentido oposto à direção do texto
- `column`-> ordenação de cima para baixo, em coluna única
- `column-reverse`-> ordenação inversa, de baixo para cima

### flex-wrap

É a propriedade que define se os itens devem ou não quebrar a linha.
Por padrão eles não quebram linhas, isso faz com que os flex items sejam compactados além do limite do conteúdo.

- `nowrap`(padrão) -> não permite a quebra de linha
- `wrap`-> permite a quebra linha assim que um dos flex items não puderem mais serem compactados
- `wrap-reverse`-> permite a quebra de linha na direção contrária

### flex-flow

É um atalho para as propriedades `flex-direction` e `flex-wrap`.
Porém seu uso não é tão comum, visto que, quando mudamos o `flex-direction` para `column`, mantemos o padrão do `flex-wrap` que é `nowrap`.

### justify-content

Essa propriedade vai se encarregar de alinhar os itens dentro do container de acordo com a direção pretendida e trata da distribuicão de espaçamento entre eles.

Obs.: caso seus itens estajam ocupando 100% de todo o container, ela não se aplica.

As variações:

- `flex-start`-> início do container
- `flex-end`-> final do container
- `center`-> centro do container
- `space-between`-> cria um espaçamento igual entre os elementos
- `space-around`-> os espaçamentos do meio são duas vezes maiores que o inicial e final

### align-items

Trata do alinhamento dos flex items de acordo com o eixo do container.
O alinhamento é diferente para quando os items estão em colunas ou linhas.
Permite o alinhamento central no eixo vertical.

Tipos de alinhamento: 

- `center`-> alinhamento dos itens ao centro
- `stretch` (padrão)-> flex items crescem igualmente
- `flex-start` -> alinhamento dos itens no início
- `flex-end` -> alinhamento dos itens no final
- `baseline` -> alinhamento de acordo com a linha base da tipografia dos itens

### align-content

É a propriedade responsável por tratar o alinhamento das linhas do container em relação ao eixo vertical do container.

Precisamos que:

- o container utilize quebra de linhas
- a altura do container seja maior que a soma das linha dos itens

Tipos de alinhamento:

- `center` -> alinhamento dos itens ao centro
- `stretch` (padrão) -> flex itens crescem igualmente
- `flex-start` -> alinhamento dos itens no início
- `flex-end` -> alinhamento dos itens no final
- `space-between` -> cria um espaçamento igual entre os elementos
- `space-around` -> os espaçamentos do meio são duas vezes maiores que o inicial e final

## Flex Item

São elementos filhos diretos do *Flex Container*, e também podem se tornar um outro Flex Container.

<img src="https://css-tricks.com/wp-content/uploads/2018/11/00-basic-terminology.svg" alt="Flex Container" width="600" />

##### Propriedades relacionadas:

- `flex-grow` -> define o fator de crescimento
- `flex-basis` -> tamanho inicial do item
- `flex-shrink` -> define a capacidade de redução
- `flex` -> shorthand para `flex-grow`, `flex-basis` e `flex-shrink`
- `order` -> define a ordem do item
- `align-self` -> define o alinhamento do item específico

### flex-grow

Define a proporcionalidade de crescimento dos itens, respeitando o tamanho de seus conteúdos internos.

Obs.: não irá funcionar caso tenhamos adicionado justify-content ao nosso flex container.

