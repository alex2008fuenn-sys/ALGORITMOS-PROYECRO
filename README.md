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
[1:19 a. m., 30/10/2026] Benja: Integrante 1: El rol del primer integrante fue realizar la arquitectura y la lógica. Diseño de las listas de datos, funciones de validación, manejo del carrito y control de sotck.

Integrante 2: El rol del segundo integrante fue realizar la interfaz visual. Adaptación de la lógica a la interfaz web, diseño responsivo y estructuración de menús dinámicos.

Integrante 3: Pruebas y Documentación. Verificación de reglas de validación, pruebas de flujo de usuario y redacción del reporte.
[1:20 a. m., 30/10/2026] Benja: Organización del Equipo
El proyecto se desarrolló mediante un flujo estructurado:

Definición de Requerimientos: Mapeo de las estructuras de datos (listas de productos y ventas) y las operaciones CRUD (crear, listar, eliminar).

Implementación de la Lógica: Programación de las funciones de acceso (login), validaciones de entrada y cálculos numéricos.

Evolución a Interfaz Gráfica (GUI): Migración de la interacción de consola a una interfaz web limpia con botones y tarjetas visuales.

Pruebas Integrales: Simulación de compras y gestión de inventario para asegurar la estabilidad del sistema.

Conclusiones
Mantener la lógica estructurada de programación (uso de listas, condiciones y funciones) facilitó enormemente la construcción del sistema, independientemente de que se haya cambiado la interfaz de consola a web.

El valor agregado de implementar una interfaz gráfica (GUI) en lugar de una consola de texto eleva sustancialmente la experiencia de uso, haciendo que el sistema sea intuitivo y profesional.

Seguridad y Reflexion

Actualmente, nuestro sistema de acceso es bastante sencillo y las credenciales están guardadas a la vista de cualquiera dentro del mismo código. Esto significa que si alguien curioso revisa el programa, podría descubrir la clave fácilmente sin ser administrador. Para mejorarlo de forma realista, lo ideal sería conectar la aplicación a un servidor básico donde las contraseñas no queden expuestas a la vista del usuario, sino que se verifiquen de forma privada y segura antes de abrir el panel de control.

```mermaid
graph TD
    %% Estilos de colores legibles y profesionales
    classDef inicio fill:#1e293b,stroke:#3b82f6,stroke-width:2px,color:#ffffff;
    classDef cliente fill:#0f172a,stroke:#06b6d4,stroke-width:2px,color:#ffffff;
    classDef admin fill:#064e3b,stroke:#10b981,stroke-width:2px,color:#ffffff;

    A([Inicio: SPORTZONE]) --> B{Seleccionar Modo}:::inicio
    
    %% Flujo Cliente
    B -->|Cliente| C[Ver Catálogo y Filtrar por Deporte]:::cliente
    C --> D[Añadir Productos al Carrito]:::cliente
    D --> E{¿Finalizar Compra?}:::cliente
    E -->|Sí| F[Actualizar Stock y Registrar Venta]:::cliente
    E -->|No| C
    
    %% Flujo Administrador
    B -->|Administrador| G[Iniciar Sesión: admin / 1234]:::admin
    G --> H{Menú de Administración}:::admin
    H -->|Inventario| I[Ver o Eliminar Productos]:::admin
    H -->|Agregar| J[Registrar Nuevo Producto]:::admin
    H -->|Ventas| K[Ver Historial de Transacciones]:::admin
    H -->|Estadísticas| L[Ver Ingresos y Unidades Vendidas]:::admin

<img width="1320" height="648" alt="image" src="https://github.com/user-attachments/assets/ee7e2a18-0883-4dc0-9f93-c9c39e706c82" />

