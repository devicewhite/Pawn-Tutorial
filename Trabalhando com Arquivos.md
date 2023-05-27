## 6. Trabalhando com Arquivos

O trabalho com arquivos é essencial em muitos programas, pois permite a leitura, escrita e manipulação de dados armazenados externamente. Nesta seção, abordaremos a leitura e escrita de arquivos em Pawn.

#### 6.1 Leitura e Escrita de Arquivos

Para ler e escrever em arquivos em Pawn, são utilizadas funções específicas da biblioteca padrão do Pawn, como `fopen`, `fread`, `fwrite` e `fclose`.

```pawn
new File:arquivo = fopen("arquivo.txt", io_write);

if(arquivo != File:0)
{
	fwrite(arquivo, "Ola, mundo!");
	fclose(arquivo);
}
```

Nesse exemplo, o arquivo "arquivo.txt" é aberto para escrita usando a função `fopen`. Em seguida, a função `fwrite` é utilizada para escrever a string "Olá, mundo!" no arquivo. Por fim, o arquivo é fechado usando a função `fclose`.

Para ler o conteúdo de um arquivo, pode-se utilizar a função `fread`. Veja o exemplo a seguir:

```pawn
new File:arquivo = fopen("arquivo.txt", io_read);

if(arquivo != File:0)
{
	new buffer[100];
	fread(arquivo, buffer, sizeof(buffer));
	printf("Conteúdo do arquivo: %s", buffer);
	fclose(arquivo);
}
```

Nesse exemplo, o arquivo "arquivo.txt" é aberto para leitura. Um buffer é declarado para armazenar o conteúdo do arquivo. A função `fread` lê o conteúdo do arquivo para o buffer. Por fim, o conteúdo do arquivo é impresso na tela.

A manipulação de arquivos em Pawn permite a interação com o sistema de arquivos e facilita a leitura e escrita de dados armazenados externamente. Essas operações são úteis para o processamento de arquivos de configuração e armazenamento de dados persistentes.

### [Sumário do Tutorial](https://github.com/device-black/pawn-tutorial/)
### [5. Manipulação de Strings e Arrays](https://github.com/Device-Black/Pawn-Tutorial/blob/DeviceBlack/Manipula%C3%A7%C3%A3o%20de%20Strings%20e%20Arrays.md)
### [7. Callbacks e Eventos](https://github.com/Device-Black/Pawn-Tutorial/blob/DeviceBlack/Callbacks%20e%20Eventos.md)