## 5. Manipulação de Strings e Arrays

A manipulação de strings e arrays é uma parte importante da programação em Pawn. Nesta seção, abordaremos as operações de string, o uso de arrays e matrizes, bem como o acesso e modificação de elementos.

#### 5.1 Operações de String

Pawn oferece um conjunto de operações para manipulação de strings. Alguns exemplos comuns incluem:

- Concatenação de strings:
A concatenação de strings é a junção de duas ou mais strings em uma única string.

```pawn
new string1[] = "Hello";
new string2[] = "World";
new resultado[50];

strcat(resultado, string1);
strcat(resultado, " ");
strcat(resultado, string2);
```

Nesse exemplo, as strings "Hello" e "World" são concatenadas usando a função `strcat`. O resultado final é armazenado na variável `resultado`.

- Comparação de strings:
A comparação de strings permite verificar se duas strings são iguais.

```pawn
new string1[] = "Hello";
new string2[] = "World";

if(strcmp(string1, string2) == 0)
{
	printf("As strings são iguais");
}
else
{
	printf("As strings são diferentes");
}
```

Nesse exemplo, a função `strcmp` é utilizada para comparar as strings "Hello" e "World". Se as strings forem iguais, a mensagem "As strings são iguais" será impressa.

#### 5.2 Arrays e Matrizes

Arrays são estruturas de dados que permitem armazenar e acessar múltiplos valores do mesmo tipo. Em Pawn, os arrays têm tamanho fixo e são indexados a partir de 0.

```pawn
new numeros[5];

numeros[0] = 10;
numeros[1] = 20;
numeros[2] = 30;
numeros[3] = 40;
numeros[4] = 50;
```

Nesse exemplo, um array chamado `numeros` é declarado com tamanho 5. Os elementos do array são acessados utilizando índices numéricos, e os valores são atribuídos a cada elemento.

As matrizes são arrays multidimensionais, ou seja, arrays que têm mais de uma dimensão. Em Pawn, as matrizes são declaradas especificando o tamanho de cada dimensão.

```pawn
new matriz[3][3];

matriz[0][0] = 1;
matriz[0][1] = 2;
matriz[0][2] = 3;
matriz[1][0] = 4;
matriz[1][1] = 5;
matriz[1][2] = 6;
matriz[2][0] = 7;
matriz[2][1] = 8;
matriz[2][2] = 9;
```

Nesse exemplo, uma matriz 3x3 chamada `matriz` é declarada. Os elementos da matriz são acessados utilizando dois índices, representando as linhas e colunas da matriz.

#### 5.3 Acesso e Modificação de Elementos

Os elementos de um array podem ser acessados e modificados utilizando os índices correspondentes.

```pawn
new numeros[3];

numeros[0] = 10;
numeros[1] = 20;
numeros[2] = 30;

printf("Valor do primeiro elemento: %d", numeros[0]);
```

Nesse exemplo, o primeiro elemento do array `

numeros` é acessado e impresso utilizando o índice 0.

Da mesma forma, os elementos de uma matriz podem ser acessados e modificados utilizando os índices das linhas e colunas.

```pawn
new matriz[2][2];

matriz[0][0] = 1;
matriz[0][1] = 2;
matriz[1][0] = 3;
matriz[1][1] = 4;

printf("Valor do elemento na segunda linha e primeira coluna: %d", matriz[1][0]);
```

Nesse exemplo, o elemento na segunda linha e primeira coluna da matriz `matriz` é acessado e impresso.

A manipulação de strings e arrays permite que os programas em Pawn trabalhem com conjuntos de dados mais complexos e realizem operações personalizadas de acordo com as necessidades do programa. Esses recursos são fundamentais para a criação de algoritmos eficientes e a manipulação de informações de forma estruturada.

### [Sumário do Tutorial](https://github.com/device-black/pawn-tutorial/)
### [4. Funções em Pawn](https://github.com/Device-Black/Pawn-Tutorial/blob/DeviceBlack/Fun%C3%A7%C3%B5es%20em%20Pawn.md)
### [6. Trabalhando com Arquivos](https://github.com/Device-Black/Pawn-Tutorial/blob/DeviceBlack/Trabalhando%20com%20Arquivos.md)