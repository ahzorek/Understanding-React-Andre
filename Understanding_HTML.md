# Revisão: Fundamentos Básicos de HTML

## Sumário dos Tópicos

### 1. Introdução ao HTML

O HTML (Linguagem de Marcação de Hipertexto) forma a espinha dorsal das páginas da web. Criado por Tim Berners-Lee em 1991, o HTML é usado para estruturar elementos e conteúdo em uma página, permitindo que os navegadores exibam informações de forma organizada.

### 2. Sintaxe Básica

A sintaxe do HTML é a base do seu funcionamento. As tags HTML envolvem o conteúdo e podem conter atributos que fornecem informações adicionais sobre os elementos. Isso permite definir a estrutura e o significado dos elementos na página.

### 3. Elementos Básicos

Os elementos HTML formam os blocos de construção das páginas. Alguns elementos básicos incluem:

- `<h1>`, `<h2>`, `<h3>`, ...: Tags de cabeçalho para títulos e subtítulos, com importância hierárquica.
- `<p>`: Tag de parágrafo para agrupar o texto em parágrafos.
- `<ul>`, `<ol>`: Tags de lista não ordenada e ordenada, respectivamente.
- `<li>`: Tag de item de lista, usada dentro de `<ul>` e `<ol>`.
- `<br>`: Tag de quebra de linha para inserir novas linhas dentro de elementos de texto.

### 4. Elementos Semânticos

Os elementos semânticos atribuem significado ao conteúdo. Tags como `<header>`, `<nav>`, `<article>` e outros definem claramente a finalidade de cada seção da página, contribuindo para uma estrutura mais compreensível.

### 5. Charset e Sua Relevância

Os charsets são cruciais para definir conjuntos de caracteres suportados em uma página. Selecionar o charset correto é essencial para garantir que o texto seja exibido corretamente em diferentes idiomas e contextos. També é necessário atentar para a codificação do charset do documento HTML em si, uma vez que caso este esteja configurado errado, ainda que o documento declare o charset adequado, poderão ocorrer problema na exibição da página.

#### Considerações sobre Tags Deprecated

A evolução da web e adoção do CSS levou à descontinuação de algumas tags. Tags como `<center>` e `<font>` não estão mais alinhadas com as práticas modernas de desenvolvimento e devem ser evitadas. Se usadas, nos browser atuais elas não terão grandes problemas, porém esse suporte pode (deve) deixar de existir.

# Revisão: Criando Layouts em HTML

##  1. Tabelas

Como inicialmente planejada para navegação entre documentos científicos, não havia dentro do padrão HTML estruturas específicas para criação de layouts da forma como conhecemos hoje. Conforme a adoção da WEB e a criação de páginas com objetivo institucional e comercial cresceu, a necessidade de organizar informações em formato tabular tornou-se cada vez mais evidente.

No contexto do HTML, as tabelas desempenham um papel fundamental na apresentação de dados de maneira organizada e acessível. Elas permitem que se exiba informações em linhas e colunas, facilitando a compreensão e a leitura por parte dos usuários. Além disso, as tabelas oferecem a flexibilidade de ajustar o tamanho das células, combinar células adjacentes e até mesmo incorporar elementos gráficos quando necessário.

Para criar uma tabela em HTML, são utilizadas as tags `<table>`, `<tr>`, `<td>`, e `<th>`. A tag `<table>` define o início da tabela, `<tr>` representa uma linha na tabela, `<td>` define uma célula com dados e `<th>` é usada para cabeçalhos de coluna ou de linha. Combinando essas tags de maneira adequada, pode-se criar tabelas que atendam às necessidades de apresentação de informações.

Antigamente, as tabelas eram frequentemente utilizadas para criar layouts de páginas da web, uma prática conhecida como "table-based layout". Isso era uma solução comum para organizar elementos na página antes do uso generalizado de CSS (Cascading Style Sheets). No entanto, essa abordagem tinha suas limitações e resultava em códigos HTML complexos e pouco semânticos.

Ainda hoje, as tabelas são ocasionalmente empregadas para layout em casos específicos, como em e-mails marketing, onde a consistência de renderização em diferentes clientes de e-mail pode ser um desafio. 

No entanto, é importante ressaltar que, com o avanço das tecnologias web e as melhores práticas de design, o uso excessivo de tabelas para criar layouts de página é desencorajado e considerado uma má prática. Em seu lugar deve se ter em mente o uso de tags semânticas combinadas com CSS. Isso ajuda a separar a estrutura do conteúdo do design, tornando seu código mais legível e acessível, além de melhorar a compatibilidade com  diferentes dispositivos e tornar a manutenção mais fácil no longo prazo.



