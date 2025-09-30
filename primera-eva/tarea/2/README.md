# Code, Learn & Practice("Introducción a Php, uso de funciones")
## Número capicúa (palíndromo numérico)
```php
<?php
// Numero capicua (palindromo numerico)
function esCapicua(int $numero): bool
{
    $numerotring = (string) $numero;
    $invertido = strrev($numerotring);

    if ($numerotring == $invertido) {
        return true;
    } else {
        return false;
    }
}

echo esCapicua(12321) . "\n";

```
---
## Escalera de asteriscos
```php

```
---
## Suma de dígitos
```php
<?php
// Suma de digitos
function sumaDigitos(int $numero): int
{
    $suma = 0;
    $numeroString = (string) $numero;
    $array = str_split($numeroString);
    $tamanio = count($array);

    for ($i = 0; $i < $tamanio; $i++) {
        $numeroActual = (int) $array[$i];
        $suma += $numeroActual;
    }

    return $suma;
}

echo sumaDigitos(2025) . "\n";

```
---
## Número secreto (múltiplos de 3 o 5)
```php
<?php
// Numero secreto (multiplos de 3 o 5)
function multiplosTresOCinco(int $numero): array
{
    $array = [];

    for ($i = 1; $i < $numero; $i++) {
        if ($i % 3 == 0 || $i % 5 == 0) {
            array_push($array, $i);
        }
    }

    return [
        "Números" => $array,
        "Suma" => array_sum($array)
    ];
}

print_r(multiplosTresOCinco(10));

```
---
## Secuencia de Collatz
```php
<?php
// Secuencia de Collatz
function secuenciaCollatz($numero): array
{
    $array = [$numero];

    while ($numero != 1) {
        if ($numero % 2 == 0) {
            $numero = $numero / 2;
        } else {
            $numero = $numero * 3 + 1;
        }
        $array[] = $numero;
    }

    return $array;
}

print_r(secuenciaCollatz(6));

```
