<?php
require "funciones.php";
// Casos de prueba (entrada => salida esperada)
$casos = [
    20 => "Mayor de edad",
    17 => "Menor de edad",
    -5 => "Edad inválida",
    "abc" => "Edad inválida",
    18 => "Mayor de edad"
];

// Ejecutar las pruebas
foreach ($casos as $entrada => $esperado) {
    $resultado = esMayorDeEdad($entrada);
    if ($resultado === $esperado) {
        echo "✅ Prueba con entrada '$entrada' correcta (Salida: $resultado)\n";
    } else {
        echo "❌ Prueba con entrada '$entrada' fallida (Esperado: $esperado, Obtenido: $resultado)\n";
    }
}