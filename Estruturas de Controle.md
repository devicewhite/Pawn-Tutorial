## 3. Estruturas de Controle

As estruturas de controle são utilizadas em Pawn para controlar o fluxo de execução do programa com base em condições e iterações. As estruturas de controle mais comuns em Pawn incluem o condicional `if-else`, os loops `for`, `while` e `do-while`, e a estrutura `switch-case`.

#### 3.1 Condicional if-else

A estrutura condicional `if-else` permite executar blocos de código com base em uma condição booleana. Se a condição for verdadeira, o bloco de código dentro do `if` é executado. Caso contrário, o bloco de código dentro do `else`, se houver, é executado.

```pawn
new idade = 20;

if(idade >= 18)
{
	// Código a ser executado se a idade for maior ou igual a 18
	printf("Pessoa é maior de idade");
}
else
{
	// Código a ser executado se a idade for menor que 18
	printf("Pessoa é menor de idade");
}
```

Nesse exemplo, o valor da variável `idade` é verificado. Se `idade` for maior ou igual a 18, a mensagem "Pessoa é maior de idade" será impressa. Caso contrário, a mensagem "Pessoa é menor de idade" será impressa.

#### 3.2 Loops(for, while, do-while)

Os loops permitem repetir a execução de um bloco de código enquanto uma determinada condição for verdadeira. Em Pawn, existem três tipos de loops: `for`, `while` e `do-while`.

- Loop `for`:
O loop `for` é utilizado quando o número de iterações é conhecido antecipadamente. Ele possui uma estrutura que inclui uma inicialização, uma condição de continuação e uma operação de atualização.

```pawn
for(new i = 1; i <= 5; i++)
{
	// Código a ser executado a cada iteração
	printf("Valor de i: %d", i);
}
```

Nesse exemplo, o loop `for` é utilizado para imprimir os valores de `i` de 1 a 5. A variável `i` é inicializada com o valor 1, a condição `i <= 5` verifica se a iteração deve continuar, e a operação `i++` incrementa o valor de `i` a cada iteração.

- Loop `while`:
O loop `while` é utilizado quando o número de iterações é desconhecido e depende de uma condição.

```pawn
new contador = 0;

while(contador < 5)
{
	// Código a ser executado enquanto a condição for verdadeira
	printf("Contador: %d", contador);
	contador++;
}
```

Nesse exemplo, o loop `while` é utilizado para imprimir o valor do `contador` enquanto ele for menor que 5. A condição `contador < 5` é verificada antes de cada iteração.

- Loop `do-while`:
O loop `do-while` é semelhante ao loop `while`, mas a condição é verificada após a execução do bloco de código.

```pawn
new numero = 1;

do
{
	// Código a ser executado pelo menos uma vez
	printf("Número: %d", numero);
	numero++;
} while(numero <= 5);
```

N

esse exemplo, o loop `do-while` é utilizado para imprimir o valor do `numero` de 1 a 5. O bloco de código é executado pelo menos uma vez, e a condição `numero <= 5` é verificada após cada iteração.

#### 3.3 Switch-Case

A estrutura `switch-case` é utilizada quando há várias condições possíveis a serem testadas. Cada caso(`case`) representa uma condição a ser verificada, e o bloco de código correspondente é executado quando a condição é satisfeita.

```pawn
new diaSemana = 3;

switch(diaSemana)
{
	case 1: {
		printf("Domingo");
	}
	
	case 2: {
		printf("Segunda-feira");
	}

	case 3: {
		printf("Terça-feira");
	}

	default:
		printf("Dia inválido");
	}
}
```

Nesse exemplo, o valor da variável `diaSemana` é verificado usando a estrutura `switch-case`. O caso `3` é satisfeito e o bloco de código correspondente é executado, imprimindo "Terça-feira". Se `diaSemana` não corresponder a nenhum dos casos, o bloco `default` é executado, imprimindo "Dia inválido".

As estruturas de controle são ferramentas essenciais para controlar o fluxo de execução do programa e tomar decisões com base em condições específicas. Elas permitem criar lógica complexa e controlar o comportamento do programa de forma dinâmica.

### [Sumário do Tutorial](https://github.com/device-black/pawn-tutorial/)
### [2. Fundamentos da Linguagem Pawn](https://github.com/device-black/pawn-tutorial/)
### [4. Funções em Pawn](https://github.com/device-black/pawn-tutorial/)