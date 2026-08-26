# Integrantes del equipo

Sistema de Gestión Integral — Vitalis Centro de Entrenamiento
Escuela Superior de Comercio N° 49 "Justo José de Urquiza" — Rosario, Santa Fe
Materia: Desarrollo Web — Analista Funcional de Sistemas
Ciclo lectivo: 2026

---

## 1. Datos del equipo

| Campo | Detalle |
|---|---|
| Nombre del grupo | Grupo 02 |
| Cantidad de integrantes | 4 |
| Cliente del proyecto | Vitalis Centro de Entrenamiento — Pueblo Esther, Santa Fe |
| Docente a cargo | Pedernera, Pablo |
| Metodología de trabajo | Ágil, con iteraciones cortas y revisión por pares |
| Organización del equipo | Horizontal, sin jefe de grupo. Las decisiones se toman por consenso. |
| Repositorio | `vitalis-sistema-gestion` |
| Rama principal | `main` |

---

## 2. Integrantes

El equipo trabaja de forma **horizontal**: los cuatro integrantes participan de todas las actividades del análisis —relevamiento, requisitos, historias, casos de uso, modelado y diseño— y ninguno concentra la decisión final sobre el proyecto. Lo que sí se reparte es la **redacción de cada artefacto**, para que el trabajo avance en paralelo y cada documento tenga un responsable claro de su escritura.

| Integrante | Artefactos que redacta | Artefactos que revisa |
|---|---|---|
| **Duran, Berenice** | `docs/requisitos.md`<br>`docs/stakeholders.md`<br>`RECURSOS.md`<br>`cuestionario/` | Los artefactos de Gómez |
| **Gómez, Felipe** | `docs/er-modelo.md`<br>`diagramas/er.puml`<br>`diagramas/casos-de-uso.puml`<br>`DoR.md` | Los artefactos de Rodriguez |
| **Rodriguez, Lautaro** | `docs/casos-de-uso.md`<br>`docs/historias-de-usuario.md`<br>`slicing.md`<br>`integrantes.md` | Los artefactos de Verduna |
| **Verduna, Valentino** | `README.md`<br>`docs/diseño-ui.md`<br>`diagramas/wireframes/` | Los artefactos de Duran |

La revisión rota en círculo, de modo que cada integrante revisa el trabajo de otro y es revisado por un tercero. Ningún documento se integra a `main` sin haber sido leído por alguien que no lo escribió.

---

## 3. Reparto de la carga de trabajo

| Actividad | Duran | Gómez | Rodriguez | Verduna |
|---|:---:|:---:|:---:|:---:|
| Relevamiento y entrevistas | Sí | Sí | Sí | Sí |
| Definición de requisitos | Sí | Sí | Sí | Sí |
| Redacción de historias de usuario | Sí | Sí | Sí | Sí |
| Desarrollo de casos de uso | Sí | Sí | Sí | Sí |
| Modelado de datos | Sí | Sí | Sí | Sí |
| Diagramas UML | Sí | Sí | Sí | Sí |
| Diseño de interfaz y wireframes | Sí | Sí | Sí | Sí |
| Control de consistencia | Sí | Sí | Sí | Sí |
| Documentos redactados | 4 | 4 | 4 | 3 |
| Documentos revisados | 4 | 4 | 3 | 4 |

Todas las actividades se realizan de manera conjunta: se discuten en reunión, se acuerda el criterio y recién después el integrante que tiene asignado el documento lo redacta. La carga de redacción quedó repartida en partes iguales (tres o cuatro documentos por integrante), y la de revisión también.

---

## 4. Forma de trabajo

### Ritmo de trabajo

| Instancia | Frecuencia | Objetivo |
|---|---|---|
| Reunión de planificación | Al inicio de cada iteración | Definir qué documentos se trabajan y repartirlos entre los cuatro. |
| Sincronización rápida | Dos veces por semana (mensajería) | Estado de cada tarea, bloqueos y dudas de interpretación. |
| Revisión de entregable | Al cierre de cada iteración | Revisar el trabajo terminado contra la Definition of Ready. |
| Retrospectiva breve | Al cierre de cada iteración | Qué funcionó, qué no y qué se ajusta para la siguiente. |

En cada iteración un integrante distinto **modera** la reunión y lleva el registro de decisiones. El rol rota siguiendo el orden alfabético del apellido, de manera que a lo largo del cuatrimestre los cuatro cumplen esa función la misma cantidad de veces.

### Flujo de trabajo en el repositorio

1. El integrante que redacta crea una rama a partir de `main` siguiendo la convención `docs/<tema>`, `diagram/<tema>` o `fix/<tema>`.
2. Trabaja sobre esa rama con commits pequeños y descriptivos.
3. Abre un Pull Request hacia `main` describiendo qué cambió y qué documentos se ven afectados.
4. El revisor que le corresponde según la rotación lee el PR y deja sus comentarios.
5. Si el cambio afecta a más de un documento, el PR requiere la aprobación de **dos** integrantes.
6. Una vez aprobado, se hace merge y se elimina la rama.
7. Ningún integrante hace push directo sobre `main`, incluido el autor del documento.

El detalle de los comandos está en [`RECURSOS.md`](RECURSOS.md).

### Criterios de calidad acordados

