# 03. Requerimientos

## Convenciones

| Prefijo | Significado |
|---|---|
| **RF-XX** | Requerimiento funcional (numeración por módulo, por ejemplo RF-CRM-01). |
| **RNF-XX** | Requerimiento no funcional. |
| **CU-XX** | Caso de uso. |

**Prioridad MoSCoW:**

- **M** (Must): obligatorio para el MVP.
- **S** (Should): deseable.
- **C** (Could): futuro.

> Cada RF debe ser **verificable**: se puede probar con un test o una demo.

---

## 1. Requerimientos funcionales

### 1.1 Módulo CRM: pacientes

| ID | Requerimiento | Prioridad | Pain point |
|---|---|:---:|:---:|
| RF-CRM-01 | Registrar paciente con nombre, apellidos, fecha de nacimiento, sexo, teléfono, email, dirección, CURP y RFC (opcional). | M | #3 |
| RF-CRM-02 | Registrar tutor responsable cuando el paciente es menor de edad (obligatorio si la edad es menor a 18 años). | M | #3 |
| RF-CRM-03 | Registrar historial médico: alergias, condiciones sistémicas, medicamentos actuales y antecedentes quirúrgicos. | M | #3 |
| RF-CRM-04 | Agregar notas libres por paciente, con fecha, autor y tipo (general, clínica o administrativa). | M | #3 |
| RF-CRM-05 | Buscar pacientes por nombre, teléfono, email o RFC con resultados en menos de 1 segundo. | M | #3 |
| RF-CRM-06 | Filtrar pacientes por sucursal, estado (activo o inactivo) y última visita. | S | #3 |
| RF-CRM-07 | Registrar comunicación con el paciente (llamada, WhatsApp o email) con resultado y próximo paso. | S | #1, #2 |
| RF-CRM-08 | Consultar la línea de tiempo del paciente: citas, tratamientos, pagos, notas y comunicaciones en orden cronológico. | M | #3 |
| RF-CRM-09 | Exportar el listado de pacientes a CSV (solo administrador). | C | n/a |

### 1.2 Módulo Agenda: citas

| ID | Requerimiento | Prioridad | Pain point |
|---|---|:---:|:---:|
| RF-AGD-01 | Agendar cita indicando paciente, dentista, sucursal, fecha, hora, duración y tipo de cita. | M | #1 |
| RF-AGD-02 | Validar que no se solapen citas del mismo dentista en la misma sucursal. | M | #1 |
| RF-AGD-03 | Mostrar calendario por día, semana y mes, filtrable por dentista y sucursal. | M | #1 |
| RF-AGD-04 | Cambiar el estado de la cita: agendada, confirmada, atendida, no-show o cancelada. | M | #1 |
| RF-AGD-05 | Reprogramar cita conservando el historial del cambio (quién, cuándo y motivo). | M | #2 |
| RF-AGD-06 | Enviar recordatorio automático 24 h antes de la cita (correo simulado; WhatsApp como futuro). | M | #2 |
| RF-AGD-07 | Detectar y listar los no-show del día para reagendamiento rápido. | M | #2 |
| RF-AGD-08 | Bloquear la agenda en días festivos o ausencias del dentista. | S | #1 |
| RF-AGD-09 | Reagendar cita en un clic desde la lista de no-show. | M | #2 |
| RF-AGD-10 | Consultar la agenda del día por sucursal en formato imprimible. | C | #1 |

### 1.3 Módulo Clínico: odontograma y tratamientos

| ID | Requerimiento | Prioridad | Pain point |
|---|---|:---:|:---:|
| RF-CLI-01 | Mostrar odontograma visual interactivo con 32 piezas (dentición permanente), dividido por cuadrantes. | M | #3 |
| RF-CLI-02 | Registrar el estado por pieza: sano, caries, obturado, corona, endodoncia, ausente, implante o extracción indicada. | M | #3 |
| RF-CLI-03 | Registrar el procedimiento realizado por pieza (con fecha, dentista y notas). | M | #3 |
| RF-CLI-04 | Consultar el historial de cambios de una pieza (qué se hizo y cuándo). | M | #3 |
| RF-CLI-05 | Crear un plan de tratamiento con lista de procedimientos y estado por procedimiento (pendiente, en proceso, completado o cancelado). | M | #3, #4 |
| RF-CLI-06 | Asociar cada procedimiento del plan a un concepto del catálogo de tratamientos (con precio base). | M | #4 |
| RF-CLI-07 | Registrar el consentimiento informado por tratamiento (fecha, firma simulada y texto aceptado). | S | #3 |
| RF-CLI-08 | Imprimir o exportar el plan de tratamiento en PDF para el paciente. | S | #4 |
| RF-CLI-09 | Mostrar una alerta si el paciente tiene alergias registradas al abrir su expediente. | M | #3 |

