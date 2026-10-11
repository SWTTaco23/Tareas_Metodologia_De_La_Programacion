# Investigación sobre metodologías ágiles

**Nombre:** Fernando Emir Walle Hernandez\
**Matrícula:** 2630316\
**Asignatura:** Metodología de la programación\
**Fecha:** 11 de Octubre del 2026

## 1. Resumen ejecutivo

Ágil es una forma de trabajar que busca entregar resultados útiles, recibir retroalimentación y adaptar el trabajo conforme se aprende. En desarrollo de software, esto implica construir y evaluar partes del producto en lugar de esperar hasta el final para comprobar si cumplen las necesidades.

El movimiento ágil surge como respuesta a las dificultades de los procesos demasiado rígidos ante cambios e incertidumbre. En 2001 se publicó el Manifiesto Ágil, que reunió valores y principios para orientar el desarrollo de software [1], [2].

Trabajar de manera ágil no significa improvisar o eliminar la documentación. Significa planear con información disponible, comprobar resultados y ajustar las decisiones.

Esta investigación explica los valores ágiles, sus beneficios y riesgos, y tres enfoques relacionados: Scrum, Kanban y Design Thinking. También presenta responsabilidades, eventos, métricas y ejemplos de aplicación.

## 2. Valores y principios ágiles

### 2.1. Los cuatro valores

El Manifiesto Ágil reconoce que ambos lados de cada comparación tienen utilidad, pero da mayor importancia al primero [1].

| **Valor**                                                                                                  | **Impacto en la gestión del trabajo**                    |
| ---------------------------------------------------------------------------------------------------------- | -------------------------------------------------------- |
| Dar más importancia a las personas y su colaboración que a depender únicamente de procesos y herramientas. | Resolver problemas mediante comunicación y acuerdos.     |
| Priorizar software que funciona sobre documentación excesiva.                                              | Evaluar avances mediante resultados utilizables.         |
| Colaborar con el cliente en lugar de limitarse a discutir el contrato.                                     | Revisar necesidades y expectativas durante el proyecto.  |
| Adaptarse a los cambios en lugar de seguir un plan rígidamente.                                            | Actualizar prioridades cuando aparece información nueva. |

Estos valores no eliminan los procesos, documentos, contratos o planes.

### 2.2. Principios e impacto

Los doce principios del Manifiesto pueden resumirse así [2]:

| **Principio**                                     | **Aplicación al trabajo**                  |
| ------------------------------------------------- | ------------------------------------------ |
| Entregar valor pronto y frecuentemente.           | Obtener retroalimentación antes del final. |
| Aceptar cambios útiles.                           | Revisar prioridades.                       |
| Entregar software funcional en periodos cortos.   | Dividir el desarrollo.                     |
| Mantener colaboración entre negocio y desarrollo. | Aclarar necesidades continuamente.         |
| Apoyar a personas motivadas.                      | Dar autonomía y recursos.                  |
| Favorecer comunicación directa.                   | Reducir malentendidos.                     |
| Medir progreso con software funcionando.          | Mostrar resultados verificables.           |
| Mantener un ritmo sostenible.                     | Evitar sobrecarga constante.               |
| Cuidar la calidad técnica y el diseño.            | Facilitar cambios futuros.                 |
| Simplificar.                                      | Evitar trabajo innecesario.                |
| Permitir organización del equipo.                 | Aprovechar conocimientos colectivos.       |
| Reflexionar y mejorar.                            | Ajustar la forma de trabajar.              |

## 3. Panorama de enfoques

Aunque suelen estudiarse juntos, Scrum, Kanban y Design Thinking cumplen funciones diferentes.

