# Manual rápido de referencia para actualizar el código en lenguaje Python con la propuesta de optimización en la asignación de horarios.

Universidad Abierta y a Distancia de México

División de Ciencias Exactas, Ingeniería y Tecnología

Licenciatura en Matemáticas

Proyecto: Aplicación de técnicas de investigación de operaciones para optimizar la asignación de horarios de trabajo en el ámbito educativo: un enfoque específico en Escuelas Secundarias de Aguascalientes

Estudiante:  Héctor Humberto Rodríguez Silva

Matrícula:   ES1821013343

Asesor Interno:  Dra. María del Alba Pacheco Blas

Sinodales:       Mtra. Laura Granados González, Mtro. Orlando Fabián Echeverría Alonso y Mtro. Manuel López Mateos

Asesor Externo:  Mtro. Humberto Rodríguez Gómez

Aguascalientes, Ags. a 22 de noviembre de 2024

______________________________________________

1. Si se desean agregar, eliminar o actualizar las listas de grupos, días, clases, disciplinas y profesores, se debe de realizar lo propio en las siguientes líenas del código:
   
grupos = ["1A", "1B", "1C", "1D", "1E", "1F", "2A", "2B", "2C", "2D", "2E", "2F", "3A", "3B", "3C", "3D", "3E", "3F"]

dias = ["Lunes", "Martes", "Miércoles", "Jueves", "Viernes"]

clases = ["Clase de 7 a 8 am", "Clase de 8 a 9 am", "Clase de 9 a 10 am", "Clase de 10 a 11 am",
          "Clase de 11 am a 12 pm", "Clase de 12 pm a 1 pm", "Clase de 1 a 2 pm"]

disciplinas = [
    "Artes", "Ciencias", "Educación Física", "Español", "Formación Cívica y Ética", "Geografía",
    "Historia", "Inglés", "Integración Curricular", "Laboratorio", "Matemáticas", "Tecnología", "Tutoría",
]

profesores = [
    "Juan Carlos Marín Esquivel", "Manuela Ramírez Medina", "Olga Herrera Mireles", ..."
]

2. Si se desean agregar, eliminar o actualizar las asignaciones de profesores asignados a ciertas disciplinas, se debe editar lo siguiente:
   
asignaciones_profesor_disciplina = {
    "Juan Carlos Marín Esquivel": ["Español"],
    "Manuela Ramírez Medina": ["Español"],
    "Olga Herrera Mireles": ["Español"],...
}

3. Si se desean agregar, eliminar o actualizar los pesos para cada disciplina, se debe editar lo siguiente:

pesos_disciplinas = {
    "Matemáticas": 10,             # Peso muy alto
    "Laboratorio": 9,              # Peso muy alto
    "Ciencias": 8,                 # Peso alto
    ...
}

4. Si se desean agregar, eliminar o actualizar los pesos para cada profesor, con base en el número de clases que imparten, se debe editar lo siguiente:

pesos_profesores = {
    "Juan Carlos Marín Esquivel": 35,                 # Peso muy alto
    "Francisco Javier Gallardo Delgado": 35,          # Peso muy alto
    "Ma. Guadalupe Rendón Álvarez": 34,               # Peso muy alto
    ...
}

5. Finalmente, si se desean agregar más restricciones al modelo, se deberán de incluir antes de la instrucción:
prob.solve()
