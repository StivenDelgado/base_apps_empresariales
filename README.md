📌 Relación entre Orden y Producto (N:M)
Este proyecto implementa una relación muchos a muchos (N:M) entre Orden y Producto. En un sistema de comercio electrónico o facturación, una orden puede contener múltiples productos, y un producto puede estar en varias órdenes.

🔗 Definición de la Relación
Orden representa una compra realizada por un usuario, con una descripción y un precio total.
Producto representa un artículo disponible en la tienda, con un precio y stock.
OrdenProducto es una entidad intermedia que almacena la cantidad de un producto en una orden específica.

🏗 Estructura de la Base de Datos

| Orden        | 🔗  | OrdenProducto  | 🔗  | Producto     |
|-------------|----|---------------|----|-------------|
| id (PK)     | ←  | orden_id (FK) | →  | id (PK)     |
| descripcion |    | producto_id (FK) |    | nombre      |
| total_price |    | cantidad      |    | descripcion |
|             |    |               |    | precio      |
|             |    |               |    | stock       |
