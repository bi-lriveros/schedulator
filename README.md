# ☕️ Schedule Generator

> ℹ️ api generadora de tareas (schedule)

## ☝️ Dependencias

* Java 11
* Gradle (Wrapper incluido)

## 🏁 Instalación y ejecución

```bash
 ./gradlew bootRun
```

## El problema

En el repositorio actual se encontrará un microservicio que generará un listado de tareas de forma aleatoria
con el siguiente formato

```
GET http://localhost:8080/generator/schedule/tasks
```

```json
[
    {
    "task_id": "65b902ef-bd60-4a1c-aebb-21f929d57474",
    "task_name": "Task 0",
    "duration": 8
    },
    {
    "task_id": "35951c98-a9c9-45f6-990b-4e746957f156",
    "task_name": "Task 1",
    "duration": 3
    },
    {
    "task_id": "328f5534-aed7-44cd-a75a-d6f367fef51e",
    "task_name": "Task 2",
    "duration": 3
    }
]
```

El objetivo es generar un api rest que organice las tareas de tal manera que retorne la minima cantidad de días en ser
resueltas considerando jornadas de trabajo de 8 horas.

Ejemplo respuesta basándose en el enunciado:

```json
{
  "hrs_jornada": 8,
  "dias_termino": 2,
  "jornadas": [
    {
      "id": 1,
      "tareas": [
        "65b902ef-bd60-4a1c-aebb-21f929d57474"
      ]
    },
    {
      "id": 2,
      "tareas": [
        "35951c98-a9c9-45f6-990b-4e746957f156",
        "328f5534-aed7-44cd-a75a-d6f367fef51e"
      ]
    }
  ]
}
```

## ☝️ Puntos a evaluar

* Solución al problema indicado
* Código limpio y ordenado
* Estructura del proyecto
* Estrategia de commits
* Documentación
* Utilización de logs de trazabilidad
* Test

## ⭐️ Desafio técnico

A continuación se encuentran las
[Instrucciones de desafío técnico](CONTRIBUTING.md)

