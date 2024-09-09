# Reto-12

Desarrollo ejercicios reto 12:

**1. Consulte que hacen los siguientes métodos de strings en python: endswith, startswith, isalpha, isalnum, isdigit, isspace, istitle, islower, isupper.**

*Desarrollo:*

- `endswith(suffix)`:

Verifica si la cadena termina con el sufijo especificado. Devuelve True si es así, de lo contrario False.
Ejemplo: `"python".endswith("on")` → True

- `startswith(prefix)`:

Verifica si la cadena comienza con el prefijo especificado. Devuelve True si es así, de lo contrario False.
Ejemplo: `"python".startswith("py")` → True

- `isalpha()`:

Devuelve True si todos los caracteres en la cadena son letras (alfabéticos) y no hay espacios ni otros caracteres. Si la cadena está vacía, devuelve False.
Ejemplo: `"abc".isalpha()` → True

- `isalnum()`:

Devuelve True si todos los caracteres en la cadena son letras o números. No debe haber espacios ni caracteres especiales.
Ejemplo: `"abc123".isalnum()` → True

- `isdigit()`:

Devuelve True si todos los caracteres en la cadena son dígitos. Si hay cualquier otro carácter (incluyendo espacios), devuelve False.
Ejemplo: `"1234".isdigit()` → True

- `isspace()`:

Devuelve True si la cadena contiene solo espacios en blanco (tabulaciones, saltos de línea, etc.), y al menos un carácter. Si está vacía o contiene algo más, devuelve False.
Ejemplo: `" ".isspace()` → True

- `istitle()`:

Devuelve True si la cadena sigue el formato de "título", es decir, si cada palabra comienza con una letra mayúscula seguida de letras minúsculas.
Ejemplo: `"Hello World".istitle()` → True

- `islower()`:

Devuelve True si todos los caracteres alfabéticos de la cadena son minúsculas y hay al menos una letra. Si no hay letras o alguna es mayúscula, devuelve False.
Ejemplo: `"hello".islower()` → True

- `isupper()`:

Devuelve True si todos los caracteres alfabéticos de la cadena son mayúsculas y hay al menos una letra. Si no hay letras o alguna es minúscula, devuelve False.
Ejemplo: `"HELLO".isupper()` → True

**2. Procesar el  <a href="https://www.py4e.com/code3/mbox.txt">archivo</a> y extraer:**

- Cantidad de vocales
- Cantidad de consonantes
- Listado de las 50 palabras que más se repiten

*Desarrollo:*
Para poder relizar el punto principalmente se creó un code que cumple con la función de extraer lo que se pide del archivo, a continuación este:

```python
import string
from collections import Counter

# Función para contar vocales y consonantes
def contar_vocales_consonantes(texto):
    vocales = "aeiouAEIOU"
    num_vocales = 0
    num_consonantes = 0
    for letra in texto:
        if letra.isalpha():
            if letra in vocales:
                num_vocales += 1
            else:
                num_consonantes += 1
    return num_vocales, num_consonantes

# Función para extraer las 50 palabras más comunes
def palabras_mas_comunes(texto, num_palabras=50):
    # Eliminar signos de puntuación
    texto = texto.translate(str.maketrans('', '', string.punctuation))
    # Convertir el texto en una lista de palabras
    palabras = texto.lower().split()
    # Contar la frecuencia de cada palabra
    contador_palabras = Counter(palabras)
    # Obtener las palabras más comunes
    palabras_comunes = contador_palabras.most_common(num_palabras)
    return palabras_comunes

# Leer el archivo de texto
with open('archivo.txt', 'r', encoding='utf-8') as archivo:
    contenido = archivo.read()

# Contar vocales y consonantes
vocales, consonantes = contar_vocales_consonantes(contenido)

# Obtener las 50 palabras más comunes
palabras_comunes = palabras_mas_comunes(contenido)

# Mostrar los resultados
print(f"Cantidad de vocales: {vocales}")
print(f"Cantidad de consonantes: {consonantes}")
print("Las 50 palabras más comunes son:")
for palabra, frecuencia in palabras_comunes:
    print(f"{palabra}: {frecuencia}")
```
En el momento en que se ejecuta y carga el archivo se obtiene que:


