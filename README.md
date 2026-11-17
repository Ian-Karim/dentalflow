<!-- ============================================================ -->
<!-- README de DentalFlow                                          -->
<!-- ============================================================ -->

<div align="center">

# 🦷 DentalFlow

### ERP + CRM ligero para clínicas dentales en México 🇲🇽

<p>
  <a href="#-qué-es"><strong>Descripción</strong></a> ·
  <a href="#-documentación"><strong>Documentación</strong></a> ·
  <a href="#️-stack"><strong>Stack</strong></a> ·
  <a href="#️-roadmap"><strong>Roadmap</strong></a> ·
  <a href="#-contacto"><strong>Contacto</strong></a>
</p>

<p>
  <img src="https://img.shields.io/badge/estado-en%20desarrollo-yellow?style=for-the-badge" alt="Estado" />
  <img src="https://img.shields.io/badge/versión-0.1.0-blue?style=for-the-badge" alt="Versión" />
  <img src="https://img.shields.io/badge/licencia-MIT-green?style=for-the-badge" alt="Licencia" />
  <img src="https://img.shields.io/badge/país-México%20🇲🇽-brightgreen?style=for-the-badge" alt="México" />
</p>

<p>
  <img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black" alt="React" />
  <img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white" alt="Next.js" />
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white" alt="NestJS" />
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" alt="PostgreSQL" />
  <img src="https://img.shields.io/badge/OpenAI-412991?style=flat-square&logo=openai&logoColor=white" alt="OpenAI" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Docker" />
</p>

</div>

---

<div align="center">
  <img src="https://user-images.githubusercontent.com/74038190/212284100-561aa473-3905-4a80-b561-0d28506553ee.gif" alt="Banner" width="600" />
  <br />
  <sub>📸 <em>Próximamente: screenshots reales del sistema cuando esté implementado.</em></sub>
</div>

---

## 🎯 Qué es

**DentalFlow** centraliza la operación completa de una clínica dental pequeña o mediana en un solo sistema:

- 👥 **Pacientes** con historial médico y línea de tiempo completa
- 📅 **Agenda** por dentista y sucursal, con recordatorios automáticos
- 🦷 **Odontograma visual** interactivo (32 piezas FDI)
- 📋 **Planes de tratamiento** con estado por procedimiento
- 💰 **Presupuestos, pagos y facturación** simulada (CFDI 4.0)
- 📦 **Inventario** con stock mínimo y alertas
- 🤖 **Asistente IA** con function calling para consultas operativas
- 🔐 **Roles y auditoría** de todas las acciones

Todo **mobile-first**, en **español de México**, con cumplimiento normativo documentado.

---

## 💡 El problema que resuelve

Las clínicas dentales pequeñas en México suelen operar con:

| ❌ Problema actual | 💥 Impacto | ✅ Solución en DentalFlow |
|---|---|---|
| Agenda en libreta o WhatsApp | Citas duplicadas, sobreventa | Agenda digital con validaciones |
| Sin recordatorios | No-shows del 20–35% | Recordatorio automático 24h antes |
| Expediente en papel | Búsqueda de 2–5 min por paciente | Expediente digital en <10 segundos |
| Presupuestos en papel | Pérdida de seguimiento comercial | Presupuesto digital con estado |
| Cobros dispersos | Cierre de caja en 45 min | Corte diario en <5 min |
| Facturación manual | 10–15 min por factura | Factura simulada en 2 clics |
| Inventario sin control | Desabasto o compras urgentes | Stock mínimo con alertas |
| Sin visibilidad multi-sucursal | Decisiones a ciegas | Dashboard consolidado |
| Sin auditoría | No se sabe quién hizo qué | Bitácora completa |

---

## 📚 Documentación

Toda la documentación vive en la carpeta [`/docs`](./docs). Está organizada por fases del proyecto.

