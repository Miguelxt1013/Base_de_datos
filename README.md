# Proyecto Final - Creando Colecciones y Documentos en MongoDB

## Descripción
Este proyecto consiste en el diseño e implementación de una aplicación de comercio electrónico utilizando **MongoDB** como base de datos principal. Se enfoca en la creación de colecciones y documentos, así como en el desarrollo de un sistema completo que incluye backend y frontend.

La solución permite gestionar usuarios, productos, categorías, carritos de compra y órdenes, aprovechando las características flexibles y escalables de MongoDB.

---

## Tecnologías utilizadas

1. **MongoDB**: Base de datos NoSQL orientada a documentos.
2. **Node.js**: Entorno de ejecución para JavaScript.
3. **Express**: Framework para construir el backend y la API REST.
4. **React**: Biblioteca de JavaScript para el desarrollo del frontend.

---

## Estructura de la base de datos

El proyecto organiza los datos en las siguientes colecciones:

1. **Usuarios (users):**
   - **Campos:**
     - `nombre`: Nombre del usuario.
     - `correo`: Correo electrónico único del usuario.
     - `direccion`: Dirección física del usuario.
     - `telefono`: Número de teléfono.
     - `rol`: Rol del usuario en el sistema (cliente o administrador).
     - `fecha_registro`: Fecha en la que el usuario se registró.
   - **Ejemplo de documento:**
     ```json
     {
       "nombre": "Juan Perez",
       "correo": "juan.perez@example.com",
       "direccion": "Calle 123",
       "telefono": "123456789",
       "rol": "cliente",
       "fecha_registro": "2024-12-10"
     }
     ```

2. **Productos (products):**
   - **Campos:**
     - `nombre`: Nombre del producto.
     - `descripcion`: Breve descripción del producto.
     - `precio`: Precio del producto.
     - `imagen`: URL de la imagen del producto.
     - `categoria`: Categoría a la que pertenece el producto.
     - `stock`: Cantidad disponible del producto.
   - **Ejemplo de documento:**
     ```json
     {
       "nombre": "Laptop x",
       "descripcion": "Laptop de alto rendimiento",
       "precio": 1200,
       "imagen": "http://example.com/laptop.jpg",
       "categoria": "Electrónica",
       "stock": 15
     }
     ```

3. **Categorías (categories):**
   - **Campos:**
     - `nombre`: Nombre de la categoría.
     - `descripcion`: Descripción breve de la categoría.
   - **Ejemplo de documento:**
     ```json
     {
       "nombre": "Electrónica",
       "descripcion": "Dispositivos y gadgets tecnológicos"
     }
     ```

4. **Carrito de compras (cart):**
   - **Campos:**
     - `usuario_id`: Identificador único del usuario propietario del carrito.
     - `productos`: Lista de productos con sus identificadores y cantidades.
   - **Ejemplo de documento:**
     ```json
     {
       "usuario_id": "64a9f1234",
       "productos": [
         { "producto_id": "12345", "cantidad": 2 },
         { "producto_id": "67890", "cantidad": 1 }
       ]
     }
     ```

5. **Órdenes (orders):**
   - **Campos:**
     - `usuario_id`: Identificador único del usuario que realizó la orden.
     - `productos`: Lista de productos con sus identificadores y cantidades.
     - `estado`: Estado actual de la orden (pendiente, pagado, enviado).
     - `total`: Monto total de la orden.
   - **Ejemplo de documento:**
     ```json
     {
       "usuario_id": "64a9f1234",
       "productos": [
         { "producto_id": "12345", "cantidad": 2 },
         { "producto_id": "67890", "cantidad": 1 }
       ],
       "estado": "pagado",
       "total": 1500
     }
     ```

---

## Objetivos

### Objetivo general
Desarrollar una aplicación de comercio electrónico que permita la gestión de usuarios, productos, categorías, carritos de compra y órdenes mediante el uso de MongoDB como base de datos principal.

### Objetivos específicos
- Diseñar una base de datos con colecciones para usuarios, productos, categorías, carritos y órdenes.
- Implementar un backend con **Node.js** y **Express** que maneje operaciones CRUD y proporcione una API REST.
- Desarrollar una interfaz de usuario intuitiva con **React** para interactuar con el sistema.
- Garantizar la integridad y seguridad de los datos mediante validaciones y controles en el backend.
- Configurar la conexión entre el backend y MongoDB para optimizar el manejo de los datos.
- Probar y documentar el sistema desarrollado.

---

## Conclusión
Este proyecto proporciona una comprensión fundamental sobre la gestión de datos en una base de datos NoSQL. Mediante referencias y documentos incrustados, se logra establecer relaciones entre datos como usuarios y órdenes, demostrando la flexibilidad y escalabilidad de **MongoDB**.

---

## Instrucciones para ejecutar el proyecto

1. **Clonar el repositorio:**
   ```bash
   git clone <URL-del-repositorio>
   cd <nombre-del-repositorio>
   ```

2. **Instalar dependencias:**
   ```bash
   npm install
   ```

3. **Configurar la base de datos:**
   - Crear una base de datos llamada `Mi_proyecto` en MongoDB.
   - Importar las colecciones descritas previamente.

4. **Ejecutar el backend:**
   ```bash
   npm run backend
   ```

5. **Iniciar el frontend:**
   ```bash
   npm run frontend
   ```

6. **Probar el sistema:**
   - Acceder a la interfaz de usuario.
   - Realizar operaciones CRUD.

---

## Autores
- **Miguel Angel Hurtado Angulo**

**Fecha:** 12 de octubre de 2024.



