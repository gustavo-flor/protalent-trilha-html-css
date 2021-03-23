## **O que é HTML e para que serve?**

HTML é a abreviação de **H**yper**T**ext **M**arkup **L**anguage que significa: Linguagem de marcação de hipertexto.

*Hipertexto: Mídia digital que contém um conjunto de informações ligadas através de link’s*, exemplos: *textos, imagens, vídeos, etc…*

Na sua essência, o HTML serve para apresentar informações na web, através da junção de textos com *tags*.

## **O que são tags?**

É a constituição do **M**arkup, elas servem para dar vida ao documento HTML, atribuindo características e hierarquia ao seu conteúdo. Ao inserir uma tag estamos criando um elemento dentro de nosso documento.

Fazendo uma analogia com um documento de texto padrão, ao invés de selecionar a opção “Negrito” para alterar nosso texto, em um documento HTML podemos colocar uma *tag* específica para isso.

> Olá eu sou um texto normal, **<b>**mas agora estou em negrito!**</b>**

E quando nosso documento for renderizado em uma página web, será exibido como:

> Olá eu sou um texto normal, **mas agora estou em negrito!**

Para apresentar um texto em itálico podemos fazer da mesma forma:

> <i>Estou em itálico</i> e agora <i><b>em itálico e negrito</b></i>.

Apresentado como:

> *Estou em itálico* e agora ***em itálico e negrito***.

Preciso gravar todas as *tags* HTML?

- Não, com o tempo e com o uso você vai naturalmente conhecendo qual *tag* precisa usar em determinados contextos.

Todas as *tags* mantém esse padrão de "abrir e fechar"?

- Não, temos elementos "vazios", que apenas abrimos e não fechamos, por exemplo a *tag* de apresentação de imagem.

```html
<img src="" alt="">
```

Outros exemplos são:

```html
<input type="text">
```

Podemos verificar que presente em `<img>` temos `src=""` e `alt=""`, que são os atributos **dessa *tag* (iremos falar mais pra frente sobre eles), mas podemos perceber que essas são *tags* sem conteúdo e que não precisam de fechamento*.* 

## O que são atributos?

Podem ser usados como informações extras ou configurações em nossas *tags*, voltando ao exemplo do `<img>`, temos o atributo `src` que é uma configuração que serve para apresentar o caminho onde está localizada a imagem que deve ser apresentada e também o `alt` que serve como um texto alternativo para caso a imagem informada no `src` não seja encontrada.

```html
<img src="logo-projuris.png" alt="Logo da ProJuris Sistemas LTDA">
```

Com esse elemento em um documento HTML, já poderemos visualizar uma imagem sendo apresentada, e isso só foi possível graças aos atributos. 

Temos atributos específicos de cada *tag* e também atributos globais, que podem ser usados em qualquer elemento (ou na maioria deles).

```html
<!--
	Atributos globais mais utilizados:
	
	- class
	- contenteditable
	- data-*
	- hidden
	- id
	- style
	- title
-->
<div class="item">
	<!-- conteúdo -->
</div>

<div class="item">
	<!-- conteúdo -->
</div>

<div class="item">
	<!-- conteúdo -->
</div>
```

Preciso gravar todos os atributos específicos ou globais?

- Não, da mesma forma que as tags, conforme vai surgindo a necessidade você vai conhecendo cada um deles.

## O que é aninhamento de tags

É a definição do fluxo, hierarquia e posicionamento dos elementos.

```html
<section>
	<h1>Título da minha seção</h1>
	<p>
		Contéudo da minha <b>seção</b>.
	</p>
	<img src="imagem.png" alt="Texto Alternativo">
</section>
```

Podemos verificar que neste trecho definimos um fluxo de apresentação das informações, começando pelo título até a imagem, e que demarcamos que a `<section>` é o maior elemento na hierarquia, envolvendo todos os elementos "filhos".

É importante lembrar que devemos fechar as *tags* corretamente dentro dos aninhamentos, sempre fechando os elementos "filhos" antes do elemento "pai".

