# *CSS3*

Seja bem-vindo(a) ao meu guia CSS3!

<div align="center">
  <img src="https://user-images.githubusercontent.com/124575968/231177216-7d316399-2d5f-4aff-b616-222707bd5f0d.png">
</div>

Olá, eu sou Maycon! Nesse arquivo eu tentei deixar bem resumido todo o conteúdo que estou aprendendo, se caso sinta que faltou algo ou não entendeu alguma coisa é só me chamar nas minhas redes sociais (que estão no meu perfil GitHub) e perguntar. Assim aprendemos juntos!

Deixe uma :star: !

Bons estudos!

---

CSS --> Cascading style sheets

### **O que é?**

Linguagem de estilo utilizada para definir a aparência e o layout de páginas da web.
Permite que desenvolvedores web alterem facilmente a aparência de um site sem ter que modificar o conteúdo subjacente.

Css interno (incorporado a página HTML)

Css externo (Em outra página)

---
## **Seletores e Classes:**

Seletores: usados para selecionar e aplicar estilos a elementos HTML específicos em uma página da web.

Classes: um dos tipos de seletores, permitem que aplique estilos a um ou mais elementos HTML que possuem a mesma classe.

---
### **Propriedade color:**

Responsável por mudar a cor do texto. Pode ser definida usando um nome de cor *pré-definido*, um *valor hexadecimal*, 
uma *função rgb(), rgba(), hsl() ou hsla()*.
 

**pré-definido:**

```
h1 {
  color: red;
}
```

**valor hexadecimal:**

```
 p {
  color: #008000;
}
```

**função rgb():**

```
a {
  color: rgb(255, 165, 0);
}
```

**função rgba():**

```
div {
  color: rgba(255, 0, 0, 0.5);
}
```

OBS.: **RGB** é um modelo de cor que representa as cores vermelho (R), verde (G) e azul (B). Ele é um modelo de cor aditivo, o que significa que as cores são criadas pela adição dessas três cores em diferentes intensidades. Já o **RGBA** é a mesma coisa, só que possui um 4º elemento que define a transparência/opacidade de um elemento.

### hsl() e hsla() são usadas para definir cores usando valores de matiz (hue), saturação (saturation) e luminosidade (lightness).


* **hsl() --> usa três valores como parâmetros:**

1º *MATRIZ*, representado por um ângulo em graus (de 0 a 360), 0 e 360 correspondem ao vermelho, 120 ao verde e 240 corresponde ao azul.

2º *SATURAÇÃO*, valor de porcentagem (de 0% a 100%) define a pureza ou intensidade da cor. Saturação de 0% resultará em uma cor acinzentada e uma de 100% produzirá a cor mais vibrante possível.

3º *LUMINOSIDADE*, valor de porcentagem (de 0% a 100%) define a claridade ou escuridão da cor. Um valor de 0% produzirá preto, de 50% produzirá a cor original e um valor de 100% produzirá branco.

```
h1 {
  color: hsl(180, 50%, 50%);
}
```
180 = matiz como verde-azulado, 50% = saturação, 50% = luminosidade como 50%.


* **hsla() adiciona um quarto valor que define a transparência da cor. valor de opacidade de 0 a 1, onde 0 é totalmente transparente e 1 é totalmente opaco.**

```
h2 {
  color: hsla(240, 100%, 50%, 0.5);
}
```
240 = matiz azul, 100% = saturação, 50% = luminosidade, 0.5 define a opacidade 50%.

---
### **Propriedade Background:**

 Definir a aparência do plano de fundo.

- Background-size --> tamanho da imagem de fundo;

- Background-repeat --> repetição  
* ex.: Background-repeat: no-repeat; --> imagem de fundo não deve ser repetida;

- Background-position --> posição; 

- Background-image --> imagem de fundo;
 
- Background-color --> cor de fundo;

- background-attachment --> A imagem de fundo deve se mover ou permanecer fixa à medida que a página é rolada;

- background-blend-mode --> controla como as cores de fundo e as imagens de fundo se misturam.

---
### **Propriedade Border:**

Adicionar uma borda ao redor de um elemento.

```
border: [espessura] [estilo] [cor];
```
 largura da borda, estilo (sólido, tracejado, pontilhado, etc.) e cor.


