# Tarea: Mi prompt profesional

## Funcionalidad elegida

Sistema de cálculo de promedio ponderado de notas de estudiantes mediante interfaz gráfica en Java Swing.

## Version 1: prompt basico
Hazme un programa en Java para calcular notas.

## Version 2

Actúa como desarrollador Java. Crea una aplicación de escritorio con Java Swing para calcular el promedio de 3 notas de un estudiante. Muestra si aprueba o reprueba.

## Version 3: prompt final

Actúa como un desarrollador Java Senior. Crea una aplicación de escritorio con Java Swing para calcular el promedio ponderado de 3 notas de un estudiante (Examen Parcial 30%, Examen Final 40%, Prácticas 30%). Muestra el estado del estudiante (Aprobado si promedio >= 13, Desaprobado en caso contrario) usando un JOptionPane.
Restricción: No uses librerías externas de terceros.
Usa este estilo de método para el cálculo: public double calcularPromedio(double n1, double n2, double n3).
Explica primero el funcionamiento del código y luego presenta la clase principal en Java.

## Componentes del prompt final

| Componente | Definición / Concepto | Fragmento de mi prompt final |
| :--- | :--- | :--- |
| **Rol** | Asigna una personalidad o nivel de experiencia a la IA | *Actúa como un desarrollador Java Senior.* |
| **Instrucción** | La acción o tarea principal que debe ejecutar la IA | *Crea una aplicación de escritorio con Java Swing para calcular el promedio ponderado de 3 notas y muestra el estado usando JOptionPane.* |
| **Contexto** | Reglas de negocio y datos de fondo | *Examen Parcial 30%, Examen Final 40%, Prácticas 30%. Aprobado si promedio >= 13, Desaprobado en caso contrario.* |
| **Ejemplos** | Patrón de código o método a seguir | *Usa este estilo de método: `public double calcularPromedio(double n1, double n2, double n3)`.* |
| **Formato** | Estructura de presentación de la respuesta | *Explica primero el funcionamiento del código y luego presenta la clase principal en Java.* |
| **Restricción** | Límite explícito para acotar la respuesta | *No uses librerías externas de terceros.* |

## Evaluacion del resultado

| Criterio de Evaluación | Cumple (Sí / No) | Observación / Justificación |
| :--- | :---: | :--- |
| **¿Usa Java Swing sin librerías externas?** | **Sí** | Se utilizaron únicamente los componentes nativos `JFrame`, `JTextField`, `JButton` y `JOptionPane` del JDK. |
| **¿Calcula el promedio ponderado (30%, 30%, 40%)?** | **Sí** | La fórmula aplica exactamente las ponderaciones requeridas para Prácticas (30%), Parcial (30%) y Final (40%). |
| **¿Evalúa la condición (>= 13) e informa con JOptionPane?** | **Sí** | Determina si el alumno está "APROBADO" o "DESAPROBADO" y despliega el resultado en una ventana emergente. |
| **¿Cumple con la firma del método requerida?** | **Sí** | Incluye explícitamente el método `public double calcularPromedio(double n1, double n2, double n3)`. |
| **¿Explica el funcionamiento antes del código Java?** | **Sí** | La respuesta inicia con una explicación técnica de la estructura y componentes antes de presentar el bloque de código. |

## Errores que evite

## Errores que evite

1. **Ser demasiado general / No dar contexto:**
   - **En qué consiste el error:** Enviar instrucciones ambiguas como *"Hazme un programa para calcular notas"*, lo que provoca que la IA asuma un entorno por consola, un promedio aritmético simple sin ponderaciones y un estilo de código genérico.
   - **Cómo lo evité:** Definí claramente el rol de experto (*Desarrollador Java Senior*), el marco de trabajo gráfico (*Java Swing*), la regla de negocio con ponderaciones específicas (30% prácticas, 30% parcial, 40% final) y la condición aprobatoria (promedio >= 13).

2. **No indicar el formato esperado de respuesta:**
   - **En qué consiste el error:** Omitir la estructura en la que se necesita la respuesta, lo que genera explicaciones teóricas dispersas mezcladas con bloques de código fragmentados o incompletos.
   - **Cómo lo evité:** Agregué una instrucción explícita indicando que la IA debía presentar primero una explicación técnica estructurada del sistema y, a continuación, la clase principal completa en Java.