# Bitacora de prompts

Laboratorio 06: Fundamentos de Ingenieria de Prompts.
Herramienta de IA usada: (Escribe aquí si usas ChatGPT, Gemini, Claude, etc.)

## Ejercicio 2: Tokens y ventana de contexto


| Texto | Caracteres | Tokens |
|-------|------------|--------|
| Los estudiantes programan en Java. | 34 | 7 |
| The students program in Java. | 29 | 6 |
| desafortunadamente | 18 | 4 |

### Observación de la ventana de contexto
* **En el mismo chat:** La IA respondió correctamente porque la información previa aún se encontraba guardada dentro de su ventana de contexto activa.
* **En el chat nuevo:** La IA no supo responder porque al iniciar una nueva conversación, la ventana de contexto empieza completamente vacía desde cero.

## Ejercicio 3: Temperatura
| Temperatura | % de BiblioTec | Nombres en los 5 intentos |
|-------------|----------------|---------------------------|
| 0 | 100,0 % | (BiblioTec, BiblioTec, BiblioTec, BiblioTec, BiblioTec) |
| 0.5 | 65,3 % | (LectoGo, BiblioTec, BiblioTec, BiblioTec, BiblioTec) |
| 1 | 44,5 % | (BiblioTec, LibroYa, PrestaLibro, PaginaLibre, LibroYa) |
| 1.8 | 32,2 % | (BiblioTec, LibroYa, PaginaLibre, LibroYa, PrestaLibro) |

Al subir la Temperatura, las probabilidades se reparten de manera proporcional y aparecen opciones menos frecuentes,hacendo que los resultados sean más variados. Sin embargo, el simulador nunca inventa un nombre nuevo porque la temperatura solo altera el nivel de riesgo al elegir entre las opciones que ya existen en su lista de conocimiento previo.
## Ejercicio 4: Prompt vago vs estructurado
| Criterio | Prompt vago | Prompt estructurado |
|----------|-------------|---------------------|
| Menciona el objetivo del sistema | Si | Si |
| Menciona a los usuarios principales | No | Si |
| Tiene exactamente 3 funcionalidades | No | Si |
| Esta en 3 parrafos | No | Si |
| Lo usaria en un informe real | No | Si |
## Ejercicio 5: Anatomia de un prompt
| Componente | Texto de mi prompt |
|------------|--------------------|
| Rol | Actua como desarrollador Java. |
| Instruccion | Crea un programa en Java usando una clase Producto con los atributos codigo, nombre, precio y stock. |
| Contexto | para gestionar los productos de una tienda |
| Ejemplo | Usa este estilo para los metodos: getPrecio(), setPrecio(double precio). |
| Formato | Explica primero la estructura de la clase y luego presenta el codigo Java. |
