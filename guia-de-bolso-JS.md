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

Ao se instalar o node JS em sua máquina você pode digitar o comando `node` em seu terminal e lá poderá executar comandos Javascript no console do node que se abrirá.

## Entendendo a linguagem

### Variáveis

Na programação, uma variável é um objeto (uma posição, frequentemente localizada na memória) capaz de reter e representar um valor ou expressão. Enquanto as variáveis só "existem" em tempo de execução, elas são associadas a "nomes", chamados identificadores, durante o tempo de desenvolvimento.

### Declarando variável em Javascript

Em outras linguagens é super comum encontrarmos o `tipo` da variável declarada juntamente com seu valor como por exemplo `int contador = 0`, essas linguagens são conhecidas como fortemente tipadas e geralmente são linguagens `compiladas`.

> Linguagem compilada é uma linguagem de programação em que o código fonte, nessa linguagem, é executado diretamente pelo sistema operacional ou pelo processador, após ser traduzido por meio de um processo chamado compilação, usando um programa de computador chamado compilador, para uma linguagem de baixo nível, como linguagem de montagem ou código de máquina. Scott, Michael L (2006).

O Javascript é uma linguagem fracamente tipada, ou seja, não é preciso declarar o tipo da variável.

Para se declarar uma variável em Javascript basta se colocar a palavra chave `var`.

```js
var contador = 0;
```

Ao receber um valor, a linguagem Javascript automaticamente entende que a variável é do tipo inteiro. 

Historicamente o Javascript é considerado uma linguagem interpretada.

> Linguagem interpretada é uma linguagem de programação, onde o código fonte nessa linguagem é executado por um programa de computador chamado interpretador, que em seguida é executado pelo sistema operacional ou processador. Mesmo que um código em uma linguagem passe pelo processo de compilação, a linguagem pode ser considerada interpretada, se o programa resultante não for executado diretamente pelo sistema operacional ou processador. Fisher, Alice; Grodzinsky, Frances S (1993).

### Tipos de dados

Alguns tipos de dados mais conhecidos.

#### Undefined

Quando criamos uma variável em Javascript e não atribuímos um valor a ela, ela é uma variável undefined.

#### Null

O null é bem parecido com undefined, porém existem algumas diferenças que veremos posteriormente.

#### Number

```js
var x = 1 ;

var y = 0.65 ;
```

#### String

```js
var mensagem = "olá mundo!" ;

var mensagem = 'olá mundo!' ;
```

#### Boolean

```js
var ligado = true ;

var ligado = false ;
```


### Object 

```js
var objeto = {};
```

Criando um objeto

```js
var lucas = { 
	altura: 1.8,
	peso: 80 
};
```

Para acessar cada valor separadamente basta "chamar" o objeto e em seguida a propriedade ou método desejado.

```js
lucas.peso ; 
// 80
lucas.altura ; 
// 1.8
```

### Array

O array é uma lista de valores, geralmente valores do mesmo tipo.

```js
var array = [];

var frutas = ["maçã", "pêra", "pêssego"] ;
```

O array é acessado por índice, onde a primeira posição do array é a posição 0. Para acessar os valores basta inserir o índice daquele dado requerido.

```js
frutas[0];
// maçã
frutas[2];
// pêssego
```
> O array na linguagem Javascript nada mais é do que um **objeto disfarçado**, e como um objeto também possui suas propriedades e métodos, sendo alguns deles:

#### length

A propriedade length retorna um número inteiro com a quantidade de itens que aquele array possui.

```js
var arr = [ 'Lucas', NaN, true, false, {}, "Atlético MG"];

// para saber a quantidade de itens que esse array possui basta invocar a propriedade length
arr.length;
// 6

// utilizando o length podemos facilmente para 'varrer' um array para analisarmos todos os itens dele
```

#### métodos push e pop

O método push serve para acrescentar itens novos ao array, enquanto o método pop serve para removê-los:

