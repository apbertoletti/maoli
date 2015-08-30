#Maoli

[![Build Status](https://travis-ci.org/aueda/maoli.svg?branch=master)](https://travis-ci.org/aueda/maoli/)

Vers�o em ingl�s: [README.md](https://github.com/aueda/maoli/)

Maoli � uma biblioteca de regras de neg�cio brasileiras comuns, compat�vel com .NET Framework 4.0 e superior.

Atualmente implementa:

* Valida��o de CEP
* Valida��o de CPF
* Valida��o de CNPJ

Para valida��o em cliente, consulte [Maoli.js](https://github.com/aueda/maoli.js/).

## Documenta��o

### Cep

``Cep.Validate(string value)`` - valida se uma string � uma representa��o v�lida de CEP. Devolve true se o CEP � v�lido; caso contr�rio, false.

```c#
	if (Cep.Validate("99999-999"))
	{
	  Console.WriteLine("CEP � v�lido");
	}
```

### Cpf

``Cpf.Validate(string value)`` - valida se uma string � uma representa��o v�lida de CPF. Devolve true se o CPF � v�lido; caso contr�rio, false.

```c#
	if (Cpf.Validate("999.999.99-99"))
	{
	  Console.WriteLine("CPF � v�lido");
	}
```

``Cpf.Complete(string value)`` - completa uma string de CPF parcial concatenando um d�gito verificador v�lido. Devolve uma string de CPF com um d�gito verificador v�lido.

```c#
	var cpf = Cpf.Complete("99999999")); // gera "99999999999" como retorno
```

### Cnpj

``Cnpj.Validate(string value)`` - valida se uma string � uma representa��o v�lida de CNPJ. Devolve true se o CNPJ � v�lido; caso contr�rio, false.

```c#
	if (Cnpj.Validate("99.999.999/9999-99"))
	{
	  Console.WriteLine("CPNJ � v�lido");
	}
```
``Cnpj.Complete(string value)`` - completa uma string de CNPJ parcial concatenando um d�gito verificador v�lido. Devolve uma string de CNPJ com um d�gito verificador v�lido.

```c#
	var cnpj = Cnpj.Complete("999999999999")); // gera "99999999999999" como retorno
```

## Pacote NuGet

Para instalar o Maoli usando o NuGet, execute o seguinte comando na linha de comando do console de Gerenciador de Pacotes:

```
Install-Package Maoli
```

## C�digo-fonte

O c�digo-fonte est� dispon�vel em [GitHub](https://github.com/aueda/maoli/).

## Licen�a

Este projeto est� sob a [licen�a MIT](http://opensource.org/licenses/MIT).

## Autor

Adriano Ueda [@adriueda](https://twitter.com/adriueda)