# Code, Learn & Practice(Acceso a Datos: "Introducción a Php")

## Bloque 1: Conceptos básicos (introducción a PHP)

### Variables y Condicionales

1. **Mayor de dos números**
```php
<?php
// Mayor de dos numeros
$numero1 = 1;
$numero2 = 1;

if ($numero1 > $numero2) {
    echo "El primer número es mayor\n";
} elseif ($numero1 < $numero2) {
    echo "El segundo número es mayor\n";
} else {
    echo "Ambos números son iguales\n";
}

```

2. **Edad permitida**
```php
<?php
// Edad permitida
$edad = 17;

if ($edad < 18) {
    echo "Eres menor de edad\n";
} else {
    echo "Eres mayor de edad\n";
}

```

3. **Positivo, negativo o cero**
```php
<?php
// Positivo, negativo o cero
$numero = 0;

if ($numero > 0) {
    echo "Es positivo\n";
} elseif ($numero < 0) {
    echo "Es negativo\n";
} else {
    echo "Es cero\n";
}

```

4. **Nota final**
```php
<?php
// Nota final
$nota = 7;

switch ($nota) {
    case $nota < 5:
        echo "Suspenso\n";
        break;
    case $nota > 4 && $nota < 7:
        echo "Aprobado\n";
        break;
    case $nota > 6 && $nota < 9:
        echo "Notable\n";
        break;
    default:
        echo "Sobresaliente\n";
        break;
}

```

---

### Bucles (for, while, foreach)

5. **Contar del 1 al 100**
```php
<?php
// Contar del 1 al 100
for ($i = 1; $i <= 100; $i++) {
    echo "$i\n";
}

```

6. **Suma acumulada**
```php
<?php
// Suma acumulada
$suma = 0;
for ($i = 1; $i <= 50; $i++) {
    $suma += $i;
}
echo "$suma\n";

```

7. **Tabla de multiplicar**
```php
<?php
// Tabla de multiplicar
$numero = 5;
for ($i = 1; $i <= 10; $i++) {
    $resultado = $numero * $i;
    echo "$numero x $i = $resultado\n";
}

```

8. **Números pares**
```php
<?php
// Numeros pares
for ($i = 1; $i <= 50; $i++) {
    if ($i % 2 == 0) {
        echo "$i\n";
    }
}

```

9. **Cuenta atrás**
```php
<?php
// Cuenta atras
for ($i = 10; $i >= 1; $i--) {
    echo "$i\n";
    if ($i == 1) {
        echo "¡Fin!\n";
    }
}

```

10. **Factorial**
```php
<?php
// Factorial
$numero = 5;
$resultado = 1;

for ($i = 1; $i <= $numero; $i++) {
    $resultado *= $i;
}

echo "$numero! = $resultado\n";

```

---

### Combinando Condicionales y Bucles  

11. **Números primos**
```php
<?php
// Numeros primos
for ($i = 2; $i <= 50; $i++) {
    $esPrimo = true;
    for ($j = 2; $j < $i; $j++) {
        if ($i % $j == 0) {
            $esPrimo = false;
            break;
        }
    }
    if ($esPrimo) {
        echo "$j\n";
    }
}

```

12. **Fibonacci**
```php
<?php
// Fibonacci
$a = 0;
$b = 1;
echo "$a\n";
echo "$b\n";

for ($i = 2; $i <= 20; $i++) {
    $siguienteNumero = $a + $b;
    $a = $b;
    $b = $siguienteNumero;
    echo "$siguienteNumero\n";
}

```

13. **Múltiplos de un número**
```php
<?php
// Multiplos de un numero
$numero = 3;
$multiplo = 0;

for ($i = 0; $i <= 100; $i++) {
    $multiplo = $numero * $i;
    echo "$multiplo\n";
}

```

14. **Suma de pares e impares**
```php
<?php
// Suma de pares e impares
$sumaPares = 0;
$sumaImpares = 0;

for ($i = 1; $i <= 100; $i++) {
    if ($i % 2 == 0) {
        $sumaPares += $i;
    } else {
        $sumaImpares += $i;
    }
}

echo "$sumaPares\n";
echo "$sumaImpares\n";

```

15. **Adivinar número**
```php
<?php
// Adivinar numero
$numero = rand(1, 20);
$adivinado = false;

while (!$adivinado) {
    $numeroIngresado = readline("Ingresa un número: \n");
    if ($numeroIngresado < $numero) {
        echo "El número ingresado es más pequeño\n";
    } elseif ($numeroIngresado > $numero) {
        echo "El número ingresado es más grande\n";
    } else {
        echo "¡Adivinaste!\n";
        break;
    }
}

```

---

### Construcción de Algoritmos  

16. **Número perfecto**
```php
<?php
// Numero perfecto
$numero = 6;
$suma = 0;

for ($i = 1; $i < $numero; $i++) {
    if ($numero % $i == 0) {
        $suma += $i;
    }
}

if ($numero == $suma) {
    echo "Es un número perfecto\n";
} else {
    echo "No es un número perfecto\n";
}

```

17. **Invertir número**
```php
<?php
// Invertir numero
$numero = 123;
echo strrev((string)$numero)."\n";

```

18. **Palíndromo**
```php
<?php
// Palindromo
$palabra = "anilina";
$invertido = strrev($palabra);

if ($palabra == $invertido) {
    echo "Es un palíndromo\n";
} else {
    "No es un palíndromo\n";
}

```

19. **Máximo común divisor (MCD)**
```php
<?php
// Maximo comun divisor (MCD)
$numero1 = 9;
$numero2 = 6;

while ($numero2 != 0) {
    $temp = $numero2;
    $numero2 = $numero1 % $numero2;
    $numero1 = $temp;
}

echo "MCD = $numero1\n";

```

20. **Triángulo de asteriscos**
```php

```