```js
var frutas = ['maçã', 'pêra', 'abacaxi'];
frutas;
// ['maçã', 'pêra', 'abacaxi']

frutas.push('ameixa');
// ['maçã', 'pêra', 'abacaxi', 'ameixa']

// O método pop sempre remove o último item do array
frutas.pop();
// ['maçã', 'pêra', 'abacaxi']
```

> Ambos os comandos são executados no **final** do array.

#### unshift e shift

Os métodos unshift e shift fazem basicamente a mesma coisa que os métodos push e pop. Porém seus comandos são executados ao **início** do array.

```js
var arr = [1, 2, 3];
arr.unshift(0);

// [0, 1, 2, 3]

arr.shift();
// [1, 2, 3]
```

#### método join

O join serve para juntar itens do array em uma string com um separador passado por parâmetro:

```js
var frutas = ['maçã', 'pêra', 'abacaxi'];
frutas.join(' ');

// "maçã pêra abacaxi" 
```

#### método sort

O método sort serve para ordenar o array em ordem crescente.

```js
var frutas = ['maçã', 'pêra', 'abacaxi'];
frutas.sort();
// ['abacaxi', 'maçã', 'pêra']
```

#### reverse

O método reverse serve para inverter o array.

```js
var frutas = ['maçã', 'pêra', 'abacaxi'];
frutas.reverse();
// ['abacaxi', 'pêra', 'maçã']
```

#### toString

Faz praticamente a mesma coisa que o método join, porém o método `toString` não aceita parâmetros e separa os itens com vírgula.

```js
var frutas = ['maçã', 'pêra', 'abacaxi'];
frutas.toString();
// 'maçã,pêra,abacaxi'
```

#### concat

Efetua a concatenação de novos valores ao array, porém diferentemente do método push, o concat **não** altera o array principal.

```js
var frutas = ['maçã', 'pêra', 'abacaxi'];

frutas.concat('pêssego');
// ['maçã', 'pêra', 'abacaxi', 'pêssego']

frutas;
// ['maçã', 'pêra', 'abacaxi']
```
#### slice

[método de array e string]

O método slice serve para obtermos itens do array a partir de dois parâmetros: O primeiro é o índice que ele irá começar o retorno, e o segundo é o índice final sem contar o último número.

```js
var arr = [1, 2, 3, 4, 5];

arr.slice(1, 4);
// [2, 3, 4]

/*
Quando não passamos o segundo parâmetro o Javascript retorna, do primeiro parâmetro até o final do array
*/
arr.slice(1);
// [2, 3, 4, 5]

/*
também podemos passar parâmetros negativos, por exemplo se passarmos -2 o Javascript retorna os dois últimos itens do array
*/

arr.slice(-2)
// [4, 5] 
```

#### splice

O método splice serve para remover e até mesmo adicionar elementos a um array de maneira bem singular.

Considere a array abaixo para todos os exemplos:

```js
var arr = [1, 2, 3, 4, 5, 6, 7];
```
Se passarmos somente um parâmetro, o método apaga os itens subsequentes a partir do número passado.

```js
arr.splice(4);
// esse comando irá apagar os itens [5, 6, 7]

arr;
// [1, 2, 3, 4]
```

O segundo parâmetro corresponde a **quantidade** de itens a ser apagada.

```js
arr.splice(1, 3);
// esse comando irá apagar os itens [2, 3, 4]

arr;
// [1, 5, 6, 7]
```

Do terceiro parâmetro em diante, os itens passados serão **inseridos** ao array.

```js
arr.splice(2, 0, 'a');
// [1, 2, 'a', 3, 4, 5, 6, 7]

arr.splice(2, 0, 'b', 'c', 'd')
// [1, 2, 'b', 'c', 'd', 'a', 3, 4, 5, 6, 7]

arr.splice(2, 4, 2.5, 2.6, 2.7, 2.8, 2.9);
// [1, 2, 2.5, 2.6, 2.7, 2.8, 2.9, 3, 4, 5, 6, 7]
```

#### forEach

O forEach serve para percorrer arrays de uma maneira mais organizada e customizável.

