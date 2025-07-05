# lista-tareas-python
Este proyecto es un script básico de línea de comandos en Python para gestionar una lista de tareas sencilla. Permite añadir, ver y eliminar tareas de forma interactiva.

## Funcionalidades
Añadir nuevas tareas a la lista.

Mostrar todas las tareas guardadas con su número.

Eliminar tareas específicas por número.

Salir del programa.

## Cómo usar
Ejecuta el script en tu consola o terminal:

python tareas.py
Selecciona una opción del menú escribiendo el número correspondiente:

1 para añadir una tarea.

2 para ver la lista de tareas.

3 para eliminar una tarea.

4 para salir del programa.

Sigue las instrucciones en pantalla para gestionar tus tareas.

## Requisitos
Python 3.x

## Código de ejemplo
```bash
tareas = []
while True:
    print("\n1. Añadir tarea")
    print("2. Ver tareas")
    print("3. Eliminar tarea")
    print("4. Salir")
    opcion = input("Selecciona opción: ")
    if opcion == "1":
        nueva_tarea = input("Introduce la nueva tarea: ")
        tareas.append(nueva_tarea)
    elif opcion == "2":
        for i, tarea in enumerate(tareas):
            print(f"{i+1}. {tarea}")
    elif opcion == "3":
        tarea_a_eliminar = int(input("Número de tarea a eliminar: ")) - 1
        if 0 <= tarea_a_eliminar < len(tareas):
            tareas.pop(tarea_a_eliminar)
        else:
            print("Tarea no válida.")
    elif opcion == "4":
        break
    else:
        print("Opción incorrecta.")