```html
<p>Dessa forma <i>está errado</p>, pois não seguimos a hierarquia definida</i>

<p>Dessa forma <i>está correto</i>, pois seguimos a hierarquia :D</p>
```

- [Praticando I](./praticando.md#praticando-i)

## Qual objetivo e como criar um documento HTML

O seu principal objetivo é estruturar e apresentar a um texto ou conteúdo com significado (semântica).

Aqui temos um template padrão de um documento HTML.

```html
<!DOCTYPE html> <!-- Serve para identificar em alguns navegadores que estamos trabalhando com HTML5 -->
<html lang="pt-BR">
	<!-- Contém configurações da página -->
	<head>
		<meta charset="utf-8"> <!-- Define que o documento trabalho com carecteres codificados em utf-8 -->
		<title>Meu Título</title> <!-- Define o título apresentado na aba do navegador -->
	</head>

	<!-- Contém o conteúdo da página -->
	<body></body>
</html>
```

- [Praticando II](./praticando.md#praticando-ii)


## Semântica

Como já sabemos, precisamos dar significado ao nosso conteúdo e, por meio de nossas *tags* e *atributos*, fazemos isto. Alguns exemplos de uso semântico das tags:

- `<main>` → Representa o conteúdo principal da nossa página, é importante termos apenas um elemento deste por página;
- `<section>` → Representa uma seção de conteúdo da nossa página, podem ter várias em um único documento;
- `<header>` → Representa o cabeçalho de nossa página;
- `<footer>` → Representa o rodapé de nossa página;
- `<p>` → Representa um parágrafo;
- `<h1>, <h2>, <h3>, ...` → Representam um título, de acordo com o nível escolhido;
- `<div>` → Representa uma subdivisão sem muita semântica, , portanto devemos ter cuidado ao utiliza-la.

Existem inúmeras outras *tags* com funcionalidades diferentes, portanto devemos analisar corretamente qual a semântica queremos dar para cada conteúdo de nossa página.

## Hyperlinks

Elemento que serve para fazer a navegação entre conteúdos e páginas em um documento HTML.

Anatomia e modos de uso: 

```html
Envia para a URL informada (na mesma aba)... 
<a href="https://google.com">Vai para o Google</a>

Envia para a URL informada (em uma nova aba)...
<a href="https://google.com" target="_blank">Abre o Google</a>

---

Envia para outra página HTML presente na pasta do projeto...
<a href="./sobre.html">Sobre nós</a>

---

Envia para o conteúdo, através de seu ID.
<a href="#contato">Contato</a>

<section id="sobre">...</section>
<section id="produto">...</section>
<section id="contato">...</section>

É importante notar que para esse caso o `id` precisa estar na mesma página HTML do hyperlink.
```

- [Praticando III](./praticando.md#praticando-iii)

# Estilizando nosso documento do CSS

## O que significa CSS?

- Acrônimo para "Cascading Style Sheets", que significa "Folha de Estilo em Cascata"
- Código para criar estilos no HTML;
- HTML é a estrutura, e o CSS é a beleza;
- Não é uma linguagem de programação, é uma linguagem de estilização.

Exemplo:

[https://codepen.io/gustavo-flor/pen/bGgGpzO](https://codepen.io/gustavo-flor/pen/bGgGpzO)

Neste exemplo podemos verificar que com a ajuda do CSS um simples `h1` e `p` tiveram seus estilos totalmente modificados, vamos entender agora como começar a utilizar o CSS.

## Anatomia

Como devemos escrever o CSS para que nosso HTML entenda e consiga ser estilizado.

```css
seletor {
	propriedade: valor;
	propriedade: valor;
	...
}

---

h1 {
	color: blue;
	font-size: 24px;
}
```

### Seletores

Os seletores, servem para filtrar e selecionar os elementos que queremos estilizar, e temos inúmeras formas de selecionar um elemento através deles, vamos mostrar aqui os mais comuns:

- Tag → Podemos selecionar um elemento através de sua tag;
- Classe → Podemos selecionar um elemento através do seu atributo "class";
- Id → Podemos selecionar um elemento através do seu atributo "id";

```
/* Tag → Podemos selecionar um elemento através de sua tag */
HTML:
<h1>...</h1>

CSS:
h1 {...}

/* Classe → Podemos selecionar um elemento através do seu atributo "class", para isso devemos colocar um "." e o nome da classe */
HTML:
<div class="carro">...</div>

CSS:
.carro {...}

/* Id → Podemos selecionar um elemento através do seu atributo "id", para isso devemos colocar um "#" e o identificador */
HTML:
<div id="bloco">...</div>

CSS:
#bloco {...}

/* Children → Podemos selecionar elementos filhos através de seus elementos pais, basta demonstrarmos a hierarquia do item pai até o item filho, deste forma estilizamos apenas elementos que seguem essa hierarquia */
HTML:
<section>
	<p>Olá Mundo</p>
</section>

CSS:
section p {...}
```

É importante notar que podemos mesclar os seletores (sempre na ordem tag → id → class).

```html
<section id="produto" class="card">...</section>
```

```css
#produto.card {...} /* Correto */

#produtosection {...} /* Errado */

.card#produto {...} /* Errado */
```

### Propriedades e Valores

As propriedades, servem para definir o que será estilizado e os valores se referem a como será feita a estilização, cada propriedade tem seus determinados tipos de valores esperados.

Depois de incluirmos nosso seletor, basta adicionarmos a propriedade que desejarmos para estilizar nosso elemento. Algumas delas são:

- `color` → Define a cor da fonte dos textos  presente no conteúdo do elemento;
- `font-size` → Define o tamanho da fonte dos textos presentes no conteúdo do elemento;
- `background` → Define toda a estilização do "pano de fundo" do conteúdo do elemento;
- `font-family` → Define qual a fonte será no conteúdo daquele elemento.

Temos inúmeras outras propriedades que podem ser encontradas facilmente em: 

[Referência de CSS](https://developer.mozilla.org/pt-BR/docs/Web/CSS/Reference)

- [Praticando IV](./praticando.md#praticando-iv)

## A Cascata

E ai está o significado do "Cascading" no acrônimo de CSS, todo o estilo que declaramos no CSS é passado para seus elementos filhos, como uma "cascata" de estilos, por exemplo:

```html
<!-- Documento HTML -->
<section>
	Parágrafo bem maneiro
	<div>
		<p>Eu sou outro texto</p>
	</div>
</section>
```

```css
/* Documento CSS */
section {
	color: blue;
}
```

Estamos declarando no CSS que o elemento `section` terá seus textos com a cor azul, porém devido ao "Cascading", elementos filhos como o `p` também receberão a estilização.

## Como integrar o CSS com o HTML

Podemos escrever o CSS diretamente no HTML através da tag `<style>` adicionando ela dentro do `<head>` do nosso documento, exemplo:

```html
<head>
	<style>
		h1 {
			color: red;
		}
	</style>
</head>
<body>...</body>
```

Porém, essa não é a forma mais recomendada e então temos a opção de separar o CSS em um arquivo diferente e depois importar no nosso HTML.

- [Praticando V](./praticando.md#praticando-v)

```markdown
Utilizando o modelo `inicial` disponibilizado...

- Usar a tag `<link>` dentro do `<head>` para fazer o import do arquivos de estilo `style.css`

> Uso da tag: <link rel="stylesheet" href="CAMINHO PARA O ARQUIVO">
```

## Conclusão

Através dessa pequena trilha podemos entender que o HTML em conjunto com o CSS é uma ferramenta muito importante na construção de páginas web.

## Próximos passos

- Acessar o site [https://app.rocketseat.com.br/discover](https://app.rocketseat.com.br/discover) ;
- Completar o cadastro e cumprir os guias estelares de HTML e CSS;
