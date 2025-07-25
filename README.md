Simulación de Asignación de Asientos — Pilas y Colas en C#

Este proyecto implementa una solución en C# para simular el ingreso ordenado de personas a una atracción con cupo limitado, utilizando la estructura de datos tipo cola (FIFO) y el paradigma de Programación Orientada a Objetos.

Objetivo académico

Aplicar los conceptos de estructuras dinámicas (pilas y colas) en un entorno práctico, consolidando habilidades de modelado, lógica secuencial, reportería técnica y documentación del proceso. El sistema garantiza que las primeras 30 personas en ingresar sean asignadas a un asiento.

<img width="419" height="561" alt="image" src="https://github.com/user-attachments/assets/a2c542b4-f113-498d-a502-4991e3f315c4" />




---

Estructura del proyecto


- `Persona.cs`: define la clase base con nombre e ID
- `Atraccion.cs`: gestiona la cola, asignación de asientos y reportería
- `Program.cs`: ejecuta la simulación principal
- `/evidencias/`: contiene las capturas de pantalla del sistema en ejecución


---

Funcionamiento del sistema

- Se simula el ingreso de 35 visitantes con nombres generados automáticamente (`Visitante1` a `Visitante35`)
- El sistema admite hasta 30 personas en cola
- Las personas restantes reciben mensaje de rechazo por falta de cupo
- Se asignan asientos en orden de llegada (FIFO)
- Se imprime un resumen en consola mostrando quién está en espera y quién ya tiene asiento

<img width="403" height="533" alt="image" src="https://github.com/user-attachments/assets/5abc611b-d76c-4cd7-ab79-4a07090e87d8" />



---

Cómo ejecutar el programa

Requisitos:
- Visual Studio o Visual Studio Code
- SDK de .NET (versión 6 o superior)

Pasos:
1. Clonar el repositorio o descargar los archivos
2. Abrir el proyecto en Visual Studio
3. Ejecutar `Program.cs` con `Ctrl + F5` o desde el menú "Iniciar"
4. Observar la salida en la consola

---

Agente de Inteligencia Artificial utilizado

- Nombre del agente: Microsoft Copilot
- Colaboración estimada: 50%
- Funciones asistidas:  
  - Estructura lógica del código  
  - Redacción técnica del informe  
  - Generación de comentarios y estructura de clases  
  - Organización del repositorio y README
- Reflexión ética: El agente fue utilizado como acompañante formativo, sin reemplazar el criterio profesional ni el razonamiento técnico de la estudiante. Se priorizó el aprendizaje genuino por encima del cumplimiento operativo.

---

Evidencias

- Las capturas de pantalla se encuentran directamente en README.md
  - Ingreso exitoso de visitantes a la cola
  - Asignación ordenada de asientos
  - Estado final del sistema
- El código fuente está documentado y comentado en los archivos `.cs`
- El enlace de este repositorio puede ser incluido en el informe final institucional como evidencia técnica

---

Autora

Sandra Rodriguez Rodriguez  
Estudiante comprometida con la aplicación práctica de estructuras dinámicas en programación, orientada a la documentación rigurosa, el aprendizaje ético y la mejora continua.

---



<img width="308" height="586" alt="image" src="https://github.com/user-attachments/assets/3a32a4fd-9371-431f-b9ac-58428195206d" />