```js
var frutas = ['pêra', 'maçã', 'abacaxi', 'manga', 'kiwi'];

frutas.forEach(function(item, index, array){
	console.log(item, index, array);
});
/*
pêra 0 [ 'pêra', 'maçã', 'abacaxi', 'manga', 'kiwi' ]
maçã 1 [ 'pêra', 'maçã', 'abacaxi', 'manga', 'kiwi' ]
abacaxi 2 [ 'pêra', 'maçã', 'abacaxi', 'manga', 'kiwi' ]
manga 3 [ 'pêra', 'maçã', 'abacaxi', 'manga', 'kiwi' ]
kiwi 4 [ 'pêra', 'maçã', 'abacaxi', 'manga', 'kiwi' ]
*/
```

#### every

Retorna true se **todos** os itens do array obedecerem a condição passada, caso contrário retorna false:

```js
var arr = [1, 2, 3, 4];

var every = arr.every(function(item) {
	return item < 2;
});
// false, pois nem TODOS os itens são menores que 2


var every = arr.every(function(item) {
	return item !== 0;
});
// true, TODOS os itens são maiores que 0
```

#### some

Retorna true se **pelo menos um** dos itens do array obedecerem a condição passada, caso contrário retorna false:

```js
var arr = [1, 2, 3, 4];

var some = arr.some(function(item) {
	return item < 2;
});
// true, pois nem PELO MENOS UM dos itens é menor que 2


var some = arr.some(function(item) {
	return === 0;
});
// false, NENHUM dos itens do array é igual a 0
```

#### map

Possui basicamente a mesma funcionalidade do forEach, a diferença é que ele retorna um **novo** array, sem modificar o array original:

```js
var arr = [1, 2, 3, 4, 5];
var map = arr.map(function(item, index, array){
	return item + 1;
});
console.log(arr, map);
// [1, 2, 3, 4, 5] [2, 3, 4, 5, 6]
```

#### filter

Filtra os dados e retorna um novo array com os itens correspondentes ao comando.

```js
var arr = [1, 2, 3, 4, 5];
var filter = arr.filter(function(item, index, array){
	return item > 2;
});

console.log(filter);
// [3, 4, 5]
```

#### reduce

O reduce funciona quando precisamos reduzir o array porém tratando com mais liberdade o item anterior na iteração:

```js
var arr = [1, 2, 3, 4];
var valorInicial = 0;

var reduce = arr.reduce(function(itemAnterior, itemAtual, index, array){
	return itemAnterior + itemAtual;
}, valorInicial)

/*
1 iteração - 0 + 1 = 1
2 iteração - 1 + 2 = 3
3 iteração - 3 + 3 = 6
4 iteração - 6 + 4 = 10
*/

console.log( reduce );
// 10
```

#### reduceRight

Faz praticamente a mesma coisa que o método reduce porém o executa de maneira inversa.

```js
var arr = ['s', 'i', 'l', 'v', 'a'];

var reduce = arr.reduceRight(function(itemAnterior, itemAtual, index, array){
	return itemAnterior + itemAtual;
});

console.log( reduce );
// avlis
```

#### indexOf

O método indexOf serve pra retornar o índice de resultados de uma busca em um array.

```js
var arr = ['l', 'u', 'c', 'a', 's'];

var index = arr.indexOf('c');
// 2

/*
quando passamos um segundo parâmetro a busca começa a partir do índice do segundo parâmetro
*/

var index2 = arr.indexOf('c', 1);
// 1

/*
quando o item passado não for encontrado o retorno é -1
*/
var index3 = arr.indexOf('l', 1);
// -1
```

#### lastIndexOf

Possui praticamente a mesma função que a função indexOf, a diferença que ele o executa de maneira inversa.

#### isArray

Retorna true se a referência passada for um array, caso contrário retorna false.

> se usarmos o operador typeof o retorno de um array é do tipo object, isso ocorre devido a um erro de implementação no Javascript, então a maneira precisa de se fazer essa verificação é pelo método isArray.

