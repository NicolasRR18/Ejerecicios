# Ejerecicios


![image](https://github.com/user-attachments/assets/23748fa3-0de9-4700-b0a6-c461967a9d46)

```
def mcd_recursivo(a, b):
    """
    Calcula el Máximo Común Divisor de dos números usando recursividad.
    
    Parámetros:
    a (int): Primer número
    b (int): Segundo número
    
    Retorna:
    int: El MCD de a y b
    """
    # Caso base: si b es 0, el MCD es a
    if b == 0:
        return abs(a)  # Usamos abs() para manejar números negativos
    
    # Caso recursivo: MCD(a,b) = MCD(b, a mod b)
    return mcd_recursivo(b, a % b)

def demo_mcd():
    """
    Función para demostrar el uso del cálculo del MCD
    """
    # Ejemplos de uso
    pares_numeros = [
        (48, 18),
        (54, 24),
        (7, 13),
        (-48, 18),
        (0, 8),
        (100, 25)
    ]
    
    for a, b in pares_numeros:
        resultado = mcd_recursivo(a, b)
        print(f"MCD({a}, {b}) = {resultado}")

# Ejecutar la demostración
if __name__ == "__main__":
    demo_mcd()
```


![image](https://github.com/user-attachments/assets/762c111b-981d-478e-b950-1ed702dbd9dc)

```
# Función lambda para calcular f(x) = x/(x^(1/3) - 1)
f = lambda x: x / (x**(1/3) - 1)

# Ejemplos de uso
try:
    # Probamos con algunos valores
    x1 = 27
    x2 = 8
    print(f"f({x1}) = {f(x1):.4f}")
    print(f"f({x2}) = {f(x2):.4f}")
except ZeroDivisionError:
    print("Error: El denominador no puede ser cero")
except ValueError:
    print("Error: Verifica que el valor de x sea válido")

```
