

# Facil
## Algoritmo de búsqueda por fuerza bruta con error

El siguiente algoritmo implementa una búsqueda por fuerza bruta para encontrar un elemento en un array ordenado. Sin embargo, contiene un error intencional que solo puede detectarse mediante la depuración.

Java

```
public class BusquedaPorFuerzaBrutaConError {

    public static boolean buscar(int[] arr, int objetivo) {
        for (int i = 0; i < arr.length; i++) {
            if (arr[i] == objetivo) {
                return true;
            }
        }
        return false;
    }

    public static void main(String[] args) {
        int[] arreglo = {1, 3, 5, 7, 9, 11, 13, 15, 17, 19};
        int objetivo = 11;

        boolean encontrado = buscar(arreglo, objetivo);

        if (encontrado) {
            System.out.println("El elemento " + objetivo + " se encuentra en el array");
        } else {
            System.out.println("El elemento " + objetivo + " no se encuentra en el array");
        }
    }
}
```

**1. Configurar el entorno de desarrollo:**

-   Importar el proyecto Java que contiene el código de la búsqueda por fuerza bruta en el IDE elegido.
-   Establecer un punto de interrupción en la línea de la condición de comparación:  `if (arr[i] == objetivo)`.

**2. Ejecutar el algoritmo:**

-   Ejecutar la búsqueda por fuerza bruta con un array de cadenas y un objetivo de tipo `String`.
-   El IDE se detendrá en el punto de interrupción.

**3. Observar el comportamiento del algoritmo:**

-   Examinar los valores de las variables `arr[i]` y `objetivo` en este punto de interrupción.
-   Observar que la comparación `arr[i] == objetivo` falla, aunque el elemento objetivo está presente en el array.

**4. Identificar el error:**

-   La comparación `arr[i] == objetivo` no es adecuada para comparar cadenas de texto, ya que compara las referencias de memoria en lugar del contenido textual.

**5. Corregir el error:**

-   Modificar la condición de comparación para utilizar el método `equals()` de la clase `String`:  `if (arr[i].equals(objetivo))`.

**6. Verificar la corrección:**

-   Continuar la ejecución del algoritmo paso a paso, observando que ahora la búsqueda funciona correctamente para el array de cadenas y el objetivo de tipo `String`.

**7. Probar con otros casos:**

-   Ejecutar la búsqueda con diferentes arrays de cadenas y objetivos para verificar su funcionamiento general.

# Medio

## Algoritmo de ordenamiento de palabras con error

El siguiente algoritmo implementa una función para ordenar una lista de palabras en orden alfabético. Sin embargo, contiene un error intencional que solo puede detectarse mediante la depuración.

Java

```
public class OrdenamientoDePalabrasConError {

    public static void ordenarPalabras(String[] palabras) {
        for (int i = 0; i < palabras.length; i++) {
            for (int j = 0; j < palabras.length - i - 1; j++) {
                if (palabras[j].compareTo(palabras[j + 1]) > 0) {
                    String temp = palabras[j];
                    palabras[j] = palabras[j + 1];
                    palabras[j + 1] = temp;
                }
            }
        }
    }

    public static void main(String[] args) {
        String[] palabras = {"hola", "mundo", "como", "estas"};

        ordenarPalabras(palabras);

        for (String palabra : palabras) {
            System.out.print(palabra + " ");
        }
    }
}
```

### introducción

 El objetivo es guiar al lector a través del proceso de identificación y corrección del error para comprender mejor la importancia de la depuración en el desarrollo de software.

### Requisitos previos

Para seguir este instructivo, se requiere lo siguiente:

-   Conocimientos básicos de programación en Java
-   Un entorno de desarrollo integrado (IDE) para Java, como IntelliJ IDEA o Eclipse
-   El código fuente del algoritmo de ordenamiento de palabras con el error introducido (proporcionado anteriormente)

### Pasos

**1. Configurar el entorno de desarrollo:**

-   Importar el proyecto Java que contiene el código del algoritmo de ordenamiento de palabras en el IDE elegido.
-   Establecer puntos de interrupción en las siguientes líneas del código:
    -   La línea que contiene la condición de comparación `if (palabras[j].compareTo(palabras[j + 1]) > 0)`.
    -   La línea que realiza el intercambio de palabras `String temp = palabras[j]; palabras[j] = palabras[j + 1]; palabras[j + 1] = temp;`.

**2. Ejecutar el algoritmo:**

-   Ejecutar el algoritmo de ordenamiento de palabras utilizando el IDE.
-   El IDE se detendrá en el primer punto de interrupción.

**3. Observar el comportamiento del algoritmo:**

-   Examinar los valores de las variables `palabras[j]`,  `palabras[j + 1]`, y `temp` en este punto de interrupción.
-   Analizar si la condición de comparación `palabras[j].compareTo(palabras[j + 1]) > 0` es correcta en este caso.
-   Si la condición de comparación es incorrecta, identificar el error y la corrección necesaria.

**4. Corregir el error:**

-   Modificar la condición de comparación para incluir también el caso de palabras iguales, utilizando `>=` en lugar de `>`.
-   Continuar la ejecución del algoritmo paso a paso, observando el comportamiento y verificando la corrección del error.

**5. Verificar el ordenamiento final:**

-   Ejecutar el algoritmo completo sin puntos de interrupción.
-   Examinar el ordenamiento final de las palabras para asegurarse de que sea correcto y alfabético.

