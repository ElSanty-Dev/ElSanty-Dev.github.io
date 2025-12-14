# Reto #1

## Simula el comportamiento de la tortuga usando solo print() e input().

Se recrea el movimiento de la tortuga únicamente con texto, usando funciones, print() y input() para pedir valores al usuario.
Este programa simula el movimiento de una tortuga de forma horizontal usando únicamente texto.
El usuario ingresa la cantidad de pasos y el programa dibuja un rastro continuo con guiones (-) y una flecha (>), representando el avance de la tortuga hacia la derecha.

```python 
def tortuga():
    pasos = int(input("¿Cuántos pasos debe dar la tortuga? "))

    print(f"Creando una tortuga simulada... que da {pasos} pasos.")
    print("-" * pasos + ">")

tortuga()
```
Asi se veria en consola:

<img width="1157" height="71" alt="image" src="https://github.com/user-attachments/assets/0dfa31d1-2b12-4594-ae69-4c354ee301f6" />

# Reto #2

## Tortuga bajando

Crea el rastro de una tortuga moviéndose hacia abajo usando únicamente print() e input().
El usuario debe ingresar la cantidad de pasos que la tortuga baja.

```python
def tortuga_bajando():
    pasos = int(input("¿Cuántos pasos debe bajar la tortuga? "))

    print(f"La tortuga baja {pasos} pasos:")
    for i in range(pasos):
        print("|")

    print("🐢")

tortuga_bajando()
```
Asi se veria en la consola:

<img width="1147" height="268" alt="image" src="https://github.com/user-attachments/assets/86a10e41-533b-4a65-8c53-c27e10214010" />