## 2. Boas Práticas Modernas: Uso de Tags Semânticas e CSS

À medida que a web evoluiu e as melhores práticas se desenvolveram, tornou-se evidente que essa abordagem anterior (uso de tabelas) não era a mais eficiente nem a mais acessível. Boas práticas modernas em design web enfatizam o uso de tags semânticas e CSS para criar layouts flexíveis e acessíveis.

### Tags Não Semânticas: Estruturando a Web

Antes de abordar as tags semânticas que conferem significado e contexto ao conteúdo, é fundamental entender o papel das tags não semânticas, como `<div>` e `<span>`. Embora essas tags não forneçam um significado intrínseco ao conteúdo, elas constituem os alicerces da estrutura da web moderna. As tags não semânticas desempenham um papel crucial na organização, agrupamento e estilização dos elementos das páginas, permitindo criar layouts flexíveis e atrativos, muito além das tabelas.


### Tags Semânticas

Tags semânticas são elementos HTML que têm significado e propósito claros, ajudando a estruturar o conteúdo de forma descritiva. Embora por si só não produzam a aparência final do seu layout, a estruturação do conteúdo através de tags semânticas irá produzir um layout muito mais compreensível do ponto de vista de legibilidade e manutenção de código. Algumas das tags semânticas mais importantes incluem:

- `<header>`: Usada para o cabeçalho de uma seção ou da página como um todo.
- `<nav>`: Utilizada para agrupar links de navegação.
- `<main>`: Define o conteúdo principal da página.
- `<section>`: Agrupa conteúdo relacionado semanticamente.
- `<article>`: Define um conteúdo independente e autossuficiente, como uma postagem em um blog.
- `<aside>`: Geralmente usada para conteúdo relacionado, como barras laterais.
- `<footer>`: Usada para definir o conteúdo de rodapé de um site.
- `<h1> <h2> ...`: Talvez tenham sido as primeiras tags com propósito semântico, visto que a numeração das tags h (heading) serve o propósito de a hierarquida de relevância dos conteúdos de uma página.

O uso adequado dessas tags também melhora a acessibilidade, tornando o conteúdo mais compreensível para leitores de tela e motores de busca.

Completando a discussão sobre acessibilidade e semântica na criação de páginas web, é fundamental destacar o papel crucial de elementos como descrições alt em imagens, títulos adequados e atributos "aria" (Accessible Rich Internet Applications) para garantir a melhor experiência possível ao usuário e seguir as melhores práticas de desenvolvimento web.


### Tag `<a>` âncora e hiperlinks

Pode ser dizer que é a base do funcionamento da internet como conhecemos. O hiperlink conecta páginas a outras páginas, através de um simples bloco de texto clicável que lhe redireciona para outro documento. A tag `<a>`, que é usada para criar links em HTML, possui diversos comportamentos e atributos que podem afetar a experiência do usuário ao navegar em uma página web. O atributo href (hiperlink de referência) especifica o destino do link. Pode apontar para várias coisas, incluindo:

- URL Absoluta: Um endereço web completo, como "https://www.site.com".
- URL Absoluta: Um endereço web completo, como "https://www.site.com".
- URL Relativa: Um caminho relativo dentro do próprio site, como "/pagina.html".
- E-mails: Para criar links de e-mail, use "mailto:exemplo@email.com".
- Âncoras Internas: Para navegar dentro da mesma página, use "#secao" para ancoras internas.

### Target

O atributo `target` em tags `<a>` (hiperlinks) desempenha um papel fundamental no controle de como os links se comportam quando clicados pelos usuários. Ele determina o destino da página que será aberta quando o link for ativado. Alguns valores comuns para o atributo `target` incluem:

- **_blank:** Ao usar `_blank`, o link abre em uma nova guia ou janela do navegador, mantendo a página atual aberta. Isso é frequentemente utilizado para abrir recursos externos sem interromper a experiência de navegação na página atual.

- **_self:** O valor `_self` faz com que o link abra na mesma janela ou guia do navegador em que a página atual está sendo exibida. Isso é útil quando desejamos que a navegação ocorra na mesma página sem substituí-la.

- **_parent:** Usando `_parent`, o link abre na janela ou frame pai da página atual. Isso é comum em páginas com frames ou iframes para direcionar o conteúdo para o quadro pai.

- **_top:** O valor `_top` faz com que o link abra na janela superior, substituindo qualquer estrutura de frames ou iframes existente.


### Elementos audiovisuais

