# 01. Visión y Alcance

## Tabla de contenidos

1. [Visión](#visión)
2. [Problema que resuelve](#problema-que-resuelve)
3. [Público objetivo](#público-objetivo)
4. [Roles de usuario](#roles-de-usuario)
5. [Alcance funcional (MVP)](#alcance-funcional-mvp)
6. [Fuera de alcance](#fuera-de-alcance-explícito)
7. [Métricas de éxito](#métricas-de-éxito-del-producto)
8. [Restricciones y supuestos](#restricciones-y-supuestos)
9. [Diferenciadores](#diferenciadores)

---

## Visión

DentalFlow es un ERP + CRM ligero para clínicas dentales pequeñas y medianas en México (de 1 a 5 consultorios y de 1 a 3 sucursales) que necesitan digitalizar su operación sin pagar un sistema empresarial ni contratar un equipo de TI.

## Problema que resuelve

Las clínicas dentales pequeñas suelen operar con los siguientes esquemas:

- **Agenda en libreta o WhatsApp**: genera citas duplicadas y un alto índice de no-shows.
- **Presupuestos en papel**: se pierde el seguimiento comercial.
- **Inventario sin control**: provoca compras de emergencia o desabasto.
- **Cobros y facturación dispersos**: alargan el cierre de caja y aumentan los errores.
- **Expediente clínico en físico**: dificulta la consulta y expone la información a pérdida.

DentalFlow centraliza en un solo sistema, con roles y auditoría, los siguientes procesos: pacientes, agenda, tratamientos, presupuestos, cobros, facturación simulada e inventario.

## Público objetivo

| Segmento | Descripción |
|---|---|
| **Primario** | Clínicas dentales independientes en México con 1 a 5 consultorios. |
| **Secundario** | Cadenas pequeñas de 2 a 3 sucursales. |
| **No objetivo** | Hospitales, clínicas multiespecialidad grandes y consultorios unipersonales que solo requieren agenda. |

## Roles de usuario

| Rol | Descripción | Permisos principales |
|---|---|---|
| Administrador | Dueño o gerente | Acceso total, incluidos usuarios y configuración. |
| Recepcionista | Front desk | Pacientes, agenda, cobros y facturación. |
| Dentista | Profesional clínico | Expediente, odontograma, tratamientos y plan de tratamiento. |
| Auditor (solo lectura) | Contador o supervisor | Consulta de reportes y bitácora de auditoría. |

## Alcance funcional (MVP)

### CRM

- Registro de pacientes con datos personales y fiscales (RFC opcional).
- Tutor responsable para pacientes menores de edad.
- Historial médico: alergias, condiciones y medicamentos.
- Notas y comunicación por paciente.
- Búsqueda y filtros avanzados.

### Agenda

- Calendario por dentista y por sucursal.
- Alta, reprogramación y cancelación de citas con validaciones.
- Estados de cita: agendada, confirmada, atendida, no-show y cancelada.
- Recordatorios automáticos simulados vía correo electrónico.

### Clínico

- Odontograma visual interactivo de 32 piezas (dentición permanente), extensible a 52 piezas en dentición mixta.
- Registro de procedimientos por pieza.
- Plan de tratamiento con estado por tratamiento.
- Consentimiento informado por tratamiento.

### Comercial

- Presupuestos con conceptos, descuentos e IVA.
- Pagos parciales y totales.
- Factura simulada con folio, RFC, IVA y PDF descargable.

> **Nota:** la factura es simulada. No existe timbrado real.

### Operación

- Inventario con stock mínimo por sucursal.
- Movimientos de entrada, salida, ajuste y traspaso.
- Alertas de stock bajo.

### Sistema

- Autenticación con roles y permisos.
- Dashboard con métricas operativas y comerciales.
- Bitácora de auditoría (quién, qué y cuándo).

## Fuera de alcance (explícito)

Las siguientes funcionalidades no forman parte del MVP. Se documentan aquí para evitar el *scope creep*:

- Timbrado real de CFDI con PAC.
- Certificación del expediente clínico por la SSA.
- Telemedicina o videoconsultas.
- Aplicación móvil nativa (se entregará una PWA responsiva).
- Integración con hardware dental (rayos X, escáner intraoral).
- Multi-idioma (solo español de México).
- Pagos en línea con pasarela real (Stripe o MercadoPago).

## Métricas de éxito del producto

| Métrica | Meta |
|---|---|
| Reducción de no-shows mediante recordatorios | Al menos 30 % |
| Tiempo de cierre de caja diario | Menos de 5 minutos |
| Localización de cualquier expediente | Menos de 10 segundos |
| Alerta de stock bajo | Antes de que ocurra el desabasto |

## Restricciones y supuestos

| Tipo | Detalle |
|---|---|
| **Regulatorio** | NOM-013-SSA2-2015, NOM-004-SSA3-2012, LFPDPPP. |
| **Técnico** | Aplicación web responsiva; funciona en tablet y escritorio. |
| **Presupuesto** | Proyecto de portafolio; despliegue en capa gratuita. |
| **Supuesto operativo** | La clínica cuenta con internet estable y dispositivos con navegador moderno. |

## Diferenciadores

1. **Odontograma visual interactivo.** La mayoría de los sistemas lo presentan como tabla y no como representación gráfica.
2. **Asistente de IA** con *function calling* para consultas operativas y resúmenes del historial.
3. **Cumplimiento normativo mexicano documentado** (NOM-013, NOM-004, LFPDPPP y CFDI 4.0).
4. **Diseño *mobile-first*** pensado para recepcionistas que trabajan en tablet.
