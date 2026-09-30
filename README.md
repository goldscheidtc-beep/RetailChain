¿Cuántas filas devuelve cada consulta y por qué son distintas? Explicá con ejemplos concretos de los datos qué filas se eliminaron con UNION.

UNION Devuelve 10 filas porque elimina duplicados (productos 103, 104 y 106 que aparecen en ambas sucursales).
Ejemplo: el producto **Monitor 4K (id 103)** aparece en ambas sucursales, pero UNION lo muestra una sola vez.
UNION ALL Devuelve más filas porque conserva todos los registros, incluyendo los repetidos.  
Ejemplo: el mismo Monitor 4K aparece dos veces (una por cada sucursal).

¿Por qué UNION ALL es más eficiente que UNION? ¿Qué operación adicional realiza UNION internamente que consume más recursos?

UNION ALL Es mas eficiente porque ejecuta mas rápido, consume menos, y cada fila la devuelve tal cual incluyendo duplicados.
UNION Opera ordenanando y comparando filas para eliminar las idénticas por eso consume mas recursos.

¿En qué casos de negocio usarías cada uno? Dá al menos dos ejemplos reales distintos a los del ejercicio.

 UNION: 
Lo usaria para crear un catálogo único de productos para marketing.  
Con UNION generaria una lista de clientes únicos en toda la empresa.
UNION ALL:  
Lo usaria para auditorías de stock físico (contar todas las unidades).  
Con UNIO ALL analizaría las ventas totales incluyendo cada transacción.

¿Qué pasa si las columnas de ambas consultas no coinciden en número o tipo? ¿Qué error genera SQL?

Si la columnas de ambas consultas no coinciden SQL, devuelve un error y no se puede ejecutar la consulta. Porque en UNION Y UNION ALL las consultas tienen que tener la misma cantidad de columnas y tipos de datos que sean compatibles.
 
