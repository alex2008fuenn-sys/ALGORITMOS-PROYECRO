Descripción del Sistema
SPORTZONE es un sistema informático de gestión y tienda deportiva que opera bajo una interfaz web moderna. Permite simular las operaciones clave de un negocio: la experiencia de compra para los clientes y el control de inventario, registro de ventas y estadísticas para los administradores.

¿Cómo lo hicimos? (De la lógica estructurada a la Web)
El proyecto se diseñó originalmente pensando en la lógica clásica de programación, pero adaptado a una interfaz visual interactiva:

Estructuras de Datos (Listas): Los productos, el carrito de compras y las ventas se manejan mediante arreglos de objetos en memoria, permitiendo agregar, buscar, listar y eliminar elementos de manera dinámica.

Menú y Navegación: En lugar de un ciclo repetitivo de consola (while), la navegación entre opciones se logra mediante funciones condicionales (if/else) disparadas por botones, actualizando la pantalla en tiempo real.

Cálculos y Operaciones: El sistema procesa automáticamente totales, conteos de stock e ingresos acumulados utilizando funciones matemáticas sobre las listas.

Validaciones de Entrada: Se incorporaron controles para evitar que el programa falle ante datos vacíos o incorrectos (por ejemplo, validando precios numéricos con isNaN o controlando el stock disponible antes de vender).

Manual de Uso
Pantalla Principal: Al abrir el programa, elige entre Ingresar como Cliente o Acceso Administrador.

Modo Cliente:

Explora el catálogo o filtra por deporte (Fútbol / Básquetbol).

Haz clic en "Añadir al carrito". El sistema validará que haya stock disponible.

Entra al carrito para ver el desglose de tu compra y presiona "Finalizar Compra" para descontar automáticamente el inventario.

Modo Administrador:

Ingresa con el usuario admin y contraseña 1234.

En el menú principal, navega para ver el inventario general, eliminar productos, registrar nuevos artículos mediante el formulario o consultar el historial de ventas y estadísticas globales.
