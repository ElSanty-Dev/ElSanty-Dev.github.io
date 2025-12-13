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
