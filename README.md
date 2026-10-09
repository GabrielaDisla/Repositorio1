# GameStoreDR : Plataforma para comprar videojuegos.
## Objetivo del sistema:
Ofrecer una plataforma digital especializada para la comercialización, exploración y la compra de juegos en el País, 
optimizando el manejo del inventario y la emisión de los comprobantes digitales.

## Problemas resueltos:
- Eliminación de la falta de control de frente inventario en tiempo real.
- Reducción del tiempo de espera del cliente al hacer pagos en linea.

## Principales funcionalidades: 
- Carrito de compras con control muy estricto de concurrencia de stock
- Panel de admin. para la gestión de inventario.
- Catálogo dinámico con filtro por categorías y fichas técnicas de videojuegos.
- Un procesamiento de pago con generación asíncrona de las facturas PDF y una notificación por correo.

## Arquitectura y Organización Decoupled (Frontend / Backend)

El sistema adopta una arquitectura desacoplada basada en servicios RESTful:

- **Frontend (Interfaz de Usuario):**
  - **Responsabilidad:** Presentación visual, renderizado del catálogo, manejo del estado de la interfaz (carrito, filtros) y consumo de datos mediante peticiones HTTP/HTTPS.
  - **Tecnologías sugeridas:** React / HTML5, CSS3, JavaScript.

 
- **Backend (Lógica de Negocio y Persistencia):**
  - **Responsabilidad:** Autenticación mediante tokens JWT, validación de reglas de negocio, control pesimista/optimista del inventario en DB y procesamiento en segundo plano para la generación de comprobantes PDF.
  - **Tecnologías sugeridas:** Node.js (Express) / C#, PostgreSQL / MySQL.
 
    
- **Comunicación entre Capas:**- Se realiza a través de un **API RESTful** utilizando intercambio de datos en formato JSON y autenticación por cabeceras HTTP (`Authorization: Bearer <token>`).

## Herramientas usadas
- **Gestión y Control de Versiones:** GitHub, GitHub Projects, GitHub Issues.
- **Diseño y Arquitectura:** Visual Paradigm Online.