```js
var obj = {};
var arr = [];

Array.isArray(obj);
// false

Array.isArray(arr);
// true
```

### Operadores Aritméticos

Os operadores aritmáticos em Javascript são:

```js
var a = 5;
var b = 2;

// Adição
var soma = a + b;
// 7

// Subtração
var sub = a - b;
// 3

// Multiplicação
var mult = a * b;
// 10

// Divisão
var div = a / b;
// 2.5
```

#### Operadores Aritméticos Abreviados

Digamos que você possua em sua aplicação uma variável chamada `contador` e o valor dessa variável é 15 e você precisa que em algum determinado momento do seu código a mesma variável tenha que atualizar o seu valor acrescentando 1 ao seu valor final. Teoricamente o código ficaria assim:

```js
var contador = 15;
contador = contador + 1 ; 

// 16
```

Porém no Javascript temos os operadores aritméticos abreviados, podendo ser feito também da seguinte maneira:

```js
contador++;
```

Nesse caso o resultado final seria o mesmo.

Esse processo é chamado de **pós incremento** por que naquele momento em que está sendo utilizada aquela determinada linha de código, o operador ainda está interpretando o valor antigo da variável. No caso do **pré incremento** é o contrário, a variável já é interpretada com o valor somado logo de início. Esses operadores são mais simples porém são uma ótima opção para deixar o código mais limpo.

* `soma++` (pós incremento)
* `++soma` (pré incremento)
* `soma--` (pós decremento)
* `--soma` (pré decremento)

Esses operadores são muito úteis, porém os operadores citados até agora são utilizados apenas para quando queremos somar 1 ou subtrair 1 do valor. Vejamos outras utilizações mais flexíveis:

```js
contador += 10;
// pega o atual valor da variável contador e SOMA 10 e atribui a variável

contador -= 10;
// pega o atual valor da variável contador e SUBTRAI 10 e atribui a variável

contador *= 10;
// pega o atual valor da variável contador e MULTIPLICA 10 e atribui a variável

contador /= 10;
// pega o atual valor da variável contador e DIVIDE 10 e atribui a variável
```

Em resumo podemos dizer que a expressão `soma = soma + 20` é equivalente a expressão `soma += 20`. 

### Operadores Relacionais

Quando usamos estruturas de decisão em nosso código geralmente precisamos que a nossa aplicação "decida" entre uma opção e outra. Para isso usamos algumas expressões de resultado final booleano que nos auxiliam nisso.

Por exemplo se executarmos o seguinte código Javascript:

`1 == 1` ele retornará true, porque lê-se 1 é igual a 1.

Porém se executarmos `1 != 1` ele retornará false, pois essa expressão é lida como 1 é diferente de 1.

Vejamos as opções que temos em Javascript para expressões com operadores relacionais:

* `==` igual a
* `!=` diferente de
* `===` igual a, e do mesmo tipo
* `!==` diferente de, porém do mesmo tipo
* `>` maior que
* `<` menor que
* `>=` maior ou igual
* `<=` menor ou igual

Quando usamos o sinal `===` também comparamos o **tipo** da variável juntamente com seu valor.

Ex:

`true == "true";` o resultado dessa expressão é true, mas se você parar pra olhar o segundo valor está entre aspas, o que caracteriza uma String e o primeiro valor é do tipo booleano então os valores são os mesmos, porém o **tipo** da variável é diferente.

> O resultado dessas expressões é controverso em algumas versões atuais do javascript, algumas versões do Javascript comparam o tipo da variável mesmo com o operador `==`.

```js
12 == '12';
// true

12 === '12';
// false

12 != '12';
// false

12 !== '12'; 
// false
// caso as duas variáveis são diferentes, porém não são do mesmo tipo, então é retornado valor false para a expressão.

13 !== 14;
// true
// são diferentes porém são do mesmo tipo.

10 < 5;
//false

10 <= 10;
//true

10 < 10;
//false
```

### Funções

As funções são blocos repetidos de códigos que podem ser chamados por uma espécie de assinatura, o uso das funções é muito importante para legibilidade e reutilização de código por exemplo.

