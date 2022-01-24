# NiceTasks

Probando distintos programas para gestionar mis tareas me di cuenta de esto:
taskwarrior es demasiado complejo; todotxt es muy feo; el método de entrada de
todoist es maravilloso, pero por lo demás es basura; las listas de markdown me
gastan pero son difíciles de manejar. `nt` es un simple script para ayudar a
manejar las listas en un archivo de texto plano con formato markdown.

## Inicio rápido

El comando `nt`, sin argumentos, mostrara la lista de tareas no completadas
ordenadas según su fecha limite.

Para agregar una tarea se utiliza `nt a`. A continuación se introduce la tarea
y después la fecha con lenguaje natural.

```sh
$ nt a
>> Make my homework
>> Weekend
```

```sh
$ nt a
>> Go to the party 
>> Next Friday
```

Para completar una tarea utilice `nt x`, a continuación la seleccionara con fzf.

Puede usar markdown al introducir la tarea. Es útil utilizar links para enlazar
la tarea a alguna otra nota. Puesto que NiceTasks solo detecta como tareas las
listas que comiencen con `- [ ]`, puede usar `+ [ ]` para tareas que no quiera
que sean analizadas. Útil para tareas a largo plazo que no tenga fecha definida
pero quiera recordar. Puede jugar con los distintos `-+*` para lograr un 
_bullete journal_.

Un archivo de tareas debería terminar teniendo la siguiente apariencia.

```markdown
# Tareas ✅

## Universidad 🪐
- [ ] (22-01-22) conjunto de problemas 5 de [[clase de álgebra]]
- [ ] (22-01-28) reunión con tutor 

## Personal 👤
- [ ] (22-02-02) organizar mis notas archivadas
+ [ ] buscar un nuevo escritorio

## Social 🥂
- [ ] (22-01-17) ir a cenar con [[Daniel Saldaña]] al centro

## Entrada 📥
- [ ] (22-01-22) leer capitulo XII de [[LLPSI]]
- [ ] (22-01-22) ejercicios de [[clase de álgebra]]

```

## Referencia

| Comando | Descripción                                        |
|---------|----------------------------------------------------|
| `nt`    | Muestra las tareas pendientes ordenadas            |
| `nt d`  | Muestra las tareas pendientes del día de hoy       |
| `nt n`  | Muestra la tarea pendiente más próxima             |
| `nt a`  | Pide al usuario introducir una tarea nueva         |
| `nt x`  | Marca como "completada" la tarea seleccionada      |
| `nt f`  | Muestra las tareas completadas                     |
| `nt c`  | Limpia las tareas completadas del archivo de texto |
| `nt e`  | Abre el archivo de tareas con el editor Vim        |

## Por hacer

Esta lista no esta en orden, y, en realidad, tampoco es que haya planes para
completarla en su totalidad.

- [ ] Algo de color
- [ ] Hora y minuto limite
- [ ] Manejo de tareas vencidas
- [ ] Tareas organizadas por proyectos
- [ ] Archivo de configuración
- [ ] Recordatorios
- [ ] Eventos (uso de calendario)
- [ ] Tareas, recordatorios y eventos recurrentes
- [ ] Entrada natural en español

