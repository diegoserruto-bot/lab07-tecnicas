# Tarea: Mi prompt avanzado

## Tarea elegida

Generar casos de prueba para un registro de usuarios.

## Version 1: prompt basico

```text
Genera casos de prueba para un registro de usuarios.
```

## Version 2

### Tecnica agregada: Role prompting

Agregue Role Prompting

```text
Actua como analista de pruebas de software especializado en aplicaciones web.

Genera casos de prueba para un registro de usuarios.
```

## Version 3: prompt final

Agregue Few-shot y Chain of Thought

```text
Actua como analista de pruebas de software especializado en aplicaciones web.

Necesito probar el registro de usuarios de una aplicacion web.
El formulario contiene nombre, correo electronico, contrasena y confirmacion de contrasena.

Ejemplos:

Ejemplo 1:
Caso: Correo electronico invalido
Entrada: usuario@
Resultado esperado: El sistema rechaza el correo y muestra un mensaje de validacion.

Ejemplo 2:
Caso: Contrasenas diferentes
Entrada: Password123 / Password456
Resultado esperado: El sistema informa que las contrasenas no coinciden.

Tarea:

Analiza el registro de usuarios siguiendo estos pasos:
1. Identifica los escenarios normales y los posibles errores.
2. Considera datos validos, invalidos y casos limite.
3. Genera 8 casos de prueba basados en ese analisis.

Formato:

Presenta la respuesta en una tabla con las columnas:
ID | Caso de prueba | Datos de entrada | Resultado esperado
```

## Tecnicas usadas en el prompt final

| Tecnica          | Parte del prompt                                                                | Para que se uso                                                  |
| ---------------- | ------------------------------------------------------------------------------- | ---------------------------------------------------------------- |
| Role prompting   | "Actua como analista de pruebas de software especializado en aplicaciones web." | Define el rol desde el que debe responder la IA.                 |
| Few-shot         | Los dos ejemplos de casos de prueba                                             | Muestra a la IA como esperamos que sean los casos.               |
| Chain of Thought | "Analiza el registro de usuarios siguiendo estos pasos"                         | Indica los pasos que debe considerar antes de generar los casos. |

## Evaluacion del resultado

| Criterio                                                        | Evaluacion |
| --------------------------------------------------------------- | ---------- |
| Utiliza un rol especifico                                       | Si         |
| Incluye ejemplos para orientar la respuesta                     | Si         |
| Indica pasos para analizar el problema                          | Si         |
| Define un formato de respuesta                                  | Si         |
| Genera casos de prueba relacionados con el registro de usuarios | Si         |
| Presenta los casos de forma ordenada                            | Si         |
| Utiliza al menos tres tecnicas de prompting                     | Si         |

## Por que elegi estas tecnicas

Elegí Role Prompting porque permite orientar a la IA para que responda desde el punto de vista de un analista de pruebas.

Elegí Few-shot porque los ejemplos ayudan a mostrar el tipo de casos de prueba que espero obtener.

Elegí Chain of Thought porque permite indicar una serie de pasos para analizar los escenarios antes de generar los casos.