Elementos audiovisuais, como áudio e vídeo, desempenham um papel significativo na criação de conteúdo web rico e envolvente. As tags `<audio>` e `<video>` são usadas para incorporar áudio e vídeo em uma página web, respectivamente. A tag `<img>`, por outro lado, é utilizada para exibir imagens. Para esses elementos, os atributos `src` e `srcset` são cruciais.

A tag `<audio>` permite incorporar arquivos de áudio em uma página web. O atributo `src` especifica o caminho do arquivo de áudio. O atributo `controls` permite que os usuários controlem a reprodução, pausa e volume do áudio. Para vídeos, a tag `<video>` é semelhante e permite incorporar arquivos de vídeo. O atributo `src` também é usado aqui para definir o arquivo de vídeo.

A tag `<img>` é usada para exibir imagens em uma página web. O atributo `src` indica o caminho da imagem a ser exibida. O atributo `alt` fornece um texto alternativo que é exibido se a imagem não puder ser carregada ou para usuários com deficiência visual, tornando a página mais acessível.

Uma prática moderna considerada boa é o uso da tag `<picture>` em conjunto com o atributo `srcset`. Isso permite que se forneça várias versões de uma imagem em diferentes resoluções ou formatos. O navegador escolherá automaticamente a imagem mais adequada com base no dispositivo do usuário, economizando largura de banda e melhorando a velocidade de carregamento da página. Essa técnica é especialmente valiosa em um mundo onde dispositivos variam amplamente em tamanho e resolução de tela.


### iFrames

Os iframes, ou "inline frames", são elementos HTML que permitem incorporar conteúdo externo dentro de uma página web, criando uma janela ou área onde outro documento ou recurso pode ser exibido. Eles são frequentemente utilizados para incorporar vídeos, mapas, conteúdo de outras páginas da web ou aplicativos interativos em uma página. Os iframes possuem atributos importantes, como "src" para especificar a origem do conteúdo a ser exibido e "width" e "height" para definir suas dimensões. O comportamento do atributo "target" em links dentro de iframes é outro aspecto relevante a considerar. Quando um link é clicado dentro de um iframe, o atributo "target" determina se o novo conteúdo será exibido dentro do próprio iframe ("_self"), substituindo a página atual, ou em uma nova janela ou guia do navegador ("_blank").


## Mais acessibilidade

As descrições `alt` em imagens são um dos pilares da acessibilidade na web. Quando um usuário com deficiência visual, que depende de leitores de tela, navega por uma página, essas descrições alt desempenham um papel fundamental. Elas fornecem uma explicação textual do conteúdo das imagens, permitindo que os usuários entendam o contexto e o significado das imagens que não podem ver.

É importante lembrar que as descrições alt devem ser concisas e informativas, transmitindo o propósito da imagem de forma clara e sucinta. Evitar descrições alt em branco ou genéricas, como "imagem123.jpg", é essencial para garantir a acessibilidade.

### Títulos Adequados e Estrutura de Títulos

A estrutura de títulos, incluindo a ordem adequada de `<h1>`, `<h2>`, `<h3>` e assim por diante, é um aspecto crítico para a acessibilidade. Os títulos fornecem uma hierarquia visual e semântica para o conteúdo, facilitando a compreensão e a navegação para todos os usuários.

O `<h1>` deve ser usado para o título principal da página, portanto único, enquanto os `<h2>`, `<h3>`, e assim por diante, devem ser usados para subtítulos e seções subsequentes. Essa estrutura ajuda os leitores de tela a entender a organização do conteúdo e permite que os usuários naveguem facilmente por ele.

### Atributos "aria" e Outros Atributos Invisíveis

Os atributos "aria" desempenham um papel fundamental na melhoria da acessibilidade em elementos interativos e dinâmicos, como menus, botões, caixas de diálogo e carrosséis. Eles fornecem informações adicionais aos leitores de tela para descrever o comportamento e a função desses elementos.

Por exemplo, o atributo `aria-label` pode ser usado para fornecer um rótulo descritivo para um elemento que não possui texto visível, como um ícone de busca. O `aria-hidden` pode ser usado para ocultar elementos decorativos de leitores de tela. A aplicação cuidadosa desses atributos garante que a experiência de todos os usuários seja consistente e informativa.

Além disso, o atributo "title" em elementos HTML, como links e elementos de formulário, pode ser usado para fornecer dicas de ferramentas (tooltips) úteis quando os usuários passam o mouse sobre esses elementos.


