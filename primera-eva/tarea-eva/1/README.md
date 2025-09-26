# Acceso a Datos: "Ficheros"

### 1) Hola fichero (crear y leer)
```php
<?php
file_put_contents("datos.txt", "Hola Mundo desde PHP\n");
echo file_get_contents("datos.txt");
```
### 2) Guardar números en un fichero
```php
<?php
$file = fopen("numeros.txt", "w");
for ($i = 0; $i <= 10; $i++) {
    fwrite($file, $i . "\n");
}
fclose($file);
$file = fopen("numeros.txt", "r");
echo fread($file, filesize("numeros.txt"));
```
### 3) Contar palabras en un fichero
```php
<?php
$contenido = file_get_contents("texto.txt");
echo $contenido . "\n";
echo str_word_count($contenido) . "\n";
```
### 4) Escribir y leer array en fichero
```php
<?php
$file = fopen("nombres.txt", "w");
$array = ["Ana", "Luis", "Marta", "Carlos", "Julia"];
for ($i = 0; $i <= sizeof($array); $i++) {
    fwrite($file, $array[$i] . "\n");
}
fclose($file);
$file = fopen("nombres.txt", "r");
echo fread($file, filesize("nombres.txt"));
```
### 5) Copiar contenido de un fichero a otro
```php
<?php
$copiar = copy("origen.txt", "copia.txt");
echo file_get_contents("origen.txt") . "\n";
echo file_get_contents("copia.txt") . "\n";
```
### 6) Invertir el contenido de un fichero
```php
<?php
$frase = file_get_contents("frase.txt");
$fraseInvertida = strrev($frase);
file_put_contents("frase_invertida.txt", $fraseInvertida);
echo file_get_contents("frase_invertida.txt") . "\n";
```
### 7) Calcular suma desde fichero
```php
<?php
$numeros = explode(",", file_get_contents("datos_numericos.txt"));
echo array_sum($numeros) . "\n";
```
### 8) Crear fichero de multiplicaciones
```php
<?php
$file = fopen("tabla5.txt", "w");
for ($i = 0; $i <= 10; $i++) {
    $resultado = 5 * $i;
    $calculo = "5 x $i = $resultado"."\n";
    $escribir = fwrite($file, $calculo);
}
fclose($file);
echo file_get_contents("tabla5.txt");
```
### 9) Registrar entradas de usuario
```php
<?php
$file = fopen("usuarios.txt", "w");
do {
    $nombre = readline("¿Quién eres? ");
    if (!empty($nombre) || !is_null($nombre)) {
        fwrite($file, $nombre . "\n");
    }
} while ($nombre);
echo implode(file("usuarios.txt"));
```
### 10) Leer JSON desde fichero
```php
<?php
$datos = file_get_contents("datos.json");
$datosConvertidos = json_decode($datos);
foreach ($datosConvertidos as $nombre => $value) {
    echo $value -> ombre . "\n";
}
```
### 11) Diario personal secreto
```php

```
### 12) Ranking de videojuegos
```php

```
### 13) Canción aleatoria
```php

```
### 14) Generador de excusas divertidas
```php

```
### 15) Lista de chistes (rotativos)
```php

```
### 16) Adivina la palabra
```php

```
### 17) Generador de nombres para superhéroes
```php

```
### 18) Encuesta de comidas favoritas
```php

```
### 19) Simulador de tweets
```php

```
20) Historias locas (Mad Libs)
```php

```
