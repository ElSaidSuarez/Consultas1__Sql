# Consulta #1 Sql

## CONSULTAS SQL


### 1. Para visualizar toda la información que contiene la tabla `usuario` se puede incluir con la instrucción SELECT el caracter `*` o cada una de los campos de la tabla 

- `SELECT * FROM usuario`

- [Consulta1](img/consulta1.png "Tabla usuario")

### 2. Seleccionar o visualizar solamente la identificación del usuario.

- `SELECT Identificación FROM usuario`

- [Consulta2](img/consulta2%20.png "Tabla Identificacion")

### 3. Si se desea obtener los registros cuya identificacion sean mayores o iguales a 150, se debe utilizar la consulta WHERE que especifica las condiciones que deben reunir los registros que se van a seleccionar-

- `SELECT * FROM usuario WHERE identificacion >= 150`

 - [Consulta3](img/consulta3.png "Tabla Mayor o igual que")

### 4. Si se desea obtener los registros cuyo sus apellidos sean Vanegas o Cetina, se debe utilizar el operador IN que especifica los registros 
- `SELECT apellidos FROM usuario WHERE apellidos IN ('Vanegas', 'Cetina')`

- [Consulta4](img/Consulta4.png "Tabla Apellidos1")

O se puede utilizar el operador OR.

- `SELECT apellidos FROM usuario WHERE apellidos='Vanegas' OR apellidos='Cetina'`

- [Consulta4.1](img/consulta4-2.png "Tabla Apellidos2")

### 5. Si se desea obtener los registros cuya identificacion sea menor de '110' y la ciudad sea 'Cali', se debe utilizar el operador AND.

- `SELECT * FROM usuario WHERE identificacion < 110 AND ciudad_nac='Cali'`

- [Consulta5](img/consulta%205.png "Tabla Apellidos2")

### 6. Si se desea obtener los registros cuyos nombres empiecen por la letra 'A', se debe usar el operador LIKE que usa los patrones '%' (todos) y '_' (caracter).

- `SELECT * FROM usuario WHERE nombre LIKE 'A%'`

- [Consulta6](img/consulta6.png "Tabla nombreA")

### 7. Si desea obtener los registros que contengan la letra 'a'.

`SELECT * FROM usuario WHERE nombre LIKE '%a%'`

- [Consulta7](img/consulta7.png "Tabla nombreConA")

### 8. Si se desea obtener los registros donde la cuarta letra del nombre sea una 'a'.

`SELECT * FROM usuario WHERE nombre LIKE '___a%'`

- [Consulta8](img/consulta8.png "Tabla nombreConA en cuarto")

### 9. Si se desea obtener los registros cuya identificacion este entre el intervalo 110 y 150, se debe utilizar la clausula BETWEEN, que sirve para especificar un intervalo de valores.

`SELECT * FROM usuario WHERE identificacion BETWEEN '110' AND '150'`

- [Consulta9](img/consulta9.png "Tabla seleccionar entre x variables")

## COMANDO DELETE

### 10. Para eleminar solamente los registro cuya identificacion sea mayor de 130.

`DELETE FROM usuario WHERE identificacion > '130'`

-[Consulta10](img/consulta10.png "Tabla delete users")

- [Consulta10.1](img/consulta10-2.png "Tabla delete users1")

## COMANDO UPDATE

### 11. Para actualizar la ciudad de nacimiento de Andres Vanegas, cuya informacion es 118.

`UPDATE usuario SET ciudad_nac = 'Manizales' WHERE identificacion='118'`

- [Consulta11](img/consulta11.png "Tabla actializar datos")
- [Consulta12](img/consulta12.png "Tabla Pedidos")

## INNER JOIN

### Permite obtener datos de dos o mas tablas. Cuando se realiza la concantenacion de las tablas, no necesariamente se deben mostrar todos los datos de las tablas.

## Tabla pedidos

### 12 para visualizar los campos identificacion, nombre, apellidos de la tabla de usuario y nropedido, fecha de compra, fecha de vencimiento y observacion de la tabla pedidos, se debe realizar la siguiente instruccion SQL:

`SELECT usuario.identificacion, usuario.nombre, usuario.apellidos, nropedido, pedidos.fechaVence, pedidos.observacion, FROM usuario INNER JOIN pedidos ON usuario.Identificacion = pedidos.Identificacion;`

- [Consulta12](img/consulta12.png "Tabla Pedidos")

### 13. Para visualizar todos los campos de la tablas "usuario" y "pedido" donde identificacion sea mayor que 100, se debe realizar la siguiente instruccion.

`SELECT usuario.*, pedidos.* FROM usuario INNER JOIN pedidos ON usuario.identificacion = pedidos.identificacion WHERE usuario.identificacion > 100 `

- [Consulta12](img/consulta13.png "Tabla Pedidos")