- **borda simples:**
 ```
 div {
  border: 1px solid black;
}
 ```
1 pixel de largura, estilo sólido e cor preta.


- **bordas diferentes para cada lado:**
```
p {
  border-top: 2px dotted blue;
  border-right: 4px dashed green;
  border-bottom: 6px double red;
  border-left: 8px groove orange;
}
```
Borda do top 2 pixels de largura, estilo pontilhado, cor azul.
Borda direita 4 pixels de largura, tracejado, cor verde.
Borda inferior 6 pixels de largura, estilo duplo e vermelha.
Borda esquerda 8 pixels de largura, estilo entalhado (groove) e laranja.


- **bordas arredondadas:**
```
button {
  border: 2px solid purple;
  border-radius: 10px;
}
```
borda 2 pixels de largura, estilo sólido e cor roxa


- **Border-radius** --> define o raio de arredondamento dos cantos da borda.

- **border-width:** define a largura da borda de um elemento. Pode ser definido como um único valor para todos os lados, ou valores separados para cada lado:

```
border-width: [cima] [direita] [baixo] [esquerda];
```

- **border-style:** define estilo da borda de um elemento. Pode ser definido como um único valor para todos os lados, ou valores separados para cada lado.
Valores possíveis são: none, solid, dashed, dotted, double, groove, ridge, inset, outset e hidden.

<div align="center">
  <img src="https://user-images.githubusercontent.com/124575968/231193504-c57eb2aa-ce9b-4ae7-ac9a-94e18f7f01f6.png" height="300">
</div>

```
border-style: [cima] [direita] [baixo] [esquerda];
```