| **Enfoque**     | **Característica principal**                                                    | **Cuándo elegirlo**                                                                              |
| --------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------ |
| Scrum           | Marco para desarrollar productos complejos mediante ciclos llamados Sprints.    | Cuando un equipo puede trabajar hacia objetivos compartidos y revisar resultados periódicamente. |
| Kanban          | Enfoque para visualizar, controlar y mejorar el flujo del trabajo.              | Cuando llegan solicitudes continuamente, como tickets de soporte o mantenimiento.                |
| Design Thinking | Enfoque centrado en las personas para comprender problemas y probar soluciones. | Cuando existe incertidumbre sobre las necesidades del usuario o la solución adecuada.            |

Design Thinking no es un marco de entrega equivalente a Scrum. Ayuda a descubrir qué conviene construir. Scrum y Kanban pueden organizar el desarrollo de las soluciones seleccionadas [3], [4], [10].

## 4. Ventajas, limitaciones y trade-offs

Un trade-off es una decisión que obtiene un beneficio a cambio de aceptar un costo o una limitación.

| **Beneficio**                        | **Limitación o riesgo**                                         | **Trade-off típico**                                           |
| ------------------------------------ | --------------------------------------------------------------- | -------------------------------------------------------------- |
| Adaptarse a necesidades nuevas.      | Cambiar prioridades constantemente puede fragmentar el trabajo. | Flexibilidad a cambio de gestionar cuidadosamente los cambios. |
| Entregar resultados temprano.        | Una entrega pequeña puede no incluir todo lo solicitado.        | Aprendizaje temprano a cambio de alcance inicial reducido.     |
| Recibir retroalimentación frecuente. | Requiere disponibilidad de usuarios o interesados.              | Mejor orientación a cambio de tiempo de participación.         |
| Detectar problemas antes.            | Necesita integración y comprobaciones frecuentes.               | Menor riesgo final a cambio de esfuerzo continuo.              |
| Dar autonomía al equipo.             | Sin objetivos claros puede haber desorganización.               | Libertad de decisión a cambio de responsabilidad.              |
| Hacer visible el trabajo.            | Las métricas pueden utilizarse para presionar injustamente.     | Transparencia a cambio de interpretación responsable.          |
| Limitar tareas simultáneas.          | Algunas solicitudes deben esperar.                              | Mayor enfoque a cambio de no comenzar todo inmediatamente.     |

Estos enfoques no garantizan el éxito por sí solos. Su utilidad depende de la calidad técnica, la colaboración y el contexto.

## 5. Scrum

### 5.1. Propósito y cuándo utilizarlo

Scrum permite abordar problemas complejos mediante inspección y adaptación. El equipo construye incrementos utilizables y aprende de los resultados.

Sus pilares son:

- **Transparencia:** conocer el estado real del trabajo.
- **Inspección:** revisar resultados y progreso.
- **Adaptación:** ajustar decisiones ante lo observado.

Conviene cuando existe incertidumbre y es posible desarrollar el producto de forma incremental [3].

### 5.2. Roles y responsabilidades

La actividad utiliza “Development Team”. La Guía Scrum de 2020 emplea “Developers” dentro de un único Scrum Team [3].

| **Responsabilidad** | **Función**                                                                                      | **Error frecuente**                                                            |
| ------------------- | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| Product Owner       | Maximizar el valor, comunicar el objetivo del producto y ordenar el Product Backlog.             | Priorizar sin explicar necesidades o actuar como un comité sin decisión clara. |
| Scrum Master        | Ayudar a comprender Scrum, mejorar la efectividad y facilitar la eliminación de impedimentos.    | Convertirse en un jefe que reparte tareas y exige reportes.                    |
| Developers          | Crear un Increment utilizable, planear el Sprint y adaptar el trabajo para alcanzar su objetivo. | Trabajar por separado y dejar integración o calidad para el final.             |

“Developers” puede incluir distintas especialidades necesarias para construir el producto, no únicamente programación.

### 5.3. Artefactos

