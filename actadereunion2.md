# Acta de Reunión 02 - Cierre Hito 1 Proyecto NOL

**Fecha:** 13 de mayo de 2026  
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
El objetivo de esta sesión es integrar todas las partes desarrolladas durante la semana y empaquetar el entregable del Hito 1[cite: 6].
* Se ha logrado integrar con éxito el inicio de sesión. El `LoginServlet` captura el DNI y password, lanza la petición a la API y recupera la `key`[cite: 6].
* Se ha implementado la compatibilidad de sesiones: la `key` devuelta por la API se almacena en la sesión de Tomcat (`HttpSession`) para futuras consultas del alumno[cite: 6].
* Se ha unificado la navegación del alumno: Pantalla de Bienvenida -> Lista de asignaturas matriculadas -> Detalle de nota (Prototipo base)[cite: 6].

## 3. Decisiones Técnicas y Librerías
* **Seguridad Tomcat:** Se han definido los roles `rolalu` y `rolpro` en `tomcat-users.xml` y se han protegido las rutas de los servlets configurando los `<security-constraint>` directamente en el `web.xml`[cite: 6].
* **Frontend:** Se ha verificado que todas las páginas generadas por los servlets comparten la misma estructura visual utilizando Bootstrap 5[cite: 6].

## 4. Dificultades y Desacuerdos
* **Dificultad:** Hubo problemas al pasar la variable `key` en el *query string* para listar las asignaturas del alumno. Se solucionó concatenando correctamente el valor de la sesión en la URL de Apache HttpClient.
* **Dificultad:** La persistencia de datos nos retrasó en las pruebas, ya que olvidábamos ejecutar el `poblar.sh` tras reiniciar CentroEducativo[cite: 6]. 
* **Desacuerdos:** Ninguno.

## 5. Reparto de Tareas (Próximos Pasos)
Asignación final para enviar el Hito 1 (Fecha límite: 17/05/2026)[cite: 6]:

| Tarea a realizar | Responsable | Fecha Límite |
| :--- | :--- | :--- |
| Comentar y documentar código Java (Servlets y Filtro) | David Sanjuan & Kristian | 15/05/2026 |
| Comprobar funcionamiento del Filtro Logs (v2) y rutas | Nicolas Rudolf | 15/05/2026 |
| Exportar proyecto a ZIP y adjuntar configuración Tomcat | David Martinez | 16/05/2026 |
| Revisar Markdown de actas y subir todo a PoliformaT | Angel Herrera | 16/05/2026 |

---

**Validado por todos los miembros del equipo en la fecha arriba indicada.**