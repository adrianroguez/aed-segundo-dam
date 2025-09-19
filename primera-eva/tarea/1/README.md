# Code, Learn & Practice (Programación de Servicios y Procesos: "Concurrencia, procesos e hilos")

## Bloque 1: Conceptos básicos (introducción a PHP)

### Variables y Condicionales

1. **Mayor de dos números**
```php
<?php
$numero1 = 1;
$numero2 = 1;

if ($numero1 == $numero2) {
    echo "Son iguales";
} elseif ($numero1 > $numero2) {
    echo "El primer número es mayor";
} else {
    echo "El segundo número es mayor";
}
?>
```

2. **Edad permitida**
```php
<?php
$edad = 17;

if ($edad < 18) {
    echo "Eres menor de edad";
} else {
    echo "Eres mayor de edad";
}
?>
```

3. **Positivo, negativo o cero**
```php
<?php
$numero = -10;

if ($numero < 0) {
    echo "El número es negativo";
} elseif ($numero == 0) {
    echo "El número es 0";
} else {
    echo "El número es positivo";
}
?>
```

4. **Nota final**
```php
<?php
$nota = 7;

if ($nota < 5) {
    echo "Suspenso";
} elseif ($nota < 7) {
    echo "Aprobado";
} elseif ($nota < 9) {
    echo "Notable";
} else {
    echo "Sobresaliente";
}
?>
```

---

### Bucles (for, while, foreach)

5. **Contar del 1 al 100**
```php
<?php
$contador = 1;
do {
    echo $contador . "\n";
    $contador++;
} while ($contador <= 100);
?>
```

6. **Suma acumulada**
```php
<?php
$contador = 1;
$suma = 0;

while ($contador <= 50) {
    $suma += $contador;
    $contador++;
}
echo "La suma es: $suma";
?>
```

7. **Tabla de multiplicar**
```php
<?php
$numero = 5;
for ($i = 1; $i <= 10; $i++) {
    echo "$numero x $i = " . ($numero * $i) . "\n";
}
?>
```

8. **Números pares**
```php
<?php
for ($i = 2; $i <= 50; $i += 2) {
    echo $i . "\n";
}
?>
```

9. **Cuenta atrás**
```php
<?php
for ($i = 10; $i >= 1; $i--) {
    echo $i . "\n";
}
echo "¡Fin!";
?>
```

10. **Factorial**
```php
<?php
$numero = 5;
$factorial = 1;

for ($i = 1; $i <= $numero; $i++) {
    $factorial *= $i;
}
echo "$numero! = $factorial";
?>
```

---

### Combinando Condicionales y Bucles  

11. **Números primos**
```php
<?php
for ($j = 2; $j <= 50; $j++) {
    $esPrimo = true;
    for ($i = 2; $i < $j; $i++) {
        if ($j % $i == 0) {
            $esPrimo = false;
            break;
        }
    }
    if ($esPrimo) {
        echo $j . "\n";
    }
}
?>
```

12. **Fibonacci**
```php
<?php
$terminos = 20;
$a = 0;
$b = 1;

echo "$a\n";
echo "$b\n";

for ($i = 3; $i <= $terminos; $i++) {
    $siguiente = $a + $b;
    echo "$siguiente\n";
    $a = $b;
    $b = $siguiente;
}
?>
```

13. **Múltiplos de un número**
```php
<?php
$numero = 4;

for ($i = $numero; $i <= 100; $i += $numero) {
    echo "$i\n";
}
?>
```

14. **Suma de pares e impares**
```php
<?php
$pares = 0;
$impares = 0;

for ($i = 0; $i <= 100; $i++) { 
    if ($i % 2 === 0) {
        $pares += $i;
    } else {
        $impares += $i;
    }
}
echo "La suma de pares es $pares y la suma de impares es $impares";
?>
```

15. **Adivinar número**
```php
<?php
$numero = rand(1, 20);
$adivinado = false;

while (!$adivinado) {
    $nDado = readline("Ingresa un número: ");
    if ($nDado < $numero) {
        echo "El número ingresado es más pequeño\n";
    } elseif ($nDado > $numero) {
        echo "El número ingresado es más grande\n";
    } else {
        $adivinado = true;
        echo "¡Adivinaste!\n";
    }
}
?>
```

---

### Construcción de Algoritmos  

16. **Número perfecto**
```php
<?php
$numero = 8128;
$sumaDivisores = 0;

for ($i = 1; $i <= $numero / 2; $i++) {
    if ($numero % $i == 0) {
        $sumaDivisores += $i;
    }
}

if ($sumaDivisores == $numero) {
    echo "$numero es un número perfecto.\n";
} else {
    echo "$numero no es un número perfecto.\n";
}
?>
```

17. **Invertir número**
```php
<?php
$numero = 123; 
$invertido = 0;

echo "$numero\n";

while ($numero > 0) {
    $digito = $numero % 10;
    $invertido = $invertido * 10 + $digito;
    $numero = intdiv($numero, 10);
}
echo "$invertido\n";
?>
```

18. **Palíndromo**
```php
<?php
$palabra = "hola"; 
$invertido = strrev($palabra);

if ($palabra == $invertido) {
    echo "$palabra es palíndromo\n";
} else {
    echo "$palabra no es palíndromo\n";
}
?>
```

19. **Máximo común divisor (MCD)**
```php
<?php
$numero1 = 28; 
$numero2 = 18; 

while ($numero2 != 0) {
    $temp = $numero2;
    $numero2 = $numero1 % $numero2;
    $numero1 = $temp;
}

echo "El MCD es: " . $numero1 . "\n";
?>
```

20. **Triángulo de asteriscos**
```php
<?php
for ($i = 1; $i <= 5; $i++) { 
    for ($j = 1; $j <= $i; $j++) { 
        echo "*";
    }
    echo "\n";
}
?>
```
