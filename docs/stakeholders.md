# Análisis de stakeholders

Sistema de Gestión Integral — Vitalis Centro de Entrenamiento
Equipo: Grupo 02
Versión: 1.1

---

## Índice

- [1. Qué es un stakeholder en este proyecto](#1-qué-es-un-stakeholder-en-este-proyecto)
- [2. Identificación](#2-identificación)
- [3. Matriz de impacto e interés](#3-matriz-de-impacto-e-interés)
- [4. Fichas de stakeholders](#4-fichas-de-stakeholders)
- [5. Matriz de participación](#5-matriz-de-participación)
- [6. Mapa de intereses en conflicto](#6-mapa-de-intereses-en-conflicto)
- [7. Estrategia de comunicación](#7-estrategia-de-comunicación)
- [8. Riesgos vinculados a los stakeholders](#8-riesgos-vinculados-a-los-stakeholders)
- [9. Trazabilidad con el resto del análisis](#9-trazabilidad-con-el-resto-del-análisis)

---

## 1. Qué es un stakeholder en este proyecto

Un stakeholder es toda persona o grupo que **afecta o resulta afectado** por el sistema. No se limita a quienes lo van a usar: incluye a quienes deciden sobre él y a quienes dependen de sus resultados sin tocarlo nunca.

Esa distinción importa en Vitalis. Los familiares de alumnos menores, por ejemplo, no tienen usuario en la versión 1.0, pero sus necesidades condicionan qué datos se registran en el alta y cómo se comunica la información de las clases infantiles.

### Clasificación utilizada

| Tipo | Definición | Stakeholders |
|---|---|---|
| Interno decisor | Define el negocio y valida el sistema. | Propietaria y directora. |
| Interno usuario operativo | Opera el sistema en el día a día. | Recepcionista, instructores, nutricionista. |
| Externo beneficiario | Recibe el servicio. Puede o no usar el sistema. | Alumnos. |
| Externo representante | Actúa en nombre de un beneficiario. | Familiares y tutores de alumnos menores. |

---

## 2. Identificación

| # | Stakeholder | Tipo | Rol en el sistema | Impacto | Interés | Prioridad de atención |
|---|---|---|---|---|---|---|
| S1 | Propietaria y directora | Interno decisor | Administrador | Alto | Alto | Máxima |
| S2 | Recepcionista y personal administrativo | Interno usuario operativo | Recepcionista | Alto | Alto | Máxima |
| S3 | Instructores y profesores | Interno usuario operativo | Instructor | Alto | Medio | Alta |
| S4 | Nutricionista | Interno usuario operativo | Nutricionista | Medio | Alto | Alta |
| S5 | Alumnos | Externo beneficiario | Alumno, solo consulta | Alto | Medio | Alta |
| S6 | Familiares y tutores de alumnos menores | Externo representante | Sin acceso en v1.0 | Medio | Medio | Media |

Los seis stakeholders provienen del relevamiento inicial. No se incorporaron partes interesadas nuevas: el análisis posterior confirmó que el mapa estaba completo.

---

## 3. Matriz de impacto e interés

La matriz clasifica a cada stakeholder según cuánto lo afecta el sistema y cuánto le interesa su resultado. De esa posición se deriva la estrategia de trabajo con cada uno.

```text
        ALTO  │                                    │
              │        S5 Alumnos                  │   S1 Directora
              │        S3 Instructores             │   S2 Recepcionista
     I        │                                    │
     M        │  Mantener informados               │   Involucrar de cerca
     P        │  y atender sus necesidades         │   en todas las decisiones
     A        │                                    │
     C   ─────┼────────────────────────────────────┼─────────────────────────
     T        │                                    │
     O        │        (sin stakeholders)          │   S4 Nutricionista
              │                                    │   S6 Familiares y tutores
        BAJO  │  Monitorear                        │   Consultar en su ámbito
              │                                    │   específico
              └────────────────────────────────────┴─────────────────────────
                        BAJO           INTERÉS            ALTO
```

### Lectura de la matriz

| Cuadrante | Stakeholders | Estrategia |
|---|---|---|
| Alto impacto, alto interés | S1, S2 | Participan de todas las decisiones. Validan cada entrega. Nada se define sin su acuerdo. |
| Alto impacto, interés medio | S3, S5 | Se los consulta sobre las funcionalidades que los afectan y se los mantiene informados del avance. |
| Impacto medio, alto interés | S4, S6 | Se los consulta específicamente sobre su ámbito. La nutricionista sobre el módulo M5; los tutores sobre la comunicación de las clases infantiles. |

**Observación del equipo.** Un error habitual sería ubicar a los instructores en el cuadrante de bajo impacto por no ser quienes deciden. Es al revés: si la pantalla de asistencia no les sirve, el módulo M4 no se usa y el sistema pierde una de sus funciones centrales. Su impacto sobre el éxito del proyecto es alto aunque su poder de decisión sea bajo.

---

## 4. Fichas de stakeholders

### S1 — Propietaria y directora

| Campo | Detalle |
|---|---|
| Tipo | Interno decisor |
| Rol en el sistema | Administrador |
| Nivel de impacto | Alto |
| Nivel de interés | Alto |
| Cantidad de personas | 1 |
| Frecuencia de uso prevista | Semanal, con picos a fin de mes. |

**Descripción**

Es la responsable máxima del negocio. Define precios, modalidades de cobro, disciplinas ofrecidas y estructura de personal. Toma las decisiones estratégicas sobre el funcionamiento del centro.

**Por qué es clave**

Es la comitente principal del sistema y la fuente primaria de requisitos de negocio. Cualquier decisión sobre tarifas, modalidades de pago, altas de disciplinas o cambios en la estructura de clases impacta directamente en las reglas del sistema. Sin su validación, ningún artefacto del proyecto puede considerarse correcto. Además, es quien necesita los reportes de ingresos y morosidad para la toma de decisiones.

**Necesidades**

| # | Necesidad | Requisitos que la atienden |
|---|---|---|
| N1 | Conocer quién debe dinero y cuánto, sin revisar la planilla fila por fila. | RF08, RF09 |
| N2 | Poder actualizar precios y modalidades sin depender del equipo técnico. | RF07, RF30 |
| N3 | Saber qué actividades sostienen el negocio y cuáles no. | RF28, RF29 |
| N4 | Reorganizar la grilla por temporada sin perder la planificación anterior. | RF13 |
| N5 | Controlar quién accede a qué información dentro del centro. | RF23, RNF03 |
| N6 | Conservar el historial de alumnos que se dan de baja y vuelven. | RF04, RF05 |

**Expectativas**

- Que el sistema le muestre el estado del negocio de un vistazo, sin tener que armar consultas.
- Que la información sea confiable: si el reporte dice que hay veinte morosos, que sean veinte.
- Que el personal lo adopte sin resistencia y sin necesidad de capacitación extensa.
- Que el sistema pueda crecer si el centro incorpora nuevas actividades o una segunda sede.

**Información que necesita**

| Información | Dónde la obtiene |
|---|---|
| Cantidad de alumnos activos y su evolución. | Dashboard, P02 |
| Alumnos morosos, días de mora y monto adeudado. | Reporte de morosos, P08 |
| Ingresos por período, modalidad y disciplina. | Reporte de ingresos, P16 |
| Ocupación y asistencia promedio de cada clase. | Reporte de ocupación, P16 |
| Alumnos inactivos con riesgo de baja. | Reporte de ocupación, P16 |
| Registro de operaciones sensibles. | Log de auditoría, P17 |

**Funcionalidades que utiliza**

Acceso completo al sistema, con excepción del contenido clínico del módulo nutricional. Pantallas: P02, P03, P04, P05, P06, P07, P08, P09, P10, P11, P12, P13, P16, P17, P18.

**Riesgos y problemas asociados**

| Riesgo | Probabilidad | Impacto | Mitigación |
|---|---|---|---|
| Cambia una regla de negocio sin avisar al equipo, y el sistema queda desactualizado. | Alta | Alto | Parametrizar todo valor de negocio: montos, umbrales de mora e inactividad (RF30, ParametroSistema). |
| Concentra todas las decisiones y su disponibilidad es limitada. | Media | Alto | Registrar cada decisión en la tabla de `integrantes.md`. Agrupar las consultas en instancias de validación programadas. |
| Espera funcionalidades que están fuera del alcance acordado, como facturación electrónica. | Media | Medio | El apartado de fuera de alcance de `docs/requisitos.md` es explícito y fue validado con ella. |
| Reclama acceso al módulo nutricional. | Baja | Medio | La decisión D10 separa administración de contenido clínico. Le da control del módulo sin exponer datos de salud. |

---

### S2 — Recepcionista y personal administrativo

| Campo | Detalle |
|---|---|
| Tipo | Interno usuario operativo |
| Rol en el sistema | Recepcionista |
| Nivel de impacto | Alto |
| Nivel de interés | Alto |
| Cantidad de personas | 2, en turnos mañana y tarde-noche. |
| Frecuencia de uso prevista | Permanente durante toda la jornada. |

**Descripción**

Es el actor que opera el sistema en el día a día: registra altas y bajas de alumnos, cobra cuotas, gestiona inscripciones a clases y resuelve consultas de los socios.

**Por qué es clave**

Es el usuario más frecuente del sistema y quien actualmente sostiene la operación mediante las planillas de Excel. El sistema debe adaptarse a su flujo de trabajo real para no generar fricción en la transición. Si la interfaz no es clara y eficiente para este actor, la adopción del sistema fracasa independientemente de su calidad técnica.

**Necesidades**

| # | Necesidad | Requisitos que la atienden |
|---|---|---|
| N1 | Encontrar a un alumno en segundos, mientras está esperando en el mostrador. | RF24 |
| N2 | Cobrar una cuota con la menor cantidad de pasos posible. | RF06, RNF08 |
| N3 | Responder al instante si un alumno está al día. | RF10 |
| N4 | Cargar un alumno sin equivocarse ni duplicar registros. | RF01, RF02 |
| N5 | Inscribir alumnos a clases sabiendo qué horarios existen. | RF14 |
| N6 | Que el sistema no le agregue trabajo respecto de la planilla. | RNF07, RNF08, RNF09 |

**Expectativas**

- Que cobrar una cuota sea más rápido que abrir Excel y buscar la fila.
- Que los mensajes de error le digan qué hacer, no un código.
- Que el sistema no se cuelgue en el horario de mayor movimiento.
- Que pueda corregir un error de carga sin depender de nadie.

**Información que necesita**

| Información | Dónde la obtiene |
|---|---|
| Padrón de alumnos con búsqueda inmediata. | P03 |
| Situación de cuenta de cada alumno. | P03, P05, P07 |
| Monto que corresponde cobrar según la modalidad. | P06 |
| Clases disponibles en la grilla activa. | P10 |
| Historial de pagos e inscripciones. | P07, P05 |

**Funcionalidades que utiliza**

Gestión de alumnos completa, registro de pagos, historial, inscripciones y consulta de la grilla. Pantallas: P02, P03, P04, P05, P06, P07, P08 en modo consulta, P09 en modo consulta, P10.

**Riesgos y problemas asociados**

| Riesgo | Probabilidad | Impacto | Mitigación |
|---|---|---|---|
| Resistencia al cambio: la planilla es conocida y el sistema no. | Alta | Muy alto | El sistema debe ser más rápido que Excel en las operaciones frecuentes. RNF08 fija el máximo de cuatro pasos para un cobro. |
| Falta de formación técnica del personal. | Alta | Alto | RNF09 exige mensajes sin tecnicismos. La restricción RE02 condiciona todo el diseño de interfaz. |
| Convivencia temporal entre el sistema y la planilla, con datos duplicados. | Media | Alto | La restricción RE01 impone una migración gradual. El slicing entrega el padrón completo en la iteración 1 para acortar la convivencia. |
| Errores de carga en el período inicial. | Media | Medio | Validación de DNI duplicado desde el slice S1.2, antes de migrar datos reales. |
| Rotación del personal administrativo. | Baja | Medio | El sistema debe ser aprendible sin capacitación formal extensa. |

---

### S3 — Instructores y profesores

| Campo | Detalle |
|---|---|
| Tipo | Interno usuario operativo |
| Rol en el sistema | Instructor |
| Nivel de impacto | Alto |
| Nivel de interés | Medio |
| Cantidad de personas | Alrededor de 10. |
| Frecuencia de uso prevista | Diaria, breve, al inicio y al final de cada clase. |

**Descripción**

Son los profesionales que dictan las clases. Cada instructor tiene asignados ciertos horarios y disciplinas, y es responsable del seguimiento de sus alumnos durante las sesiones.

**Por qué es clave**

Representan el eslabón operativo de la prestación del servicio. El sistema debe ofrecerles una vista específica de sus clases del día, el listado de alumnos inscriptos y la posibilidad de registrar asistencia. Si este actor no dispone de una interfaz adecuada, el control de asistencia continuará siendo informal o inexistente.

**Necesidades**

| # | Necesidad | Requisitos que la atienden |
|---|---|---|
| N1 | Saber qué clases tiene asignadas sin preguntar en recepción. | RF26 |
| N2 | Ver quiénes están inscriptos en la clase que va a dictar. | RF15 |
| N3 | Registrar la asistencia rápido, desde el salón. | RF16, RF17, RNF07 |
| N4 | Registrar al alumno que se presentó sin estar inscripto. | RF27 |
| N5 | Enterarse cuando cambia la grilla y sus horarios se modifican. | RF13, RF26 |

**Expectativas**

- Que tomar asistencia lleve menos tiempo que pasar lista en papel.
- Que la aplicación funcione en la tablet del salón, con la conectividad que hay.
- Que no le pidan datos que no tiene ni le corresponden.
- Que su agenda esté actualizada cuando la dirección reorganiza la grilla.

**Información que necesita**

| Información | Dónde la obtiene |
|---|---|
| Sus clases de la semana con día, horario y disciplina. | P12 |
| Sus clases del día en curso. | P02, P12 |
| Listado de alumnos inscriptos por clase. | P13 |
| Si ya registró la asistencia de una clase. | P12 |

**Funcionalidades que utiliza**

Agenda propia, control de asistencia y registro de asistentes ocasionales. Consulta limitada del padrón. Pantallas: P02, P03 en modo consulta, P12, P13.

**Riesgos y problemas asociados**

| Riesgo | Probabilidad | Impacto | Mitigación |
|---|---|---|---|
| La conectividad wifi del salón es inestable y se pierde el registro. | Alta | Alto | Confirmación única para toda la clase en lugar de guardado por alumno. Los datos se conservan en pantalla ante una falla (P13, E4). |
| El instructor no adopta la herramienta y sigue usando papel. | Media | Muy alto | La toma de asistencia se diseñó para tablet, con botones grandes y marcado masivo. Si es más lenta que el papel, no se usa. |
| Niveles heterogéneos de alfabetización digital en el plantel. | Media | Medio | La agenda es la pantalla de entrada y lleva a la asistencia con un solo toque. |
| Un instructor accede a datos de clases que no le corresponden. | Baja | Alto | RNF03 y el slice S6.3 bloquean el acceso incluso por dirección directa, y registran el intento. |
| Reemplazos entre profesores no previstos en el modelo. | Media | Bajo | Las especialidades son informativas y no restringen la asignación a clases (CU-15). |

---

### S4 — Nutricionista

| Campo | Detalle |
|---|---|
| Tipo | Interno usuario operativo |
| Rol en el sistema | Nutricionista |
| Nivel de impacto | Medio |
| Nivel de interés | Alto |
| Cantidad de personas | 1 |
| Frecuencia de uso prevista | Semanal, los martes de 15:00 a 18:00. |

**Descripción**

Profesional que atiende a alumnos del gimnasio en un horario fijo. Lleva un seguimiento de peso, medidas y objetivos de cada paciente.

**Por qué es clave**

Representa un módulo diferenciado dentro del sistema: sus datos son de carácter sensible y su interfaz debe ser independiente de la gestión de cuotas y clases. Su incorporación al sistema es una oportunidad para eliminar el uso de registros físicos y garantizar la confidencialidad del historial de cada alumno.

**Necesidades**

| # | Necesidad | Requisitos que la atienden |
|---|---|---|
| N1 | Registrar cada consulta sin usar fichas de papel. | RF19 |
| N2 | Comparar la evolución del paciente entre consultas. | RF20 |
| N3 | Que nadie más acceda a la información clínica de sus pacientes. | RF21, RNF06 |
| N4 | Que el sistema calcule solo lo que hoy calcula a mano. | RN26, IMC derivado |
| N5 | Que un error de tipeo no distorsione la curva de evolución. | HU-05a, criterio 9 |

**Expectativas**

- Que el módulo sea suyo y no una sección más del sistema administrativo.
- Que la información de salud esté protegida y ella pueda garantizarlo a sus pacientes.
- Que cargar una consulta no le lleve más tiempo que completar la ficha de papel.
- Que pueda ver de un vistazo si el paciente progresó desde la consulta anterior.

**Información que necesita**

| Información | Dónde la obtiene |
|---|---|
| Listado de sus pacientes con fecha de última consulta. | P14 |
| Valores de la consulta anterior como referencia. | P14 |
| Historial completo con variaciones entre consultas. | P15 |
| Datos del tutor, si el paciente es menor. | P14 |

**Funcionalidades que utiliza**

Exclusivamente el módulo M5. Pantallas: P02, P14, P15. No accede a pagos, grilla, padrón general ni reportes.

**Riesgos y problemas asociados**

| Riesgo | Probabilidad | Impacto | Mitigación |
|---|---|---|---|
| Exposición de datos de salud a roles no autorizados. | Baja | Muy alto | RNF06 y la regla RN29 aíslan el módulo. El slice S6.3 bloquea el acceso por dirección directa y registra el intento. |
| Los parámetros definidos no coinciden con lo que registra en la práctica. | Media | Medio | La regla RN26 se definió a partir de su consulta directa. El punto abierto A1 se resolvió con la decisión D11. |
| Falta de consentimiento documentado para pacientes menores. | Media | Alto | La regla RN27 exige tutor y fecha de autorización antes de la primera consulta. |
| Uso esporádico del sistema, con olvido de la operatoria entre semanas. | Media | Bajo | El módulo tiene solo dos pantallas y un flujo lineal. |
| Reclamo de los pacientes por no poder ver su historial. | Media | Bajo | La decisión D13 lo deja fuera de la versión 1.0. La cuestión diferida B1 lo registra para una versión posterior. |

---

### S5 — Alumnos

| Campo | Detalle |
|---|---|
| Tipo | Externo beneficiario |
| Rol en el sistema | Alumno, con permisos de solo consulta |
| Nivel de impacto | Alto |
| Nivel de interés | Medio |
| Cantidad de personas | Más de 200 registrados. |
| Frecuencia de uso prevista | Esporádica, concentrada en fin de mes. |

**Descripción**

Son las personas que se inscriben, abonan cuotas y asisten a las clases del centro. Su perfil es variado: desde adultos mayores hasta niños, con diferentes modalidades de participación.

**Por qué es clave**

Son el usuario final del servicio y los destinatarios indirectos del valor que genera el sistema. Aunque en una primera versión el acceso del alumno es limitado, sus necesidades determinan los requisitos más críticos: claridad en el estado de su cuenta, acceso a información de clases y comunicación oportuna sobre vencimientos.

**Necesidades**

| # | Necesidad | Requisitos que la atienden |
|---|---|---|
| N1 | Saber si está al día sin preguntar en recepción. | RF10 |
| N2 | Consultar los horarios de sus clases. | RF13, RF14 |
| N3 | Ver su historial de asistencia. | RF18 |
| N4 | Que su historial se conserve si se da de baja y vuelve. | RF04, RF05 |
| N5 | Que sus datos personales estén protegidos. | RNF03, RNF04 |

**Expectativas**

- Que no le cobren de más ni le reclamen una cuota que ya pagó.
- Que si vuelve después de unos meses, no tenga que registrarse de cero.
- Que la información de horarios esté actualizada cuando cambia la grilla.
- Que sus datos de salud, si es paciente del consultorio, no circulen por el mostrador.

**Información que necesita**

| Información | Dónde la obtiene |
|---|---|
| Estado de cuenta y monto adeudado. | P19 |
| Historial de pagos propio. | P19, P07 |
| Clases en las que está inscripto, con horario e instructor. | P19 |
| Asistencias propias. | P19 |

**Funcionalidades que utiliza**

Consulta de su propia información. Pantallas: P01, P19 y P07 limitado a sus registros. No modifica ningún dato salvo su contraseña.

**Riesgos y problemas asociados**

| Riesgo | Probabilidad | Impacto | Mitigación |
|---|---|---|---|
| Un alumno accede a información de otro. | Baja | Muy alto | El rol Alumno solo consulta sus propios registros. RNF03 lo verifica en el servidor, no solo en la interfaz. |
| Reclamo por un pago registrado incorrectamente. | Media | Medio | El historial de pagos indica quién registró cada cuota (RNF05). |
| El alumno reactivado pierde su antigüedad o su historial. | Baja | Alto | La regla RN04 conserva el legajo original. La decisión de baja lógica preserva todo el historial. |
| Baja adopción del portal por parte de los alumnos. | Alta | Bajo | El portal es un complemento, no un canal obligatorio. La recepción sigue respondiendo las consultas. |
| Alumnos sin acceso a internet o sin dispositivo. | Media | Bajo | Ninguna funcionalidad crítica depende del acceso del alumno. |

---

### S6 — Familiares y tutores de alumnos menores

| Campo | Detalle |
|---|---|
| Tipo | Externo representante |
| Rol en el sistema | Sin acceso directo en la versión 1.0 |
| Nivel de impacto | Medio |
| Nivel de interés | Medio |
| Cantidad de personas | Estimada en 30 a 40, correspondientes a las disciplinas infantiles. |
| Frecuencia de uso prevista | No aplica. Se relacionan a través de la recepción. |

**Descripción**

Padres o tutores que inscriben y abonan las cuotas de menores que participan en disciplinas como Kids Fit and Fun o Aeróbica Infantil. Son quienes autorizan la participación y gestionan los trámites administrativos en nombre del alumno.

**Por qué es clave**

Tienen necesidades específicas en cuanto a información: quieren saber los horarios de las clases de sus hijos, confirmar el estado de pago y recibir avisos de cambios o ausencias de docentes. Su consideración es importante para diseñar una comunicación adecuada desde el sistema.

**Necesidades**

| # | Necesidad | Requisitos que la atienden |
|---|---|---|
| N1 | Que el centro tenga sus datos de contacto para una emergencia. | RF01, RN05 |
| N2 | Confirmar el estado de pago de la cuota de su hijo. | RF10, a través de recepción |
| N3 | Conocer los horarios de las clases infantiles. | RF11, RF13, a través de recepción |
| N4 | Autorizar de forma documentada el seguimiento nutricional del menor. | RN27 |
| N5 | Enterarse si se suspende una clase o cambia el profesor. | Fuera de alcance en v1.0 |

**Expectativas**

- Que el centro sepa a quién llamar si su hijo se descompone durante una clase.
- Que no le pidan los mismos datos cada vez que inscribe a otro hijo.
- Que el consentimiento para el seguimiento nutricional quede registrado.
- Que le avisen con tiempo si se modifica el horario de la clase.

**Información que necesita**

| Información | Cómo la obtiene |
|---|---|
| Horario y días de la clase del menor. | A través de recepción. |
| Estado de cuenta del menor. | A través de recepción. |
| Confirmación de que la autorización nutricional está registrada. | A través de recepción. |
| Avisos de cambios de grilla. | Fuera de alcance en la versión 1.0. |

**Funcionalidades que utiliza**

Ninguna de forma directa. Sus datos se registran en la entidad `Tutor` durante el alta del alumno menor (P04) y condicionan el acceso al módulo nutricional (P14).

**Riesgos y problemas asociados**

| Riesgo | Probabilidad | Impacto | Mitigación |
|---|---|---|---|
| El centro no tiene un contacto válido ante una emergencia con un menor. | Media | Muy alto | El teléfono del tutor es obligatorio para todo alumno menor de 18 años (RN05, P04). |
| Datos de tutor duplicados cuando hay hermanos inscriptos. | Media | Bajo | `Tutor` es una entidad separada con relación de uno a muchos hacia `Alumno`. |
| Reclamo por falta de aviso ante un cambio de grilla. | Media | Medio | La comunicación masiva está fuera de alcance en v1.0. El sistema registra las inscripciones afectadas para que recepción contacte a cada familia (CU-10, E1). |
| Registro de datos de salud de un menor sin autorización documentada. | Baja | Muy alto | La regla RN27 bloquea la primera consulta nutricional sin tutor y fecha de autorización. |
| Expectativa de un portal para tutores que no está previsto. | Media | Bajo | Queda registrado como posible evolución. El alcance de la v1.0 fue validado con la dirección. |

---

## 5. Matriz de participación

Grado de participación de cada stakeholder en las actividades del proyecto.

Referencias: **D** decide, **V** valida, **C** es consultado, **I** es informado, **N** no participa.

| Actividad | S1 Directora | S2 Recepcionista | S3 Instructores | S4 Nutricionista | S5 Alumnos | S6 Tutores |
|---|:---:|:---:|:---:|:---:|:---:|:---:|
| Definición del alcance | D | C | I | C | N | N |
| Requisitos funcionales | D | C | C | C | N | N |
| Reglas de negocio de cobro | D | C | N | N | I | I |
| Reglas del módulo nutricional | V | N | N | D | I | C |
| Diseño de la pantalla de cobro | V | D | N | N | N | N |
| Diseño de la toma de asistencia | V | I | D | N | N | N |
| Modelo de datos | V | C | C | C | N | N |
| Prioridad del backlog | D | C | C | C | N | N |
| Validación de cada entrega | D | V | V | V | I | I |
| Definición de parámetros del sistema | D | C | N | N | N | N |

### Lectura de la matriz

La directora decide sobre alcance, requisitos y prioridades, pero **no** sobre el diseño de las pantallas operativas. La recepcionista decide cómo debe funcionar la pantalla de cobro y el instructor cómo debe funcionar la toma de asistencia, porque son quienes las van a usar todos los días. La directora valida, no impone.

Esta distribución responde a una lección del relevamiento: la mayor causa de fracaso en la adopción de un sistema administrativo no es técnica, sino que el usuario operativo encuentre que la herramienta le complica el trabajo que antes hacía de otra forma.

---

## 6. Mapa de intereses en conflicto

Los stakeholders no quieren todos lo mismo. Estos son los conflictos identificados y cómo se resolvieron.

| # | Conflicto | Posiciones | Resolución adoptada |
|---|---|---|---|
| CF1 | Acceso al módulo nutricional. | La directora necesita administrar el módulo y garantizar el resguardo de los datos. La nutricionista necesita que nadie vea el contenido clínico. | Separación en dos planos: administración para el Administrador, contenido clínico para la Nutricionista (decisión D10, regla RN29). |
| CF2 | Nivel de detalle en el alta de alumnos. | La directora quiere registrar la mayor cantidad de datos posible. La recepcionista necesita que el alta sea rápida en el mostrador. | Solo cuatro campos obligatorios en el alta. El resto es opcional y se completa después desde la ficha (P04). |
| CF3 | Bloqueo de la baja de alumnos con deuda. | La directora prefiere que no se pueda dar de baja a quien debe dinero. La recepcionista necesita registrar la realidad: el alumno dejó de venir. | El sistema advierte la deuda pero permite la baja. El dato queda registrado y la deuda no se pierde (CU-05, A1). |
| CF4 | Superposición horaria en las inscripciones. | La dirección quiere control sobre la grilla. Los alumnos se anotan en dos clases del mismo horario para elegir según el día. | El sistema advierte pero no bloquea (CU-11, A2). |
| CF5 | Acceso del alumno a su historial nutricional. | Los alumnos y tutores querrían consultarlo. La nutricionista prefiere entregar los resultados con su interpretación. | Fuera de alcance en v1.0. La devolución se hace en consultorio (decisión D13, regla RN28). |
| CF6 | Comunicación de cambios de grilla. | Los tutores esperan aviso anticipado. La comunicación masiva está fuera de alcance. | El sistema identifica las inscripciones afectadas para que recepción contacte a cada familia (CU-10, E1). |

**Observación del equipo.** Ninguno de estos conflictos es técnico. Todos se resolvieron definiendo con precisión quién necesita qué y para qué. Documentarlos evita que se vuelvan a discutir en cada iteración.

---

## 7. Estrategia de comunicación

| Stakeholder | Qué se le comunica | Con qué frecuencia | Formato |
|---|---|---|---|
| S1 Directora | Avance del proyecto, decisiones pendientes, cambios de alcance. | Al cierre de cada iteración. | Reunión de revisión con demostración de lo entregado. |
| S2 Recepcionista | Funcionalidades que se van habilitando y cambios en su operatoria. | Al cierre de cada iteración. | Demostración práctica sobre el sistema. |
| S3 Instructores | Habilitación de la agenda y de la toma de asistencia. | Al momento de la puesta en marcha del módulo M4. | Instructivo breve y prueba acompañada en el salón. |
| S4 Nutricionista | Habilitación del módulo M5 y confirmación de los parámetros. | Antes del inicio del módulo y al entregarlo. | Reunión específica sobre el módulo. |
| S5 Alumnos | Disponibilidad del portal de consulta. | Al liberar el portal. | Aviso en recepción y cartelería en el centro. |
| S6 Tutores | Registro obligatorio de datos de contacto y autorización nutricional. | Al inscribir a un menor. | Comunicación de recepción en el momento del alta. |

### Instancias de validación previstas

| Instancia | Participantes | Objetivo |
|---|---|---|
| Validación de requisitos | S1, S2 | Confirmar que los RF y las reglas de negocio reflejan la operación real. |
| Validación de la pantalla de cobro | S2 | Verificar que el flujo no supera los cuatro pasos y es más rápido que la planilla. |
| Validación de la toma de asistencia | S3 | Probar la pantalla en la tablet del salón, en condiciones reales de uso. |
| Validación del módulo nutricional | S4 | Confirmar los parámetros de la consulta y el aislamiento de los datos. |
| Validación de reportes | S1 | Verificar que la información responde a las decisiones que necesita tomar. |

---

## 8. Riesgos vinculados a los stakeholders

Consolidación de los riesgos identificados en las fichas, ordenados por criticidad.

| # | Riesgo | Stakeholder | Probabilidad | Impacto | Criticidad | Mitigación |
|---|---|---|---|---|---|---|
| R1 | La recepcionista rechaza el sistema porque le complica el trabajo respecto de Excel. | S2 | Alta | Muy alto | Crítica | RNF08 fija el máximo de pasos. La recepcionista decide el diseño de la pantalla de cobro. |
| R2 | Los instructores siguen tomando asistencia en papel. | S3 | Media | Muy alto | Alta | Diseño para tablet con marcado masivo. Validación en el salón antes de liberar el módulo. |
| R3 | Exposición de datos de salud a roles no autorizados. | S4, S5 | Baja | Muy alto | Alta | RNF06, regla RN29 y bloqueo efectivo por dirección directa (S6.3). |
| R4 | El centro no tiene contacto válido ante una emergencia con un menor. | S6 | Media | Muy alto | Alta | Teléfono del tutor obligatorio para todo alumno menor (RN05). |
| R5 | La dirección cambia reglas de negocio sin avisar. | S1 | Alta | Alto | Alta | Parametrización de montos y umbrales (RF30, ParametroSistema). |
| R6 | Pérdida del registro de asistencia por conectividad inestable. | S3 | Alta | Alto | Alta | Confirmación única por clase y conservación de los datos en pantalla ante fallas. |
| R7 | Convivencia prolongada entre sistema y planilla, con datos duplicados. | S2 | Media | Alto | Media | Migración gradual con el padrón completo en la iteración 1 (RE01, `slicing.md`). |
| R8 | Expectativas fuera del alcance acordado. | S1, S6 | Media | Medio | Media | Apartado de fuera de alcance explícito y validado en `docs/requisitos.md`. |
| R9 | Los parámetros del módulo nutricional no coinciden con la práctica real. | S4 | Media | Medio | Media | Definidos por consulta directa. Punto abierto A1 resuelto con la decisión D11. |
| R10 | Baja adopción del portal por parte de los alumnos. | S5 | Alta | Bajo | Baja | El portal es complementario. Ninguna función crítica depende de él. |

---

## 9. Trazabilidad con el resto del análisis

| Stakeholder | Rol del sistema | Historias que lo tienen como protagonista | Casos de uso | Pantallas |
|---|---|---|---|---|
| S1 Directora | Administrador | HU-03, HU-11, HU-12, HU-13, HU-14, HU-18, HU-21, HU-22, HU-23 | CU-03, CU-07, CU-08, CU-09, CU-10, CU-15, CU-16 | P08, P09, P11, P16, P17, P18 |
| S2 Recepcionista | Recepcionista | HU-01, HU-02, HU-06, HU-07, HU-08, HU-09, HU-10, HU-15, HU-16 | CU-01, CU-02, CU-04, CU-05, CU-06, CU-11 | P03, P04, P05, P06, P07, P10 |
| S3 Instructores | Instructor | HU-04, HU-17, HU-19 | CU-12 | P12, P13 |
| S4 Nutricionista | Nutricionista | HU-05a, HU-05b | CU-13, CU-14 | P14, P15 |
| S5 Alumnos | Alumno | HU-10, HU-16 en modo consulta | — | P19 |
| S6 Tutores | Sin acceso | Presente como dato en HU-01 y HU-05a | CU-01, CU-13 | P04 como dato |

### Verificación

| Control | Resultado |
|---|---|
| Stakeholders identificados | 6 de 6 del relevamiento inicial. |
| Stakeholders con ficha completa | 6 de 6. |
| Stakeholders con necesidades vinculadas a requisitos | 6 de 6. |
| Stakeholders con riesgos identificados y mitigación | 6 de 6. |
| Roles del sistema sin stakeholder asociado | Ninguno. |
| Conflictos de interés identificados y resueltos | 6 de 6. |

---

## Historial de versiones

| Versión | Fecha | Cambio |
|---|---|---|
| 1.0 | 05/2026 | Identificación de los seis stakeholders con su descripción, justificación y tabla de tipo e impacto. |
| 1.1 | 05/2026 | Incorporación de la matriz de impacto e interés, fichas completas con necesidades, expectativas, información requerida, funcionalidades y riesgos. Agregado de la matriz de participación, el mapa de intereses en conflicto, la estrategia de comunicación, la consolidación de riesgos y la trazabilidad con historias, casos de uso y pantallas. |

---

<sub>Escuela Superior de Comercio N° 49 "Justo José de Urquiza" — Desarrollo Web / Analista Funcional de Sistemas — 2026.</sub>
