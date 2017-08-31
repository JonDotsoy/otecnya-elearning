# Otecnya E-Learning

Casos de uso e-learning.

### Tabla Comparativa

|      Caso      | Kampus Project | Otecnya |
|----------------|----------------|---------|
| SSL            | No             |         |
| Requiere Flash | Si             |         |
|                |                |         |
|                |                |         |

### Casos de uso

```plantuml
@startuml
' Configs
left to right direction

:Administrador: <<Usuario>> as adm
:Alumno: <<Usuario>> as alumn
:Punto Superior: <<Usuario>> as ptsup

(Listar alumnos) ..> (Ver Estadísticas de Alumnos) : <<include>>
adm --> (Listar alumnos)
alumn --> (Ver cursos)
alumn --> (Ver foro)
alumn --> (Ver Tareas)
alumn --> (Ver Herramientas)
alumn --> (Ver Evaluaciones)
alumn --> (Ver Calificaciones)
adm --> (Ver Calificaciones)
adm --> (Ver Mensajes)
alumn --> (Ver Mensajes)
ptsup --> (Ver Mensajes)
alumn --> (Ver Eventos)
adm --> (Ver Eventos <<Administración>>)

(Ver Eventos <<Administración>>) ..> (Agregar nuevo evento) : <<extends>>
(Ver Eventos <<Administración>>) ..> (Editar evento) : <<extends>>

(Ver Mensajes) ..> (Leer Mensajes) : <<include>>

(Ver cursos) ..> (Crear Nota) : <<extends>>
(Ver cursos) ..> (Ver Notas) : <<extends>>
(Ver Notas) ..> (Imprimir Todas las Notas) : <<extends>>
(Ver cursos) ..> (Ver Contenido) : <<extends>>

(Ver foro) ..> (Crear Tema) : <<extends>>
(Ver foro) ..> (Ver Tema) : <<extends>>
(Ver Tema) ..> (Listar Respuesta al Tema) : <<include>>

(Listar Respuesta al Tema) ..> (Citar Respuesta) : <<extends>>
(Listar Respuesta al Tema) ..> (Eliminar Respuesta) : <<extends>>
(Listar Respuesta al Tema) ..> (Editar Respuesta) : <<extends>>
(Listar Respuesta al Tema) ..> (Crear Respuesta) : <<extends>>

(Ver Tareas) ..> (Enviar Tarea) : <<extends>>
(Ver Tareas) ..> (Ver cursos) : <<extends>>

(Ver Herramientas) ..> (Ver Herramienta) : <<include>>
(Ver Herramientas) ..> (Eliminar Herramienta) : <<include>>
(Ver Herramientas) ..> (Subir Herramienta) : <<extends>>

(Ver Evaluaciones) ..> (Realizar Evaluación) : <<extends>>

(Realizar Evaluación) ..> (Ver Puntuación Examen) : <<include>>
(Ver Evaluaciones) ..> (Ver Puntuación Examen) : <<extends>>
@enduml
```




