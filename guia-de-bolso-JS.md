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

`var contador = 0;`

Ao receber um valor, a linguagem Javascript automaticamente entende que a variável é do tipo inteiro. 

Historicamente o Javascript é considerado uma linguagem interpretada.

> Linguagem interpretada é uma linguagem de programação, onde o código fonte nessa linguagem é executado por um programa de computador chamado interpretador, que em seguida é executado pelo sistema operacional ou processador. Mesmo que um código em uma linguagem passe pelo processo de compilação, a linguagem pode ser considerada interpretada, se o programa resultante não for executado diretamente pelo sistema operacional ou processador. Fisher, Alice; Grodzinsky, Frances S (1993).

### Tipos de dados

Alguns tipos de dados mais conhecidos.

#### Undefined

Quando criamos uma variável em Javascript e não atribuímos um valor a ela, ela é uma variável undefined.

#### Null

O null é bem parecido com undefined, porém existem algumas diferenças que veremos posteriormente.

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


### Operadores Aritméticos

Os operadores aritmáticos em Javascript são:

* `Adição +` ( `1 + 2 ; //3`)
* `Subtração -` ( `5 - 1 ; //4`)
* `Multiplicação *` ( `3 * 5 ; //15`)
* `Divisão /` ( `10 / 2 ; //5`)

#### Operadores Aritméticos Abreviados

Digamos que você possua em sua aplicação uma variável chamada `contador` e o valor dessa variável é 15 e você precisa que em algum determinado momento do seu código a mesma variável tenha que atualizar o seu valor acrescentando 1 ao seu valor final. Teoricamente o código ficaria assim:

`contador = contador + 1 ; //16`

Porém no Javascript temos os operadores aritméticos abreviados, podendo ser feito também da seguinte maneira:

`contador++`

Nesse caso o resultado final seria o mesmo.

Esse processo é chamado de **pós incremento** por que naquele momento em que está sendo utilizada aquela determinada linha de código, o operador ainda está interpretando o valor antigo da variável. No caso do **pré incremento** é o contrário, a variável já é interpretada com o valor somado logo de início. Esses operadores são mais simples porém são uma ótima opção para deixar o código mais limpo.

* `soma++` (pós incremento)
* `++soma` (pré incremento)
* `soma--` (pós decremento)
* `--soma` (pré decremento)

Esses operadores são muito úteis, porém os operadores citados até agora são utilizados apenas para quando queremos somar 1 ou subtrair 1 do valor. Vejamos outras utilizações mais flexíveis:

* `contador += 10` (pega o atual valor da variável contador e **soma** 10 e atribui a variável)
* `contador -= 10` (pega o atual valor da variável contador e **subtrai** 10 e atribui a variável)
* `contador /= 10` (pega o atual valor da variável contador e **divide** 10 e atribui a variável)
* `contador *= 10` (pega o atual valor da variável contador e **multiplica** 10 e atribui a variável)

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

`12 == '12'; // true`.

`12 === '12'; // false`.

`12 != '12'; // false`.

`12 !== '12'; // false`, nesse último caso as duas variáveis são diferentes, porém não são do mesmo tipo, então é retornado valor false para a expressão.


`13 !== 14; //true`, são diferentes porém são do mesmo tipo.

`10 < 5; //false`. 

`10 <= 10; //true`.

`10 < 10; //false`.

### Funções

