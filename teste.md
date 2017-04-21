# Menu
- [Variáveis](#variaveis)
- [Constantes](#constantes)

# Variáveis
>Variáveis são tipos de dados armazenados na memória RAM que tem valores que variam.

#### Regras
- Começam sempre com um cifrão antes do nome ($).
- São CaseSensitive. Fazem diferenciação entre minusculo e maiusculo.
- São fracamente tipada. O tipo da váriavel é definide de acordo com seu conteúdo.
- Nome não pode começar com numeros. Não pode conter caracteres especiais e acentuação.
- Pode conter underline no inicio ou em outras partes do nome.
- Não é necessário um valor inicial na declaração.


#### Declaração
```php
    <?php
    $nomeDaVariavel = "Valor da variável";
    $variavel = 12;
```


#### Tipos
Forçando tipo da variável com typecast: `$variavel = (int) 10;` //variavel com typecast força a conversão do tipo da variavel.
- Inteiro: `int`, `integer`.
- Real: `real`, `double`, `float`.
- Caractere: `string`.
- Lógica: `bool`, `boolean`. (variaveis logicas são considerados numeros inteiros. true=1 e false=vazio).


#### Referenciação (&)
Uma Variavel referenciada cria uma ligação/referencia entre variaveis com o simbolo &.
Sempre que uma variável referenciada mudar o valor, sua ligação tambem mudará.
EX:
```php
    <?php
    $a = 1;
    $b = &$a;
    $a = 7;
    echo $b;	// Imprime que $b = 7 pois $a e $b tem uma ligação de mão dupla por referencia.
    // Ambas apontam para o mesmo endereço de memoria;
```

#### Variaveis Variantes / Variaveis de Variaveis
Variaveis que recebem o nome com base no valor de outra variavel.
```php
    $site = "cursoemvideo";
    $$site = "CursoPHP";
```
O código acima é o mesmo que o seguinte:
```php
    $site = "cursoemvideo";
    $cursoemvideo = "CursoPHP";
```

# Constantes

Constantes são tipos de dados tambem armazenadam na memória, porém não podem variar.

#### Regras
- Regras semelhantes às regras de váriaveis, porém com algumas recomendações a mais. 
- Devem ser declaradas sempre com letras MAIUSCULAS.
- Não possuem $cifrão.
- São declaradas com o comando const ou pela função define().

#### Exemplos
```php
    <?php
    const CONSTANTE1 = 10; // Comando const
    define("CONSTANTE2", 10); // Função  define

    echo CONSTANTE1;
    echo CONSTANTE2; 
```


# Outras coisas para depois:

```php
    <?php
    echo `ls`; // é o mesmo que system('ls');
```



