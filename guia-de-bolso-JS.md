# Introdução ao Javascript

## Lugares para se escrever o código Javascript


* Navegador (inspecionar elemento)

* Editor de textos (Sublime text)

* Node JS (https://nodejs.org)


### Navegador

Para acessar o console do seu navegador é muito fácil, no Google Chrome por exemplo basta clicar com o botão direito com uma janela aberta e escolher a opção `inspect`.


![Inspect Element](/imagens/inspect-element.png)


E depois disso a janela de console se abrirá.


![Console do Navegador](/imagens/console-navegador.png)


Pronto, agora você pode digitar seu código Javascript aqui.

### Editor de Textos

Os editores de texto são extremamente úteis pois são muito bem organizados e possuem funcionalidades extremamente produtivas.


### Node JS

Node.js é uma plataforma construída sobre o motor JavaScript do Google Chrome para facilmente construir aplicações de rede rápidas e escaláveis. Node.js usa um modelo de I/O direcionada a evento não bloqueante que o torna leve e eficiente, ideal para aplicações em tempo real com troca intensa de dados através de dispositivos distribuídos.

## Entendendo a linguagem

### Variáveis

Na programação, uma variável é um objeto (uma posição, frequentemente localizada na memória) capaz de reter e representar um valor ou expressão. Enquanto as variáveis só "existem" em tempo de execução, elas são associadas a "nomes", chamados identificadores, durante o tempo de desenvolvimento.

### Declarando variável em Javascript

Em outras linguagens é super comum encontrarmos o `tipo` da variável declarada juntamente com seu valor como por exemplo `int contador = 0`, essas linguagens são conhecidas como fortemente tipadas e geralmente são linguagens `compiladas`.

> Linguagem compilada é uma linguagem de programação em que o código fonte, nessa linguagem, é executado diretamente pelo sistema operacional ou pelo processador, após ser traduzido por meio de um processo chamado compilação, usando um programa de computador chamado compilador, para uma linguagem de baixo nível, como linguagem de montagem ou código de máquina. Scott, Michael L (2006).

O Javascript é uma linguagem fracamente tipada, ou seja, não é preciso declarar o tipo da variável.

Para se declarar uma variável em Javascript basta se colocar a palavra chave `var`.

`var contador = 0;`

Ao receber um valor, a linguagem Javascript automaticamente entende que a variável é do tipo inteiro. 

Historicamente o Javascript é considerado uma linguagem interpretada.

> Linguagem interpretada é uma linguagem de programação, onde o código fonte nessa linguagem é executado por um programa de computador chamado interpretador, que em seguida é executado pelo sistema operacional ou processador. Mesmo que um código em uma linguagem passe pelo processo de compilação, a linguagem pode ser considerada interpretada, se o programa resultante não for executado diretamente pelo sistema operacional ou processador. Fisher, Alice; Grodzinsky, Frances S (1993).

### Tipos de dados

Alguns tipos de dados mais conhecidos.

#### Undefined

Quando criamos uma variável em Javascript e não atribuímos um valor a ela, ela é uma variável undefined.

`var x ;`

#### Number

`var x = 1 ;`

`var y = 0.65 ;`


#### String

`var mensagem = "olá mundo!" ;`

`var mensagem = 'olá mundo! ;'`

#### Boolean

`var ligado = true ;`

`var ligado = false ;`


#### Object 

`var objeto = {}`

Criando um objeto

`var lucas = { altura: 1.8, peso: 80 }`

Para acessar cada valor separadamente basta "chamar" o objeto e em seguida a propriedade ou método desejado.

`lucas.peso ; // 80`

`lucas.altura ; // 1.8`

### Array

O array é uma lista de valores, geralmente valores do mesmo tipo.

`var array = []`

`var frutas = ["maçã", "pêra", "pêssego"] ;`

O array é acessado por índice, onde a primeira posição do array é a posição 0. Para acessar os valores basta inserir o índice daquele dado requerido.

`frutas[0]; // maçã`

`frutas[2]; // pêssego`

