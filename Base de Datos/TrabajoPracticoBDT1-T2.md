## Gabinete de Abogados

### Entidad: Asunto
- Atributos:
  - Número de expediente (clave primaria)
  - Fecha de inicio
  - Fecha de archivo o finalización
  - Estado (en trámite, archivado, etc.)

### Entidad: Cliente
- Atributos:
  - DNI (clave primaria)
  - Nombre
  - Dirección
  - Otros datos personales del cliente

### Entidad: Procurador
- Atributos:
  - ID del procurador (clave primaria)
  - Nombre
  - Dirección
  - Otros datos personales del procurador

#### Primera Forma Normal (1FN):
- Cada atributo debe contener un solo valor, es decir, no debe haber atributos multivaluados o repetidos en una fila.
- Todos los valores deben ser atómicos, lo que significa que no se pueden descomponer en partes más pequeñas.

#### Segunda Forma Normal (2FN):
- En 1FN, aseguramos que los valores sean atómicos. En 2FN, nos aseguramos de que todos los atributos no clave (que no son parte de la clave primaria) dependan completamente de la clave primaria.
- Si tienes una clave compuesta (compuesta por varios atributos), cada atributo no clave debe depender de la clave completa, no solo de una parte de ella.

#### Tercera Forma Normal (3FN):
- En 3FN, eliminamos las dependencias transitivas. Esto significa que si un atributo depende de otro atributo que no sea la clave primaria, se debe separar en una nueva entidad.

## Compañía Aérea

### Entidad Avión:
- Atributos:
  - Código del avión (clave primaria)
  - Tipo de avión
  - Base de mantenimiento

### Entidad Piloto:
- Atributos:
  - Código del piloto (clave primaria)
  - Nombre del piloto
  - Horas de vuelo acumuladas

### Entidad Miembro de Tripulación:
- Atributos:
  - Código del miembro de tripulación (clave primaria)
  - Nombre del miembro de tripulación

### Entidad Vuelo:
- Atributos:
  - Número de vuelo (clave primaria)
  - Origen del vuelo
  - Destino del vuelo
  - Hora del vuelo
  - Fecha del vuelo
  - Estado del vuelo

#### Primera Forma Normal (1FN):
- Cada celda (posición en la tabla) debe contener un solo valor, no una lista de valores.
- Cada fila debe ser única, es decir, no debe haber duplicados en la tabla.

#### Segunda Forma Normal (2FN):
- Cumple con 1FN.
- Todos los atributos no clave (campos que no son parte de la clave primaria) deben depender completamente de la clave primaria.

#### Tercera Forma Normal (3FN):
- Cumple con 2FN
- No debe haber dependencias transitivas. Esto significa que si un atributo depende de otro atributo que no es la clave primaria, ese atributo debe moverse a su propia tabla.

## Concesionario de Autos

### Entidad Auto:
- Atributos:
  - ID de auto (clave primaria)
  - Marca
  - Modelo
  - Precio
  - Descuento (si tiene)
  - Datos técnicos (potencia, cilindrada, etc.)

### Entidad Características de Equipamiento:
- Atributos:
  - ID de característica (clave primaria)
  - Nombre de la característica

### Entidad Extras:
- Atributos:
  - ID de extra (clave primaria)
  - Nombre del extra
  - Precio del extra

### Entidad Modelo de Auto:
- Atributos:
  - ID del modelo (clave primaria)
  - Marca
  - Nombre del modelo
  - Precio del modelo (sin extras)
  - ID de característica (clave foránea)
  - ID de extra (clave foránea)

### Entidad Concesionario:
- Atributos:
  - ID de concesionario (clave primaria)
  - Nombre del concesionario
  - Dirección
  - CUIT

### Entidad Stock de Autos:
- Atributos:
  - ID de auto en stock (clave primaria)
  - ID de auto (clave foránea)
  - Ubicación (local del concesionario o servicio oficial)
  - Estado (disponible, vendido, etc.)

### Entidad Servicio Oficial:
- Atributos:
  - ID de servicio oficial (clave primaria)
  - Nombre del servicio oficial
  - Dirección
  - CUIT del servicio oficial
  - ID de concesionario (clave foránea)

### Entidad Vendedor:
- Atributos:
  - ID de vendedor (clave primaria)
  - Nombre del vendedor
  - DNI del vendedor
  - Dirección del vendedor

### Entidad Venta de Auto:
- Atributos:
  - ID de venta (clave primaria)
  - ID de automóvil vendido (clave foránea)
  - ID de vendedor (clave foránea)
  - ID de servicio oficial (clave foránea, si corresponde)
  - Precio de venta (incluyendo extras, si los hay)
  - Modo de pago (al contado o financiera)
  - Fecha de entrega
  - Matrícula del automóvil vendido
  - Origen (de stock o encargado a fábrica)

#### Primera Forma Normal (1FN):
- Cada celda (posición en la tabla) debe contener un solo valor, no una lista de valores.
- Cada fila debe ser única, es decir, no debe haber duplicados en la tabla.

#### Segunda Forma Normal (2FN):
- Cumple con 1FN.
- Todos los atributos no clave (campos que no son parte de la clave primaria) deben depender completamente de la clave primaria.

#### Tercera Forma Normal (3FN):
- Cumple con 2FN
- No debe haber dependencias transitivas. Esto significa que si un atributo depende de otro atributo que no es la clave primaria, ese atributo debe moverse a su propia tabla.