```js
function somarNumeros() {
	var a;
	var b;
	return a + b;
}
```

As funções podem conter ou não conter parâmetros, que nada mais são do que as variáveis que a função precisaria externamente para gerar um resultado (retorno). 

```js
function verificarSeONumeroEPar(numero){
	if (numero % 2 === 0)
		return true;
	return false;
}
```
Para invocar a função acima basta usar o nome dela e passar o valor desejado dentro dos parênteses, dessa maneira:

```js
verificarSeONumeroEPar(2);
// true

verificarSeONumeroEPar(1889231);
// false
```
Como mencionado o parâmetro `número` é a referência que essa função precisa, que venha externa ao valor.

As Principais características das funções são:

* Retornam valores

* Criam escopo

* São blocos de códigos nomeados onde podemos invocá-las no código sempre que possível

* Podem receber argumentos ou parâmetros

### Diferentes formas de se declarar uma função

Existem formas diferentes de se declarar uma função em Javascript, são elas:

#### função literal

Sintaxe:

> function nome_da_função() { }

```js
function soma() {
	return 1 + 3;
}
console.log( soma() );
// 4
```
#### função anônima

Sintaxe:

> var nome_da_variavel = function () { }

```js
var varSoma = function() {
	return 6 + 9;
}
console.log( varSoma() );
// 15
```

Desta maneira você pode ver a soma não possui nome (anônima), porém ela está sendo atribuida a uma variável então podemos invocá-la diretamente pelo nome da variável.

#### função nomeada e atribuida a uma variável

Sintaxe:

> var nome_da_variavel = function nome_da_função() { }

```js
var varSoma = function soma() { 
	return 9 + 14;
}

console.log( varSoma() );

/*
Quando declaramos a função dessa maneira podemos pegar por exemplo o nome da função através do atributo name.
*/

console.log( varSoma.name );
// soma
```
#### IIFE

A IIFE ou *Immediately-Invoked Function Expression* como o nome diz é uma função que é invocada no momento em que ela é definida. 

```js
(function(){
	console.log('Olá mundo!');
}());
```

A grande vantagem de utilizarmos IIFE se deve a criação do escopo, ou seja, tudo existente dentro daquela expressão, não é acessível fora dela, portanto não polui seu código do lado de fora.

```js
(function () {
  'use strict'
 
  var sayHi = 'oi'
  console.log(sayHi) // oi
}());
 
console.log(sayHi) // ReferenceError: sayHi is not defined
``` 

### Exercícios de Fixação 1 

Exercício de Fixação 1 em arquivo separado

### Truthy e Falsy

Como vimos anteriormente, existem expressões e/ou declarações de variáveis que se limitam somente a duas opções, `true` ou `false`. Quando declaramos uma variável em Javascript, automaticamente ela assume uma dessas propriedades por padrão. 

#### Falsy

As variáveis que são tidas pelo Javascript como falsy são:

```js
false;
NaN; // Not a Number
0;
-0;
null;
undefined;
''; // String vazia com aspas simples
""; // String vazia com aspas duplas
```

Ao analisarmos essas variáveis veremos que elas automaticamente tidas como `false`.

#### Truthy

As variáveis Truthy são todas as outras.

> Para analisarmos se uma variável é Truthy ou Falsy, basta usarmos o operador **!!**

```js
!!NaN;
// false

!!"";
// false

!!false;
// false

!!"false";
// true
``` 

> A maneira mais comum de se usar o conceito de variáveis Truthy e Falsy é em validação de dados, veja o exemplo abaixo:

