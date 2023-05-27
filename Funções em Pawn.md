## 4. Funções em Pawn

As funções desempenham um papel fundamental em Pawn, permitindo a modularização e organização do código em blocos reutilizáveis. Nesta seção, exploraremos os conceitos de declaração e definição de funções, bem como os parâmetros, retorno e recursividade.

#### 4.1 Declaração e Definição de Funções

Para utilizar uma função em Pawn, é necessário declará-la antes de usá-la. A declaração de função especifica o nome da função, os tipos dos parâmetros que ela recebe(se houver) e o tipo de retorno(se houver). A definição de função contém a implementação do código da função.

```pawn
forward MyFunction(arg1, arg2);
```

Na declaração acima, a função `MyFunction` é declarada, indicando que ela recebe `arg1` e `arg2` como parâmetros, mas não especifica o tipo de retorno.

```pawn
MyFunction(arg1, arg2)
{
	// Código da função
}
```

Na definição acima, a função `MyFunction` é definida com o código a ser executado. Aqui, você pode escrever o corpo da função, que consiste nas instruções que serão executadas quando a função for chamada.

#### 4.2 Parâmetros e Retorno de Funções

As funções em Pawn podem receber parâmetros e retornar valores. Os parâmetros são valores passados para a função quando ela é chamada, permitindo que a função trabalhe com dados específicos. O valor de retorno é o valor que a função retorna após a execução.

```pawn
public MyFunction(arg1, arg2)
{
	// Código da função
	
	return resultado;
}
```

Na definição acima, `arg1` e `arg2` são os parâmetros que a função `MyFunction` recebe. Dentro da função, você pode manipular esses parâmetros e realizar operações com eles. A instrução `return` é utilizada para especificar o valor de retorno da função.

#### 4.3 Funções Predefinidas

Pawn fornece uma variedade de funções predefinidas que podem ser usadas para realizar operações comuns. Essas funções estão disponíveis para uso sem a necessidade de definição adicional. Algumas funções predefinidas comuns em Pawn incluem `printf` para impressão de texto, `strlen` para obter o comprimento de uma string e `random` para gerar números aleatórios.

Exemplo de uso da função predefinida `printf`:

```pawn
new mensagem[] = "Olá, mundo!";
printf("%s", mensagem);
```

Nesse exemplo, a função `printf` é usada para imprimir a mensagem "Olá, mundo!" na saída.

#### 4.4 Recursividade

Recursividade é a capacidade de uma função chamar a si mesma. Isso permite que a função resolva problemas complexos dividindo-os em problemas menores e resolvendo cada parte individualmente.

```pawn
forward CalculaFatorial(valor);
public CalculaFatorial(valor)
{
	if(valor <= 1)
	{
		return 1;
	}
	else
	{
		return valor * CalculaFatorial(valor - 1);
	}
}
```

Nesse exemplo, a função `CalculaFatorial` é definida de forma recursiva para calcular o fatorial de um número. A função verifica se o número é menor ou igual a 1. Se for, retorna 1. Caso contrário, chama a própria função com um número menor e multiplica o número atual pelo resultado dessa chamada.

A recursividade pode ser uma técnica poderosa, mas é importante usá-la com cuidado para evitar loops infinitos ou desempenho excessivo.

### [Sumário do Tutorial](https://github.com/device-black/pawn-tutorial/)
### [3. Estruturas de Controle](https://github.com/Device-Black/Pawn-Tutorial/blob/DeviceBlack/Estruturas%20de%20Controle.md)
### [5. Manipulação de Strings e Arrays](https://github.com/Device-Black/Pawn-Tutorial/blob/DeviceBlack/Manipula%C3%A7%C3%A3o%20de%20Strings%20e%20Arrays.md)