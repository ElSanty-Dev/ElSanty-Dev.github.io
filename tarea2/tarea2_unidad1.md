Reto #1

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
