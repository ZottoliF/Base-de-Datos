# 1. Entidades:

## Asunto
- Número de expediente
- Cliente
- Fecha de inicio
- Fecha de archivo/finalización
- Estado

## Cliente
- DNI
- Nombre
- Dirección
- Otros datos personales del cliente

## Procurador
- ID de procurador
- Nombre
- Otros datos personales del procurador

La entidad "Asunto" tiene una relación con la entidad "Cliente" a través del atributo "Cliente".

La entidad "Asunto" podría tener una relación con la entidad "Procurador" si un asunto puede ser llevado por uno o varios procuradores. Esto podría ser una relación de muchos a muchos, lo que requeriría una tabla intermedia para manejar esta relación.

# 2. Entidades:

## Avión
- Código
- Tipo
- Base de mantenimiento

## Piloto
- Código
- Nombre
- Horas de vuelo

## Miembro de tripulación
- Código
- Nombre

## Vuelo
- Número de vuelo
- Origen
- Destino
- Hora
- Fecha

La entidad "Vuelo" tiene una relación con la entidad "Avión" a través del atributo "Avión".

La entidad "Vuelo" tiene una relación con la entidad "Piloto" a través del atributo "Piloto".

La entidad "Vuelo" tiene una relación con la entidad "Miembro de Tripulación" a través del atributo "Miembro de Tripulación".

# 3. Entidades:

## Marca
- Id de marca
- Nombre de la marca

## Modelo
- Id de modelo
- Id de marca
- Nombre de modelo
- Precio base
- Datos técnicos

## Equipamiento
- Id de equipamiento
- Id de modelo
- Nombre de elemento
- Precio adicional

## Automóvil
- Número de bastidor
- ID de modelo
- ID de concesionario
- ID de vendedor
- Precio de venta
- Modo de pago
- Fecha de entrega
- Matrícula
- Tipo

## Concesionario
- Id de concesionario
- Nombre de concesionario

## Servicio oficial
- ID de servicio oficial
- ID de concesionario
- Nombre del servicio oficial
- Domicilio
- CUIT

## Vendedor
- ID de vendedor
- Nombre
- DNI
- Domicilio

## Venta
- ID de venta
- Número de bastidor
- ID de vendedor
- Precio de venta
- Modo de pago
- Fecha de venta

## Extra venta
- ID de extras venta
- ID de venta
- ID de equipamiento
- Precio adicional

La entidad "Modelo" tiene una relación con la entidad "Marca" a través del atributo "ID de marca".

La entidad "Modelo" tiene una relación con la entidad "Equipamiento" a través del atributo "ID de modelo".

La entidad "Automóvil" tiene relaciones con las entidades "Modelo", "Concesionario", "Vendedor", y "Servicio Oficial" a través de los atributos mencionados.

La entidad "Venta" tiene relaciones con las entidades "Automóvil" y "Vendedor" a través de los atributos mencionados.

La entidad "Extras Venta" tiene relaciones con las entidades "Venta" y "Equipamiento" a través de los atributos mencionados.