| **Artefacto**   | **Definición**                                                        | **Compromiso asociado** | **Criterio práctico de calidad**                                           |
| --------------- | --------------------------------------------------------------------- | ----------------------- | -------------------------------------------------------------------------- |
| Product Backlog | Lista ordenada y cambiante de lo necesario para mejorar el producto.  | Product Goal.           | Los elementos próximos deben ser comprensibles y suficientemente pequeños. |
| Sprint Backlog  | Objetivo del Sprint, elementos seleccionados y plan para realizarlos. | Sprint Goal.            | Debe reflejar el trabajo real y actualizarse conforme se aprende.          |
| Increment       | Resultado utilizable que se suma al producto existente.               | Definition of Done.     | Debe estar integrado y cumplir la calidad acordada.                        |

Los compromisos permiten evaluar el progreso con una referencia compartida [5].

### 5.4. Definition of Done y criterios de aceptación

| **Aspecto** | **Definition of Done**                                                               | **Criterios de aceptación**                                         |
| ----------- | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------- |
| Función     | Define la calidad necesaria del Increment.                                           | Describe condiciones específicas de una funcionalidad.              |
| Alcance     | Se aplica de manera común al trabajo incorporado al producto.                        | Se aplica a un elemento particular.                                 |
| Ejemplo     | Código integrado, pruebas acordadas aprobadas y documentación necesaria actualizada. | Un usuario puede recuperar su contraseña mediante un enlace válido. |

Los criterios de aceptación son una práctica complementaria; no sustituyen la Definition of Done [6].

**Ejemplo académico:**

Para una función de registro de usuarios:

- Criterio de aceptación: impedir registrar dos cuentas con el mismo correo.
- Definition of Done: código revisado, integrado y comprobado con las pruebas acordadas.

Una función puede cumplir su comportamiento esperado y todavía presentar problemas de calidad. En ese caso, no está terminada según la Definition of Done.

### 5.5. Eventos

Las duraciones sugeridas son propuestas para un equipo pequeño. Los máximos indicados corresponden al marco Scrum [7].

| **Evento**           | **Objetivo**                                                   | **Duración sugerida**                                                  | **Antipatrón**                                 |
| -------------------- | -------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------- |
| Sprint               | Construir valor hacia un objetivo.                             | Dos semanas; su duración es de un mes o menos.                         | Alargarlo porque faltan tareas.                |
| Sprint Planning      | Acordar por qué el Sprint es valioso, qué se realizará y cómo. | Dos horas para iniciar; máximo de ocho horas para un Sprint de un mes. | Elegir tareas sin objetivo compartido.         |
| Daily Scrum          | Revisar progreso hacia el Sprint Goal y adaptar el plan.       | Quince minutos.                                                        | Convertirlo en un reporte al jefe.             |
| Sprint Review        | Revisar el resultado con interesados y adaptar lo siguiente.   | Una hora; máximo de cuatro horas para un Sprint de un mes.             | Mostrar diapositivas sin analizar el producto. |
| Sprint Retrospective | Mejorar calidad y efectividad del equipo.                      | Una hora; máximo de tres horas para un Sprint de un mes.               | Buscar culpables sin acordar mejoras.          |

Los eventos ocurren dentro del Sprint. Si alcanzan su propósito antes del tiempo previsto, pueden finalizar.

La Retrospective debe producir mejoras concretas. Por ejemplo: “revisaremos los cambios de código el mismo día para reducir esperas” [12].

### 5.6. Métricas

Velocity y burndown son prácticas complementarias, no requisitos obligatorios de Scrum.

| **Métrica** | **Qué indica**                                                               | **Interpretación útil**                                          | **Uso incorrecto**                                               |
| ----------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- |
| Velocity    | Cantidad estimada de trabajo terminado por Sprint, frecuentemente en puntos. | Ayuda al mismo equipo a elaborar pronósticos.                    | Comparar equipos o evaluar personas.                             |
| Burndown    | Trabajo estimado restante durante un periodo.                                | Permite detectar acumulación o cambios de alcance.               | Exigir que la curva siga perfectamente una línea ideal.          |
| WIP         | Elementos iniciados y no terminados.                                         | Ayuda a observar tareas simultáneas y favorecer la finalización. | Considerar que más tareas abiertas significan más productividad. |

