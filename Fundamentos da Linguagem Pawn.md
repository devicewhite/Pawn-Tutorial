## 2. Fundamentos da Linguagem Pawn
#### 2.1 Escopo e Blocos

Em Pawn, o escopo refere-se à região do código onde uma variável, função ou outro elemento é visível e pode ser acessado. O escopo é delimitado por blocos de código, que são conjuntos de instruções agrupadas entre chaves ({ }). Um bloco de código pode ser definido em várias partes do programa, como funções, estruturas de controle condicional (if, else), laços de repetição (for, while) ou até mesmo blocos aninhados dentro de outros blocos.

Por exemplo, considere o seguinte trecho de código em Pawn:

```pawn
// Escopo global
new x = 10;

main()
{
	// Escopo local
	new y = 5;
	print(x + y); // Resultado: 15
}
```

Nesse exemplo, temos um escopo global e um escopo local. A variável `x` é definida no escopo global e pode ser acessada tanto no escopo global quanto no escopo local. A variável `y`, por sua vez, é definida apenas no escopo local e só pode ser acessada dentro dele. O `print` exibe a soma de `x` e `y`, resultando em 15.

#### 2.2 Definições e Declarações

Em Pawn, definição e declaração são dois conceitos relacionados ao uso e à criação de elementos como variáveis, funções e constantes.

Uma definição é a criação de um elemento juntamente com sua alocação de memória. Por exemplo:

```pawn
new x = 10;
const MAX_VALUE = 100;
```

Nesse exemplo, a variável `x` é definida e inicializada com o valor 10. A constante `MAX_VALUE` é definida com o valor 100 e não pode ser alterada posteriormente.

Por outro lado, uma declaração é uma instrução que informa ao compilador a existência de um elemento, sem necessariamente alocar memória para ele. Isso permite que o compilador reconheça o elemento e permita seu uso posteriormente no programa. Por exemplo:

```pawn
forward MyFunction();
```

Nesse exemplo, a função `MyFunction` é declarada antes de sua implementação, permitindo que o compilador saiba que essa função será utilizada mais adiante.

A linguagem Pawn oferece várias palavras-chave e diretivas que são usadas em definições e declarações. Vejamos alguns exemplos:

- `new`:
```pawn
new x = 10;
```
A palavra-chave `new` é usada para criar uma nova variável e alocar memória para ela.

- `const`:
```pawn
const MAX_VALUE = 100;
```
A palavra-chave `const` é usada para definir constantes, cujo valor não pode ser alterado durante a execução do programa.

- `enum`:
```pawn
enum Days { MONDAY, TUESDAY, WEDNESDAY, THURSDAY, FRIDAY, SATURDAY, SUNDAY };
```
A palavra-chave `enum` é usada para definir um tipo de dado enumerado, onde um conjunto de valores é associado a identificadores.

- `forward`:
```pawn
forward MyFunction();
```
A palavra-chave `forward` é usada para declarar uma função/variavel antes de sua implementação, permitindo que o compilador reconheça a função/variavel antes de ela ser definida.

- `static`:
```pawn
static counter = 0;
```
A palavra-chave `static` é usada para criar uma variável estática, que mantém seu valor entre chamadas de função e só pode ser usada no arquivo em que é definida. A palavra-chave `static` também pode ser usada em funções para torná-las estáticas, com efeito similar.

- `public`:
```pawn
forward MyFunction();
public MyFunction()
{
	/ Implementação da função
}
```
A palavra-chave `public` é usada para declarar uma função como pública, permitindo seu acesso de outros arquivos, desde que a função seja declarada com `forward`.

- `stock`:
```pawn
stock MyFunction()
{
	// Implementação da função
}
```
A palavra-chave `stock` é usada para declarar funções que são criadas pelo próprio programador no script. Essas funções podem ser chamadas e utilizadas dentro do programa, caso não utilizado é descartado na compilação.

- `#define`:
```pawn
#define MAX_SIZE 100
```
A diretiva `#define` é usada para criar macros, que são substituições de texto no código fonte.

#### 2.3 Variáveis e Tipos de Dados

Em Pawn, as variáveis são utilizadas para armazenar valores em memória e podem ser de diferentes tipos de dados. Os tipos de dados mais comuns em Pawn são `int`, `bool` e `float`.

- `int`: Representa números inteiros. O tipo `int` é o tipo padrão para variáveis numéricas e não requer uma declaração explícita do tipo. Por exemplo:

```pawn
new idade = 25;
```

