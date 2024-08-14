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

```csharp
Cliente cliente1 = new ClienteVIP("Juan Pérez", "juan@example.com", "Calle Falsa 123");
clientes.Add(cliente1);
```

### Ejemplo de Registro de Vehículo

```csharp
Vehiculo vehiculo1 = new VehiculoPersonal("ABC123", "Toyota Corolla", "Gasolina");
vehiculos.Add(vehiculo1);
```

### Ejemplo de Registro de Pedido

```csharp
Pedido pedido1 = new Pedido(1, DateTime.Now, cliente1);
pedido1.Productos.Add(new Producto("Producto A", 100));
pedido1.Productos.Add(new Producto("Producto B", 200));
pedidos.Add(pedido1);
```