La velocity no mide directamente valor, calidad ni esfuerzo individual [8].

**Ejemplo:**

Un equipo termina 18, 22 y 20 puntos en tres Sprints. Puede utilizar ese historial como referencia, pero no como garantía de que terminará exactamente 20 puntos en el siguiente.

Si el burndown permanece plano varios días, conviene revisar bloqueos, tareas demasiado grandes o problemas de actualización. La gráfica por sí sola no demuestra falta de trabajo.

## 6. Kanban

### 6.1. Fundamentos

Kanban permite mejorar el flujo sin necesitar reemplazar inmediatamente la organización existente. Se comienza con el trabajo actual y se introducen cambios de manera evolutiva [4].

Sus prácticas principales son:

1. **Visualizar:** mostrar estados y elementos.
2. **Limitar WIP:** controlar lo iniciado y no terminado.
3. **Gestionar flujo:** atender esperas y bloqueos.
4. **Hacer políticas explícitas:** aclarar reglas.
5. **Crear retroalimentación:** revisar servicio y resultados.
6. **Mejorar:** experimentar con ajustes.

Se trabaja con un sistema de extracción o pull: se toma trabajo nuevo cuando existe capacidad.

### 6.2. Propuesta de tablero

Se propone este tablero para un equipo académico de cuatro integrantes.

| **Columna** | **Qué contiene**                              | **Límite inicial**                              |
| ----------- | --------------------------------------------- | ----------------------------------------------- |
| Pendiente   | Solicitudes aún no preparadas.                | Sin límite WIP; revisar y ordenar regularmente. |
| Listo       | Elementos aclarados que pueden iniciarse.     | Máximo cinco como política de cola.             |
| Desarrollo  | Trabajo en construcción.                      | Dos.                                            |
| Revisión    | Cambios esperando o recibiendo revisión.      | Uno.                                            |
| Pruebas     | Elementos en comprobación.                    | Uno.                                            |
| Terminado   | Trabajo que cumple las condiciones de salida. | No aplica.                                      |

**Justificación de los límites:**

El WIP iniciado máximo sería cuatro: dos en desarrollo, uno en revisión y uno en pruebas. Esto busca evitar que todos comiencen tareas nuevas mientras se acumulan pendientes.

“Listo” todavía no cuenta como trabajo iniciado. Su límite controla la cola preparada.

Los límites son una hipótesis inicial. Deben ajustarse con datos de flujo y disponibilidad; no son números universales.

### 6.3. Reglas del tablero

- Revisar las columnas más cercanas a “Terminado” antes de iniciar trabajo.
- Tomar un elemento nuevo únicamente si hay capacidad.
- Marcar bloqueos dentro de su columna.
- Los elementos bloqueados siguen contando como WIP.
- Si una columna alcanza el límite, ayudar a liberar trabajo.
- Dividir elementos demasiado grandes.
- Hacer visibles los cambios de estado.

### 6.4. Métricas de flujo

Para evitar confusiones, el equipo debe definir los puntos de medición.

En este ejemplo:

- Lead time: desde la recepción de la solicitud hasta su terminación.
- Cycle time: desde que empieza Desarrollo hasta Terminado.

| **Métrica**      | **Qué mide**                                              | **Cómo interpretarla**                                             |
| ---------------- | --------------------------------------------------------- | ------------------------------------------------------------------ |
| Lead time        | Tiempo total que espera quien solicita el trabajo.        | Incluye espera antes de comenzar.                                  |
| Cycle time       | Tiempo transcurrido desde el inicio hasta la terminación. | Incluye esperas y bloqueos después de iniciar.                     |
| Throughput       | Elementos terminados por unidad de tiempo.                | Muestra el ritmo de salida, considerando tamaño y tipo de trabajo. |
| Edad del trabajo | Tiempo de un elemento iniciado que sigue abierto.         | Ayuda a detectar elementos que envejecen.                          |
| WIP              | Elementos iniciados y no terminados.                      | Permite controlar la carga simultánea.                             |