- **border-color:** define a cor da borda de um elemento. Definido como um único valor para todos os lados, ou valores separados para cada lado:
Valores possíveis são: nomes (red ou blue), valores hexadecimais (como #FF0000 ou #0000FF) ou valores de cor RGB (como rgb(255, 0, 0) ou rgba(0, 0, 255, 0.8)).

```
border-color: [cima] [direita] [baixo] [esquerda];
```

- **border-image:** define uma imagem que deve ser usada como a borda de um elemento.

```
border-image: url('imagem') valor valor valor valor;
```
url('imagem') caminho da imagem de borda, os valores especificam a largura, estilo e a porcentagem de preenchimento da borda. 


- *usadas juntas para personalizar a aparência de uma borda:*
```
div {
  border-width: 2px 4px 6px 8px;
  border-style: solid dotted double dashed;
  border-color: red blue green yellow;
  border-image: url('borda.png') 20 30 round;
}
```

---
### **Propriedade Margin:**
 
Define o espaço entre os elementos. Uma margem transparente em torno de um elemento e é usada para criar espaço entre os elementos na página.
Tem quatro valores que representam o espaço ao redor de um elemento.

```
margin: [cima] [direita] [baixo] [esquerda];
```

OBS.: Único valor for definido, será aplicado a todos os quatro lados. Se dois, o primeiro valor margem superior e inferior, e o segundo se aplicará à margem esquerda e direita. Se três, primeiro margem superior, o segundo valor se aplicará à margem esquerda e direita, e o terceiro à margem inferior.

---
### **Propriedade Padding:**

Define o preenchimento interno de um elemento. Tem quatro valores que representam o preenchimento interno:

```
padding: [cima] [direita] [baixo] [esquerda];
```

Pode ser definido como um número positivo (em pixels) ou como um valor percentual (que especifica o preenchimento interno em relação ao tamanho do elemento). Usa valores como 'auto' para centralizar um elemento horizontalmente em seu contêiner.


Se um único valor for definido, aplicará à todos os quatro lados. Se dois, o primeiro aplicará ao preenchimento interno superior e inferior, e o segundo ao preenchimento interno esquerdo e direito. Se três, primeiro se aplicará ao preenchimento interno superior, o segundo ao preenchimento interno esquerdo e direito, e o terceiro valor se aplicará ao preenchimento interno inferior.

Útil para controlar a aparência visual de um elemento e pode ser usada em conjunto com outras propriedades para controlar o layout da página.

---
### **Propriedade Width e height:**

 Define a largura e a altura de um elemento.

 Usadas também em conjunto com outras propriedades de layout, como margin e padding, para controlar o tamanho e a aparência visual de um elemento na página.

- Width: largura
- max-width: largura máxima
- min-widht: largura minima

- height: altura
- max-height: largura máxima  
- min-height: largura minima

--- 
### **Propriedade Text:**

Usada para definir vários aspectos do texto em um elemento. Incluem a cor, o tamanho, o estilo, o alinhamento e o recuo do texto. 

- text-align: define o alinhamento horizontal do texto dentro do elemento. Definida como left, right, center ou justify;

- text-decoration: define a decoração do texto, como sublinhado;

- text-indent: recuo da primeira linha do texto dentro do elemento;

- text-transform: define a transformação do texto, torná-lo todo maiúsculo ou minúsculo. Definida como none, uppercase, lowercase ou capitalize;

- line-height: define a altura da linha do texto dentro do elemento. Definida em pixels, em porcentagem ou com a palavra-chave normal;

- word-space: espaço entre as palavras;

---
### **Propriedade Font:**

Define a fonte, tamanho, estilo ...

```
font: estilo tamanho/altura família;
```

- estilo: normal, italic ou oblique;

- tamanho: pixels, em, rem ou porcentagem;

- altura: opcional, controlar a altura da linha;

- família: fonte a ser usada. definida com várias opções de fallback;

```
font: italic 20px/1.5 "Helvetica Neue", Helvetica, Arial, sans-serif;
```

Tamanho 20 pixels, altura da linha como 1,5 vezes o tamanho da fonte e a fonte 'Helvetica Neue', seguida por 'Helvetica, Arial' e uma fonte genérica 'sans-serif' como fallback.


- font-family: fontes do css;

- font-size: tamanho da fonte;

- font-style: estilo;

- font-weight: grossura da fonte;

- line-height: define a altura da linha de um elemento que contém texto;

---
### **Propriedade align-items:**
Define como os itens de um container flex são alinhados verticalmente no eixo transversal (ou eixo Y). aplicada ao container flex (ou ao elemento com a propriedade display: flex) e afeta todos os itens filhos do container.

stretch: Este é o valor padrão, e faz com que os itens sejam esticados verticalmente para preencher todo o espaço disponível no container. útil quando não se sabe a altura dos itens.

flex-start: Alinha os itens no topo do container flex.

flex-end: Alinha os itens na parte inferior do container flex.

center: Centraliza os itens verticalmente no container flex.

baseline: Alinha os itens com suas linhas de base (ou seja, a linha imaginária na qual as letras "sentam").


se quiser alinhar os itens no centro vertical do container flex:

```
.container {
  display: flex;
  align-items: center;
}
```

Todos os itens dentro do elemento com a classe .container sejam centralizados verticalmente. align-items só afeta o alinhamento vertical dos itens. O alinhamento horizontal pode ser controlado pela propriedade justify-content.

---
### **Propriedade Display:**

Usada para definir como um elemento deve ser exibido na página. determina o tipo de caixa que o elemento deve ser

- none: Faz com que o elemento seja totalmente removido do fluxo da página e não seja exibido na tela. Isso é diferente de usar visibility: hidden, que esconde o elemento, mas ainda ocupa espaço na página.

- block: Faz com que o elemento seja exibido como um bloco retangular com largura total disponível. Isso significa que ele sempre começa em uma nova linha e empurra qualquer elemento abaixo dele para uma nova linha.

- inline: Faz com que o elemento seja exibido como uma caixa em linha, com apenas o tamanho necessário para conter o conteúdo. Isso significa que ele não começa em uma nova linha e só afeta o layout horizontalmente.

- inline-block: Combina as características de bloco e inline. O elemento é exibido como uma caixa em linha, mas ainda pode ter largura e altura definidas e afeta o layout horizontal e verticalmente.

- flex: Faz com que o elemento se torne um container flex, permitindo organizar seus filhos em um ou dois eixos.

- grid: Faz com que o elemento se torne um container grid, permitindo organizar seus filhos em uma grade bidimensional.

OBS.: container flex (ou flex container) é um elemento que usa a propriedade CSS display: flex (ou display: inline-flex) para criar um layout flexível. Ao aplicar display: flex a um elemento, você pode criar um container flex que é capaz de organizar seus filhos (ou itens flex) em um eixo principal (ou eixo X) e um eixo transversal (ou eixo Y).

---
### **Propriedade Position:**

Define a posição de um elemento. Permite que você controle como um elemento é posicionado em relação ao seu contêiner ou em relação à janela de visualização do navegador.

- position: static -->  valor padrão, significa que o elemento será posicionado normalmente, seguindo a ordem do fluxo do documento HTML.

- position: fixed -->  o elemento é posicionado em relação à janela de visualização do navegador, em vez de em relação ao elemento pai mais próximo.

- position: relaive --> permite que você posicione o elemento em relação à sua posição normal. Você pode usar as propriedades "top", "bottom", "left" e "right" para definir a posição relativa do elemento.

- position: absolute --> Quando um elemento é definido com a posição "absolute", ele é removido do fluxo normal do documento e posicionado em relação ao elemento pai mais próximo que tem a posição definida como "relative" ou "absolute". Você pode usar as propriedades "top", "bottom", "left" e "right" para definir a posição absoluta do elemento.

- top: topo
- bottom: abaixo
- right: direita
- left: esquerda

---
### **Propriedade Overflow:**

Define como o conteúdo que excede o tamanho do elemento deve ser tratado.

"overflow: auto" adicionará uma barra de rolagem apenas se o conteúdo exceder as dimensões do elemento;
"overflow: scroll" adicionará uma barra de rolagem mesmo que o conteúdo do elemento não exceda suas dimensões.

- visible - o conteúdo que excede o tamanho do elemento será exibido fora do elemento.

- hidden - indica que o conteúdo que excede o tamanho do elemento será ocultado e não será exibido.

- scroll - adiciona barras de rolagem ao elemento, permitindo que o usuário role o conteúdo que excede o tamanho do elemento.

- auto - Este valor adiciona barras de rolagem apenas quando o conteúdo exceder o tamanho do elemento, caso contrário, o comportamento será o mesmo que o valor "visible".

```
Define a cor de fundo da barra de rolagem 
::-webkit-scrollbar {
  background-color: #f5f5f5;
}

Define a cor da barra de rolagem 
::-webkit-scrollbar-thumb {
  background-color: #999;
}

Define a cor do indicador de rolagem ao passar o mouse
::-webkit-scrollbar-thumb:hover {
  background-color: #555;
}

Define a largura da barra de rolagem 
::-webkit-scrollbar {
  width: 12px;
}

Define a altura da barra de rolagem 
::-webkit-scrollbar {
  height: 12px;
}

Define a borda da barra de rolagem 
::-webkit-scrollbar {
  border: 1px solid #f5f5f5;
}
```

---
### **Propriedade Float:**

Define a posição de um elemento em relação a outros elementos no fluxo normal do documento. Usada para posicionar imagens e elementos ao lado do texto.

Quando um elemento é definido com a propriedade "float", ele é retirado do fluxo normal do documento e posicionado na esquerda ou na direita do elemento que o precede. Isso permite que outros elementos no fluxo normal do documento preencham o espaço restante ao redor do elemento flutuante.

- left - Esse valor faz com que o elemento flutue para a esquerda do elemento que o precede.

- right - Esse valor faz com que o elemento flutue para a direita do elemento que o precede.

- none - Esse valor é o padrão e significa que o elemento não será flutuado.

- float" pode ser usada em combinação com outras propriedades, como "width", "height" e "margin", para posicionar elementos de forma precisa na página.

pode afetar a altura do elemento pai, fazendo com que ele não envolva completamente o elemento filho flutuante. Para corrigir isso, é recomendável usar a propriedade "clear" no elemento pai, o que fará com que ele se expanda para cobrir todo o conteúdo dentro dele.

---
### **Propriedade Opacity:**

Define a transparência de um elemento, permitindo que você faça um elemento parecer mais ou menos transparente. Tem um valor entre 0 e 1, onde 0 significa completamente transparente e 1 significa completamente opaco.

criar efeitos visuais, como camadas translúcidas, sobreposições e sombras. Afeta todos os elementos dentro do elemento pai, incluindo texto e imagens. Se você quiser aplicar a transparência a um elemento específico, é melhor usar a propriedade "background-color" com um valor de transparência, em vez de usar a propriedade "opacity".


---
### Unidades de medida do css:

- px (pixels): é a unidade de medida mais comum no CSS. Um pixel é a menor unidade de exibição em uma tela e é geralmente usado para definir tamanhos absolutos.

- % (porcentagem): é uma unidade de medida relativa ao tamanho do elemento pai. Por exemplo, se definirmos a largura de um elemento como 50%, ele terá metade da largura do elemento pai.

- vh (viewport height): é uma unidade de medida relativa à altura da janela de visualização (viewport). Por exemplo, se definirmos a altura de um elemento como 50vh, ele terá metade da altura da janela de visualização.

- vw (viewport width): é uma unidade de medida relativa à largura da janela de visualização (viewport). Por exemplo, se definirmos a largura de um elemento como 50vw, ele terá metade da largura da janela de visualização.

medida relativas (%, vh e vw) são calculadas em relação às dimensões do elemento pai ou da janela de visualização, enquanto as unidades de medida absolutas (px) são definidas em unidades fixas e não dependem do contexto de exibição.

---
### **Propriedades Text shadown e box shadown:**

* Text shadown: usada para adicionar sombra ao texto.

 sintaxe básica:

 ```
 text-shadow: X Y BLUR COLOR;
 ```

X: A posição horizontal da sombra em relação ao texto.

Y: A posição vertical da sombra em relação ao texto.

BLUR: O desfoque da sombra.

COLOR: A cor da sombra.


* box-shadown: usada para adicionar sombra a um elemento, como uma caixa (div) ou imagem.

 sintaxe básica:

 ```
 box-shadow: X Y BLUR SPREAD COLOR;
 ```

X: A posição horizontal da sombra em relação ao elemento.

Y: A posição vertical da sombra em relação ao elemento.

BLUR: O desfoque da sombra.

SPREAD: A expansão da sombra.

COLOR: A cor da sombra.

---

## Animações em CSS

- animation-name: fly;

- animation-duration: 1s;

- animation-timing-function: linear;

- animation-delay: 1s;

- animation-iteration-count: infinite;

- animation-direction: alternative-reverse;

- animation-fill-mode: backwards;

- animation-play-state: paused;

- animation: name, duração, timing-funcion, delay, iteration-count, direction, fil-mode, play-state;


## Propriedade Content

A propriedade CSS content é usada com os pseudoelementos ::before e ::after para gerar conteúdo em um elemento. Objetos inseridos usando a propriedade content são elementos substituídos anônimos 1.

aceitar vários tipos de valores. Alguns exemplos incluem:

normal: Este é o valor inicial e não gera nenhum conteúdo.
none: Este valor especifica que nenhum conteúdo deve ser gerado.
<string>: Você pode especificar uma ou mais strings de texto para serem geradas como conteúdo.
<url>: Você pode especificar uma URL para um recurso externo, como uma imagem, para ser gerado como conteúdo.
attr(x): Você pode usar o valor do atributo x do elemento como conteúdo gerado.


## Propriedade inset

propriedade CSS que define a distância entre um elemento e seu elemento pai. É uma propriedade abreviada para as propriedades , , , etoprightbottomleft12. Os valores para a propriedade podem ser definidos de maneiras diferentes, dependendo do número de valores especificadosinset1.


---
Achou esse guia insuficiente? Acesse:
[Guia completo Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)

---



# **Flexbox:**

alinha elementos dentro de uma caixa (contêiner)

Display-flex: identifica que a tag vai ser o conteiner do flexbox

[![Display](https://user-images.githubusercontent.com/124575968/225451951-0318b9ea-62c8-4273-847f-8a85de224eda.png)]()

Após o display:flex

[![flex](https://user-images.githubusercontent.com/124575968/225451995-fd7eb019-cd19-4aff-be27-b222a2394845.png)]()


- flex-direction --> Define qual o eixo principal dos elementos (vertical/horizontal)
- flex-direction: row  --> sentido linha
- flex-direction: row-reverse --> linha reversa 
- flex-direction: column  --> linha em forma de coluna
- flex-direction: column-reverse --> linha em forma de coluna de baixo pra cima

[![Flex-d](https://user-images.githubusercontent.com/124575968/225462800-83aac2d5-c163-4a58-b411-f32b3c9472d3.png)]()


- Justify-content  --> Alinha os elementos no eixo principal
- Justify-content: flex-start   --> os elementos vão pro inicio do eixo principal
- Justify-content: flex-end  --> os elementos vão para o final do eixo principal
- Justify-content: center  --> agrupa os elementos no centro do eixo principal
- Justify-content: space-between -->  distribui os elementos ao longo do eixo principal (inicio, medio, fim), espaço entre os elementos
- Justify-content: space-around -->  coloca um espaço entre e por fora dos elementos
- justify-content: center --> coloca os elementos no centro do eixo (sem espaços)

[![Justify](https://user-images.githubusercontent.com/124575968/225462948-64cfc1d0-cc07-47f4-8110-0a16f0971031.png)]()
[![just](https://user-images.githubusercontent.com/124575968/225463296-3974d83e-f4ad-47ed-b3fa-2a948e00fc04.png)]()


 - align-items --> alinha os elementos no eixo perpendicular
 - align-items: flex-start  --> coloca os elementos no centro e no top
 - align-items: flex-end --> coloca os elementos no centro e embaixo
 - align-items: center  --> coloca os elementos no centro do eixo vertical e horizontal
 - align-items: stretch  --> ocupa todo o espaço no eixo perpendicular
 - align-items: baseline  -->  alinha os elementos com base nos conteúdos 

[![Align](https://user-images.githubusercontent.com/124575968/225463450-9326f528-5eef-471b-8f1f-5aaa0ba38676.png)]()
[![al](https://user-images.githubusercontent.com/124575968/225464390-62ae264a-9fb4-4429-a90c-35f4a7673694.png)]()


 - Flex-wrap --> Decide se os elementos irão para a linha de baixo quando chegarem no final ou se ficarão espremidos
 - Flex-wrap: nowrap
 - Flex-wrap: wrap
 - Flex-wrap wrap-reverse
 - flex-flow --> Identificar o flex-direction e o flex-wrap de uam vez só
 - flex-flow: rowrap

[![fel](https://user-images.githubusercontent.com/124575968/225463876-ebbd7872-156f-413d-82f1-c281fcc9cbaf.png)]()
[![ff](https://user-images.githubusercontent.com/124575968/225464500-efa67586-29a3-48a7-bf83-f1a579049118.png)]()


- Align-content --> Quando existe o flex-wrap e queremos alinhar as linhas no nosso eixo perpendicular
- Align-content: flex-start
- Align-content: flex-end
- Align-content: center
- Align-content: space-between
- Align-content: space-around

[![align-con](https://user-images.githubusercontent.com/124575968/225466368-37902b4c-259c-4f4d-ba54-4e3d6d6467c0.png)]()
[![al](https://user-images.githubusercontent.com/124575968/225464796-c0575255-e249-4569-8a91-92f7e84dee6b.png)]()


Gap, row-gap, column-gap -->Para fixar algum tamanho no espaço entre os elementos. Seja eles lado a lado ou entre eles em cada linha.

[![gap](https://user-images.githubusercontent.com/124575968/225464894-24e2ea88-0fd7-43ed-9c71-52faac25e21c.png)]()
[![row](https://user-images.githubusercontent.com/124575968/225464898-03f992ed-834e-45e3-880f-770341f29dcc.png)]()


# **Flex grid:**





# **Efeito Dropdown:**

Técnica comumente usada em design de interface de usuário que permite aos usuários selecionar uma opção de uma lista suspensa que aparece quando um elemento de interface é clicado ou passado o mouse sobre ele. O elemento de interface pode ser um botão, um menu ou uma caixa de seleção, por exemplo.

O efeito dropdown é útil para economizar espaço na tela, já que apenas um único elemento é exibido na tela, enquanto as opções adicionais ficam ocultas até que o usuário solicite sua visualização. Isso torna a interface mais limpa e organizada.

O efeito dropdown pode ser implementado em diferentes tecnologias, amplamente utilizado em sites e aplicativos.