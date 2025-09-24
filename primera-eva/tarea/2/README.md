# Code, Learn & Practice("Introducción a Php, uso de funciones")
## Número capicúa (palíndromo numérico)
```php
<?php
function esCapicua(int $n): bool
{
    $nString = (String) $n;
    $nInvertido = strrev($nString);

    if ($nString == $nInvertido) {
        return true;
    } else {
        return false;
    }
}
echo esCapicua(12321);
echo esCapicua(12345);
?>
```
---
## Escalera de asteriscos
```php
<?php
function montaniaAsteriscos(int $altura, int $repeticiones): void {
    for ($i = 1; $i <= $altura; $i++) {
        $linea = "";
        $espacios = ($altura - $i) * 2;

        for ($j = 1; $j <= $repeticiones; $j++) {
            if ($j % 2 == 0) { 
                $linea .= str_repeat(" ", $espacios) . str_repeat("*", $i);
            } else {           
                $linea .= str_repeat("*", $i);
            }
        }
        echo $linea . "\n";
    }
}
montaniaAsteriscos(4, 3);
?>
```
---
## Suma de dígitos
```php
<?php
function sumaDigitos(int $n): int
{
    $nString = (string) $n;
    $array = str_split($nString);
    $tamanio = count($array);
    $suma = 0;

    for ($i = 0; $i < $tamanio; $i++) {
        $numero = (int) $array[$i];
        $suma += $numero;
    }
    return $suma;
}
sumaDigitos(2025);
?>
```
---
## Número secreto (múltiplos de 3 o 5)
```php
<?php
function multiplosTresOCinco(int $n): array
{
    $array = [];
    for ($i = 0; $i < $n; $i++) {
        if ($i % 3 == 0 || $i % 5 == 0) {
            $array[] = 1;
        }
    }
    return $array;
}
$multiplos = multiplosTresOCinco(10);
echo array_sum($multiplos);
?>
```
---
## Secuencia de Collatz
```php
<?php
    function secuenciaCollatz(int $n): array{
        $array = [$n];
        while ($n != 1) {
            if ($n % 2 === 0) {
            $n /= 2;
            $array[] = $n;
        }else{
            $n *= 3;
            $n += 1; 
            $array[] = $n;
        }
        }
        return $array;
    }
    $secuencia = secuenciaCollatz(6);
    echo implode(", ", $secuencia);
?>
```
