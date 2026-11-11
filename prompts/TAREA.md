# Tarea: Mi prompt profesional

## Funcionalidad elegida
Cálculo y evaluación de promedio final de notas de un estudiante en Java.

## Version 1: prompt basico
```text
Haz un codigo en Java que calcule el promedio de notas.
```
* **Qué cambié:** Es la versión inicial sin detalles.
* **Por qué:** Para observar qué asume la IA cuando no tiene restricciones ni contexto.
* **Qué mejoró:** Sirvió como línea base, aunque generó un código muy simple con notas fijas en consola.

## Version 2
```text
Actua como docente de programacion en Java. Crea una clase Evaluacion que calcule el promedio ponderado de 3 notas (Examen 1: 30%, Examen 2: 30%, Proyecto Final: 40%) e indique si el alumno aprueba con nota minima de 13.
```
* **Qué cambié:** Agregué el rol, el contexto académico, los porcentajes exactos y la nota mínima aprobatoria.
* **Por qué:** En la versión 1 la IA calculó un promedio simple sin reglas de negocio reales.
* **Qué mejoró:** El cálculo ahora refleja un sistema real de evaluación universitaria y determina el estado del estudiante.

## Version 3: prompt final
```text
Actua como desarrollador backend senior en Java. Crea una clase llamada CalculadoraNotas para un sistema academico universitario que calcule el promedio ponderado de un estudiante (Examen 1: 30%, Examen 2: 30%, Proyecto Final: 40%) y determine si aprueba (nota minima 13.0 sobre 20). Restriccion: No uses librerias externas ni Scanner, recibe las notas como parametros en el metodo. Sigue este estilo de firma para el metodo principal: public String evaluarEstudiante(double ex1, double ex2, double proy). Presenta primero una tabla explicando las validaciones de rango (0 a 20) y luego entrega el bloque de codigo Java comentado.
```
* **Qué cambié:** Incorporé una restricción estricta, un ejemplo de firma de método y el formato exacto de salida.
* **Por qué:** Para evitar código innecesario de entrada por consola (`Scanner`) y asegurar validación de datos.
* **Qué mejoró:** La respuesta es limpia, modular, lista para integrar en un backend y documentada exactamente como se pidió.

## Componentes del prompt final

| Componente | Texto de mi prompt |
|------------|--------------------|
| Rol | Actua como desarrollador backend senior en Java. |
| Instruccion | Crea una clase llamada CalculadoraNotas que calcule el promedio ponderado y determine si aprueba. Restriccion: No uses librerias externas ni Scanner. |
| Contexto | para un sistema academico universitario (Examen 1: 30%, Examen 2: 30%, Proyecto Final: 40%, nota minima 13.0 sobre 20). |
| Ejemplo | Sigue este estilo de firma para el metodo principal: public String evaluarEstudiante(double ex1, double ex2, double proy). |
| Formato | Presenta primero una tabla explicando las validaciones de rango (0 a 20) y luego entrega el bloque de codigo Java comentado. |

## Evaluacion del resultado

| Criterio | Cumple (Sí / No) |
|----------|------------------|
| Usa los porcentajes ponderados exactos (30%, 30%, 40%) | Sí |
| Respeta la restricción de no usar Scanner ni librerías externas | Sí |
| Incluye la tabla de validaciones antes del código | Sí |
| Usa exactamente la firma de método solicitada en el ejemplo | Sí |

## Errores que evite
1. **No dar contexto:** En la versión 1 la IA asumió un promedio aritmético simple; lo evité especificando los pesos porcentuales y la escala vigesimal (0 a 20).
2. **No indicar el formato:** Evité que la IA entregara texto desordenado exigiendo primero una tabla de validaciones y luego un bloque de código comentado.
