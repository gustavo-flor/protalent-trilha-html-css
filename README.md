# HTML & CSS

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

### Praticando I

```html
Escrever uma seção com 2 parágrafos, utilizando ênfase e importância para algumas palavras.

- use a tag <section> para a seção;
- use a tag <i> para ênfase;
- use a tag <b> para importância;
```

## Como criar um documento

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

### Praticando II

```html
Conhecendo o template padrão, vamos criar um documento HTML do zero, 

1° Vamos criar uma pasta na Área de Trabalho do seu sistema;
2° Dentro da pasta criada, vamos inserir um documento chamado `index.html`;
3° Vamos COPIAR o template padrão.
4° Vamos inserir um título na página e adicionar no conteúdo um título e uma seção com 2 parágrafos.

- use como base o template padrão;
- use a tag `<title>` para definir o título da página;
- use a tag `<h1>` para definir o título do conteúdo;
```