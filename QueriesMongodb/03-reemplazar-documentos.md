**Seleccionar todos los documentos el donde el titulo termine con la palabra tos**

```m
db.libros.find({titulo:/tos$/})
```

**Seleccionar todos los documentos en donde el titulo termine con j**

```m
db.libros.find({titulo:/J$/})
```
## Operadores $regex
**Seleccionar todos los documentos dodne el titulo contenga la palabra para**

```m
db.libros.find({titulo:{$regex: 'para'}})
```
```m
db.libros.find({titulo:{$regex: 'para()}})
```

## Ver solo ciertas columnas
```m
db.libros.find({}, {titulo:1})
```
**Seleccionar todos los documentos de la editorial planeta, pero mostrando solamente el titulo y la editorial**

```m
db.libros.find({editorial:'Planeta'}, {_id:0,titulo:1, editorial:1},)
```
### Operador exist
_Permite buscar la existencia de una columna_

```m
db.libros.find({titulo:{$exists: false}})
```
### Operador type

```m
db.libros.find({titulo:{$exists: false}})
```
### Tabla tipos de datos mongodb
# Operadores de Comparación
| Type | Number | Alias |
| -- | -- |-- |
| Double | 1 |"double"|
| String | 2 |"string"|
| Object | 3|"object"|
| Array | 4|"array"|
| Binary data| 5 |"binData"|
|Undefined | 6 |"undefined"|
| ObjectId | 7|"objectId"|
| Date|9|"date"|
| Boolean|8|"bool"|
|Null|10|"null"|
| Regular Expression|11|"regex"|
| DBPointer|12|"dbPointer"|
| JavaScript|13|"javascript"|
| Symbol|14|"symbol"|
| 32-bit integer|16|"int"|
| Timestamp|17|"timestamp"|
| 64-bit integer|18|"long"|
| Decimal128|19|"decimal"|
| Min key|-1|"minKey"|
| Max key|127|"maxKey"|



### Operador $set
 _Sirve para cambiar el valor de un campo dentro de la colección_

 ```m
db.libros.updateOne({titulo: 'Java como Programas'}.{$set:{titulo:"Java como Programar"}})
```

**Actualizar el valor de la cantidad a 50 y el precio a 10 donde el id = 9**
 ```m
db.libros.updateOne({_id: 9},{$set:{cantidad: 50, cantidad: 10}})
  ```
**Actualizar todos los documentos donde el prcio sea mayor a 10 por el precio a 150**

 ```m
db.libros.updateOne({precio: {$gt: 10}},{$set: {precio: 150}})
  ```
## Operador sort
_Permite ordenar_

**Ordenar todos los documentos de forma ascendente por la editorial y mostrar solamente titulo, precio, editorial y id** 
 ```m
db.libros.find({},{titulo:1, precio:1, editorial:1, _id:0}).sort({editorial:1})
  ```
  _Descendente_

   ```m
db.libros.find({},{titulo:1, precio:1, editorial:1, _id:0}).sort({editorial:-1})
  ```