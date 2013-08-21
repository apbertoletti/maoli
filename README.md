#Maoli

Maoli is C# helper library for common brazilian business rules (CPF and CNPJ),
compatible with .NET Framework 4.0 and above.

Currently implements:

* CPF validation
* CNPJ validation

For client-side validation of CPF and CNPJ, please see [Maoli.js](https://github.com/aueda/maoli.js/).

## Documentation

### Cpf

``Cpf.Validate(string value)`` - checks if a string value is a valid CPF representation. Returns true if CPF string is valid; false otherwise.

```c#
	if (Cpf.Validate("999.999.99-99"))
	{
	  Console.WriteLine("CPF is valid");
	}
```

``Cpf.Complete(string value)`` - completes a partial CPF string by appending a valid checksum trailing.
Returns a CPF string with a valid checksum trailing.

```c#
	var cpf = Cpf.Complete("99999999")); // outputs "99999999999"
```

### Cnpj

``Cnpj.Validate(string value)`` - checks if a string value is a valid CNPJ representation. Returns true if CNPJ string is valid; false otherwise.

```c#
	if (Cnpj.Validate("99.999.999/9999-99"))
	{
	  Console.WriteLine("CPNJ is valid");
	}
```
``Cnpj.Complete(string value)`` - completes a partial CNPJ string by appending a valid checksum trailing.
Returns a CNPJ string with a valid checksum trailing.

```c#
	var cnpj = Cnpj.Complete("999999999999")); // outputs "99999999999999"
```

## NuGet Package

To install Maoli using NuGet, run the following command in the Package Manager Console:

```
Install-Package Maoli
```

## Source Code

Source code is available at [GitHub](https://github.com/aueda/maoli/).

## License

This project is licensed under the [MIT License](http://opensource.org/licenses/MIT).

## Author

Adriano Ueda [@adriueda](https://twitter.com/adriueda)