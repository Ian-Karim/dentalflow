# 02. Caso de Negocio

## Tabla de contenidos

1. [Contexto del sector](#contexto-del-sector)
2. [Personas](#personas-roles-del-sistema)
3. [Journeys](#journeys-flujos-clave)
4. [Puntos de dolor y solución](#puntos-de-dolor-consolidados-y-solución)
5. [KPIs del negocio](#kpis-del-negocio)
6. [Flujo de ingresos y egresos](#flujo-de-ingresos-y-egresos)
7. [Supuestos del dominio](#supuestos-y-consideraciones-del-dominio)

---

## Contexto del sector

En México existen más de 40,000 consultorios dentales, en su mayoría micro y pequeñas empresas (de 1 a 5 consultorios). La adopción de software especializado es baja: predominan la agenda en papel, las hojas de cálculo, WhatsApp y los sistemas genéricos adaptados. Esto genera:

- Pérdida de citas por falta de seguimiento.
- Tasas de no-show entre 20 % y 35 %, según la clínica.
- Presupuestos sin seguimiento comercial.
- Inventario descontrolado y compras de emergencia.
- Facturación manual y cierre de caja lento.
- Expedientes físicos difíciles de consultar y sin respaldo.

DentalFlow atiende estos puntos con un ERP + CRM ligero, *mobile-first*, en español de México y con cumplimiento normativo documentado.

---

## Personas (roles del sistema)

### Persona 1: Laura, recepcionista

| Atributo | Detalle |
|---|---|
| Edad | 28 años |
| Contexto | Clínica de 3 consultorios con 2 dentistas |
| Herramientas actuales | Libreta, WhatsApp, Excel y terminal de cobro |

**Un día típico:**

1. Llega a las 9:00 y revisa la agenda del día en libreta.
2. Llama o envía mensajes por WhatsApp a los pacientes de la mañana para confirmar.
3. Recibe a los pacientes, registra su llegada y los pasa al consultorio.
4. Cobra consultas y anticipos de tratamientos.
5. Al final del día cuadra la caja contra la libreta y la terminal.

**Dolores:**

- Citas duplicadas o sobrevendidas.
- No-shows no anticipados.
- Cobros anotados en papel que luego no cuadran.
- Pacientes que llaman para preguntar "¿cuándo es mi cita?".
- La facturación toma entre 10 y 15 minutos por paciente.

**Qué necesita de DentalFlow:** agenda clara, recordatorios automáticos, cobro rápido, facturación en dos clics y cierre de caja diario en 5 minutos.

---

### Persona 2: Dr. Ricardo, dentista

| Atributo | Detalle |
|---|---|
| Edad | 42 años |
| Contexto | Dueño de la clínica; atiende de 6 a 8 pacientes al día |
| Herramientas actuales | Expediente en papel y radiografías en carpeta física |

**Un día típico:**

1. Revisa la agenda del día (en papel o dictada por Laura).
2. Atiende pacientes y anota los procedimientos en papel.
3. Dicta el presupuesto a Laura para que lo pase a máquina.
4. Revisa a los pacientes de seguimiento.

**Dolores:**

- No recuerda el historial completo del paciente sin buscar el expediente.
- No tiene visibilidad del plan de tratamiento a futuro.
- El odontograma en papel es difícil de leer y de actualizar.
- No mide qué tratamientos son más rentables.

**Qué necesita:** expediente digital con odontograma visual, historial completo en segundos y plan de tratamiento claro.

---

### Persona 3: Sra. Mónica, administradora y dueña

| Atributo | Detalle |
|---|---|
| Edad | 50 años |
| Contexto | Dueña de 2 sucursales; no atiende pacientes |
| Herramientas actuales | Hojas de cálculo, estados de cuenta bancarios y contador externo |

**Un día típico (semanal):**

1. Revisa los ingresos de la semana en su hoja de cálculo.
2. Compara los ingresos contra los depósitos bancarios.
3. Consulta con cada sucursal los gastos y compras.
4. Revisa el inventario de insumos críticos.

**Dolores:**

- No tiene visibilidad consolidada de sus dos sucursales.
- No sabe qué tratamientos son más rentables.
- Descubre los gastos cuando ya ocurrieron.
- No puede auditar quién hizo qué.

**Qué necesita:** dashboard con KPIs por sucursal, reportes de rentabilidad, auditoría de acciones y control de inventario consolidado.

---

### Persona 4: Paciente (usuario indirecto)

| Atributo | Detalle |
|---|---|
| Edad | Variable |
| Contexto | Acude de 1 a 10 veces según el tratamiento |

**Dolores actuales:**

- No recibe recordatorios claros.
- No sabe cuánto le falta por pagar.
- No tiene copia de su presupuesto.
- No ve su plan de tratamiento completo.

**Qué mejora con DentalFlow** (aunque no use el sistema directamente): recibe recordatorios, tiene claridad sobre su plan y sus pagos, y su información queda respaldada.

---

## Journeys (flujos clave)

### Journey 1: Del primer contacto al alta del tratamiento

```text
Paciente llama o llega
  -> Recepcionista agenda cita
  -> Recibe recordatorio 24 h antes
  -> Llega; recepcionista registra llegada
  -> Dentista atiende y registra hallazgos en el odontograma
  -> Dentista genera el plan de tratamiento
  -> Recepcionista arma el presupuesto
  -> Paciente acepta (total o parcial) y paga anticipo
  -> Se agenda la siguiente cita del plan
  -> Al terminar el tratamiento se cierra el plan y se da seguimiento
  -> Recordatorio de revisión a los 6 meses
```

**Puntos de dolor actuales:**

| Paso | Dolor |
|---|---|
| 1 | Agenda en libreta; riesgo de doble reserva. |
| 2 | Recordatorio manual por WhatsApp; se olvida. |
| 4 | Hallazgos en papel; se pierden. |
| 5 y 6 | Presupuesto a máquina; sin seguimiento. |
| 9 | No existe seguimiento posterior al tratamiento. |

---

### Journey 2: Un día de la recepcionista

| Hora | Actividad |
|---|---|
| 08:45 | Abre el sistema y revisa la agenda del día. |
| 09:00 | Confirma citas pendientes (el sistema sugiere a quién llamar). |
| 09:30 | Recibe al primer paciente y marca su llegada en el sistema. |
| 10:00 | Cobra la consulta y genera factura si aplica. |
| 14:00 | Pausa; revisa los no-show. |
| 18:00 | Cierre de caja. |

**Cierre de caja:**

1. El sistema muestra los cobros del día por método de pago.
2. Compara contra el efectivo y la terminal.
3. Genera el corte Z (simulado).
4. Marca el cierre y bloquea los movimientos del día.

**Puntos de dolor actuales:**

- El cierre de caja manual tarda entre 30 y 45 minutos.
- Los no-show se detectan tarde y no hay oportunidad de reagendar.
- La facturación interrumpe el flujo de trabajo.

---

### Journey 3: Un día del dentista

| Hora | Actividad |
|---|---|
| 09:00 | Revisa la agenda del día (pacientes y motivos). |
| 09:15 | Primer paciente: abre el expediente y revisa el historial. |
| 09:20 | Atiende al paciente y registra hallazgos en el odontograma. |
| 09:45 | Genera el plan de tratamiento y marca los procedimientos. |
| 09:50 | Pasa a recepción para el presupuesto. |
| 18:00 | Revisa los pacientes del día siguiente con tratamientos pendientes. |

**Puntos de dolor actuales:**

- Abrir un expediente físico toma entre 2 y 5 minutos.
- El odontograma en papel no refleja la evolución del paciente.
- No es posible consultar qué procedimientos se hicieron a un paciente en el último año.

---

## Puntos de dolor consolidados y solución

| # | Dolor actual | Impacto | Solución en DentalFlow | Módulo |
|---|---|---|---|---|
| 1 | Agenda en libreta | Citas duplicadas y no-shows | Agenda digital con validaciones y recordatorios | Agenda |
| 2 | No-shows de 20 % a 35 % | Pérdida de ingresos | Recordatorio automático 24 h antes y reagendamiento en un clic | Agenda |
| 3 | Expediente físico | Pérdida de información y búsqueda lenta | Expediente digital con búsqueda y odontograma visual | Clínico |
| 4 | Presupuesto en papel | Sin seguimiento y pérdida de ventas | Presupuesto digital con estado (enviado, aceptado, rechazado) | Comercial |
| 5 | Cobros dispersos | Cierre de caja lento | Registro unificado de pagos y corte diario | Comercial |
| 6 | Facturación manual | 10 a 15 minutos por factura | Factura simulada en dos clics con PDF | Comercial |
| 7 | Inventario sin control | Desabasto o compras de emergencia | Inventario con stock mínimo y alertas | Operación |
| 8 | Sin visibilidad multisucursal | Decisiones a ciegas | Dashboard consolidado y por sucursal | Sistema |
| 9 | Sin auditoría | No se sabe quién hizo qué | Bitácora de auditoría | Sistema |
| 10 | Sin seguimiento posterior al tratamiento | Pérdida de recurrencia | Recordatorio de revisión a los 6 meses | CRM |

---

## KPIs del negocio

### Operativos

- **Tasa de no-show:** citas no atendidas / citas agendadas.
- **Ocupación de agenda:** slots ocupados / slots disponibles.
- **Tiempo de cierre de caja:** minutos al final del día.
- **Rotación de inventario:** días de stock disponible.

### Comerciales

- **Ticket promedio por paciente.**
- **Tasa de aceptación de presupuestos:** aceptados / enviados.
- **Ingresos por tratamiento:** ranking de rentabilidad.
- **Pacientes nuevos vs. recurrentes.**
- **Tasa de retención a 6 meses.**

### Clínicos

- **Tratamientos completados vs. iniciados.**
- **Tiempo promedio entre diagnóstico y primer tratamiento.**

---

## Flujo de ingresos y egresos

### Ingresos

- Consulta de valoración.
- Tratamientos (por procedimiento o plan completo).
- Venta de productos (blanqueamientos, kits, etc.).

### Egresos

- Insumos dentales (guantes, anestesia, resinas, etc.).
- Nómina de dentistas y personal.
- Renta, servicios y mantenimiento de equipo.
- Comisiones de terminal bancaria.
- Publicidad y marketing.

### Formas de pago aceptadas

- Efectivo.
- Transferencia.
- Tarjeta de débito o crédito (terminal).
- Pago en parcialidades (tratamientos largos).

---

## Supuestos y consideraciones del dominio

- Un paciente puede tener **un plan de tratamiento activo a la vez**. Es una regla simplificada: en la práctica pueden existir varios, pero el MVP lo limita.
- El **odontograma** se modela para dentición permanente (32 piezas). La dentición mixta se considera una extensión futura.
- La **factura es simulada**: no se timbra con PAC, pero sigue el formato CFDI 4.0 (RFC, régimen fiscal, uso de CFDI e IVA).
- Los **servicios odontológicos** pueden tener un tratamiento fiscal distinto según el servicio (exento o gravado). Este punto se documenta en el documento 07.
- El sistema **no sustituye** al expediente clínico certificado; es una herramienta de gestión con valor clínico complementario.