```js
var operation = {
	'+': function(num1, num2) {
		return num1 + num2;
	},
	'-': function(num1, num2) {
		return num1 - num2;
	},
	'*': function(num1, num2) {
		num1 * num2;
	},
	'/': function(num1, num2) {
		num1 / num2;
	},
	'%': function(num1, num2) {
		num1 % num2;
	}
};
/*
Suponhamos que precisemos criar uma função de validação do objeto acima, essa função deve retornar true se o operador passado for algum dos operadores contidos no objeto, e false se o argumento não existir no objeto.
*/

function isOperationValid(operator) {
	return !!operation[operator];
}

/*
Dessa maneira entendemos que se passado um operador válido o Javascript irá retornar uma **função** que é truthy, e se passarmos um parâmetro inválido, ele irá retornar **undefined** que é falsy, e através do comando **!!** a função irá retornar o booleano daquela operação.
*/

console.log(isOperationValid('+'));
// true

console.log(isOperationValid('/'));
// true

console.log(isOperationValid('X'));
// false
```

### If Ternário

```js
var pessoa = {
	sexo: "Masculino"
};
var sexo = pessoa.sexo === "Feminino" ? "a"; "o";

sexo;
// o



NaN ? "verdadeiro" : "falso";
// falso

```

#### if Ternário utilizando return

Também podemos **retornar** dados de uma função com a notação ternária:

```js
function VerificaSeONumeroEPar(num) {
	return num % 2 === 0 ? true : false;
}

```

## Escopo de variáveis

Escopo é o local onde declaramos a variável. 

Existem dois tipos de escopo de variável o `global` e o `local`.

### Global

Sempre que declaramos uma variável fora de função, essa variável está sendo declarada no escopo `global`. 

```js
var nome = "lucas";
```
### Local

Quando criamos a variável dentro da função, ela está sendo criada pelo escopo `local`.

```js
var declaraNome = function() {
	var nome = "lucas";
}
```

> Legal, mas qual a diferença?

Bom, a grosso modo é que a variável criada em escopo `local`, ou seja, dentro da função, não pode ser acessada pelo lado de fora.

```js
var declaraNome = function() {
	var nome = "lucas";
}

nome;
// undefined
```

É importante sabermos que o Javascipt assim como as outras linguagens possui o *garbage collector*, que nada mais é do que um ciclo executado para limpar o ambiente daquelas variáveis ou qualquer outra coisa que não esteja sendo mais utilizada naquele momento. 

Por isso que quando criamos uma variável em Javascript devemos utilizar a palavra chave **var** porque é ela que diz ao javascript que aquela variável está no escopo local e assim assumir isso como uma boa prática na hora da programação.

```js
var MyFunction = function() {
	var x = 5;
	y = 18;
}

x;
// undefined

y;
// 18
```

> Declarar uma variável sem o prefixo **var** pode acarretar vários problemas, tais como: não reconhecimento do garbage collector, conflito de nomes, etc.

Parâmetros de funções também são locais:

```js
soma(a, b){
	return a + b;
}
soma(5, 10);
// 15

a;
// undefined

b;
// undefined
```

## Switch

sintaxe:
**switch( parametro ) {**
	**case 'opção':**
		**...;**
		**break;**
	**default:**
		**...;**
**}**

Switch é um tipo de estrutura condicional, ou seja uma estrutura de decisão utilizada para definir alguma ação para o código. Geralmente é usada para substituir o `If` em situações mais complexas.

```js
function menu(option) {
	switch(option) {
		case 'home':
			console.log('chamar página principal aqui');
			break;
		case 'about':
			console.log('página about');
			break;
		default:
			console.log('página não encontrada');
	}	
}
```

> O comando `break` é extremamente importante pois é o comando que diz ao seu código para parar de analisar a estrutura de decisão e sair dela. Portanto não podemos esquecer de utilizar esse comando.

## Estruturas de repetição (Loops)

### While

```js

```

### Do While

```js

```


### For

sintaxe:
**for( inicializador; condição; expressão final ){ ... }**

```js
for(var cont = 0; cont < 10; cont++) {
	console.log(cont);
}
/*
0
1
2
3
4
5
6
7
8
9
*/ 
```

### For In

Usado geralmente para percorrer objetos:

sintaxe:
**for( propriedades in objeto ){ ... }**