**Ejemplo:**

Una solicitud llega el lunes, comienza el miércoles y termina el viernes. Considerando el mismo horario:

- Lead time: cuatro días transcurridos.
- Cycle time: dos días transcurridos.

Debe aclararse si se utilizan días naturales o laborales [9].

### 6.5. Diagrama de flujo acumulado

El diagrama de flujo acumulado muestra cantidades acumuladas de elementos por estado a lo largo del tiempo.

| **Lo observado**                                          | **Interpretación**                               |
| --------------------------------------------------------- | ------------------------------------------------ |
| La banda de Revisión aumenta de grosor.                   | Se acumula trabajo en ese estado.                |
| La frontera de Terminado sube de manera constante.        | Hay una salida sostenida de elementos.           |
| La frontera de Terminado se aplana.                       | Durante ese periodo no se completaron elementos. |
| Aumenta la distancia vertical entre iniciado y terminado. | Aumenta el WIP.                                  |

La separación horizontal entre curvas compatibles puede aproximar tiempos de flujo, pero no sustituye medir el tiempo de cada elemento [4], [11].

### 6.6. Políticas explícitas

Ejemplos propuestos:

- Entrar a Desarrollo exige una necesidad clara y criterios de aceptación.
- Entrar a Revisión exige código integrado en una solicitud de revisión.
- Terminar exige cumplir la calidad acordada.
- Un bloqueo debe registrar causa y siguiente acción.
- Dentro de la clase estándar se toma normalmente el elemento más antiguo.
- Las excepciones se acuerdan y hacen visibles.

### 6.7. Clases de servicio

Las clases de servicio definen cómo tratar trabajo con distintos riesgos de demora [4].

| **Clase**  | **Ejemplo**                            | **Política propuesta**                               |
| ---------- | -------------------------------------- | ---------------------------------------------------- |
| Estándar   | Mejorar un formulario.                 | Atender según orden y capacidad.                     |
| Expedita   | Restablecer un sistema caído.          | Prioridad excepcional y máximo un elemento expedito. |
| Fecha fija | Cambio necesario para una inscripción. | Iniciar con anticipación suficiente.                 |
| Intangible | Mejorar una herramienta interna.       | Reservar capacidad para evitar su abandono.          |

Una urgencia no elimina la capacidad limitada. Acelerar un elemento puede retrasar otros, por lo que la decisión debe explicarse.

### 6.8. Cuándo elegir Kanban

Es útil cuando:

- Llegan tickets continuamente.
- Existen diferentes tipos y tamaños de solicitud.
- Las prioridades cambian con frecuencia.
- Se necesita reducir tiempos de espera.
- Hay dificultades para comprometer un conjunto de tareas durante un Sprint.

Scrum puede resultar más adecuado cuando el equipo puede concentrarse en un objetivo por ciclo. También es posible aplicar prácticas Kanban dentro de Scrum sin eliminar sus elementos.

## 7. Design Thinking

### 7.1. Visión general

Design Thinking busca comprender a las personas y explorar soluciones antes de invertir demasiado en desarrollarlas.

Considera:

- Deseabilidad: que responda a una necesidad.
- Factibilidad: que pueda construirse.
- Viabilidad: que pueda sostenerse.

En software ayuda a cuestionar si una función realmente resuelve el problema del usuario [10].

### 7.2. Fases

Las cinco fases son una forma habitual de explicar el proceso. No son una secuencia rígida: una prueba puede hacer necesario redefinir el problema.

