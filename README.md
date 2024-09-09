# Reto-12

Desarrollo ejercicios reto 12:

**1. Consulte que hacen los siguientes métodos de strings en python: endswith, startswith, isalpha, isalnum, isdigit, isspace, istitle, islower, isupper.**

- endswith(suffix):

Verifica si la cadena termina con el sufijo especificado. Devuelve True si es así, de lo contrario False.
Ejemplo: "python".endswith("on") → True

- startswith(prefix):

Verifica si la cadena comienza con el prefijo especificado. Devuelve True si es así, de lo contrario False.
Ejemplo: "python".startswith("py") → True

- isalpha():

Devuelve True si todos los caracteres en la cadena son letras (alfabéticos) y no hay espacios ni otros caracteres. Si la cadena está vacía, devuelve False.
Ejemplo: "abc".isalpha() → True
isalnum():

Devuelve True si todos los caracteres en la cadena son letras o números. No debe haber espacios ni caracteres especiales.
Ejemplo: "abc123".isalnum() → True

- isdigit():

Devuelve True si todos los caracteres en la cadena son dígitos. Si hay cualquier otro carácter (incluyendo espacios), devuelve False.
Ejemplo: "1234".isdigit() → True

- isspace():

Devuelve True si la cadena contiene solo espacios en blanco (tabulaciones, saltos de línea, etc.), y al menos un carácter. Si está vacía o contiene algo más, devuelve False.
Ejemplo: " ".isspace() → True

- istitle():

Devuelve True si la cadena sigue el formato de "título", es decir, si cada palabra comienza con una letra mayúscula seguida de letras minúsculas.
Ejemplo: "Hello World".istitle() → True

- islower():

Devuelve True si todos los caracteres alfabéticos de la cadena son minúsculas y hay al menos una letra. Si no hay letras o alguna es mayúscula, devuelve False.
Ejemplo: "hello".islower() → True

- isupper():

Devuelve True si todos los caracteres alfabéticos de la cadena son mayúsculas y hay al menos una letra. Si no hay letras o alguna es minúscula, devuelve False.
Ejemplo: "HELLO".isupper() → True
