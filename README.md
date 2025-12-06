# Implementación de Tabla Hash (HashMap desde Cero)
Estructura de Datos — Semestre 2025  
Autor: Aby Piña Bernal  

Este proyecto implementa una estructura de datos tipo HashMap creada desde cero, utilizando encadenamiento separado para manejar colisiones y rehashing dinámico cuando el factor de carga alcanza el valor máximo establecido (0.75).  
Se emplea un arreglo de listas enlazadas (LinkedList) como estructura base, junto con tipos genéricos <K, V>.

--------------------------------------------------------------------

## Estructura del Proyecto (NetBeans)
```
HashMap/
├── nbproject/ # Archivos de configuración del proyecto NetBeans
│ ├── private/
│ │ └── private.properties
│ ├── build-impl.xml
│ ├── genfiles.properties
│ ├── project.properties
│ └── project.xml
├── src/
│ └── hashmap/ # Código fuente de Java
│ ├── Diccionario.java # Clase para manejar diccionarios
│ ├── TablaHash.java # Implementación de la tabla hash
│ └── TestTablaHash.java # Clase de prueba de la tabla hash
├── build.xml # Archivo de construcción Ant
├── manifest.mf # Manifest del proyecto
├── .gitignore
└── README.md
```
Todas las clases pertenecen al paquete:
```
package hashmap;
```
--------------------------------------------------------------------
Descripción de las Clases

## Diccionario.java
Interfaz que define las operaciones básicas del mapa:
-put(K key, V value)
-get(K key)
-remove(K key)
-containsKey(K key)
-size()


## TablaHash.java
Implementación completa de una tabla hash con las siguientes características:
-Manejo de colisiones mediante listas enlazadas
-Redimensionamiento automático de la tabla (rehashing)
-Factor de carga máximo de 0.75
-Clase interna Nodo que almacena clave y valor
-Método hash seguro que convierte hashCode en un índice válido
-Operaciones en tiempo promedio O(1)
-Documentación Javadoc incluida en los métodos principales

Métodos implementados:
-hash
-put
-get
-remove
-containsKey
-size
-resize

## TestTablaHash.java
Clase utilizada para comprobar el funcionamiento de la tabla hash.
Incluye pruebas de inserción, actualización de valores, eliminación, búsqueda y comprobación de claves.

---------------------------------------------------------------------
## Salida Real del Programa
```
Insertando valores...
manzana = 5
pera = 3

Actualizando 'manzana'...
manzana = 99

Removiendo 'pera'...
Valor eliminado: 3

Size actual: 2

Probando containsKey...
Existe 'uva'? true
Existe 'pera'? false
```
---------------------------------------------------------------------
## Ejecución en NetBeans
-Abrir el proyecto en NetBeans.
-Localizar el archivo TestTablaHash.java dentro del paquete hashmap.
-Hacer clic derecho sobre el archivo y seleccionar "Run File".
NetBeans compilará y ejecutará el proyecto automáticamente.
---------------------------------------------------------------------

## Generación de Documentación (opcional)
javadoc -d docs src/hashmap/*.java

## Compilación manual (opcional)
javac src/hashmap/*.java

## Ejecución manual (opcional)
java hashmap.TestTablaHash