### 1.4 Módulo Comercial: presupuestos, pagos y facturas

| ID | Requerimiento | Prioridad | Pain point |
|---|---|:---:|:---:|
| RF-COM-01 | Crear un presupuesto a partir de un plan de tratamiento, con conceptos, cantidad, precio unitario, descuento e IVA. | M | #4 |
| RF-COM-02 | Calcular automáticamente subtotal, descuento, IVA (16 % o exento según el tratamiento) y total. | M | #4 |
| RF-COM-03 | Cambiar el estado del presupuesto: borrador, enviado, aceptado, rechazado o vencido. | M | #4 |
| RF-COM-04 | Generar PDF del presupuesto con logotipo de la clínica, datos del paciente y vigencia. | M | #4 |
| RF-COM-05 | Registrar un pago (total o parcial) asociado a un presupuesto, con método de pago (efectivo, transferencia o tarjeta). | M | #5 |
| RF-COM-06 | Mostrar el saldo pendiente por presupuesto y por paciente. | M | #5 |
| RF-COM-07 | Generar factura simulada con folio interno, RFC, régimen fiscal, uso de CFDI, IVA y PDF descargable. **No hay timbrado real.** | M | #6 |
| RF-COM-08 | Asociar una o varias facturas a un pago (o viceversa). | S | #6 |
| RF-COM-09 | Registrar nota de crédito simple (cancelación de pago) con motivo. | S | #5 |
| RF-COM-10 | Realizar el cierre de caja diario: total cobrado por método de pago, número de transacciones y diferencia contra el monto declarado. | M | #5 |
| RF-COM-11 | Bloquear movimientos del día después del cierre de caja (solo el administrador puede reabrirlo). | S | #5 |

### 1.5 Módulo Operación: inventario

| ID | Requerimiento | Prioridad | Pain point |
|---|---|:---:|:---:|
| RF-OPS-01 | Registrar insumos con nombre, SKU, unidad, stock actual, stock mínimo, costo y proveedor. | M | #7 |
| RF-OPS-02 | Registrar movimientos: entrada (compra), salida (consumo), ajuste (conteo) y traspaso entre sucursales. | M | #7 |
| RF-OPS-03 | Descontar stock automáticamente al registrar un procedimiento que consume insumos (configurable). | S | #7 |
| RF-OPS-04 | Alertar cuando el stock sea menor al mínimo (en el dashboard y por correo). | M | #7 |
| RF-OPS-05 | Consultar el historial de movimientos por insumo, con filtros por fecha y sucursal. | M | #7 |
| RF-OPS-06 | Registrar compras a proveedor con detalle de conceptos y costo. | S | #7 |
| RF-OPS-07 | Generar reporte de insumos más consumidos en un periodo. | C | #7 |

### 1.6 Módulo Sistema: autenticación, usuarios, dashboard y auditoría

