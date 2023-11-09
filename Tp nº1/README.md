# Trabajo Práctico - Base de Datos

## Alumno
- Gonzalo Isaías Bouso

## Parte 1 - Base de Datos de un Gabinete de Abogados

### Entidades
1. Asunto
2. Cliente
3. Procurador

### Atributos
#### Asunto:
- Número de expediente (clave primaria)
- Fecha de inicio
- Fecha de archivo o finalización
- Estado

#### Cliente:
- DNI (clave primaria)
- Nombre
- Dirección

#### Procurador:
- DNI (clave primaria)
- Nombre
- Otros datos personales del procurador

### Relaciones
1. Asunto - Cliente: Un asunto está asociado a un único cliente, pero un cliente puede tener varios asuntos.
   - Clave foránea en la entidad Cliente: ID_ASUNTO
   - Clave primaria en la entidad Asunto: Numero de expediente 

2. Asunto - Procurador: Un asunto puede ser llevado por uno o varios procuradores, y un procurador puede estar involucrado en varios asuntos.
   - Clave foránea en la entidad Asunto: ID_Procurador 
   - Clave primaria en la entidad Procurador: DNI del procurador

## Parte 2 - Base de Datos de una Compañía Aérea

### Entidades
1. Avión
2. Piloto
3. Miembro de Tripulación
4. Vuelo

### Atributos
#### Avión:
- Código (clave primaria)
- Tipo
- Base de mantenimiento

#### Piloto:
- Código (clave primaria)
- Nombre
- Horas de vuelo

#### Miembro de Tripulación:
- Código (clave primaria)
- Nombre

#### Vuelo:
- Número de vuelo (clave primaria)
- Origen
- Destino
- Hora
- Fecha (para vuelos futuros y pasados)

### Relaciones
1. Vuelo - Avión: Cada vuelo está asociado a un avión.
   - Clave foránea en la entidad Vuelo: ID_Avion
   - Clave primaria en la entidad Avión: Código

2. Vuelo - Piloto: Cada vuelo está asignado a un piloto.
   - Clave foránea en la entidad Vuelo: ID_Piloto
   - Clave primaria en la entidad Piloto: Código Piloto

3. Vuelo - Miembro de Tripulación: Cada vuelo tiene varios miembros de tripulación.
   - Clave foránea en la entidad Miembros de la tripulacion: ID_vuelos
   - Clave primaria en la entidad Vuelo: Numero de vuelo

## Parte 3 - Base de Datos de un Concesionario de Automóviles

### Entidades
1. Marca
2. Modelo
3. Automóvil
4. Característica (Equipamiento de serie)
5. Extra
6. Concesionario
7. Servicio Oficial
8. Vendedor
9. Venta

### Atributos
#### Marca:
- ID (clave primaria)
- Nombre

#### Modelo:
- ID (clave primaria)
- Nombre
- Marca (clave foránea hacia Marca)

#### Automóvil:
- Número de bastidor (clave primaria)
- Marca (clave foránea hacia Marca)
- Modelo (clave foránea hacia Modelo)
- Precio
- Descuento
- Datos técnicos (potencia, cilindrada, etc.)

#### Característica (Equipamiento de serie):
- ID (clave primaria)
- Descripción

#### Extra:
- ID (clave primaria)
- Descripción
- Precio

#### Concesionario:
- ID (clave primaria)
- Nombre
- Domicilio
- CUIT

#### Servicio Oficial:
- ID (clave primaria)
- Nombre
- Domicilio
- CUIT
- Concesionario al que pertenece (clave foránea hacia Concesionario)

#### Vendedor:
- ID (clave primaria)
- Nombre
- DNI
- Domicilio

#### Venta:
- ID (clave primaria)
- Automóvil vendido (clave foránea hacia Automóvil)
- Vendedor (clave foránea hacia Vendedor)
- Servicio Oficial (clave foránea hacia Servicio Oficial)
- Precio de venta
- Modo de pago (al contado o financiera)
- Extras incluidos
- Precio de cada extra
- Fecha de entrega
- Matrícula
- Origen (de stock o encargado a fábrica)

### Relaciones
1. Marca - Modelo: Cada modelo está asociado a una marca pero una marca puede tener varios modelos.
   - Clave foránea en la entidad Modelo: ID_marca (FK)

2. Modelo - Característica: Cada modelo puede tener varias características de equipamiento de serie.
   - Relación muchos a muchos a través de una tabla intermedia, ya que las características pueden ser compartidas por varios modelos.

3. Modelo - Extra: Cada modelo puede tener varios extras disponibles.
   - Relación muchos a muchos a través de una tabla intermedia, ya que los extras pueden ser opcionales para varios modelos.

4. Automóvil - Modelo y Marca: Cada automóvil pertenece a un modelo y una marca.
   - Claves foráneas en la entidad Automóvil: ID_marca (FK) y ID_modelo (FK)

5. Automóvil - Venta: Cada venta está asociada a un automóvil.
   - Clave foránea en la entidad Venta: ID_automovil (FK)

6. Venta - Vendedor: Cada venta está asociada a un vendedor, pero un vendedor puede estar relacionado con varias ventas.
   - Clave foránea en la entidad Venta: ID_vendedor (FK)

7. Venta - Servicio Oficial: Cada venta puede estar asociada a un servicio oficial.
   - Clave foránea en la entidad Venta: ID_servicio_oficial (FK)

8. Venta - Extra: Cada venta puede incluir varios extras.
   - Relación muchos a muchos a través de una tabla intermedia, ya que los extras pueden ser incluidos en varias ventas y una venta puede incluir varios extras


ACTUALIZADO