```js
var carro = {
	marca: 'VW',
	modelo: 'Fusca',
	ano: 1970,
	cor: 'vermelho'
}

for (var prop in carro) {
	console.log( prop, carro[prop] );
}
/*
marca VW
modelo Fusca
ano 1970
cor vermelho
*/
```

Ele também é usado para verificar se existe uma propriedade naquele objeto.

```js
console.log( 'marca' in carro );
// true
```

## Operador módulo %

O operador de módulo nos retorna o resto da divisão inteiro, ou seja, a representação inteira do valor que restou da divisão entre dois números.

```js
5 % 2 = 1
// ou seja o resultado da divisão é 2 e sobra 1. (2 x 2 = 4 e 5 - 4 sobra 1).
```
> Esse operador é útil por exemplo para descobrirmos se um número é par, pois é só dividir ele por 2, se houver resto ele é ímpar, e se não houver ele é par.

## Programação Funcional

```js
function calculator(operador) {
	return function calc(num1, num2) {
		var resultado = true;
		var calculo = 0;
		switch (operador) {
			case '+':
				calculo = num1 + num2;
				break;
			case '-':
				calculo = num1 - num2;
				break;
			case '*':
				calculo = num1 * num2;
				break;
			case '/':
				calculo = num1 / num2;
				break;
			case '%':
				calculo = num1 % num2;
				break;
			default:
				resultado = false;
				break;
		}
		if(resultado)
			return 'Resultado da operação: ' + num1 + operador + num2 + ' = ' + calculo;
		return 'Operação inválida';
	}
}

var sum = calculator('+');

console.log(sum(1,2));
// Resultado da operação: 1+2 = 3

var subtraction = calculator('-');
var multiplication = calculator('*');
var division = calculator('/');
var mod = calculator('%');

console.log(subtraction(4, 5));
// Resultado da operação: 4-5 = -1

console.log(multiplication(20, 5));
// Resultado da operação: 20*5 = 100

console.log(division(300, 5));
// Resultado da operação: 300/5 = 60

console.log(mod(5, 2));
// Resultado da operação: 5%2 = 1
```

### Callbacks

Callbacks basicamente são chamadas função contidas como parâmetro dentro de outra função.

```js
function calculator(number1, number2) {
	return function(callback) {
		return callback(number1, number2);
	}
}

// usando o callback através da estrutura criada acima
var soma = calculator(20, 10);
soma(function(num1, num2){
	return num1 + num2;
});
// 30
```

Como Javascript é uma linguagem baseada em eventos, é muito útil a utilização de callbacks para *encadear* funções baseadas em eventos executados.

## Typeof

Podemos verificar o **tipo** da variável usando o operador typeof:

```js
var soma = function(){}

typeof soma;
// function

typeof 'Lucas';
// string

typeof {};
// object

typeof NaN;
// number

typeof 20;
// number
```

## Herança

Herança em Javascript é um conceito que para leigos, pode ser descrito como um tanto quanto utópico, mas existe sim herança em Javascript, veja o exemplo:

```js
var objPai = { fruit: 'banana', color: 'red' }

// declaramos a herança através do método Object.create()
var objFilho = Object.create( objPai );


// até aqui tudo normal, ao executar o log do objFilho o Javascript nos diz que não existe nenhum dado dentro dele
console.log( objFilho );
// {}


// mas e se executarmos o log pedindo pra ele mostrar alguma propriedade existente SOMENTE no objPai?
console.log( objFilho.color );
// red
```

Isso é um conceito extremamente interessante para trabalharmos com reaproveitamento de código, onde podemos reaproveitar funções e métodos de maneira genérica através da herança.

### O método hasOwnProperty

Como executamos propriedades de um objeto pai dentro do objeto filho, pode ser que surja em algum momento a necessidade de verificar se aquela propriedade pertence a aquele objeto em específico, ou se essa propriedade pertence ao objeto pai, para isso usamos o método hasOwnProperty();

```js
var obj = { x: 1, y: 2 };
var obj2 = Object.create(obj);

obj2.z = 3;
console.log( obj2 );
// { z: 3 }

obj2.hasOwnProperty( 'z' );
// true

obj2.hasOwnProperty( 'x' );
// false
```