| ID | Requerimiento | Prioridad | Pain point |
|---|---|:---:|:---:|
| RF-SIS-01 | Autenticación con email y contraseña (hash con bcrypt o argon2). | M | n/a |
| RF-SIS-02 | Roles: administrador, recepcionista, dentista y auditor. Permisos por módulo y por acción. | M | #9 |
| RF-SIS-03 | Un dentista solo ve los pacientes de su(s) sucursal(es) asignada(s). | M | #8 |
| RF-SIS-04 | Dashboard con KPIs: citas del día, ingresos del mes, no-show, stock bajo y presupuestos pendientes. | M | #8 |
| RF-SIS-05 | Dashboard filtrable por sucursal (si el usuario tiene acceso a varias). | M | #8 |
| RF-SIS-06 | Bitácora de auditoría: quién, qué acción, sobre qué entidad, cuándo e IP. | M | #9 |
| RF-SIS-07 | Búsqueda en la bitácora por usuario, entidad, fecha y tipo de acción. | S | #9 |
| RF-SIS-08 | Gestión de usuarios (alta, baja, cambio de rol y reinicio de contraseña) solo por administrador. | M | n/a |
| RF-SIS-09 | Sesión con expiración por inactividad configurable. | S | n/a |
| RF-SIS-10 | Recuperación de contraseña por correo (simulada). | S | n/a |

### 1.7 Módulo IA: asistente y automatizaciones

| ID | Requerimiento | Prioridad | Pain point |
|---|---|:---:|:---:|
| RF-IA-01 | Asistente conversacional que responde preguntas operativas mediante *function calling* a la API (por ejemplo, "¿cuántas citas tuve esta semana?"). | S | #8 |
| RF-IA-02 | Botón "resumir historial" en la ficha del paciente que genera un resumen de notas y procedimientos con un LLM. | S | #3 |
| RF-IA-03 | Sugerir texto de nota clínica estructurada (SOAP) a partir de texto libre dictado o escrito. | C | #3 |
| RF-IA-04 | Todos los resultados de IA deben ser **revisables y editables** por el usuario antes de guardarse. | M | n/a |
| RF-IA-05 | Registrar en auditoría cuándo se usó la IA y qué se guardó o editó. | M | #9 |

---

## 2. Requerimientos no funcionales

### 2.1 Rendimiento

| ID | Requerimiento |
|---|---|
| RNF-01 | Tiempo de carga de cualquier pantalla principal menor a 2 segundos en red 4G. |
| RNF-02 | Búsqueda de pacientes en menos de 1 segundo para hasta 10,000 registros. |
| RNF-03 | Dashboard con KPIs cargado en menos de 3 segundos. |
| RNF-04 | La API responde con p95 menor a 500 ms en endpoints CRUD. |

### 2.2 Seguridad

| ID | Requerimiento |
|---|---|
| RNF-05 | Contraseñas hasheadas con bcrypt (costo mayor o igual a 12) o argon2. |
| RNF-06 | HTTPS obligatorio en producción. |
| RNF-07 | JWT con expiración corta (15 min) y refresh token (7 días). |
| RNF-08 | Validación y sanitización de todos los insumos (OWASP Top 10). |
| RNF-09 | Protección contra inyección SQL mediante ORM o consultas parametrizadas. |
| RNF-10 | Rate limiting en endpoints de autenticación (5 intentos por cada 15 minutos). |
| RNF-11 | Datos sensibles (RFC, CURP e historial clínico) nunca aparecen en logs. |
| RNF-12 | Aviso de privacidad accesible desde el login (LFPDPPP). |

### 2.3 Usabilidad

| ID | Requerimiento |
|---|---|
| RNF-13 | Diseño *mobile-first*: usable en tablet de 768 px sin scroll horizontal. |
| RNF-14 | Español de México en toda la interfaz (fechas DD/MM/AAAA, moneda MXN). |
| RNF-15 | Las acciones críticas (cancelar cita, eliminar pago) requieren confirmación. |
| RNF-16 | Mensajes de error claros y accionables (no "Error 500"). |
| RNF-17 | Tema claro por defecto; modo oscuro como futuro. |

### 2.4 Disponibilidad y confiabilidad

| ID | Requerimiento |
|---|---|
| RNF-18 | Disponibilidad objetivo de 99 % mensual (para demo, no es un SLA real). |
| RNF-19 | Respaldos diarios de la base de datos (en despliegue: snapshots de Supabase o Railway). |
| RNF-20 | Migraciones de base de datos versionadas y reversibles. |
| RNF-21 | Endpoint de healthcheck `/health` para monitoreo. |

### 2.5 Mantenibilidad

