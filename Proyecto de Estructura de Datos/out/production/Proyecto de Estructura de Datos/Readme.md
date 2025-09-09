<p align="center">
<img src="img.png" width="100">
</p>
<p align="center">
<h2 style="color: violet; font-weight: bold;">
Proyecto Biblioteca En Consola
</h2>
<h2 style="color: purple; font-weight: bold;">
Autores 
</h2>

_Gabriela Martinez_  
_Karen Andrea Martinez_  
_Carlos Andres Castrillon Oviedo_

---

##  Descripción del proyecto
Este proyecto implementa un **sistema de gestión de biblioteca en consola** con menús interactivos.  
El objetivo es administrar **usuarios, libros y préstamos**, aplicando conceptos de **Programación Orientada a Objetos (POO)**, **colecciones genéricas de Java** y **patrones de diseño simples**.

---

##  Requisitos
- Java JDK 8 o superior.
- IDE (IntelliJ, Eclipse, NetBeans) o consola con `javac/java`.

---

##  Ejecución
1. Compilar todos los archivos:
   ```bash
   javac *.java
Ejecutar el menú principal:

 1. Diseño general  
Se utilizó el paradigma POO, con las clases principales:

Usuarios

Libros

Prestamo

Cada clase cuenta con atributos privados, constructores, getters/setters y un método toString() para mostrar su información.
 con fines de manejo modular se crearon Managers que implementan una interfaz genérica Managers<T>, con operaciones CRUD:

agregar(T obj)

eliminar(String id)

modificar(String id, T nuevo)

buscar(String id)

listar()

Esto garantiza que todos los módulos (Usuarios, Libros y Préstamos) usen la misma estructura de operaciones.

 2. Decisiones de diseño
 Uso de ArrayList
Se utilizó en UsuariosManager y LibrosManager porque:

Permite acceso rápido por índice.

Las operaciones más frecuentes son búsquedas y listados, que en ArrayList son eficientes.

El tamaño puede crecer dinámicamente, sin necesidad de manejar arreglos fijos.

Uso de LinkedList
Se utilizó en PrestamosManager porque:

Los préstamos cambian de estado con frecuencia (se crean y eliminan).

LinkedList es eficiente para inserciones y eliminaciones, ya que no necesita desplazar elementos como en ArrayList.

El acceso por índice no es tan necesario en préstamos.

3. Menús
El programa se organiza a través de un menú principal (Menu.java) que dirige a cada módulo.

Cada manager tiene su propio menú CRUD:

menuUsuarios()

menuLibros()

menuPrestamos()

Se agregó un módulo de Consultas que permite búsquedas avanzadas (por título, autor, ISBN, nombre de usuario o cédula).

Ejemplo de flujo

Copiar código
------ Bienvenidos ------  
****** Menu Principal ******

1. Gestión de Usuarios.
2. Gestión de Préstamos.
3. Gestión de Libros.
4. Consultas.
5. Salir.

Digita la opción: 1

----- Gestión de Usuarios -----  
A. Registrar Usuario.  
B. Eliminar Usuario.  
C. Modificar Usuario.  
D. Listar Usuarios.  
S. Salir.

Digite la opción:  
A  
ID: 123  
Nombre: Ana Torres  
Correo: ana@mail.com  
Usuario agregado.  
Conclusiones  
◘ Se aplicó POO y se utilizó una interfaz genérica para estandarizar los CRUD.

◘ La elección de ArrayList y LinkedList fue fundamentada en las necesidades de cada módulo.

◘ El sistema permite administrar la biblioteca en consola de forma clara y modular.

Gracias a los menús, es fácil de usar incluso para usuarios sin conocimientos técnicos.
