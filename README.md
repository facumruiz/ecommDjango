# Proyecto de eCommerce con Django

Este proyecto de eCommerce construido con Django incluye una serie de modelos que representan diferentes aspectos del sistema. Aquí se detallan las funciones de cada modelo:

## Modelos

### 1. USER
- Modelo de Usuario incorporado en Django.
- Se crea una instancia para cada cliente que se registra en el sistema.

### 2. CUSTOMER
- Además del modelo de Usuario, cada cliente contiene un modelo Customer que mantiene una relación uno a uno con cada usuario (OneToOneField).

### 3. PRODUCT
- El modelo de Producto representa los diferentes tipos de productos disponibles en la tienda.

### 4. ORDER
- El modelo de Pedido representa una transacción realizada o pendiente en el sistema.
- Contiene información como ID de transacción, fecha de completado y estado del pedido.
- Este modelo es un hijo del modelo de Cliente y un padre de los elementos del Pedido (Order Items).

### 5. ORDERITEM
- Un elemento de Pedido es un producto individual dentro de un pedido.
- Por ejemplo, un carrito de compras puede contener múltiples elementos, pero todos son parte de un solo pedido.
- Por lo tanto, el modelo OrderItem es un hijo del modelo de Producto y del modelo de Pedido.

### 6. SHIPPING
- No todos los pedidos requerirán información de envío.
- Para pedidos que incluyan productos físicos que necesiten ser enviados, se creará una instancia del modelo de Envío para saber a dónde enviar el pedido.
- El modelo Shipping es simplemente un hijo del modelo de Pedido cuando sea necesario.

## Uso del Proyecto
Este proyecto de eCommerce proporciona una estructura de datos sólida para administrar usuarios, clientes, productos, pedidos y envíos. Además, ofrece la base para construir una plataforma de compras en línea completamente funcional.

### Notas Adicionales
Es importante señalar que este archivo README.md proporciona una descripción general de los modelos utilizados en el proyecto. Para una implementación detallada, se recomienda revisar el código fuente y las relaciones específicas entre los modelos dentro de la aplicación Django.

¡Gracias por revisar este proyecto de eCommerce construido con Django!

# using pip
pip install -r requirements.txt

python manage.py runserver

http://127.0.0.1:8000/admin/
root
tabata12
