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


#### Object 

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

#### método push

O método push serve para acrescentar itens novos ao array, esse método é extremamente utilizado.

```js
var frutas = ['maçã', 'pêra', 'abacaxi'];
frutas;
// ['maçã', 'pêra', 'abacaxi']

frutas.push('ameixa');
// ['maçã', 'pêra', 'abacaxi', 'ameixa']
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
			break;
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
**for( inicializador; condição; expressão final )**

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

### Foreach

```js

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