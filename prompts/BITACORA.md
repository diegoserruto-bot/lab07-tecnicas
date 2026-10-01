# Bitacora de tecnicas avanzadas

Laboratorio 07: Tecnicas Avanzadas de Prompting.

Herramienta de IA usada: ChatGPT

## Ejercicio 2: Zero-shot, one-shot y few-shot

| Tipo      | Aciertos (de 5) | Formato de la respuesta              | Todas con el mismo formato (Si/No) |
| --------- | --------------: | ------------------------------------ | ---------------------------------- |
| Zero-shot |             5/5 | Tabla con comentario y clasificación | Si                                 |
| One-shot  |             5/5 | Lista numerada                       | Si                                 |
| Few-shot  |             5/5 | Comentario -> clasificación          | Si                                 |

## Ejercicio 3: Chain of Thought

| Pedido                                          | Respuesta de IA | Muestra pasos (Si/No) | Correcta (Si/No) |
| ----------------------------------------------- | --------------- | --------------------- | ---------------- |
| Responde solo con el número                     | 318.60          | No                    | Si               |
| Resuélvelo paso a paso y comprueba el resultado | 318.60          | Si                    | Si               |

Ver los pasos permite entender cómo se llegó al resultado y detectar posibles errores en los cálculos.

También ayuda a comprobar que la respuesta final tenga sentido y seguir el procedimiento para resolver ejercicios similares.

## Ejercicio 4: Role prompting

| Version                      | Vocabulario (sencillo/tecnico) | Usa ejemplos o codigo     | A quien le sirve mas                        |
| ---------------------------- | ------------------------------ | ------------------------- | ------------------------------------------- |
| A: Sin rol                   | Sencillo                       | Si, usa Python            | Persona que esta empezando                  |
| B: Profesor                  | Sencillo                       | Si, usa ejemplos y Python | Estudiantes que nunca han programado        |
| C: Desarrollador Java senior | Tecnico                        | Si, usa Java              | Programadores o estudiantes con experiencia |

## Ejercicio 5: Descomposicion

### Pedido completo

Se pidio a la IA crear un sistema de inventario para una tienda en un solo pedido. La respuesta fue general y propuso varias funciones y clases.

### Pedido por pasos

Se dividio el problema en cuatro pasos: primero se obtuvieron los requisitos, luego se disenaron las clases, despues se creo la clase Producto y finalmente se reviso el codigo para proponer mejoras.

La descomposicion permitio trabajar el problema de forma mas ordenada y obtener resultados especificos en cada etapa.

## Ejercicio 6: Prompt estructurado y autocritica

| Criterio                                   | Evaluacion                    |
| ------------------------------------------ | ----------------------------- |
| Tiene las 4 columnas solicitadas           | Si                            |
| Considera el bloqueo despues de 3 intentos | Si                            |
| Incluye campos vacios                      | Si, despues de la autocritica |
| Incluye correo sin @                       | Si, despues de la autocritica |
| Incluye contrasena con espacios            | Si, despues de la autocritica |
| Indica cuales casos agrego                 | Si, agrego CP-07 a CP-11      |
| Hay duplicados o casos sin sentido         | No                            |

### Prompt estructurado y autocritica

```text
<rol>Actua como analista de pruebas de software.</rol>

<contexto>Login web con correo y contrasena. La cuenta se bloquea despues de 3 intentos fallidos.</contexto>

<tarea>Piensa paso a paso que puede fallar y escribe 6 casos de prueba.</tarea>

<formato>Tabla con las columnas: ID, escenario, datos de entrada, resultado esperado.</formato>
```

```
Revisa tu tabla: faltan casos limite como campos vacios, correo sin @ o contrasena con espacios? Agrega los que falten e indica cuales agregaste.
```