| **Fase**   | **Objetivo**                            | **Técnicas sugeridas**                     | **Entregable mínimo**                   |
| ---------- | --------------------------------------- | ------------------------------------------ | --------------------------------------- |
| Empatizar  | Comprender necesidades y contexto.      | Entrevistas y observación.                 | Registro de necesidades y dificultades. |
| Definir    | Delimitar un problema relevante.        | Agrupar hallazgos y formular una pregunta. | Enunciado del problema.                 |
| Idear      | Explorar alternativas.                  | Lluvia de ideas y bocetos.                 | Opciones y selección razonada.          |
| Prototipar | Hacer tangible una idea con poco costo. | Pantallas en papel o simulación.           | Prototipo evaluable.                    |
| Probar     | Observar su utilidad.                   | Tareas con usuarios.                       | Hallazgos y cambios propuestos.         |

Las herramientas de Stanford d.school permiten practicar estos modos de trabajo [13].

### 7.3. Mini-caso hipotético

**Problema:** estudiantes de ingeniería pierden de vista tareas porque las fechas están repartidas entre mensajes, plataformas y apuntes.

Las actividades siguientes son una propuesta, no resultados de una investigación realizada.

| **Fase**   | **Actividad**                                                                |
| ---------- | ---------------------------------------------------------------------------- |
| Empatizar  | Entrevistar a cinco estudiantes y observar cómo consultan pendientes.        |
| Definir    | Plantear cómo reunir fechas importantes sin aumentar el trabajo de registro. |
| Idear      | Comparar una agenda compartida, un panel semanal y recordatorios.            |
| Prototipar | Crear tres pantallas en papel: semana, nueva tarea y detalle.                |
| Probar     | Pedir que encuentren una entrega, agreguen una tarea y la marquen terminada. |

### 7.4. Prototipo de baja fidelidad

**Pantalla: Mis entregas**

| **Elemento**     | **Contenido**                                   |
| ---------------- | ----------------------------------------------- |
| Encabezado       | Mis entregas de la semana                       |
| Filtro           | Todas las materias / Matemáticas / Programación |
| Tarea 1          | Reporte de sensores — martes                    |
| Tarea 2          | Ejercicios de factorización — jueves            |
| Tarea 3          | Programa en Python — viernes                    |
| Acción principal | Agregar tarea                                   |
| Acción por tarea | Ver detalle / Marcar terminada                  |

**Pantalla: Nueva tarea**

| **Campo**    | **Contenido**       |
| ------------ | ------------------- |
| Materia      | Seleccionar materia |
| Nombre       | Escribir actividad  |
| Fecha y hora | Elegir entrega      |
| Recordatorio | Elegir anticipación |
| Botones      | Guardar / Cancelar  |

**Qué se observaría al probarlo:**

- Si se identifica fácilmente la entrega más cercana.
- Si los nombres de los botones se entienden.
- Si registrar una tarea resulta sencillo.
- Qué información hace falta.

El prototipo busca aprender sobre la interacción; todavía no demuestra que el sistema completo funcione.

### 7.5. Relación con SDLC y Ágil

SDLC significa ciclo de vida del desarrollo de software e incluye actividades como análisis, diseño, construcción, pruebas, entrega y mantenimiento.

Design Thinking puede apoyar el análisis y el diseño, y volver a utilizarse cuando aparecen dudas sobre el producto.

| **Enfoque**     | **Aportación**                                                      |
| --------------- | ------------------------------------------------------------------- |
| Design Thinking | Comprender el problema y validar alternativas.                      |
| Scrum           | Construir incrementos hacia objetivos y revisar resultados.         |
| Kanban          | Gestionar solicitudes y mejorar su flujo.                           |
| SDLC            | Considerar las actividades necesarias durante la vida del software. |

En el mini-caso, el equipo podría validar primero las pantallas y después incorporar al Product Backlog una función para registrar entregas. Con Kanban podría organizar correcciones y mejoras que lleguen continuamente.

Design Thinking reduce el riesgo de construir algo poco útil, pero no lo elimina. La calidad de la evidencia depende de los participantes, las tareas y las pruebas.