| ID | Requerimiento |
|---|---|
| RNF-22 | Cobertura de pruebas mayor o igual a 60 % en la lógica de negocio (servicios). |
| RNF-23 | Linter y formateador configurados (ESLint y Prettier o equivalente). |
| RNF-24 | CI en GitHub Actions que ejecute lint y pruebas en cada PR. |
| RNF-25 | Commits con la convención Conventional Commits. |
| RNF-26 | Código documentado con comentarios donde la lógica no sea obvia. |

### 2.6 Compatibilidad

| ID | Requerimiento |
|---|---|
| RNF-27 | Navegadores: Chrome, Edge, Firefox y Safari (últimas dos versiones). |
| RNF-28 | PWA instalable (manifest y service worker básico). |

### 2.7 Legal y cumplimiento (México)

| ID | Requerimiento |
|---|---|
| RNF-29 | Aviso de privacidad conforme a la LFPDPPP. |
| RNF-30 | Mecanismo de consentimiento explícito para el tratamiento de datos. |
| RNF-31 | Retención del expediente clínico de al menos 5 años (NOM-013). |
| RNF-32 | Bitácora de acceso a expedientes clínicos (NOM-004 y NOM-013). |

---

## 3. Casos de uso

### CU-01: Agendar cita

| Campo | Detalle |
|---|---|
| **Actor** | Recepcionista |
| **Precondición** | El paciente y el dentista existen en el sistema. |
| **Postcondición** | Cita creada en estado "agendada" y recordatorio programado. |

**Flujo principal:**

1. El recepcionista abre la agenda del día.
2. Hace clic en un slot libre.
3. Selecciona al paciente (búsqueda por nombre o teléfono).
4. Selecciona dentista, sucursal, duración y tipo de cita.
5. El sistema valida la disponibilidad y confirma.
6. El sistema programa el recordatorio a 24 h.

**Flujos alternos:**

- **5a.** Slot ocupado: el sistema sugiere horarios cercanos.
- **3a.** Paciente no existe: el sistema permite crearlo dentro del mismo flujo.

---

### CU-02: Registrar consulta y actualizar odontograma

| Campo | Detalle |
|---|---|
| **Actor** | Dentista |
| **Precondición** | Cita en estado "confirmada" o "atendida". |
| **Postcondición** | Odontograma actualizado, plan de tratamiento creado y auditoría registrada. |

**Flujo principal:**

1. El dentista abre la cita del día.
2. El sistema muestra el expediente, el odontograma actual y las alertas (alergias).
3. El dentista marca los estados de las piezas afectadas.
4. El dentista agrega procedimientos al plan de tratamiento.
5. El dentista guarda; el sistema registra la acción en auditoría.
6. El sistema ofrece generar el presupuesto.

**Flujos alternos:**

- **2a.** Paciente nuevo: el sistema crea el odontograma inicial (todas las piezas en "sano").
- **5a.** El dentista sale sin guardar: el sistema pide confirmación antes de salir.

---

### CU-03: Generar y aceptar presupuesto

| Campo | Detalle |
|---|---|
| **Actor** | Recepcionista (genera) y paciente (acepta fuera del sistema) |
| **Precondición** | El plan de tratamiento tiene procedimientos. |
| **Postcondición** | Presupuesto con estado asignado y PDF generado. |

**Flujo principal:**

1. El recepcionista abre el plan de tratamiento.
2. Hace clic en "Generar presupuesto".
3. El sistema prellena los conceptos con los precios del catálogo.
4. El recepcionista ajusta los descuentos si aplica.
5. El sistema calcula IVA y total.
6. El recepcionista marca el presupuesto como "enviado".
7. Al recibir respuesta, lo marca como "aceptado" o "rechazado".

**Flujos alternos:**

- **4a.** Descuento mayor a 15 %: requiere aprobación del administrador.
- **7a.** Vigencia de 30 días cumplida: el estado cambia automáticamente a "vencido".

---

### CU-04: Cobrar y facturar

| Campo | Detalle |
|---|---|
| **Actor** | Recepcionista |
| **Precondición** | Presupuesto aceptado con saldo pendiente. |
| **Postcondición** | Pago registrado, factura generada y saldo actualizado. |

**Flujo principal:**

