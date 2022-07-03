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

### Flex-wrap

É a propriedade que define se os itens devem ou não quebrar a linha.
Por padrão eles não quebram linhas, isso faz com que os flex items sejam compactados além do limite do conteúdo.

- `nowrap`(padrão) -> não permite a quebra de linha
- `wrap`-> permite a quebra linha assim que um dos flex items não puderem mais serem compactados
- `wrap-reverse`-> permite a quebra de linha na direção contrária
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