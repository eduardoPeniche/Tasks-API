# API Tareas

## Instrucciones

##### Habilitar entorno virtual para terminal
Windows:
`.\venv\Scripts\activate`

_*Si la terminal no permite ejecutar script:_
```
Set-ExecutionPolicy RemoteSigned -Scope Process
.\venv\Scripts\activate
```

Mac:
`source venv/bin/activate`

##### Instalar librerias necesarias
`pip install -r requirements.txt`

##### Iniciar servidor
entrar a carpeta core `cd core`

`python manage.py runserver`

Usar VSCode Thunder Client Extension o Navegador a "http://localhost:8000/api/tasks"

### Visualizar todas las tareas en la Base de datos
GET a http://localhost:8000/api/tasks
```json
{
  "id": 1,
  "title": "Programar",
  "description": "Java",
  "is_complete": false,
  "created_at": "2023-12-21T01:45:51.691174Z"
}
```

### Crear tarea en la Base de datos
POST a http://localhost:8000/api/tasks
```json
{
  "title": "Nombre de Tarea",
  "description": "Descripción de Tarea"
}
```

### Visualizar tarea especifica en la Base de datos
GET a http://localhost:8000/api/tasks/{task_id}

*Reemplazar {task_id} con el id de la tarea principal

### Actualizar tarea especifica en la Base de datos
PUT a http://localhost:8000/api/tasks/{task_id}

*Reemplazar {task_id} con el id de la tarea principal
```json
{
  "title": "Actualizar",
  "description": "Actualizar",
  "is_complete": true,
}
```

### Eliminar tarea especifica en la Base de datos
DELETE a http://localhost:8000/api/tasks/{task_id}

*Reemplazar {task_id} con el id de la tarea principal

### Visualizar todas las subtareas de tarea princial en la Base de datos
GET a http://localhost:8000/api/tasks/{task_id}/subtask

*Reemplazar {task_id} con el id de la tarea principal

### Crear subtarea para tarea princial en la Base de datos
POST a http://localhost:8000/api/tasks/{task_id}/subtask

*Reemplazar {task_id} con el id de la tarea principal
```json
{
  "title": "Nombre de Subtarea"
}
```

### Visualizar subtarea especifica de tarea princial en la Base de datos
GET a http://localhost:8000/api/tasks/{task_id}/subtask/{subtask_id}

*Reemplazar {task_id} con el id de la tarea principal

*Reemplazar {subtask_id} con el id de la sub tarea perteneciente a la tarea principal

### Actualizar subtarea especifica en la Base de datos
PUT a http://localhost:8000/api/tasks/{task_id}/subtask/{subtask_id}

*Reemplazar {task_id} con el id de la tarea principal

*Reemplazar {subtask_id} con el id de la sub tarea perteneciente a la tarea principal
```json
{
  "is_complete": true
}
```

### Eliminar subtarea especifica en la Base de datos
DELETE a http://localhost:8000/api/tasks/{task_id}/subtask/{subtask_id}

*Reemplazar {task_id} con el id de la tarea principal

*Reemplazar {subtask_id} con el id de la sub tarea perteneciente a la tarea principal