<table>
  <thead>
    <tr>
      <th align="center">#</th>
      <th align="left">Documento</th>
      <th align="center">Estado</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center">01</td>
      <td><a href="./docs/01-vision-y-alcance.md">Visión y alcance</a></td>
      <td align="center">✅</td>
    </tr>
    <tr>
      <td align="center">02</td>
      <td><a href="./docs/02-caso-de-negocio.md">Caso de negocio</a></td>
      <td align="center">✅</td>
    </tr>
    <tr>
      <td align="center">03</td>
      <td><a href="./docs/03-requerimientos.md">Requerimientos</a></td>
      <td align="center">✅</td>
    </tr>
    <tr>
      <td align="center">04</td>
      <td><a href="./docs/04-modelo-de-datos.md">Modelo de datos</a></td>
      <td align="center">✅</td>
    </tr>
    <tr>
      <td align="center">05</td>
      <td><a href="./docs/05-arquitectura.md">Arquitectura</a></td>
      <td align="center">🚧</td>
    </tr>
    <tr>
      <td align="center">06</td>
      <td><a href="./docs/06-decisiones-tecnicas.md">Decisiones técnicas (ADRs)</a></td>
      <td align="center">📋</td>
    </tr>
    <tr>
      <td align="center">07</td>
      <td><a href="./docs/07-cumplimiento-mexico.md">Cumplimiento México</a></td>
      <td align="center">📋</td>
    </tr>
    <tr>
      <td align="center">08</td>
      <td><a href="./docs/08-manual-usuario.md">Manual de usuario</a></td>
      <td align="center">📋</td>
    </tr>
    <tr>
      <td align="center">09</td>
      <td><a href="./docs/09-api.md">API</a></td>
      <td align="center">📋</td>
    </tr>
    <tr>
      <td align="center">10</td>
      <td><a href="./docs/10-roadmap.md">Roadmap</a></td>
      <td align="center">📋</td>
    </tr>
  </tbody>
</table>

<sub>✅ Completado · 🚧 En progreso · 📋 Pendiente</sub>

---

## 🛠️ Stack

<table>
  <tr>
    <td align="center" width="120"><strong>Frontend</strong></td>
    <td>
      <img src="https://img.shields.io/badge/React-61DAFB?logo=react&logoColor=black" />
      <img src="https://img.shields.io/badge/Next.js-000000?logo=nextdotjs&logoColor=white" />
      <img src="https://img.shields.io/badge/Tailwind-06B6D4?logo=tailwindcss&logoColor=white" />
      <img src="https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white" />
    </td>
  </tr>
  <tr>
    <td align="center"><strong>Backend</strong></td>
    <td>
      <img src="https://img.shields.io/badge/NestJS-E0234E?logo=nestjs&logoColor=white" />
      <img src="https://img.shields.io/badge/Prisma-2D3748?logo=prisma&logoColor=white" />
      <img src="https://img.shields.io/badge/JWT-000000?logo=jsonwebtokens&logoColor=white" />
    </td>
  </tr>
  <tr>
    <td align="center"><strong>Base de datos</strong></td>
    <td>
      <img src="https://img.shields.io/badge/PostgreSQL-4169E1?logo=postgresql&logoColor=white" />
      <img src="https://img.shields.io/badge/Supabase-3ECF8E?logo=supabase&logoColor=white" />
    </td>
  </tr>
  <tr>
    <td align="center"><strong>IA</strong></td>
    <td>
      <img src="https://img.shields.io/badge/OpenAI-412991?logo=openai&logoColor=white" />
    </td>
  </tr>
  <tr>
    <td align="center"><strong>DevOps</strong></td>
    <td>
      <img src="https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white" />
      <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?logo=githubactions&logoColor=white" />
      <img src="https://img.shields.io/badge/Vercel-000000?logo=vercel&logoColor=white" />
      <img src="https://img.shields.io/badge/Railway-0B0D0E?logo=railway&logoColor=white" />
    </td>
  </tr>
</table>

> ⚠️ Stack **propuesto**, aún no implementado. Se confirmará en `docs/05-arquitectura.md`.

---

## ✨ Diferenciadores clave

<div align="center">

