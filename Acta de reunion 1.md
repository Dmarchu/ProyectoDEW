# Acta de Reunión 01 - Seguimiento Proyecto NOL

**Fecha:** 06 de mayo de 2026  
**Hora de inicio:** 15:00  
**Hora de fin:** 17:00  
**Lugar:** Laboratorio 3T111/3T112 (Sesión de prácticas)  

---

## 1. Asistentes
* [x] Angel Herrera Lozano (Secretario)
* [x] David Martinez Alonso (Presidente)
* [x] David Sanjuan Gonzalez
* [x] Nicolas Rudolf Greshake Pinedo
* [x] Kristian Alexander Elias Duarte

## 2. Resumen de la Reunión y Temas Tratados
El objetivo principal de esta sesión ha sido arrancar el desarrollo técnico de cara al Hito 1 (entrega el 17/05). 
* Se ha puesto en marcha la aplicación CentroEducativo en el puerto 9090 de la máquina de portal[cite: 6].
* Se ha configurado el proyecto web dinámico (`no12526`) en Eclipse IDE y se ha enlazado con Apache Tomcat v10.1[cite: 5, 6].
* Hemos redactado y probado el script de shell (`poblar.sh`) haciendo uso de `curl` para poblar la base de datos cada vez que se reinicia el servidor[cite: 6].

## 3. Decisiones Técnicas y Librerías
* **Librerías HTTP:** Tras evaluar las opciones del enunciado, el equipo ha decidido utilizar **Apache HttpComponents (HttpClient 5.4)** para realizar las peticiones REST desde los servlets hacia CentroEducativo[cite: 6].
* **Decodificación JSON:** Se utilizará la librería **Gson** (de Google) por su facilidad de uso para parsear las respuestas de la API[cite: 6].
* **Filtro Logs:** Se ha implementado la Versión 2 del filtro (`Logs.java`), configurado exclusivamente a través del archivo `web.xml` sin usar anotaciones[cite: 6].

## 4. Dificultades y Desacuerdos
* **Dificultad:** Eclipse IDE marcaba errores de sintaxis en el archivo `web.xml`. Se solucionó habilitando la resolución de entidades externas en las preferencias de XML de Eclipse[cite: 5].
* **Desacuerdos:** Ninguno. Todos los miembros están de acuerdo con las librerías seleccionadas.

## 5. Reparto de Tareas (Próximos Pasos)
Se asignan las tareas para completar antes de la próxima reunión:

| Tarea a realizar | Responsable | Fecha Límite |
| :--- | :--- | :--- |
| Desarrollar `LoginServlet` e integrar HttpClient 5.4 | David Martinez & David Sanjuan | 10/05/2026 |
| Compatibilizar sesión Tomcat con clave `key` de la API | Nicolas Rudolf | 11/05/2026 |
| Crear vistas HTML base con Bootstrap 5 (Bienvenida y Alumno) | Kristian Alexander | 11/05/2026 |
| Revisión del Filtro Logs y actualización de `web.xml` | Angel Herrera | 11/05/2026 |

---

**Validado por todos los miembros del equipo en la fecha arriba indicada.**