1. El recepcionista abre el presupuesto del paciente.
2. Registra el pago (monto, método y referencia).
3. El sistema actualiza el saldo.
4. Si el paciente solicita factura, el recepcionista captura RFC y régimen fiscal.
5. El sistema genera la factura simulada y su PDF.
6. El sistema registra la acción en auditoría.

**Flujos alternos:**

- **2a.** Pago parcial: el saldo restante queda pendiente.
- **4a.** RFC inválido: el sistema valida el formato y emite una alerta.

---

### CU-05: Cierre de caja diario

| Campo | Detalle |
|---|---|
| **Actor** | Recepcionista (cierra) y administrador (verifica) |
| **Precondición** | Al menos un pago registrado en el día. |
| **Postcondición** | Corte Z generado y movimientos bloqueados. |

**Flujo principal:**

1. El recepcionista abre el módulo de cierre.
2. El sistema muestra los totales por método de pago.
3. El recepcionista declara los montos físicos por método.
4. El sistema calcula las diferencias.
5. Si la diferencia supera el umbral, se requiere un motivo.
6. El recepcionista confirma el cierre; el sistema bloquea los movimientos del día.

**Flujo alterno:**

- **5a.** Diferencia mayor a $500 MXN: requiere aprobación del administrador.

---

### CU-06: Consultar al asistente de IA

| Campo | Detalle |
|---|---|
| **Actor** | Administrador y dentista |
| **Precondición** | Sesión autenticada con permisos. |
| **Postcondición** | Respuesta mostrada y uso de IA registrado en auditoría. |

**Flujo principal:**

1. El usuario abre el chat del asistente.
2. Escribe una pregunta, por ejemplo: "¿cuántas citas tuve esta semana?".
3. El sistema identifica la intención y llama a la función correspondiente.
4. El LLM genera la respuesta en lenguaje natural.
5. El sistema muestra la respuesta junto con su fuente (consulta ejecutada).

**Flujos alternos:**

- **3a.** Intención no reconocida: el sistema sugiere preguntas de ejemplo.
- **4a.** El LLM alucina datos: el *system prompt* obliga a usar exclusivamente los datos devueltos por la API.

---

## 4. Matriz de trazabilidad (pain point a RF)

| Pain point | RF que lo resuelven |
|---|---|
| #1 Agenda en libreta | RF-AGD-01, 02, 03, 04, 08, 10 |
| #2 No-shows | RF-AGD-06, 07, 09; RF-CRM-07 |
| #3 Expediente físico | RF-CRM-01 a 05, 08; RF-CLI-01 a 09; RF-IA-02 |
| #4 Presupuesto en papel | RF-CLI-05, 06; RF-COM-01 a 04 |
| #5 Cobros dispersos | RF-COM-05, 06, 09, 10, 11 |
| #6 Facturación manual | RF-COM-07, 08 |
| #7 Inventario sin control | RF-OPS-01 a 07 |
| #8 Sin visibilidad multisucursal | RF-SIS-04, 05; RF-IA-01 |
| #9 Sin auditoría | RF-SIS-06, 07; RF-IA-05 |
| #10 Sin seguimiento posterior al tratamiento | RF-CRM-07; RF-AGD-06 |

---

## 5. Resumen de alcance del MVP

### Dentro del MVP (prioridad M)

- Módulos completos: CRM, Agenda, Clínico, Comercial, Operación y Sistema.
- Autenticación, roles y auditoría.
- Factura simulada (sin timbrado).

### Deseable (prioridad S)

- Asistente de IA (RF-IA-01 y RF-IA-02).
- Cierre de caja con reapertura (RF-COM-11).
- Registro de comunicaciones (RF-CRM-07).
- Consentimiento informado (RF-CLI-07).
- Exportación del plan de tratamiento en PDF (RF-CLI-08).

### Futuro (prioridad C)

- Resumen clínico con IA (RF-IA-03).
- Exportación de pacientes (RF-CRM-09).
- Reporte de insumos más consumidos (RF-OPS-07).
- PWA con funcionamiento sin conexión.

### Fuera del alcance

- Timbrado real de CFDI.
- Telemedicina.
- Aplicación nativa.
- Pagos en línea con pasarela real.
- Integración con hardware dental.
- Multi-idioma.