Nesse exemplo, a variável `idade` é do tipo `int` e é inicializada com o valor 25.

- `bool`: Representa valores booleanos, ou seja, valores que podem ser verdadeiros ou falsos. O tipo `bool` só possui dois valores possíveis: `true` e `false`. Por exemplo:

```pawn
new bool:casado = true;
```

Nesse exemplo, a variável `casado` é do tipo `bool` e é inicializada com o valor `true`.

- `float`: Representa números de ponto flutuante, ou seja, números com casas decimais. Ao contrário do tipo `int`, o tipo `float` requer uma especificação explícita do tipo ao declarar a variável. Por exemplo:

```pawn
new Float:valor = 3.14;
```

Nesse exemplo, a variável `valor` é do tipo `float` e é inicializada com o valor 3.14.

Além desses tipos de dados básicos, Pawn também suporta o uso de tags para criar tipos personalizados. As tags permitem agrupar variáveis relacionadas sob um mesmo tipo. Por exemplo:

```pawn
new Casa:primeiro;
new Homem:segundo;
```

Nesse exemplo, `Casa` e `Homem` são tags que servem como identificadores de tipos personalizados. A variável `primeiro` é do tipo `Casa`, enquanto a variável `segundo` é do tipo `Homem`.

#### 2.4 Operações Aritméticas

Pawn suporta várias operações aritméticas comuns para manipulação de valores numéricos. As operações aritméticas disponíveis incluem adição (+), subtração (-), multiplicação (*), divisão (/) e módulo (%).

Por exemplo:

```pawn
new a = 4;
new b = 2;

new soma = a + b;		// Resultado: 6
new subtracao = a - b;   // Resultado: 2
new multiplicacao = a * b;  // Resultado: 8
new divisao = a / b;	 // Resultado: 2
new modulo = a % b;	 // Resultado: 0
```

Nesse exemplo, as variáveis `a` e `b` são utilizadas para realizar operações aritméticas básicas. A variável `soma` armazena o resultado da adição de `a` e `b`, a variável `subtracao` armazena o resultado da subtração de `a` por `b`, e assim por diante.

#### 2.5 Operações Lógicas e Relacionais

Em Pawn, as operações lógicas e relacionais são utilizadas para testar condições e obter resultados booleanos. As operações lógicas mais comuns são `&&` (AND lógico), `||` (OR lógico) e `!` (NOT lógico). As operações relacionais comparam valores e retornam verdadeiro (`true`) ou falso (`false`).

Por exemplo:

```pawn
new a = 5;
new b = 3;
new c = 7;

new resultado1 = (a > b) && (b < c);	 // Resultado: true
new resultado2 = (a == b) || (b != c);  // Resultado: true
new resultado3 = !(a < b);			  // Resultado: true
```

Nesse exemplo, as variáveis `a`, `b` e `c` são utilizadas para realizar operações lógicas e relacionais.
`resultado1` é verdadeiro se `a` for maior que `b` e `b` for menor que `c`.
`resultado2` é verdadeiro se `a` for igual a `b` ou `b` for diferente de `c`.
`resultado3` é verdadeiro se `a` não for menor que `b`.

#### 2.6 Operações Lógicas Bit a Bit

Pawn também oferece suporte a operações lógicas bit a bit, que operam em nível de bits em vez de valores inteiros completos. As principais operações lógicas bit a bit incluem `&` (AND bit a bit), `|` (OR bit a bit), `^` (XOR bit a bit) e `~` (NOT bit a bit).

Por exemplo:

```pawn
new a = 5;   // 00000101
new b = 3;   // 00000011

new resultado1 = a & b;   // Resultado: 00000001 (1)
new resultado2 = a | b;   // Resultado: 00000111 (7)
new resultado3 = a ^ b;   // Resultado: 00000110 (6)
new resultado4 = ~a;	  // Resultado: 11111010 (-6)
```

Nesse exemplo, as variáveis `a` e `b` são utilizadas para realizar operações lógicas bit a bit.
`resultado1` armazena o resultado da operação AND bit a bit entre `a` e `b`.
`resultado2` armazena o resultado da operação OR bit a bit entre `a` e `b`.
`resultado3` armazena o resultado da operação XOR bit a bit entre `a` e `b`.
`resultado4` armazena o resultado da operação NOT bit a bit em `a`.

Essas operações lógicas e relacionais, bem como as operações aritméticas e lógicas bit a bit, são fundamentais para a manipulação e o processamento de dados em Pawn.