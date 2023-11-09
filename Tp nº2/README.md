## Formas Normales en la Normalización de Bases de Datos

En el diseño de bases de datos, las Formas Normales son reglas que se aplican para normalizar una base de datos y eliminar la redundancia de datos. Existen tres Formas Normales principales: 1FN, 2FN y 3FN.

### 1ra Forma Normal (1FN)

La 1ra Forma Normal se refiere a que cada valor en una columna de una tabla debe ser atómico, es decir, no debe ser subdivisible en partes más pequeñas. Además, cada fila en la tabla debe ser única y estar identificada por una clave primaria. En resumen, 1FN asegura que los datos estén organizados de manera que no haya conjuntos repetitivos o campos múltiples en una sola columna.

### 2da Forma Normal (2FN)

La 2da Forma Normal se aplica una vez que la base de datos ha alcanzado la 1ra Forma Normal. Para cumplir con la 2FN, se deben eliminar las dependencias parciales. Esto significa que cada columna no clave debe depender únicamente de la clave primaria completa, no de una parte de ella. En otras palabras, 2FN asegura que los datos estén organizados de manera que no haya redundancia en la información.

### 3ra Forma Normal (3FN)

La 3ra Forma Normal se aplica cuando la base de datos ha alcanzado la 2da Forma Normal. Para cumplir con la 3FN, se deben eliminar las dependencias transitivas. Esto significa que, además de cumplir con la 2FN, ningún atributo no clave debe depender de otro atributo no clave. En resumen, 3FN asegura que los datos estén organizados de manera que no haya dependencias indirectas entre las columnas.

La normalización de bases de datos es un proceso importante para garantizar la integridad y la eficiencia de una base de datos, al minimizar la redundancia y evitar problemas de actualización y eliminación no deseados.
