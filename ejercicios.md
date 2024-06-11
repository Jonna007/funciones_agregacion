# Tarea TAS9 - Funciones de Agregación

## 1. Obtener la edad promedio de los miembros
  - Sentencia:
  ```sql
    SELECT AVG(EXTRACT(YEAR FROM AGE(birth_date))) AS average_age
    FROM members;
  Captura:

![sentence01](https://github.com/Jonna007/funciones_agregacion/assets/146044709/f6354ca8-db5f-42a5-beb4-d39eb6d2f4e5)

## 2. Obtener la edad mínima de los miembros
  - Sentencia:
  ```sql
    SELECT MIN(EXTRACT(YEAR FROM AGE(birth_date))) AS minimum_age
    FROM members;
  Captura:
<img src="./Capturas/sentence02.png" alt="drawing" width="500"/>

## 3. Obtener el número total de registros asistidos
  - Sentencia:
  ```sql
    SELECT COUNT(*) AS total_registrations
    FROM registrations;
  Captura:
<img src="./Capturas/sentence03.png" alt="drawing" width="500"/>

## 4. Obtener el número total de asistentes a todas las conferencias
  - Sentencia:
  ```sql
    SELECT COUNT(DISTINCT member_id) AS total_attendees
    FROM registrations;
  Captura:
<img src="./Capturas/sentence04.png" alt="drawing" width="500"/>

## 5. Obtener el número total de eventos por cada ciudad
  - Sentencia:
  ```sql
    SELECT city, COUNT(*) AS total_events
    FROM events
    GROUP BY city;
  Captura:
<img src="./Capturas/sentence05.png" alt="drawing" width="500"/>

## 6. Obtener el número de registros por cada miembro
  - Sentencia:
  ```sql
    SELECT member_id, COUNT(*) AS total_registrations
    FROM registrations
    GROUP BY member_id;
  Captura:
<img src="./Capturas/sentence06.png" alt="drawing" width="500"/>

## 7. Obtener el número de registros por cada conferencia
  - Sentencia:
  ```sql
    SELECT event_id, COUNT(*) AS total_registrations
    FROM registrations
    GROUP BY event_id;
  Captura:
<img src="./Capturas/sentence07.png" alt="drawing" width="500"/>
