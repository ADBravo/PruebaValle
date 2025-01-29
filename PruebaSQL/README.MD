# Documentación: Prueba de Programación - Adrián David Bravo Montoya

## Instrucciones para importar la base de datos y ejecutar los scripts

Para importar y ejecutar correctamente los scripts, es necesario copiar cada archivo de la carpeta `scripts SQL` en una consulta individual y ejecutarlo según el orden indicado por los nombres de los scripts.

---

## Decisiones tomadas en el diseño del MER y limpieza de datos

![Imagen del MER](imagenes\Prueba.png)

### Decisiones del MER

Para el diseño del MER, inicialmente se evaluó la cantidad de información disponible en el archivo Excel. Esto permitió identificar las claves foráneas, las claves primarias y la forma en que se relacionan entre sí. Este modelo fue cuidadosamente estructurado para identificar correctamente las tablas principales (padres) y secundarias (hijas).

### Limpieza de datos

Para la limpieza de datos, se tomó la decisión de utilizar una herramienta de inteligencia artificial (IA) con el objetivo de minimizar errores humanos. Gracias a la información proporcionada previamente sobre posibles inconsistencias, se lograron resolver problemas como:

- Autores duplicados o mal escritos.
- Libros con fechas de publicación no normalizadas o faltantes.
- Géneros mal organizados o desordenados.
- Usuarios con datos incompletos o inconsistentes.
- Registros de préstamos con fechas en formatos inconsistentes o estados ambiguos.

---

## Ejemplo de ejecución de las consultas solicitadas

### Consultas realizadas

1. **Listar los 5 libros más prestados en los últimos 6 meses, junto con sus géneros y autores.**  
   ![Consulta 1](imagenes\Consulta1.png)

2. **Obtener el total de préstamos activos por usuario, ordenado por cantidad de manera descendente.**  
   ![Consulta 2](imagenes\Consulta2.png)

3. **Mostrar los usuarios con más de 3 préstamos retrasados, incluyendo su nombre y el total de retrasos.**  
   ![Consulta 3](imagenes\Consulta3.png)

4. **Listar los géneros más populares (basados en la cantidad de préstamos), ordenados de mayor a menor.**  
   ![Consulta 4](imagenes\Consulta4.png)

5. **Calcular la cantidad promedio de días de retraso en devoluciones por usuario.**  
   ![Consulta 5](imagenes\Consulta5.png)

6. **Generar un informe que muestre, por mes, la cantidad de préstamos realizados y cuántos fueron devueltos a tiempo.**  
   ![Consulta 6](imagenes\Consulta6.png)

---

## Ejecuciones con triggers

### Ejemplo 1: Verificación de préstamo no devuelto y fecha límite

- **Consulta antes del trigger:** Verifica si el préstamo no ha sido devuelto y si la fecha actual es posterior a la fecha límite. (32 respuestas)  
  ![Consulta antes del trigger](imagenes\AntesT1.png)

- **Consulta después del trigger:** (39 respuestas) 
  ![Consulta después del trigger](imagenes\DespuesT1.png)

### Ejemplo 2: Verificación de modificación del estado

- **Consulta antes del trigger:** Verifica si el estado fue modificado.  
  ![Consulta antes del trigger](imagenes\AntesT2.png)

- **Consulta después del trigger:**  
  ![Consulta después del trigger](imagenes\DespuesT2.png)