## 8. Conclusiones

En mi contexto académico, los enfoques ágiles pueden ayudar a organizar proyectos y evitar que todo el trabajo se acumule al final. Su mayor aportación sería hacer visible el avance y revisar resultados antes de entregar.

Para desarrollar una aplicación en equipo elegiría Scrum si podemos acordar objetivos por periodos. Usaría Kanban para tareas y correcciones que llegan continuamente. Antes de programar una solución nueva, aplicaría Design Thinking para comprender a sus usuarios.

En ingeniería y mecatrónica también pueden ser útiles para organizar programación, pruebas e integración. Sin embargo, el trabajo con componentes físicos exige considerar compras, fabricación y seguridad, porque no todos los cambios tienen el mismo costo.

Considero que lo más importante es seleccionar prácticas según el problema. Un tablero o una reunión no vuelven ágil a un equipo si no existe colaboración, calidad y disposición para aprender.

## 9. Referencias

1. **Autores del Manifiesto Ágil.** *Manifiesto por el Desarrollo Ágil de Software*. 2001.\
   [https://agilemanifesto.org/iso/es/manifesto.html](https://agilemanifesto.org/iso/es/manifesto.html)
2. **Autores del Manifiesto Ágil.** *Principios del Manifiesto Ágil*. 2001.\
   [https://agilemanifesto.org/iso/es/principles.html](https://agilemanifesto.org/iso/es/principles.html)
3. **Schwaber, Ken y Sutherland, Jeff.** *La Guía Scrum*. 2020.\
   [https://scrumguides.org/docs/scrumguide/v2020/2020-Scrum-Guide-Spanish-European.pdf](https://scrumguides.org/docs/scrumguide/v2020/2020-Scrum-Guide-Spanish-European.pdf)
4. **Kanban University.** *The Official Guide to the Kanban Method*. s. f.\
   [https://kanban.university/kanban-guide/](https://kanban.university/kanban-guide/)
5. **Scrum.org.** *The Scrum Artifacts*. s. f.\
   [https://www.scrum.org/resources/scrum-artifacts](https://www.scrum.org/resources/scrum-artifacts)
6. **Scrum.org.** *Definition Of Done (DOD) Explanation and Example*. s. f.\
   [https://www.scrum.org/resources/blog/definition-done-dod-explanation-and-example](https://www.scrum.org/resources/blog/definition-done-dod-explanation-and-example)
7. **Scrum.org.** *Introduction to the Scrum Events*. s. f.\
   [https://www.scrum.org/resources/introduction-scrum-events](https://www.scrum.org/resources/introduction-scrum-events)
8. **Iqbal, Mary. Scrum.org.** *Don't Confuse Velocity with Success*. 2024.\
   [https://www.scrum.org/resources/blog/dont-confuse-velocity-success](https://www.scrum.org/resources/blog/dont-confuse-velocity-success)
9. **Kanban Guides.** *La Guía Kanban*. 2025.\
   [https://kanbanguides.org/es-es/the-kanban-guide/](https://kanbanguides.org/es-es/the-kanban-guide/)
10. **IDEO.** *Design Thinking: Human-Centered Innovation*. s. f.\
    [https://designthinking.ideo.com/](https://designthinking.ideo.com/)
11. **Kanban University.** *The Kanban Method Glossary*. s. f.\
    [https://kanban.university/glossary/](https://kanban.university/glossary/)
12. **Scrum.org.** *What is a Sprint Retrospective?*. s. f.\
    [https://www.scrum.org/resources/what-is-a-sprint-retrospective](https://www.scrum.org/resources/what-is-a-sprint-retrospective)
13. **Stanford University, d.school.** *Tools in Translation*. s. f. Incluye herramientas de Design Thinking traducidas al español.\
    [https://dschool.stanford.edu/tools/tools-in-translation](https://dschool.stanford.edu/tools/tools-in-translation)