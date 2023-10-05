# CSS: Cascading Style Sheets

O CSS (Cascading Style Sheets) é uma linguagem de estilo utilizada para controlar a apresentação e o design de documentos HTML em páginas web. É essencial para a criação de layouts atraentes, coesos e responsivos, e é fundamental para a experiência de navegação na web que estamos acostumados.

## 1. Introdução ao CSS

### O que é CSS?

O CSS é uma linguagem de estilo, stylesheets, que baseando-se na estrutura do conteúdo (HTML) de um documento na web (página), define como cada elemento HTML de tal página deve ser exibido na tela, incluindo cores, fontes, tamanhos, margens, espaçamento e muito mais.

### Vantagens do uso de CSS

- **Separação de preocupações**: Ao declarar o CSS em um bloco ou arquivo separado da estrutura HTML em si, permite-se separar o conteúdo de uma página das definições de sua apresentação visual, tornando o código mais organizado e mais fácil de manter.

- **Reutilização de estilos**: Você pode aplicar um estilo a vários elementos, economizando tempo e esforço.

- **Responsividade**: CSS, em especial sua prática moderna, permite criar layouts responsivos, que se adaptam a diferentes tamanhos de tela e dispositivos.

- **Acessibilidade**: Com a estruturação adequada e o uso de técnicas de acessibilidade, o CSS pode melhorar a experiência de usuário para pessoas com necessidades especiais.

## 2. Sintaxe CSS

### Seletores

Os seletores são padrões que definem quais elementos HTML serão estilizados. Os seletores podem ser baseados em elementos, classes, IDs, atributos, descendência e pseudo-classes.

### Propriedades e Valores

As propriedades CSS determinam como os elementos selecionados serão estilizados. Cada propriedade tem um valor que especifica como ela deve ser aplicada. Por exemplo, a propriedade `color` define a cor do texto e seu valor pode ser "red", "#FF0000" ou outra cor.

### Regras CSS

As regras CSS consistem em um seletor seguido por um bloco de declarações, dentro de chaves { ~ }. Uma declaração é composta por uma propriedade e um valor separados por dois pontos. Por exemplo:

```css
p {
  color: red;
  font-size: 16px;
}
```

Neste exemplo, `p` é o seletor, `color` e `font-size` são propriedades, e "red" e "16px" são valores.

## 3. Especificidade e Cascading

### Como o CSS resolve conflitos

Quando múltiplas regras CSS se aplicam a um elemento, o CSS utiliza a especificidade e a ordem de precedência para determinar qual regra deve ser aplicada.

### Ordem de precedência

A ordem de precedência em CSS é a seguinte (da mais alta à mais baixa):

1. !important // não é recomendável que se faça, ou ao menos que se reduza ao mínimo possivel, o uso de !important
2. Especificidade // quanto mais específico a determinado bloco de código é o seletor, maior sua força ex. seletores id (#) ganham de seletores de classe (.)
3. Ordem de código // a ordem em que as stylesheets são lidas pelo interpretador. quanto antes são lidas, menor a importância no final.  ex. estilos do navegador

### A importância do !important

A propriedade `!important` é usada para dar prioridade absoluta a uma regra CSS, ignorando a ordem de precedência normal.

## 4. Seletores CSS

### Seletores de Tipo

Seletores de tipo aplicam estilos a elementos HTML específicos, como `<p>` para parágrafos ou `<h1>` para cabeçalhos de nível 1.

### Seletores de Classe

Seletores de classe são usados com uma classe específica, como `.botao`, para aplicar estilos a elementos com essa classe.

### Seletores de ID

Seletores de ID são usados com um ID específico, como `#cabecalho`, para aplicar estilos a um elemento com esse ID.

### Seletores de Atributo

Seletores de atributo selecionam elementos com atributos específicos, como `[type="text"]` para elementos com `type` igual a "text".

### Seletores de Descendência

Seletores de descendência selecionam elementos que são descendentes de outro elemento, por exemplo, `ul li` seleciona todos os elementos `<li>` dentro de uma lista `<ul>`.

### Pseudo-classes e Pseudo-elementos

Pseudo-classes e pseudo-elementos são usados para aplicar estilos com base em estados ou partes específicas de elementos, como `:hover` para estilizar elementos quando o mouse está sobre eles ou `::before` para criar conteúdo antes de um elemento.

### Box model

O modelo de caixa (box model) é um conceito fundamental em CSS que descreve como os elementos HTML são renderizados no navegador. Cada elemento é considerado uma "caixa" retangular, que consiste em quatro componentes principais: conteúdo, recuo (padding), borda (border) e margem (margin). Esses componentes afetam o tamanho total da caixa e sua posição em relação a outros elementos na página.

O conteúdo representa o espaço ocupado pelo próprio conteúdo do elemento, como texto, imagens ou outros elementos que sejam 'filhos'. O recuo ou preenchimento(padding), é uma área transparente ao redor do conteúdo dentro da caixa, proporcionando espaço adicional entre o conteúdo e a borda. A borda é uma linha visível que circunda a caixa, e a margem é uma área transparente que fica fora da borda, criando espaço entre a caixa atual e elementos adjacentes.

O box model é fundamental para controlar o layout e o dimensionamento dos elementos em uma página web, permitindo que se ajuste o tamanho, o espaçamento e a aparência dos elementos de maneira precisa e consistente. 


## 5. Propriedades CSS Comuns

Existem centenas de propriedades CSS, mas algumas das mais comuns incluem:

- **Cores e Fundos**: Propriedades como `color`, `background-color` e `background-image` controlam as cores e os fundos dos elementos.

- **Texto e Fontes**: Propriedades como `font-size`, `font-family` e `text-align` controlam a aparência do texto.

- **Margens e Recuos**: Propriedades como `margin` e `padding` controlam o espaçamento ao redor dos elementos.

- **Layout e Posicionamento**: Propriedades como `display` e `position` controlam o layout, o posicionamento dos elementos e seu comportamento em relação a outros elementos e à página de forma geral.

- **Bordas e Sombras**: Propriedades como `border` e `box-shadow` adicionam bordas e sombras aos elementos.

- **Transições e Animações**: Propriedades como `transition` e `animation` permitem criar transições suaves e animações.

## 6. Layout Responsivo

### Media Queries

As Media Queries podem ser usadas, entra várias possibilidades, para criar layouts responsivos, adaptando o design da página a diferentes tamanhos de tela e dispositivos. Também para definir estilos que são específicos para determinada midia, como os estilos que serão usados ao imprimir a página.

### Unidades Relativas

Unidades como `%`, `em`, `vw` e `vh` são usadas para criar layouts flexíveis e adaptáveis.

### Flexbox

O Flexbox é um modelo de layout que facilita o posicionamento e a distribuição de elementos em um contêiner, especialmente útil para criar layouts flexíveis.

[Kevin Powel, desenvolvedor frontend, especialista em CSS fala sobre flexbox](https://www.youtube.com/watch?v=u044iM9xsWU)

### Grid Layout

O Grid Layout é uma técnica poderosa para criar layouts bidimensionais, permitindo controle preciso sobre as linhas e colunas de um layout.

[Jen Simmons, designer gráfica, desenvolvedora web e membro do CSS Working Group fala sobre Grid, ainda na fase de implementação da funcionalidade](https://www.youtube.com/watch?v=t0b3uBoDkBs)