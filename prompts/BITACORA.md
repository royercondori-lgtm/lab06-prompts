# Bitacora de prompts
 
Laboratorio 06: Fundamentos de Ingenieria de Prompts.
 
Herramienta de IA usada: (escribe aqui cual usaste)
 
## Ejercicio 2: Tokens y ventana de contexto

## Ejercicio 2: Tokens y ventana de contexto

| Texto | Caracteres | Tokens |
|-------|------------|--------|
| Los estudiantes programan en Java. | 35 | 7 |
| The students program in Java. | 31 | 7 |
| desafortunadamente | 19 | 5 |
 
## Ejercicio 3: Temperatura

| Temperatura | % de BiblioTec | Nombres en los 5 intentos |
|-------------|----------------|---------------------------|
| 0 |100.0%|5 intentos: BiblioTec, BiblioTec, BiblioTec, BiblioTec, BiblioTec |
| 0.5 |65.3% |5 intentos: LectoGo, BiblioTec, LibroYa, BiblioTec, LectoGo |
| 1 | 44.5%  |5 intentos: PrestaLibro, LibroYa, LibroYa, LibroYa, PrestaLibr |
| 1.8 | 32.2%  |5 intentos: BiblioTec, BiblioTec, BiblioTec, LibroYa, LibroYa |

Al subir la temperatura, las probabilidades se distribuyen haciendo las respuestas más variadas e impredecibles.
El simulador nunca inventa un nombre nuevo porque solo elige entre las opciones preexistentes dentro de su vocabulario.


## Ejercicio 4: Prompt vago vs estructurado


| Criterio | Prompt vago | Prompt estructurado |
|----------|-------------|---------------------|
| Menciona el objetivo del sistema | No | Sí |
| Menciona a los usuarios principales | No | Sí |
| Tiene exactamente 3 funcionalidades | No | Sí |
| Esta en 3 parrafos | No | Sí |
| Lo usaria en un informe real | No | Sí |
 
## Ejercicio 5: Anatomia de un prompt

### Desglose de componentes del prompt final

| Componente | Texto de mi prompt |
|------------|--------------------|
| Rol | Actua como desarrollador Java |
| Instrucción | Crea un programa en Java |
| Contexto | para gestionar los productos de una tienda |
| Ejemplo | Usa este estilo para los metodos: getPrecio(), setPrecio(double precio) |
| Formato | Explica primero la estructura de la clase y luego presenta el codigo Java |

### Evolución de las respuestas por nivel

- **Nivel 1 (Básico):** La IA genera un código genérico cualquier estilo ("Hola Mundo" o calculadora) al no tener restricciones.
- **Nivel 2 (+ Rol):** Adopta una postura técnica orientada a mejores prácticas de desarrollo en Java.
- **Nivel 3 (+ Contexto):** Orienta el problema hacia el dominio de una tienda y sus productos.
- **Nivel 4 (+ Instrucción):** Crea exactamente la clase `Producto` con los cuatro campos requeridos (`codigo`, `nombre`, `precio`, `stock`).
- **Nivel 5 (+ Formato y Ejemplo):** Separa la explicación teórica del código y sigue la convención exacta indicada para los métodos getter/setter.
 
## Ejercicio 6: Del prompt basico al profesional

### Evaluación del Prompt Profesional

| Qué revisar | Cumple (Sí / No) |
|-------------|------------------|
| ¿Está escrito en Java y usa Swing? | Sí |
| ¿Pide correo y contraseña? | Sí |
| ¿Explica el funcionamiento antes o después del código? | Sí |
| ¿El código está organizado en clases? | Sí |
| ¿Valida los datos que ingresa el usuario? | Sí |

### Prompt Final e Iteración

```text
Actua como desarrollador Java. Crea un ejemplo de login para una aplicacion de escritorio utilizando Swing. El usuario debe ingresar correo y contrasena. Explica brevemente el funcionamiento y presenta el codigo organizado por clases.

[Mejora enviada en la misma conversación]
Mejora el codigo anterior con estas restricciones: no uses librerias externas, valida que el correo contenga @ y que la contrasena tenga al menos 8 caracteres, y muestra los mensajes con JOptionPane.