- Todo requisito debe tener un ID único y estable. Los IDs nunca se reutilizan ni se renumeran.
- Toda historia de usuario debe indicar a qué requisitos responde.
- Todo caso de uso debe indicar a qué historia y a qué requisitos corresponde.
- Toda entidad del modelo debe justificarse por al menos un requisito.
- Si un cambio en un documento obliga a modificar otro, ambos cambios viajan en el mismo Pull Request.
- Antes de cerrar una entrega se revisa la matriz de trazabilidad completa entre los cuatro integrantes.

---

## 5. Canales de comunicación

| Canal | Uso |
|---|---|
| Grupo de mensajería del equipo | Coordinación diaria, dudas rápidas, avisos. |
| Issues de GitHub | Registro de tareas pendientes, inconsistencias detectadas y decisiones a tomar. |
| Pull Requests | Discusión sobre el contenido de cada documento. |
| Reuniones presenciales / videollamada | Planificación, revisión y retrospectiva. |
| Consultas al docente | Dudas de metodología, alcance del trabajo y criterios de evaluación. |

---

## 6. Registro de decisiones del equipo

Las decisiones que afectan a más de un documento se toman en reunión, por consenso de los cuatro integrantes, y se registran acá para mantener la consistencia del repositorio.

| # | Fecha | Decisión | Impacto |
|---|---|---|---|
| D1 | 05/2026 | Los requisitos funcionales se numeran `RF01`…`RFnn` y los no funcionales `RNF01`…`RNFnn`, sin guion intermedio. | Todos los documentos. |
| D2 | 05/2026 | La sede documentada es Pueblo Esther, Santa Fe. La referencia a Rosario corresponde a la institución educativa. | `README.md`, `docs/requisitos.md`. |
| D3 | 05/2026 | Pilates se incorpora a la oferta de disciplinas, ya que la modalidad de cobro combinada la contempla. | `README.md`, `docs/requisitos.md`, `docs/er-modelo.md`. |
| D4 | 05/2026 | Se incorporan los módulos M6 (instructores), M7 (seguridad y roles) y M8 (reportes), con requisitos identificados como adicionales. | `docs/requisitos.md` y derivados. |
| D5 | 05/2026 | El alumno es un actor del sistema con permisos de solo consulta. | `docs/casos-de-uso.md`, `docs/diseño-ui.md`. |
| D6 | 05/2026 | El umbral de morosidad es de 30 días y se define como parámetro configurable por la dirección. | `docs/requisitos.md`, `docs/casos-de-uso.md`. |
| D7 | 05/2026 | El registro de asistencia admite alumnos no inscriptos en la clase (asistente ocasional). | `docs/er-modelo.md`, `diagramas/er.puml`. |
| D8 | 05/2026 | La modalidad de cobro se guarda tanto en el alumno (vigente) como en cada cuota (aplicada), para preservar el histórico ante cambios de precio. | `docs/er-modelo.md`, `diagramas/er.puml`. |
| D9 | 05/2026 | El equipo trabaja de forma horizontal: no hay jefe de grupo y toda decisión de alcance o modelado se toma por consenso. | `integrantes.md`, `DoR.md`. |
| D10 | 05/2026 | El acceso al módulo nutricional se separa en dos planos: el contenido clínico es exclusivo de la nutricionista (RF21) y la administración del módulo corresponde al Administrador, sin ver consultas (RNF06). Resuelve el punto abierto A2. | `docs/requisitos.md`, `docs/casos-de-uso.md`, `docs/diseño-ui.md`. |
| D11 | 05/2026 | La consulta nutricional registra peso, altura, perímetro de cintura, perímetro de cadera, porcentaje de masa grasa, objetivo y observaciones, con IMC calculado. Reemplaza el campo genérico `medidas`. Resuelve A1. | `docs/requisitos.md`, `docs/er-modelo.md`, `diagramas/er.puml`, `docs/diseño-ui.md`. |
| D12 | 05/2026 | La modalidad de cobro por clase no genera morosidad, porque el pago es anticipado. Estos alumnos se clasifican como inactivos tras 60 días sin pagos ni asistencias. Resuelve A3. | `docs/requisitos.md`, `docs/casos-de-uso.md`. |
| D13 | 05/2026 | El rol Alumno no accede a su historial nutricional en la versión 1.0. La devolución se realiza en consultorio. Resuelve A4. | `docs/requisitos.md`, `docs/diseño-ui.md`. |
| D14 | 05/2026 | Para registrar como paciente nutricional a un alumno menor de 18 años, el sistema exige el tutor responsable y la fecha de autorización. Resuelve A5. | `docs/requisitos.md`, `docs/er-modelo.md`, `docs/casos-de-uso.md`. |
| D15 | 05/2026 | La arquitectura prevista es Web App, back-end y PostgreSQL, con **n8n** como motor de automatización e integración. n8n no contiene lógica de negocio ni reemplaza al back-end: ejecuta procesos periódicos y distribuye resultados. Ningún requisito funcional depende de él. | `README.md`, `RECURSOS.md`, `docs/requisitos.md` (RE11), `docs/diseño-ui.md`. |

Toda decisión nueva se agrega a esta tabla mediante un Pull Request que también actualice los documentos afectados.

---

<sub>Escuela Superior de Comercio N° 49 "Justo José de Urquiza" — Desarrollo Web / Analista Funcional de Sistemas — 2026.</sub>
