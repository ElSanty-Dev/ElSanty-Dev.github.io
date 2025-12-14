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

# Reto #3

## Girar y dibujar usando solo print() e input()

Ahora la tortuga no solo avanza: también gira.

Este programa simula el movimiento de una tortuga que avanza hacia la derecha y luego gira para bajar.
El tramo horizontal se representa con guiones y una flecha (---->), mientras que el tramo vertical se dibuja con |.
El emoji 🐢 indica la posición final de la tortuga, formando visualmente una letra “L”.

```python
def tortuga_en_L():
    pasos = int(input("¿Cuántos pasos debe dar la tortuga? "))

    print(f"Creando una tortuga simulada... que da {pasos} pasos.")

    print("-" * pasos + ">")

    for i in range(pasos - 1):
        print(" " * pasos + "|")

    print(" " * pasos + "🐢")

tortuga_en_L()
```
Asi se veria en la consola:

<img width="1152" height="257" alt="image" src="https://github.com/user-attachments/assets/8a8f96e5-6d6a-40e8-bfe8-300e6ddd1fe2" />

# Reto #4

## Encapsula los comportamientos anteriores usando funciones

Reescribe los retos anteriores creando funciones que representen los movimientos de la tortuga solo con texto.
Usa las siguientes funciones como interfaz:

```
adelante(n)   # Dibuja el movimiento hacia la derecha (→) por n pasos
abajo(n)      # Dibuja el movimiento hacia abajo (↓) por n pasos
```
Por ejemplo, al ejecutar:
```
adelante(5)
abajo(3)
```
Debería producir un patrón en forma de L como en la figura

<img width="161" height="173" alt="image" src="https://github.com/user-attachments/assets/a580e0a7-c107-4e9b-8bae-94057072001d" />

En este reto se encapsulan los movimientos de la tortuga en funciones.
La función adelante(n) simula el avance horizontal y abajo(n) simula el descenso vertical.
El emoji 🐢 representa la posición final de la tortuga, formando visualmente una figura en forma de “L”.

```python
posicion_horizontal = 0

def adelante(n):
    global posicion_horizontal
    print("-" * n + ">")
    posicion_horizontal += n

def abajo(n):
    for i in range(n - 1):
        print(" " * posicion_horizontal + "|")
    print(" " * posicion_horizontal + "🐢")

# Ejecución de ejemplo
adelante(10)
abajo(3)

```
Asi se veria en la consola:

<img width="1151" height="103" alt="image" src="https://github.com/user-attachments/assets/08a00eac-8a94-4ad3-89fa-3f32cf0b7332" />

# Reto #5

## La tortuga baja las escalas

Ajusta tus funciones para que la tortuga pueda bajar escalones.
Cada escalón debe conservar la posición horizontal acumulada y dibujar correctamente tanto el tramo horizontal como el vertical.

Por ejemplo:

```
# Escalón 1
adelante(5)
abajo(2)

# Escalón 2
adelante(5)
abajo(2)

# Escalón 3
adelante(5)
abajo(2)
```
Comportamiento esperado:

<img width="314" height="355" alt="image" src="https://github.com/user-attachments/assets/9f84e7fc-f354-41f6-abc5-ec6c00c96158" />

```python
posicion_horizontal = 0

def adelante(n):
    global posicion_horizontal
    # Dibuja espacios hasta la posición actual y luego el tramo horizontal
    print(" " * posicion_horizontal + "-" * n + ">")
    posicion_horizontal += n

def abajo(n):
    # Dibuja el descenso vertical alineado al final del escalón
    for i in range(n - 1):
        print(" " * posicion_horizontal + "|")
    print(" " * posicion_horizontal + "|")

# Escalón 1
adelante(10)
abajo(3)

# Escalón 2
adelante(10)
abajo(3)

# Escalón 3
adelante(10)
abajo(3)

# Tortuga al final del recorrido
print(" " * posicion_horizontal + "🐢")
```
Este programa simula una escalera descendente utilizando únicamente texto.
Cada llamada a adelante() dibuja un tramo horizontal y actualiza la posición horizontal acumulada.
La función abajo() dibuja el descenso vertical con el símbolo "|"

Asi se veria en la consola:

<img width="1152" height="242" alt="image" src="https://github.com/user-attachments/assets/8d57c520-0651-442f-a516-e8905325d6e5" />

### Referencias de IA
- ChatGPT: https://chatgpt.com/share/693e14fe-4ba4-8003-ab61-e6a5aac7a653

El uso de esta herrameinta fue de gran ayuda para aclarar ideas y maximizar la eficiencia en la elaboracion de esta actividad.
