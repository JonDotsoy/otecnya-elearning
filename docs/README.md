# Otecnya E-Learning

### Tabla Comparativa

|          Caso         |   Kampus Project  | Otecnya |
|-----------------------|-------------------|---------|
| Experiencia Mobile    | No                |         |
| SSL (Sitio Seguro)    | No                |         |
| Requiere Flash        | Si                |         |
| Responsiva            | Si (Parcialmente) |         |
| Offline               | No                |         |
| Porcentaje lighthouse | 48,75%            |         |

### Casos de uso Kampus Project

[![](https://www.planttext.com/plantuml/svg/fLLBRjim4Dtp5DmrMIG7C08XXY4q1PAWIDBkMN7iJY6I0Zz6sZjrrIFaOXsAYaLPL1qq2yF0lFTc7cU6rBNpmlgWMlQ1RupUuiwn5hQUUyCjxhvxBj52uz5enbPhgL2ZyrP8OrVywkgB2yAYgIek71TI4QKDIfiv5iDizJbeIlmOEY1adg7pBdICdTrYj9L4nftpoykAdtq5oskAovVVpcD3T0by_Kg9kL0tRP1GLOoiy8iB4Xrb6e6FG4bU_kYOfBFc9vsnnoCnCMAz9bXN26-DDRFWax0WvjmRi5Oe1EqBOBsdW6Yekp07DwB5BHtq0BzwFmdUWNRYHo7b2FIjVeEYtfDpSrnWY5BFnvLeOZkhwfpcTugI1hhUMTZHS7I0lU7GyzCWuTc3beu6-SPKjSGuvd8EDZrXKjp293PT7vOFF_4tD5pBxuqNHOiJRWn4fYjI1wHdVbATHOMqF4RIGhVqMnREQj259GBAXHFtMvgxVm9LTfyn-qrUuYKWzIzTh0TmNQ2h9EYAPRgybSlCP0qdwApk2NdTKl_qkpB8zpb8lLsKi_nn62hgFOeXLkvppiv7NqezUM16IHO-dicIxD3B_z0-XczO41wRdJnuIVa0z9Jz4YD65tikBhCEfuqVbY7AwsUXG1UD5yh_IpqQkAP_-ah-1G00)](https://www.planttext.com/plantuml/svg/fLLBRjim4Dtp5DmrMIG7C08XXY4q1PAWIDBkMN7iJY6I0Zz6sZjrrIFaOXsAYaLPL1qq2yF0lFTc7cU6rBNpmlgWMlQ1RupUuiwn5hQUUyCjxhvxBj52uz5enbPhgL2ZyrP8OrVywkgB2yAYgIek71TI4QKDIfiv5iDizJbeIlmOEY1adg7pBdICdTrYj9L4nftpoykAdtq5oskAovVVpcD3T0by_Kg9kL0tRP1GLOoiy8iB4Xrb6e6FG4bU_kYOfBFc9vsnnoCnCMAz9bXN26-DDRFWax0WvjmRi5Oe1EqBOBsdW6Yekp07DwB5BHtq0BzwFmdUWNRYHo7b2FIjVeEYtfDpSrnWY5BFnvLeOZkhwfpcTugI1hhUMTZHS7I0lU7GyzCWuTc3beu6-SPKjSGuvd8EDZrXKjp293PT7vOFF_4tD5pBxuqNHOiJRWn4fYjI1wHdVbATHOMqF4RIGhVqMnREQj259GBAXHFtMvgxVm9LTfyn-qrUuYKWzIzTh0TmNQ2h9EYAPRgybSlCP0qdwApk2NdTKl_qkpB8zpb8lLsKi_nn62hgFOeXLkvppiv7NqezUM16IHO-dicIxD3B_z0-XczO41wRdJnuIVa0z9Jz4YD65tikBhCEfuqVbY7AwsUXG1UD5yh_IpqQkAP_-ah-1G00)

```plantuml
@startuml
' Configs
left to right direction

:Administrador: <<Usuario>> as adm
:Alumno: <<Usuario>> as alumn
:Punto Superior: <<Usuario>> as ptsup

(Listar alumnos) ..> (Ver Estadísticas de Alumnos) : <<include>>
adm --> (Listar alumnos)
adm --> (Gestión de proyectos)
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