Em resumo, o uso adequado de descrições alt em imagens, a estrutura de títulos correta e a inclusão de atributos "aria" e "title" são componentes essenciais para a criação de páginas web acessíveis. Essas práticas não apenas atendem às necessidades de usuários com deficiências, mas também melhoram a experiência de todos os visitantes, resultando em um ambiente online mais inclusivo e eficaz. Portanto, ao desenvolver conteúdo web, é vital considerar esses aspectos para garantir a acessibilidade e a usabilidade.

## Formulários e campos input

Os formulários desempenham um papel essencial na interação entre os usuários e as páginas web, permitindo que os visitantes insiram e enviem informações de maneira conveniente. Para criar um formulário, utilizamos a tag `<form>`, que age como um container para os campos de entrada e os elementos relacionados. Cada campo de entrada é representado pela tag `<input>`, que é extremamente versátil e oferece vários tipos para coletar diferentes tipos de dados.

Os campos `<input>` podem assumir diversos tipos, dependendo da informação que desejamos coletar. Alguns dos tipos mais comuns incluem:

- **Text (`<input type="text">`):** Usado para coletar texto curto, como nomes, sobrenomes ou mensagens curtas, limitado a uma linha.
- **Number (`<input type="number">`):** Permite a entrada de números, incluindo opções para limitar um intervalo específico e qtd de incremento.
- **Checkbox (`<input type="checkbox">`):** Oferece uma caixa de seleção que permite aos usuários escolher entre várias opções independentes.
- **Radio (`<input type="radio">`):** Usado para criar uma lista de opções mutuamente exclusivas, onde os usuários podem escolher apenas uma.
- **Select (`<select>` com `<option>`):** Ideal para criar menus suspensos que permitem aos usuários selecionar uma opção a partir de uma lista predefinida.
- **Textarea (`<textarea>`):** Permite aos usuários inserir texto longo, como comentários ou mensagens extensas.
- **Date (`<input type="date">`):** Utilizado para coletar datas, permitindo que os usuários selecionem uma data a partir de um calendário, navegadores modernos ja implementam esse calendário por padrão.
- **Datetime-local (`<input type="datetime-local">`):** Soma-se ao camop anterior, coleta data e hora, permitindo que os usuários escolham uma data e hora em conjunto.
- **Datalist (`<datalist>` com `<input>`):** Utilizado para criar listas de sugestões em campos de texto, melhorando a usabilidade ao apresentar opções predefinidas enquanto os usuários digitam.

Além disso, para agrupar campos relacionados e melhorar a acessibilidade, pode-se usar a tag `<fieldset>` junto com `<legend>`. O `<fieldset>` age como um contêiner que envolve um grupo de campos de entrada relacionados, enquanto `<legend>` fornece uma legenda descritiva para o grupo. Essa estrutura ajuda os usuários a entender o propósito do grupo de campos e a melhorar a experiência geral de preenchimento do formulário. Em resumo, os formulários, campos `<input>` e elementos relacionados desempenham um papel vital na coleta de informações dos usuários e devem ser projetados com atenção para garantir usabilidade e acessibilidade.

## Estilização de tudo isso: CSS

O Cascading Style Sheets (CSS) desempenha um papel fundamental no design moderno de páginas web. Ele permite que se controle a apresentação visual do conteúdo, separando-a da estrutura do documento HTML. Algumas práticas-chave de CSS para criar layouts modernos incluem:

- **Flexbox e Grid**: O uso de CSS Flexbox e Grid Layout torna a criação de layouts complexos mais simples e flexíveis, permitindo o posicionamento e o dimensionamento de elementos de forma eficiente.

- **Responsividade**: O design responsivo é essencial para garantir que a página funcione bem em dispositivos de diferentes tamanhos e orientações. Media queries e unidades flexíveis (como % e em) são comumente usados para isso.

- **Acessibilidade**: Certifique-se de que seu design seja acessível, usando cores devidamente contrastantes, fontes legíveis e que respeitando as preferências do usuário e estruturas que sejam compreensíveis para todos os usuários, incluindo aqueles com deficiências. Outra parte dessa acessibilidade passa também por respeitar preferências do usuário, como manter uma navegação consistente em dark mode, reduzir o uso de animações quando assim configurado pelo usuário.

#### Mais em outro documento

## No geral

Seguir essas boas práticas modernas não apenas resulta em páginas web e sistemas visualmente mais atraentes (assim espero, pelo menos), mas também melhora a compatibilidade e acessibilidade, seja para casos de us específicos com leitores de tela, outros dispositivos de acessibilidade (no sentido mais literal da palavra) e navegação assistida mas também para sistemas de indexação (engines de busca) e dispositivos inteligentes (Alexa, Siri). Eventualmente, um código semântico e bem escrito também vai contribuir para sua mais fácil manutenção.