<table>
  <tr>
    <td align="center" width="25%">
      <h3>🦷</h3>
      <strong>Odontograma visual</strong>
      <p><sub>Interactivo, no una tabla. 32 piezas FDI con estados clínicos y historial por pieza.</sub></p>
    </td>
    <td align="center" width="25%">
      <h3>🤖</h3>
      <strong>Asistente IA</strong>
      <p><sub>Function calling real contra la API. "¿Cuántas citas tuve esta semana?" con datos reales.</sub></p>
    </td>
    <td align="center" width="25%">
      <h3>🇲🇽</h3>
      <strong>Cumplimiento MX</strong>
      <p><sub>NOM-013-SSA2, NOM-004-SSA3, LFPDPPP y CFDI 4.0 documentados y aplicados.</sub></p>
    </td>
    <td align="center" width="25%">
      <h3>📱</h3>
      <strong>Mobile-first</strong>
      <p><sub>Diseñado para tablet en recepción. Español de México, moneda MXN.</sub></p>
    </td>
  </tr>
</table>

</div>

---

## 🗺️ Roadmap

<details open>
<summary><strong>📖 Fase 1 — Documentación</strong> (en progreso)</summary>

- [x] 01 — Visión y alcance
- [x] 02 — Caso de negocio
- [x] 03 — Requerimientos
- [x] 04 — Modelo de datos
- [ ] 05 — Arquitectura
- [ ] 06 — Decisiones técnicas (ADRs)
- [ ] 07 — Cumplimiento México
- [ ] 08 — Manual de usuario
- [ ] 09 — API
- [ ] 10 — Roadmap final

</details>

<details>
<summary><strong>⚙️ Fase 2 — MVP Backend</strong></summary>

- [ ] Setup monorepo + deploy inicial
- [ ] Auth + roles + permisos
- [ ] CRUD pacientes + historial médico
- [ ] Agenda con validaciones de solapamiento
- [ ] Odontograma + planes de tratamiento
- [ ] Presupuestos + pagos + factura simulada
- [ ] Inventario con alertas
- [ ] Dashboard con KPIs
- [ ] Auditoría
- [ ] Asistente IA (function calling)
- [ ] Resumen de historial con IA

</details>

<details>
<summary><strong>🎨 Fase 3 — Frontend y UX</strong></summary>

- [ ] Diseño responsive mobile-first
- [ ] Calendario interactivo
- [ ] Odontograma SVG interactivo
- [ ] Dashboard con gráficas
- [ ] Modo PWA instalable

</details>

<details>
<summary><strong>🧪 Fase 4 — Calidad y lanzamiento</strong></summary>

- [ ] Tests ≥ 60% cobertura en lógica de negocio
- [ ] CI/CD con GitHub Actions
- [ ] Seeds de demo
- [ ] Deploy público con datos demo
- [ ] Video demo (3–5 min)
- [ ] Documentación de API (Swagger)

</details>

---

## 🏗️ Estado actual

<div align="center">

| Fase | Progreso |
|---|---|
| 📖 Documentación | ![](https://geps.dev/progress/40) |
| ⚙️ Backend MVP | ![](https://geps.dev/progress/0) |
| 🎨 Frontend | ![](https://geps.dev/progress/0) |
| 🧪 Calidad | ![](https://geps.dev/progress/0) |

</div>

> El proyecto está en **fase de diseño y documentación**. La implementación comenzará una vez cerrada la arquitectura (doc 05).

---

## 🚀 Cómo correrlo (cuando esté listo)

```bash
# Próximamente...
git clone https://github.com/TU-USUARIO/dentalflow.git
cd dentalflow
pnpm install
docker-compose up -d
pnpm dev
<sub>📌 Esta sección se actualizará cuando el MVP esté implementado.</sub>

Contribuciones
Este es un proyecto de portafolio personal, pero issues y sugerencias son bienvenidos. Si encuentras algo interesante o quieres discutir decisiones de diseño, abre un issue.

Licencia
Este proyecto está bajo la licencia MIT. Ver LICENSE para más detalles.

📬 Contacto
<div align="center">
Tu Nombre · Desarrollador

https://img.shields.io/badge/GitHub-TU--USUARIO-181717?style=for-the-badge&logo=github
https://img.shields.io/badge/LinkedIn-TU--PERFIL-0A66C2?style=for-the-badge&logo=linkedin
https://img.shields.io/badge/Email-tu%40email.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white

</div>
<div align="center"> <sub>Hecho con ❤️ y mucho ☕ en México 🇲🇽</sub> <br /> <sub>⭐ Si el proyecto te parece interesante, dale una estrella ⭐</sub> </div> ```


