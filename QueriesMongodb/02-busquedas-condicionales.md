## Búsquedas

_Selecciona todos los documentos de una colección_

```m
db.libros.find()
db.libros.find({})
```
_Seleccionar todos los documentos de la colección donde la editorial sea biblio_

```m
 db.libros.find({editorial:'Biblio'})
```
_Seleccionar todos los documentos de la colección libros dodne el precio sea igual a 25_
```m
 db.libros.find({precio:25})
 ```
 ## Busqueda con operadores logicos

 **Sintaxis**
 ```m
 {<columna>:
 {<operador>:<valor>}, ...}
 ```

 _Seleccionar todos aquellos documentos de la colección libros donde el precio sea mayor a 25_

```m
db.libros.find({precio:{$gt:25}})
```
 