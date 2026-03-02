<!-- 
Autor: Andreu
Fecha: 09/02/2026
Documento final con todas las tareas de HTML y CSS (1 a 9)
Incluye comentarios, estilos, colores, transparencias y opacidades.
-->

<!DOCTYPE html> <!-- Tarea 3 -->
<html lang="es"> <!-- Tarea 3 -->

<head>
    <meta charset="UTF-8"> <!-- Tarea 3 -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0"> <!-- Tarea 3 -->
    <title>Mi primera página CSS</title>

    <style>
        /* Estilos generales (Tareas 1 y 2) */
        body {
            background-color: lightblue;
            font-family: Arial;
        }

        /* Tarea 6: H1 color rojo (luego cambiado a HEX en Tarea 7) */
        h1 {
            color: #FF0000; /* Tarea 7 */
            text-align: center;
        }

        /* Tarea 5: fondo gris en P */
        /* Tarea 6: borde verde */
        /* Tarea 7: borde verde en HEX */
        p {
            font-size: 20px;
            color: black;
            background-color: lightgray;
            border: 5px solid #008000;
            padding: 10px;
        }

        /* Tarea 8: transparencia con RGBA */
        .transparente {
            background-color: rgba(255, 99, 71, 0.5);
            padding: 10px;
        }

        /* Tarea 9: opacity 0.5 */
        .transparencia {
            opacity: 0.5;
        }
    </style>
</head>

<body> <!-- Tarea 3 -->

    <!-- Tarea 5: H1 con fondo naranja inline -->
    <h1 style="background-color: orange;">Bienvenido a mi página</h1>

    <p>Estoy aprendiendo CSS desde cero.</p>

    <!-- Tarea 8 -->
    <h1 class="transparente">Este H1 tiene transparencia 0.5</h1>

    <!-- Tarea 9 -->
    <p class="transparencia">Transparencia 0.5</p>

</body>
</html>
classDiagram

class Cantante {
    +int id
    +string nombre
    +string generoMusical
    +string pais
}

class Concierto {
    +int id
    +string nombre
    +date fecha
    +string lugar
    +int entradasDisponibles
    +double precioEntrada
    +agregarCantante(c: Cantante)
    +reducirEntradas(cantidad: int)
}

class Entrada {
    +int id
    +string codigo
    +string tipo
    +double precio
}

class Compra {
    +int id
    +string nombreComprador
    +string correoComprador
    +date fechaCompra
    +int cantidadEntradas
    +calcularTotal()
}

%% Relaciones
Concierto "1" -- "0..*" Entrada : genera
Concierto "1" -- "1..*" Cantante : presenta
Compra "1" -- "1..*" Entrada : incluye
Compra "0..*" -- "1" Concierto : pertenece_a
