# Descripción del proyecto (A)

**TiendaManager** es una aplicación de gestión para una tienda que permite registrar y administrar clientes, vehículos y pedidos. La aplicación está diseñada para facilitar la gestión de datos y mejorar la eficiencia operativa de la tienda.

## Características

1. **Registrar Clientes**:
   - Añadir nuevos clientes al sistema.
   - Tipos de clientes: Cliente Regular, Cliente VIP, Cliente Corporativo.
   - Los Clientes VIP y Corporativos tienen descuentos especiales en sus pedidos.

2. **Registrar Vehículos**:
   - Asociar vehículos a los clientes.
   - Tipos de vehículos: Vehículo Personal, Vehículo Corporativo.
   - Los Vehículos Corporativos están asociados únicamente a Clientes Corporativos.

3. **Registrar Pedidos**:
   - Crear pedidos para los clientes.
   - Cada pedido incluye un número único, fecha y lista de productos.
   - El total del pedido se calcula aplicando descuentos según el tipo de cliente.

4. **Mostrar Detalles**:
   - Ver listas de todos los clientes, vehículos y pedidos registrados.
   - Mostrar detalles específicos de cada cliente, vehículo y pedido.

5. **Buscar**:
   - Buscar clientes por nombre.
   - Buscar vehículos por matrícula.
   - Buscar pedidos por número.

6. **Manejo de Errores**:
   - Utiliza `try-catch` para manejar excepciones comunes como duplicados y búsquedas fallidas.

## Requisitos

- .NET Core SDK
- Visual Studio o cualquier otro IDE compatible con C#

## Uso

### Menú Principal

1. Registrar Cliente
2. Registrar Vehículo
3. Registrar Pedido
4. Mostrar Detalles
5. Buscar
6. Salir

### Ejemplo de Registro de Cliente

```
Cliente cliente1 = new ClienteVIP("Juan Pérez", "juan@example.com", "Calle Falsa 123");
clientes.Add(cliente1);
```

### Ejemplo de Registro de Vehículo

```
Vehiculo vehiculo1 = new VehiculoPersonal("ABC123", "Toyota Corolla", "Gasolina");
vehiculos.Add(vehiculo1);
```

### Ejemplo de Registro de Pedido

```
Pedido pedido1 = new Pedido(1, DateTime.Now, cliente1);
pedido1.Productos.Add(new Producto("Producto A", 100));
pedido1.Productos.Add(new Producto("Producto B", 200));
pedidos.Add(pedido1);
```

# Descripción del Proyecto (B)

Este proyecto es una aplicación de consola en C# que gestiona un sistema de reservas para un restaurante. Permite registrar clientes, crear reservas y calcular totales con descuentos basados en el tipo de cliente (Regular o VIP).

## Estructura del Código

### Clases Principales

1. **Cliente (abstract)**: Clase base para los clientes.
   - Propiedades:
     - `Nombre`: Nombre del cliente.
     - `Correo`: Correo electrónico del cliente.
     - `Telefono`: Número de teléfono del cliente.
   - Método abstracto:
     - `ObtenerDescuento()`: Devuelve el descuento aplicable.

2. **ClienteRegular**: Hereda de `Cliente`. 
   - Implementa `ObtenerDescuento()` devolviendo 0 (sin descuento).

3. **ClienteVIP**: Hereda de `Cliente`.
   - Implementa `ObtenerDescuento()` devolviendo 0.1 (10% de descuento).

4. **Plato**: Representa un plato del menú.
   - Propiedades:
     - `Nombre`: Nombre del plato.
     - `Precio`: Precio del plato.

5. **Reserva**: Representa una reserva en el restaurante.
   - Propiedades:
     - `Numero`: Número de la reserva.
     - `Fecha`: Fecha de la reserva.
     - `Hora`: Hora de la reserva.
     - `Cliente`: Cliente asociado a la reserva.
     - `Platos`: Lista de platos seleccionados.
   - Método:
     - `CalcularTotal()`: Calcula el total de la reserva aplicando el descuento correspondiente.

### Funcionalidades

- **Registrar Cliente Regular**: Permite registrar un cliente regular.
- **Registrar Cliente VIP**: Permite registrar un cliente VIP.
- **Registrar Reserva**: Permite crear una nueva reserva, asociando un cliente y añadiendo platos.
- **Mostrar Detalles de Clientes**: Muestra la lista de clientes registrados.
- **Mostrar Detalles de Reservas**: Muestra la lista de reservas registradas.
- **Buscar Cliente por Nombre**: Busca y muestra los detalles de un cliente específico.
- **Buscar Reserva por Número**: Busca y muestra los detalles de una reserva específica.

### Manejo de Errores

El programa incluye manejo de excepciones para errores comunes, como:
- Formatos incorrectos en la entrada de datos.
- Números fuera del rango permitido.

## Requisitos

- .NET SDK (versión compatible con C#)
- Un entorno de desarrollo (como Visual Studio o Visual Studio Code)

## Ejecución

1. Clona o descarga el repositorio.
2. Abre el proyecto en tu entorno de desarrollo.
3. Compila y ejecuta el programa.
4. Sigue las instrucciones en pantalla para interactuar con el sistema.

## Contribuciones

Si deseas contribuir a este proyecto, por favor abre un issue o envía un pull request con tus sugerencias o mejoras.


