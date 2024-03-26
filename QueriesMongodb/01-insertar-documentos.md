# Insertar Documentos 

---
```
db.Alumnos.insertOne(
{
    nombre: "Jovany"
})
```
_Inserción de un documento mas compleojo con array_


```m
db.Alumnos.insertOne(
    {
        nombre:"Rosa"
        edad: 22,
        apellidos: "Estrada"
        aficiones: ["Paracaidismo", "Lectura", "Futbol"]
    }
)
```
_Inertar multiples documentos_
```m
db.Alumnnos.insertMany(
    [
        {
            _id:2,
            nombre: "Diana",
        },
        {
            _id:3,
            nombre: "Flor"
            edad: 43,
        },
        {
            _id: 4,
            nombre: "Francisco",
            edad: 34,
        },
    ]
)
```
---
# Operadores de Comparación
| Operador | Descripción |
| -- | -- |
| $eq | igual |
| $gt | Mayor que |
| $gte | Mayor o igual |
| $in | Buscar un elemento en un array |
| $lt | Menor que |
| $lte | Menor o igual |
| $ne | Todos los elementos que no sean iguales |
| $nin |