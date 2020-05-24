# Resumen-manejo-de-colecciones
En este repositorio se encuentra un resumen del taller Manejo de colecciones Java 8 de OpenWebinars.

## ¿Qué es una colección de Java?
Una colección en Java es un **contenedor** de elementos de un solo tipo que los reune en una sola unidad. Las colecciones se utilizan para **almacenar**, **recuperar** y **manipular** datos. Uno de los ejemplos más comunes del uso de colecciones es un carrito de compra, donde se almacenarán múltiples objetos.

Las colecciones nos ofrecen estos elementos:
* Interfaces
* Implementaciones
* Algoritmos

## Ventajas de utilizar colecciones
* Disminuye el esfuerzo de programar.
* Aumenta la calidad y velocidad del programa.
* Reduce el esfuerzo para aprender y utilizar otras librerías.
* Permite la interoperabilidad con librerías de terceros.
* Fomenta la reutilización de software.

# Tipos de colecciones en Java

## Iterables 
Un iterador nos permite recorrer y eliminar elementos. También nos permite el uso de forEach para recorrerlo.

```java
public class demoIterables {
  public static void main(String[] args) {
  
    // Declaramos el Iterable que vamos a utilizar
    Iterable<String> pruebaIterable = getIterable();
    
    // Lo recorremos con un bucle del tipo for each
    for (String entrada : prueba) {
    System.out.println(entrada);
    }
    
  }
  
  private static Iterable<String> getIterable() {
    return Arrays.asList("String1", "String2", "String3");
  }
  
}
```

## Collections
* Heredan la funcionalidad de Iterable y la extienden.
* Representan a un grupo de elementos.
* Nos permiten manipular colecciones de forma general.
* Pueden realizar operaciones como .isEmpty o .toArray.

## Set
* Hereda de Collection y no permite duplicados.
* No dispone de acceso posicional.
* Supera la implementación de equals y hashCode.

### Implementaciones de Set
**HashSet**
Almacena valores en una tabla Hash. Nos ofrece mayor velocidad y permite valores nulos.

**LinkedHashSet**
Almacena valores en una tabla Hash manteniendo su orden de inserción. Al igual que HashSet, permite valores nulos.

**TreeSet**
Almacena los valores en orden en un árbol Red-Black. Obtenemos peor rendimiento que con las demás implementaciones debido a su estructura de árbol, además de no permitir valores nulos.

## List
* Hereda de Collection y permite duplicados
* Dispone de acceso posicional

### Implementaciones de List
* **ArrayList**

* **Vector**

* **LinkedList**

* **Queue** Mediante el método FIFO.

* **Deque** Mediante el método FIFO o como pila LIFO.

## Map
* NO hereda de Collection
* Maneja las claves y su valor.
* Cada clave es única y no se puede repetir.
* También es conocido como **diccionario**.

### Operaciones de Map
* put(clave, valor)
* get(clave)
* containsKey(clave)
* containsValue(valor)
* remove (clave)

### Implementaciones de Map
* TreeMap: Tiene el peor rendimiento, pero almacena las claves en orden.
* HashMap: El más común y el más rápido. Se caracteriza por su ejecución constante.
* LinkedHashMap: Rendimiento por debajo de HashMap, a cambio de ordenar las claves y valores según su inserción.

# Colecciones especiales
## Colecciones no modificables
Tras su creación no se pueden modificar, y en caso de intentarlo lanzará una excepción.
## Colecciones sincronizadas
Se utilizan para aprovechar otros hilos de ejecución