### Método prototypeOf

Esse método verifica se o objeto é herdado de algum outro objeto, caso sim ele retorna true, e caso não ele retorna false.

```js
objPai.isPrototypeOf( objFilho );
// true

objFilho.isPrototypeOf( objPai );
// false
```

### Método stringify e parse

O método stringify transforma o objeto inteiro em String:

```js
var obj = { carro: 'Onix', cor: 'Cinza', ano: 2017 };

JSON.stringify( obj );

// "{ carro: 'Onix', cor: 'Cinza', ano: 2017 }"
```

Já o método parse faz exatamente o contrário: 

```js
var objEmString = obj.stringify( obj );
// "{ carro: 'Onix', cor: 'Cinza', ano: 2017 }"


JSON.parse( objEmString );
// { carro: 'Onix', cor: 'Cinza', ano: 2017 }
```

### delete

O método delete como o próprio nome diz, apaga uma propriedade de um objeto:

```js
var obj = { x: 2, y: 56, z: 13 };

delete obj.y;

console.log(obj);
// { x: 2, z: 13 }
```

### with

[método de objeto]

O método with serve para "diminuir" caminhos em um objeto, facilitando a escrita e a legibilidade do código.

```js
var obj = {
	prop1: {
		prop2: {
			prop3: {
				prop31: 'prop 3.1',
				prop32: 'prop 3.2',
				prop33: 'prop 3.3'
			}
		}
	}
};

with( obj.prop1.prop2.prop3 ) {
	console.log( prop31, prop32, prop33);
}

// prop 3.1 prop 3.2 prop 3.3
```

### Replace

[método de String]

Substitui um char ou mais, para outro, ambos passados em parâmetro.

> replace(string, novaString)

```js
var name = 'lucas-maia-e-silva';
name.replace('-', ' ');
// lucas maiaesilva
// o método replace para sua execução no primeiro item encontrado
```

### Substring

O método substring funciona basicamente da mesma maneira que o método slice, porém a diferença entre eles é que o substring só funciona para strings e, diferente do método slice, o método substring **também** aceita que o primeiro parâmetro seja maior que o segundo.

```js
'lucas'.substring(5, 2);
// cas

'lucas'.substring(2, 5);
// cas
```

## Expressões Regulares

Expressões regulares são comandos escritos em uma sintaxe diferente da habitual da linguagem e que servem basicamente para **manipulação avançada de strings**.

sintaxe:
**/expressão/modificador**

### Modificadores

Os modificadores são usados como um parâmetro no final da regex para nos mostrar qual será a forma de capturar essas expressões:

* O modificador `g` significa que iremos capturar todas as expressões que fizerem o *match* com a string

* O modificador `i` siginifica *ignore case*, ou seja, ele irá ignorar se a letra buscada na regex é maiúscula ou minúscula e irá tratar as duas da mesma forma

* O Multiline `m` serve para tratarmos strings que possuem quebra de linha, e para tratarmos todas as linhas como início de linha, através do caractere ^ o qual veremos mais sobre ele abaixo.

### lista []

A lista serve para capturar ou fazer *match* com algum dos itens contidos nela. Ao usarmos a sintaxe ela faz o match da expressão se pelo menos UM item estiver na string.

### Grupo ou Captura ()

Os parênteses servem para agrupar itens ou para capturar trechos específicos da nossa expressão regular.

### Caracteres Alfanuméricos \w

Os caracteres alfanuméricos, são reconhecidos pelo `\w` ou em representação de lista, os seguintes caracteres `[A-Za-z0-9_]`.


### Dígitos \d

Usamos a expressão `\d` quando queremos pegar os dígitos, ou seja, caracteres numéricos `[0-9]`. 


### Espaço em branco \s, quebra de linha \n e tabulação \t

A expressão `\s` serve para selecionarmos os espaços em branco na expressão regular e `\n` todas as quebras de linha dentro da String e com `\t`, selecionamos todas as tabulações no código.

