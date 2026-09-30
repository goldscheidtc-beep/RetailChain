¿Cuántas filas devuelve cada consulta y por qué son distintas? Explicá con ejemplos concretos de los datos qué filas se eliminaron con UNION.

En mi ejecución, UNION y UNION ALL devolvieron 14 filas.
Esto pasa porque los productos repetidos entre sucursales (ej. Monitor 4K, Teclado Mecánico, SSD Externo) tienen distinto stock.
UNION elimina duplicados solo si todas las columnas coinciden exactamente; como los valores de stock son diferentes, no se eliminó ninguna fila.
UNION ALL conserva todos los registros, por eso en este caso devuelve la misma cantidad de filas que UNION.

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
 
