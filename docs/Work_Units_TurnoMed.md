# Mapa Definitivo de Historias de Usuario (Work Units) — Proyecto TurnoMed

**Proyecto:** TurnoMed — *El Asana del turno médico*  
**Autores:** Javier Arias Fuentes · José Antonio García Cadenas  
**Base metodológica:** Lean Canvas (`TurnoMed.pdf`), Memoria CMEPPS 2026 (`TurnoMed_Memoria.pdf`) y plantilla de referencia *Caso de Estudio GESCON*.  
**Archivo de Mockups en Figma (Material 3 Expressive · 20 frames verificados):** [TurnoMed — Mockup Inicial (Material 3 Expressive)](https://www.figma.com/design/7laFRj9vs1fFfJOvPW4M1M)  
**Hoja de Cálculo Scrum en Google Sheets (9 pestañas + 8 gráficas nativas · equipo 2 personas):** [TurnoMed — Planificación Scrum, Burn-Up y Burn-Down](https://docs.google.com/spreadsheets/d/1qL701EOC4GaMRSGrcTq-fuIUbtDCPi0PBlGLCfoaxNA/edit)  
**Documento Entregable Maquetado en Google Docs (35 págs. · 8 gráficas + 20 mockups):** [TurnoMed — Memoria Scrum, Historias de Usuario, Mockups y Medición (Google Docs)](https://docs.google.com/document/d/1ZHkfnNMYOtaFF8DL-vyzU8p1XcJS6Bp5340Wi5yr8K0/edit) · Copia PDF: [`TurnoMed_Memoria_SCRUM_GoogleDocs.pdf`](TurnoMed_Memoria_SCRUM_GoogleDocs.pdf)  
**Planificación Scrum, Sprints, Burn-Up, Burn-Down y Medición (Tema 5):** [`Planificacion_SCRUM_TurnoMed.md`](Planificacion_SCRUM_TurnoMed.md) · Copia PDF Sheets: [`TurnoMed_SCRUM_GoogleSheets.pdf`](TurnoMed_SCRUM_GoogleSheets.pdf)

---

## 1. Decisiones y Correcciones respecto al Borrador Inicial

1. **Fuente única de verdad y suma verificada:** Se unifican las discrepancias entre las versiones previas (`87` vs. `92` vs. `95` pts) y se calibra toda la escala de Fibonacci (`1, 2, 3, 5, 8, 13`), quedando el Product Backlog en **94 puntos de historia** repartidos en **19 Work Units** (mismo orden de magnitud que *GESCON*: 19 WUs, 93 pts).
2. **Roles estrictamente humanos en Scrum:** En **WU-03** se sustituye *"Sistema Validador"* por **`Sanitario / Supervisor de Planta`**.
3. **Coherencia de Riesgos y Urgencias:** Se elevan a `Riesgo: Medio` las historias con impacto legal/RGPD o pagos (**WU-16**, **WU-17**, **WU-18**, **WU-19**), y a `Urgencia: Media` los habilitadores de arranque (**WU-16**, **WU-18**).
4. **Sprints equilibrados para Burn-Up / Burn-Down:** Se corrige el desequilibrio anterior (`41 / 18 / 18 / 18`) hacia **4 Sprints de velocidad estable (`25 / 24 / 23 / 22` pts)** con **Release 1.0 (MVP) en el Sprint 2 (49 pts)**.
5. **Arquitectura coherente con la Memoria:**
   * **App Móvil (412×915 · Material 3 Expressive):** Historias operativas del Sanitario (**WU-01, 02, 03, 07, 08, 10, 15, 18**).
   * **Panel Web (1280×820 · Material 3 Expressive):** Gestión de Supervisión (**WU-04, 05, 06, 09, 11**), Dirección/RRHH (**WU-12, 13, 14**), Administración (**WU-16, 19**) y Alta B2B (**WU-17**).
6. **Reutilización realista de pantallas (mocks compartidos):** Siguiendo el criterio de *GESCON*, varias historias comparten la misma pantalla base cambiando el desplegable, pestaña o modal abierto (p. ej. **WU-02 + WU-03 + WU-01 + WU-10**, **WU-05 + WU-09 + WU-06**, **WU-16 + WU-19**).
7. **Pruebas de aceptación:** Se incluyen en las historias con lógica de negocio relevante; en **WU-18** y **WU-19** se marcan como opcionales/ligeras (en *GESCON* dichas historias no requieren pruebas exhaustivas).

---

## 2. Resumen del Product Backlog (19 Work Units · 94 Puntos)

| ID | Nombre de la Work Unit (HU) | Usuario / Rol | Importancia | Urgencia | Riesgo | Esfuerzo (Fibonacci) | Sprint | Plataforma y Mockup en Figma |
| :--- | :--- | :--- | :---: | :---: | :---: | :---: | :---: | :--- |
| **WU-01** | Publicación de guardia para intercambio | Sanitario | Muy Alta | Alta | Bajo | **5** | S1 | Móvil · Sheet sobre WU-02 |
| **WU-02** | Solicitud y acuerdo de cambio entre compañeros (P2P) | Sanitario | Muy Alta | Alta | Medio | **5** | S1 | Móvil · Base Tablón P2P |
| **WU-03** | Validación automática del descanso normativo (Regla 12h) | Sanitario / Supervisor | Muy Alta | Muy Alta | Alto | **13** | S2 | Móvil · Bottom Sheet sobre WU-02 |
| **WU-04** | Panel de aprobación en un clic para el supervisor | Supervisor de Planta | Muy Alta | Alta | Bajo | **3** | S2 | Web · Bandeja Aprobación 1-Clic |
| **WU-05** | Actualización y exportación automática del cuadrante oficial | Supervisor de Planta | Alta | Media | Medio | **5** | S2 | Web · Base Cuadrante + Menú Exportar |
| **WU-06** | Alerta de guardia urgente / Cobertura exprés de bajas | Supervisor de Planta | Alta | Alta | Medio | **8** | S3 | Web · Side Sheet sobre WU-05 |
| **WU-07** | Calendario personal interactivo y sincronización externa | Sanitario | Media | Media | Bajo | **8** | S3 | Móvil · Base Agenda Personal |
| **WU-08** | Banco de saldos de guardias y turnos (Fair-Play) | Sanitario / Supervisor | Media | Baja | Bajo | **3** | S4 | Móvil · Vista Fair-Play |
| **WU-09** | Carga y gestión del cuadrante base mensual del servicio | Supervisor de Planta | Alta | Alta | Medio | **8** | S1 | Web · Modo Borrador sobre WU-05 |
| **WU-10** | Modificación o retirada de oferta/propuesta de cambio | Sanitario | Baja | Baja | Bajo | **2** | S3 | Móvil · Pestaña *Mis ofertas* + Menú |
| **WU-11** | Gestión de avisos y comunicados de planta | Supervisor de Planta | Media | Baja | Bajo | **2** | S4 | Web · Avisos y Borradores |
| **WU-12** | Parametrización de reglas normativas y convenios del centro | Dirección RRHH / Admin | Media | Media | Medio | **3** | S2 | Web · Convenios y Catálogo Turnos |
| **WU-13** | Cuadro de mandos y analítica de cumplimiento legal (B2B) | Dirección RRHH / Gerencia | Media | Baja | Bajo | **5** | S4 | Web · Dashboard B2B |
| **WU-14** | Auditoría de permutas y certificados de trazabilidad legal | Supervisor / Dirección RRHH | Media | Baja | Bajo | **3** | S4 | Web · Tabla Auditoría + Preview PDF |
| **WU-15** | Gestión de indisponibilidades, vacaciones y permisos | Sanitario / Supervisor | Media | Media | Bajo | **5** | S3 | Móvil · Pestaña Permisos sobre Agenda |
| **WU-16** | Gestión de personal sanitario y estructura de servicios | Administrador | Baja | Media | Medio | **5** | S1 | Web · Base Admin Personal/Servicios |
| **WU-17** | Suscripción de centro hospitalario y Plan (Freemium / PRO) | Gestor Hospitalario / Visitante | Baja | Baja | Medio | **8** | S4 | Web Pública · Alta y Planes B2B |
| **WU-18** | Autenticación y control de acceso multi-rol | Visitante / Usuario | Baja | Media | Medio | **2** | S1 | Móvil · Login + Sheet Multi-Rol |
| **WU-19** | Registro de accesos al sistema (Seguridad RGPD) | Administrador | Baja | Muy Baja | Medio | **1** | S4 | Web · Logs RGPD sobre WU-16 |

**Verificación de Fibonacci:** `1 (×1) + 2 (×3) + 3 (×4) + 5 (×6) + 8 (×4) + 13 (×1) = 1 + 6 + 12 + 30 + 32 + 13 = 94 puntos`.

---

## 3. Plan de Entregas (Releases), Sprints Equilibrados y Trazabilidad Figma

* **Horizonte y capacidad (equipo real de 2 personas — Javier y José Antonio):** 4 Sprints de 2 semanas (10 días laborables c/u · `05 Oct – 27 Nov 2026`) · `160 h reales/sprint` → `30 %` sobrecarga → `112 h ideales` disponibles · `1 SP = 4 h ideales` (`376 h ideales` totales; velocidad prevista `V = 24 pts/sprint = 96 h`).
* **Desarrollo completo en Google Sheets (tablas con fórmulas vivas y 8 gráficas nativas):** [Hoja Google Sheets TurnoMed](https://docs.google.com/spreadsheets/d/1qL701EOC4GaMRSGrcTq-fuIUbtDCPi0PBlGLCfoaxNA/edit) y [`Planificacion_SCRUM_TurnoMed.md`](Planificacion_SCRUM_TurnoMed.md).

| Sprint | Fechas | Work Units planificadas | Plan (SP / h ideales) | Ejecución real simulada (SP) | Acumulado Real | Hito / Release | Objetivo del Incremento |
| :---: | :---: | :--- | :---: | :---: | :---: | :--- | :--- |
| **Sprint 1** | 05–16 Oct | `WU-18 (2)` + `WU-16 (5)` + `WU-09 (8)` + `WU-01 (5)` + `WU-02 (5)` | **25** (100 h) | **25** | 25 | Base Operativa | Acceso multi-rol, plantilla de planta, cuadrante base mensual y tablón P2P activo. |
| **Sprint 2** | 19–30 Oct | `WU-12 (3)` + `WU-03 (13)` + `WU-04 (3)` + `WU-05 (5)` | **24** (96 h) | **24** | **49** | **Release 1.0 (MVP)** | Motor legal de 12h parametrizable, aprobación en 1 clic y cuadrante oficial exportable. |
| **Sprint 3** | 02–13 Nov | `WU-06 (8)` + `WU-07 (8)` + `WU-15 (5)` + `WU-10 (2)` | **23** (92 h) | **21** *(WU-10 → S4)* | **70** | **Release 1.1** | Cobertura exprés de bajas, calendario móvil con Google/iCal y permisos *(carry-over `WU-10` por OAuth)*. |
| **Sprint 4** | 16–27 Nov | `WU-10 (2)*` + `WU-08 (3)` + `WU-11 (2)` + `WU-13 (5)` + `WU-14 (3)` + `WU-17 (8)` + `WU-19 (1)` | **22** *(24 adj. / 96 h)* | **24** | **94** | **Release 1.2 (B2B)** | Cierre de `WU-10`, Fair-Play, avisos de planta, Dashboard B2B Lean, certificados legales, planes Freemium/PRO y auditoría RGPD. |

### 3.1 Inventario Verificado de Mockups en Figma (`7laFRj9vs1fFfJOvPW4M1M`)

Todos los frames están construidos con **40 variables locales (`TurnoMed · M3 Expressive`)**, componentes nativos del **Material 3 Design Kit** y **3 componentes propios locales** (`3:44` Brand Logo, `3:70` Shift Badge, `3:85` Legal 12h Shield), con `0` imágenes rasterizadas:

| Página en Figma | Node IDs y Pantallas Verificadas |
| :--- | :--- |
| **01 · Design System & App Móvil (Sanitario)** *(9 frames · `412×915`)* | `00 · Guía Visual` ([`3:87`](https://www.figma.com/design/7laFRj9vs1fFfJOvPW4M1M?node-id=3-87)) · `01 · WU-02 Tablón P2P` ([`3:88`](https://www.figma.com/design/7laFRj9vs1fFfJOvPW4M1M?node-id=3-88)) · `02 · WU-03 Bloqueo 12h` ([`3:89`](https://www.figma.com/design/7laFRj9vs1fFfJOvPW4M1M?node-id=3-89)) · `03 · WU-01 Publicar Guardia` ([`9:179`](https://www.figma.com/design/7laFRj9vs1fFfJOvPW4M1M?node-id=9-179)) · `04 · WU-10 Mis Ofertas` ([`9:315`](https://www.figma.com/design/7laFRj9vs1fFfJOvPW4M1M?node-id=9-315)) · `05 · WU-07 Mi Agenda` ([`9:419`](https://www.figma.com/design/7laFRj9vs1fFfJOvPW4M1M?node-id=9-419)) · `06 · WU-15 Permisos` ([`10:316`](https://www.figma.com/design/7laFRj9vs1fFfJOvPW4M1M?node-id=10-316)) · `07 · WU-08 Fair-Play` ([`10:414`](https://www.figma.com/design/7laFRj9vs1fFfJOvPW4M1M?node-id=10-414)) · `08 · WU-18 Login Multi-Rol` ([`10:538`](https://www.figma.com/design/7laFRj9vs1fFfJOvPW4M1M?node-id=10-538)) |
| **02 · Panel Web · Supervisor de Planta** *(5 frames · `1280×820`)* | `09 · WU-04 Aprobación 1-Clic` ([`13:404`](https://www.figma.com/design/7laFRj9vs1fFfJOvPW4M1M?node-id=13-404)) · `10 · WU-05 Cuadrante Oficial` ([`13:535`](https://www.figma.com/design/7laFRj9vs1fFfJOvPW4M1M?node-id=13-535)) · `11 · WU-09 Borrador Mensual` ([`13:717`](https://www.figma.com/design/7laFRj9vs1fFfJOvPW4M1M?node-id=13-717)) · `12 · WU-06 Alerta Urgente` ([`14:460`](https://www.figma.com/design/7laFRj9vs1fFfJOvPW4M1M?node-id=14-460)) · `13 · WU-11 Avisos de Planta` ([`14:730`](https://www.figma.com/design/7laFRj9vs1fFfJOvPW4M1M?node-id=14-730)) |
| **03 · Panel Web · RRHH, Admin y Planes B2B** *(6 frames · `1280×820`)* | `14 · WU-13 Dashboard B2B` ([`13:872`](https://www.figma.com/design/7laFRj9vs1fFfJOvPW4M1M?node-id=13-872)) · `15 · WU-12 Convenios y Reglas` ([`13:1004`](https://www.figma.com/design/7laFRj9vs1fFfJOvPW4M1M?node-id=13-1004)) · `16 · WU-14 Auditoría PDF` ([`13:1130`](https://www.figma.com/design/7laFRj9vs1fFfJOvPW4M1M?node-id=13-1130)) · `17 · WU-16 Personal y Servicios` ([`15:444`](https://www.figma.com/design/7laFRj9vs1fFfJOvPW4M1M?node-id=15-444)) · `18 · WU-19 Accesos RGPD` ([`15:680`](https://www.figma.com/design/7laFRj9vs1fFfJOvPW4M1M?node-id=15-680)) · `19 · WU-17 Suscripción Freemium/PRO` ([`18:803`](https://www.figma.com/design/7laFRj9vs1fFfJOvPW4M1M?node-id=18-803)) |

---

## 4. Dataset Coherente Compartido entre Todos los Mockups

Para evitar contradicciones entre pantallas, todos los mocks utilizan el mismo escenario de **Hospital Universitario · Unidad de Urgencias (Noviembre–Diciembre 2026)**:
* **Sanitario autenticado (App Móvil):** Laura Gómez (`ENF-042`, Enfermería, Urgencias, Fair-Play `+1`). Turnos Noviembre: `16 M`, `19 M`, `21 M (Cobertura urgente)`, `22 G24`, `25 T (Ofertado)`, `27 T (Propuesta de Elena)`, `28 N`.
* **Compañeros de Urgencias:** Carlos Ruiz (`ENF-019`, Fair-Play `0`), Elena Morales (`ENF-014`, Fair-Play `-1`), Marta Sánchez (`ENF-031`, Fair-Play `-1`, baja imprevista Noche), Javier Castro (`ENF-027`, Fair-Play `+2`, saliente de Noche → conflicto `<12h`), Ana Belén Gil (`ENF-024`, Fair-Play `0`, vacaciones `20–26 Nov`), David López (`ENF-055`, Fair-Play `0`).
* **Supervisor de Planta (Web):** Dr. Martín Vega (`SUP-008`, roles: `Sanitario` + `Supervisor`).
* **Dirección RRHH (Web):** Elena Torres (`RRHH-002`).
* **Administrador (Web):** Admin Sistema (`ADM-001`).

---

## 5. Fichas Detalladas de las 19 Work Units (Formato GESCON)

### WU-01 — Publicación de guardia para intercambio
| Campo | Valor | Campo | Valor |
| :--- | :--- | :--- | :--- |
| **Usuario** | Sanitario | **Nombre** | Publicación de guardia para intercambio |
| **Importancia** | Muy Alta | **Urgencia** | Alta |
| **Riesgo** | Bajo | **Esfuerzo a priori (en puntos)** | **5** |

* **Descripción:** El sanitario selecciona uno de sus turnos futuros asignados y lo publica en el tablón de su servicio indicando qué fechas o franjas prefiere a cambio, o marcándolo como abierto a propuestas / cesión al banco de saldos. La oferta únicamente es visible para compañeros de su misma categoría profesional y unidad.
* **Mockup Figma:** Página 1 · `03 · WU-01 · Publicar Guardia (Sheet sobre Tablón)` *(comparte marco base con WU-02)*.
* **Pruebas de Aceptación (algunas ideas):**
  * Solo permitir publicar turnos asignados al sanitario autenticado y con fecha futura superior a la antelación mínima.
  * Impedir publicar un turno que ya tenga una oferta activa o un acuerdo pendiente.
  * Permitir seleccionar fechas/franjas preferidas o activar la modalidad «Abierto / Banco Fair-Play».
  * Restringir la visibilidad de la oferta a profesionales de la misma categoría y servicio.
  * Cambiar el estado visual del turno a «Ofertado» en el calendario personal tras publicar.

---

### WU-02 — Solicitud y acuerdo de cambio entre compañeros (Peer-to-Peer)
> *Nota:* Conviene implementar esta WU tras **WU-01**, ya que opera sobre las ofertas publicadas en el tablón.

| Campo | Valor | Campo | Valor |
| :--- | :--- | :--- | :--- |
| **Usuario** | Sanitario | **Nombre** | Solicitud y acuerdo de cambio entre compañeros (Peer-to-Peer) |
| **Importancia** | Muy Alta | **Urgencia** | Alta |
| **Riesgo** | Medio | **Esfuerzo a priori (en puntos)** | **5** |

* **Descripción:** Un sanitario consulta las guardias publicadas por compañeros de su misma categoría y servicio y se postula proponiendo un turno propio disponible a cambio (o asumiéndola contra el banco de saldos). Cuando el ofertante acepta una propuesta, se cancelan las demás postulaciones y el acuerdo cerrado pasa automáticamente a la bandeja del supervisor.
* **Mockup Figma:** Página 1 · `01 · WU-02 · Tablón P2P (App Sanitario)`.
* **Pruebas de Aceptación (algunas ideas):**
  * Listar únicamente ofertas de compañeros de la misma categoría profesional y servicio, filtrables por tipo de turno.
  * Impedir postularse a una oferta propia o proponer un turno ya comprometido en otro acuerdo.
  * Notificar al ofertante cada nueva propuesta y permitirle aceptarla o rechazarla.
  * Al aceptar una propuesta, descartar automáticamente el resto de postulaciones sobre esa guardia y enviarla al supervisor.

---

### WU-03 — Validación automática del descanso normativo (Regla de las 12 horas)
> *Nota:* Núcleo diferencial del MVP; se invoca en tiempo real durante **WU-02**, **WU-06** y **WU-09**. Comparte interfaz con **WU-02** mediante un Modal Bottom Sheet.

| Campo | Valor | Campo | Valor |
| :--- | :--- | :--- | :--- |
| **Usuario** | Sanitario / Supervisor de Planta | **Nombre** | Validación automática del descanso normativo (Regla de las 12 horas) |
| **Importancia** | Muy Alta | **Urgencia** | Muy Alta |
| **Riesgo** | Alto | **Esfuerzo a priori (en puntos)** | **13** |

* **Descripción:** Antes de confirmar cualquier propuesta o cobertura, el sistema evalúa automáticamente los turnos inmediatamente anteriores y posteriores de ambos implicados (incluyendo turnos nocturnos que cruzan medianoche y guardias de 24h). Si el intercambio supone menos de 12 horas de descanso obligatorio, solapes horarios, distinta categoría o exceso de jornada semanal, bloquea la operación explicando el conflicto exacto.
* **Mockup Figma:** Página 1 · `02 · WU-03 · Bloqueo Regla 12h (Estado Compartido)` *(Bottom Sheet sobre WU-02)*.
* **Pruebas de Aceptación (algunas ideas):**
  * Bloquear cualquier intercambio en el que alguno de los dos sanitarios disponga de menos de 12 horas continuadas entre jornadas.
  * Bloquear la operación si existe solapamiento horario, ausencia/baja activa o distinta categoría profesional.
  * Verificar que no se supera el tope máximo de horas semanales definido en convenio (**WU-12**).
  * Mostrar un desglose claro de los turnos en conflicto y la regla vulnerada antes de impedir el envío.
  * Etiquetar el acuerdo como «Cumple 12h legales» cuando supere todas las comprobaciones.

---

### WU-04 — Panel de aprobación en un clic para el supervisor
> *Nota:* Conviene implementar esta WU tras **WU-02** y **WU-03**, pues recibe únicamente acuerdos pre-validados legalmente.

| Campo | Valor | Campo | Valor |
| :--- | :--- | :--- | :--- |
| **Usuario** | Supervisor de Planta | **Nombre** | Panel de aprobación en un clic para el supervisor |
| **Importancia** | Muy Alta | **Urgencia** | Alta |
| **Riesgo** | Bajo | **Esfuerzo a priori (en puntos)** | **3** |

* **Descripción:** Presenta al supervisor de planta la bandeja de acuerdos cerrados entre sanitarios y ya pre-validados por el motor legal de 12 horas, ordenados por proximidad de la guardia. Permite aprobar cada solicitud en un solo clic (o en lote) o rechazarla indicando un motivo obligatorio, notificando el resultado al instante a ambos implicados.
* **Mockup Figma:** Página 2 · `09 · WU-04 · Panel Aprobación 1-Clic (Supervisor)`.
* **Pruebas de Aceptación (algunas ideas):**
  * Ordenar automáticamente las solicitudes pendientes por cercanía temporal de la guardia afectada.
  * Aprobar una permuta en un único clic, cambiando su estado a «Aprobada» y notificando a ambos sanitarios.
  * Exigir un motivo de rechazo obligatorio antes de confirmar un rechazo y mantener intacta la titularidad original.
  * Consultar el historial de resoluciones aprobadas y rechazadas en la unidad.

---

### WU-05 — Actualización y exportación automática del cuadrante oficial
| Campo | Valor | Campo | Valor |
| :--- | :--- | :--- | :--- |
| **Usuario** | Supervisor de Planta | **Nombre** | Actualización y exportación automática del cuadrante oficial |
| **Importancia** | Alta | **Urgencia** | Media |
| **Riesgo** | Medio | **Esfuerzo a priori (en puntos)** | **5** |

* **Descripción:** Cada vez que el supervisor aprueba una permuta o se adjudica una cobertura urgente, el sistema actualiza automáticamente la titularidad de los turnos en el cuadrante general del servicio, resalta los turnos modificados y registra la operación en auditoría. Permite exportar la vista semanal o mensual en PDF, Excel (`.xlsx`) o CSV para Dirección y RRHH.
* **Mockup Figma:** Página 2 · `10 · WU-05 · Cuadrante Oficial y Exportación`.
* **Pruebas de Aceptación (algunas ideas):**
  * Reflejar en tiempo real los nuevos titulares en el cuadrante del servicio tras cada aprobación o cobertura.
  * Resaltar visualmente las celdas permutadas respecto a la planificación inicial con información del cambio.
  * Registrar automáticamente en el log de auditoría fecha/hora, implicados, verificación 12h y supervisor aprobador.
  * Exportar el cuadrante semanal o mensual en formatos PDF, `.xlsx` y `.csv`.

---

### WU-06 — Alerta de guardia urgente / Cobertura exprés de bajas
> *Nota:* Reutiliza el motor legal de **WU-03** y la vista base del cuadrante (**WU-05**) mediante un panel lateral de alerta urgente.

| Campo | Valor | Campo | Valor |
| :--- | :--- | :--- | :--- |
| **Usuario** | Supervisor de Planta | **Nombre** | Alerta de guardia urgente / Cobertura exprés de bajas |
| **Importancia** | Alta | **Urgencia** | Alta |
| **Riesgo** | Medio | **Esfuerzo a priori (en puntos)** | **8** |

* **Descripción:** Ante una baja médica imprevista, el supervisor marca el turno como descubierto y lanza una alerta urgente en un clic. El sistema filtra automáticamente a los sanitarios de la misma categoría libres, sin permisos activos y que cumplan las 12 horas de descanso, les envía notificación push/email y adjudica la guardia al primero que acepte cerrando la convocatoria para el resto.
* **Mockup Figma:** Página 2 · `12 · WU-06 · Alerta Guardia Urgente (Side Sheet sobre WU-05)`.
* **Pruebas de Aceptación (algunas ideas):**
  * Permitir declarar un turno como «Baja urgente» y lanzar la convocatoria en un clic desde el cuadrante.
  * Excluir automáticamente a sanitarios de otra categoría, con solape, permiso/baja activa o menos de 12h de descanso.
  * Mostrar al supervisor la lista de elegibles notificados y el motivo de exclusión de los no elegibles.
  * Adjudicar atómicamente el turno al primer profesional que acepte, cerrando la alerta para los demás y actualizando cuadrante y Fair-Play.

---

### WU-07 — Calendario personal interactivo y sincronización externa
| Campo | Valor | Campo | Valor |
| :--- | :--- | :--- | :--- |
| **Usuario** | Sanitario | **Nombre** | Calendario personal interactivo y sincronización externa |
| **Importancia** | Media | **Urgencia** | Media |
| **Riesgo** | Bajo | **Esfuerzo a priori (en puntos)** | **8** |

* **Descripción:** Ofrece al sanitario su agenda personal en vista mensual y semanal con sus turnos codificados por color e icono (Mañana, Tarde, Noche, Guardia 24h) y su estado (Confirmado, Ofertado, Pendiente). Permite vincular la agenda con Google Calendar o suscribirse mediante enlace iCal (`.ics`) con actualización automática ante cambios aprobados.
* **Mockup Figma:** Página 1 · `05 · WU-07 · Mi Agenda y Sincronización`.
* **Pruebas de Aceptación (algunas ideas):**
  * Alternar entre vista mensual y semanal mostrando el código de color y estado de cada turno.
  * Consultar el detalle completo de cualquier día al pulsar sobre él.
  * Generar enlace de suscripción `.ics` y vincular con Google Calendar mediante OAuth.
  * Actualizar automáticamente el calendario externo al aprobarse una permuta o cobertura.

---

### WU-08 — Banco de saldos de guardias y turnos (Fair-Play)
| Campo | Valor | Campo | Valor |
| :--- | :--- | :--- | :--- |
| **Usuario** | Sanitario / Supervisor de Planta | **Nombre** | Banco de saldos de guardias y turnos (Fair-Play) |
| **Importancia** | Media | **Urgencia** | Baja |
| **Riesgo** | Bajo | **Esfuerzo a priori (en puntos)** | **3** |

* **Descripción:** Contabiliza automáticamente el balance de guardias asumidas o cedidas sin devolución recíproca inmediata (coberturas urgentes o cesiones abiertas), mostrando a cada sanitario su saldo neto (`+1` a favor / `-1` pendiente) y al supervisor el balance de equidad de la planta para evitar sobrecargar al mismo personal.
* **Mockup Figma:** Página 1 · `07 · WU-08 · Banco de Saldos Fair-Play`.
* **Pruebas de Aceptación (algunas ideas):**
  * Sumar `+1` al profesional que cubre un turno sin trueque recíproco y restar `-1` al cedente.
  * Dejar el saldo inalterado (`0`) en los trueques equivalentes 1×1.
  * Permitir filtrar el historial entre cambios de saldo y trueques recíprocos.
  * Mostrar el ranking de saldos de la unidad para favorecer un reparto equitativo.

---

### WU-09 — Carga y gestión del cuadrante base mensual del servicio
> *Nota:* Es imprescindible en el **Sprint 1** para poblar los turnos iniciales. Comparte la vista base de cuadrante (**WU-05**) en modo borrador/edición.

| Campo | Valor | Campo | Valor |
| :--- | :--- | :--- | :--- |
| **Usuario** | Supervisor de Planta | **Nombre** | Carga y gestión del cuadrante base mensual del servicio |
| **Importancia** | Alta | **Urgencia** | Alta |
| **Riesgo** | Medio | **Esfuerzo a priori (en puntos)** | **8** |

* **Descripción:** Permite al supervisor crear la planificación mensual de su servicio editando la cuadrícula o importando una plantilla Excel/CSV. Antes de publicarla, el sistema señala alertas de descanso inferior a 12 horas, solapes y franjas por debajo de la dotación mínima requerida, permitiendo guardar borradores antes de notificar al equipo.
* **Mockup Figma:** Página 2 · `11 · WU-09 · Carga Cuadrante Base (Modo Borrador sobre WU-05)`.
* **Pruebas de Aceptación (algunas ideas):**
  * Importar turnos mensuales desde Excel/CSV o editar manualmente celdas en la cuadrícula.
  * Detectar y resaltar en rojo cualquier encadenamiento que vulnere las 12 horas de descanso (p. ej. Noche → Mañana).
  * Advertir en ámbar si algún día no cubre la dotación mínima configurada para cada franja.
  * Guardar el cuadrante como borrador y publicarlo notificando a los sanitarios de la unidad.

---

### WU-10 — Modificación o retirada de oferta/propuesta de cambio
> *Nota:* Reutiliza la interfaz del Tablón P2P (**WU-02**) en la vista *Mis ofertas* con menú contextual abierto.

| Campo | Valor | Campo | Valor |
| :--- | :--- | :--- | :--- |
| **Usuario** | Sanitario | **Nombre** | Modificación o retirada de oferta/propuesta de cambio |
| **Importancia** | Baja | **Urgencia** | Baja |
| **Riesgo** | Bajo | **Esfuerzo a priori (en puntos)** | **2** |

* **Descripción:** Permite al sanitario editar las preferencias de una oferta publicada o retirar una oferta/propuesta enviada mientras no haya sido aprobada por el supervisor ni haya vencido el plazo mínimo previo al inicio del turno.
* **Mockup Figma:** Página 1 · `04 · WU-10 · Mis Ofertas · Editar / Retirar (Estado Compartido)`.
* **Pruebas de Aceptación (algunas ideas):**
  * Permitir editar fechas preferidas o cancelar ofertas propias aún no aprobadas.
  * Permitir retirar una propuesta enviada antes de su aprobación definitiva.
  * *(Excepción)* Bloquear edición y retirada si el cambio ya fue aprobado o supera el plazo límite previo al turno.
  * Notificar automáticamente a los compañeros postulados cuando se retira una oferta con candidaturas activas.

---

### WU-11 — Gestión de avisos y comunicados de planta
| Campo | Valor | Campo | Valor |
| :--- | :--- | :--- | :--- |
| **Usuario** | Supervisor de Planta | **Nombre** | Gestión de avisos y comunicados de planta |
| **Importancia** | Media | **Urgencia** | Baja |
| **Riesgo** | Bajo | **Esfuerzo a priori (en puntos)** | **2** |

* **Descripción:** Permite al supervisor redactar, guardar como borrador, modificar, eliminar (si no han sido enviados) y emitir comunicados internos por notificación push y email dirigidos a toda la unidad, a una categoría concreta o al personal de turno en una fecha específica.
* **Mockup Figma:** Página 2 · `13 · WU-11 · Gestión de Avisos de Planta`.
* **Pruebas de Aceptación (algunas ideas):**
  * Filtrar destinatarios por unidad completa, categoría profesional o fecha asignada.
  * Guardar borradores para editarlos posteriormente y eliminar únicamente los avisos no enviados.
  * Consultar el histórico de avisos enviados en modo solo lectura con fecha, destinatarios y asunto.

---

### WU-12 — Parametrización de reglas normativas y convenios del centro
| Campo | Valor | Campo | Valor |
| :--- | :--- | :--- | :--- |
| **Usuario** | Dirección de RRHH / Administrador | **Nombre** | Parametrización de reglas normativas y convenios del centro |
| **Importancia** | Media | **Urgencia** | Media |
| **Riesgo** | Medio | **Esfuerzo a priori (en puntos)** | **3** |

* **Descripción:** Permite adaptar el motor validador (**WU-03**) al convenio autonómico o interno del hospital: descanso mínimo entre jornadas (nunca inferior a 12h legales), descanso semanal (36h), tope semanal (48h), antelación mínima de solicitud y catálogo editable de tipos de turno (código, horario, duración y color).
* **Mockup Figma:** Página 3 · `15 · WU-12 · Parametrización Reglas y Convenios`.
* **Pruebas de Aceptación (algunas ideas):**
  * Editar los parámetros normativos solicitando confirmación explícita antes de aplicarlos al motor validador.
  * Impedir guardar un descanso interjornada inferior a las 12 horas estatutarias.
  * Añadir, editar y eliminar tipos de turno (código único, horario, duración calculada y color identificativo).

---

### WU-13 — Cuadro de mandos y analítica de cumplimiento legal (Dashboard B2B)
| Campo | Valor | Campo | Valor |
| :--- | :--- | :--- | :--- |
| **Usuario** | Dirección de RRHH / Gerencia | **Nombre** | Cuadro de mandos y analítica de cumplimiento legal (Dashboard B2B) |
| **Importancia** | Media | **Urgencia** | Baja |
| **Riesgo** | Bajo | **Esfuerzo a priori (en puntos)** | **5** |

* **Descripción:** Proporciona a Gerencia y Dirección de RRHH las métricas clave definidas en la Memoria filtrables por unidad (Urgencias, UCI, Quirófanos, Planta) y rango de fechas: tiempo medio de resolución (`< 2h`), tasa de cobertura de bajas (`> 95%`), cumplimiento de la regla de 12h (`100%`) con intentos bloqueados y usuarios activos (`WAU/MAU`), con exportación a PDF.
* **Mockup Figma:** Página 3 · `14 · WU-13 · Dashboard B2B Cumplimiento Legal`.
* **Pruebas de Aceptación (algunas ideas):**
  * Filtrar todos los KPIs, gráficos y tablas por unidad clínica (incluyendo Planta) y rango de fechas.
  * Mostrar el recuento de intentos de infracción de descanso bloqueados preventivamente.
  * Comparar gráficamente rendimiento y cobertura entre unidades y exportar el informe ejecutivo en PDF.

---

### WU-14 — Auditoría de permutas y certificados de trazabilidad legal
| Campo | Valor | Campo | Valor |
| :--- | :--- | :--- | :--- |
| **Usuario** | Supervisor de Planta / Dirección de RRHH | **Nombre** | Auditoría de permutas y certificados de trazabilidad legal |
| **Importancia** | Media | **Urgencia** | Baja |
| **Riesgo** | Bajo | **Esfuerzo a priori (en puntos)** | **3** |

* **Descripción:** Permite consultar, buscar, ordenar y configurar columnas del histórico inmutable de permutas y coberturas (implicados seudonimizados, turnos, verificación 12h y aprobador), así como previsualizar y descargar certificados PDF con sello temporal ante Inspección de Trabajo.
* **Mockup Figma:** Página 3 · `16 · WU-14 · Auditoría y Certificados Legales`.
* **Pruebas de Aceptación (algunas ideas):**
  * Filtrar registros por sanitario/código RGPD, unidad, rango de fechas y estado (Aprobada / Rechazada).
  * Permitir seleccionar columnas visibles y ordenar por fecha de guardia o fecha de resolución.
  * Generar certificado PDF oficial con sello temporal y desglose exacto de horas de descanso.

---

### WU-15 — Gestión de indisponibilidades, vacaciones y permisos reglamentarios
> *Nota:* Reutiliza la navegación base del Sanitario (**WU-07**) en la sección de Permisos y se integra con **WU-03** y **WU-06** para excluir automáticamente al profesional ausente.

| Campo | Valor | Campo | Valor |
| :--- | :--- | :--- | :--- |
| **Usuario** | Sanitario / Supervisor de Planta | **Nombre** | Gestión de indisponibilidades, vacaciones y permisos reglamentarios |
| **Importancia** | Media | **Urgencia** | Media |
| **Riesgo** | Bajo | **Esfuerzo a priori (en puntos)** | **5** |

* **Descripción:** Permite al sanitario solicitar vacaciones, días de libre disposición o comunicar bajas médicas, y al supervisor validarlas. Las ausencias aprobadas bloquean esas fechas en el calendario, avisan si dejan alguna guardia asignada descubierta (ofreciendo lanzar cobertura urgente) y excluyen automáticamente al sanitario de alertas urgentes.
* **Mockup Figma:** Página 1 · `06 · WU-15 · Permisos y Ausencias (Estado Compartido)`.
* **Pruebas de Aceptación (algunas ideas):**
  * Registrar solicitudes con tipo de permiso, fecha inicio/fin válida y observaciones.
  * Detectar y advertir si existen turnos asignados dentro del periodo solicitado.
  * Ofrecer publicar en tablón o lanzar alerta urgente sobre los turnos afectados al aprobar la ausencia.
  * Excluir automáticamente al sanitario de alertas de guardia urgente durante el periodo bloqueado.

---

### WU-16 — Gestión de personal sanitario y estructura de servicios
| Campo | Valor | Campo | Valor |
| :--- | :--- | :--- | :--- |
| **Usuario** | Administrador | **Nombre** | Gestión de personal sanitario y estructura de servicios |
| **Importancia** | Baja | **Urgencia** | Media |
| **Riesgo** | Medio | **Esfuerzo a priori (en puntos)** | **5** |

* **Descripción:** Permite al administrador dar de alta, editar, consultar y dar de baja servicios hospitalarios y usuarios con código seudonimizado RGPD, categoría profesional (Enfermero/a, MIR, Adjunto) y asignación multi-rol (Sanitario, Supervisor, RRHH, Administrador), enviando las credenciales iniciales por correo corporativo.
* **Mockup Figma:** Página 3 · `17 · WU-16 · Gestión de Personal y Servicios`.
* **Pruebas de Aceptación (algunas ideas):**
  * Buscar, filtrar (por servicio, categoría y rol) y ordenar el listado de usuarios y gestionar los servicios del centro.
  * Permitir alta, edición y baja de usuarios con confirmación previa y envío automático de credenciales por email.
  * Impedir la baja de un sanitario que tenga turnos futuros asignados o acuerdos en curso.
  * Validar unicidad de correo y código RGPD y obligatoriedad de al menos un rol asignado.

---

### WU-17 — Suscripción de centro hospitalario y gestión de Plan (Freemium / PRO)
| Campo | Valor | Campo | Valor |
| :--- | :--- | :--- | :--- |
| **Usuario** | Gestor Hospitalario / Visitante | **Nombre** | Suscripción de centro hospitalario y gestión de Plan (Freemium / PRO) |
| **Importancia** | Baja | **Urgencia** | Baja |
| **Riesgo** | Medio | **Esfuerzo a priori (en puntos)** | **8** |

* **Descripción:** Permite dar de alta una unidad piloto en el Plan Freemium (gratuito hasta 15 sanitarios en 1 planta) o contratar el Plan PRO B2B Hospitalario (plantas ilimitadas, motor normativo completo, exportación RRHH y Dashboard B2B), calculando el coste según el número de plantas, procesando pago seguro con tarjeta y emitiendo factura PDF.
* **Mockup Figma:** Página 3 · `19 · WU-17 · Suscripción Centro Hospitalario (Freemium / PRO)`.
* **Pruebas de Aceptación (algunas ideas):**
  * Controlar el límite de 15 profesionales y 1 unidad en modalidad Freemium, sugiriendo cambio a PRO si se supera.
  * Advertir ante intentos de registro duplicado de un mismo centro (nombre o CIF).
  * Calcular dinámicamente el importe total según plantas/licencias, validar pago con tarjeta y generar recibo PDF.

---

### WU-18 — Autenticación y control de acceso multi-rol
| Campo | Valor | Campo | Valor |
| :--- | :--- | :--- | :--- |
| **Usuario** | Visitante / Usuario Registrado | **Nombre** | Autenticación y control de acceso multi-rol |
| **Importancia** | Baja | **Urgencia** | Media |
| **Riesgo** | Medio | **Esfuerzo a priori (en puntos)** | **2** |

* **Descripción:** Control de acceso mediante `userid` o correo corporativo y contraseña, con recuperación por email. Si el usuario autenticado dispone de múltiples roles (p. ej. Sanitario y Supervisor), muestra un selector de perfil antes de iniciar la sesión.
* **Mockup Figma:** Página 1 · `08 · WU-18 · Autenticación y Selector Multi-Rol`.
* **Pruebas de Aceptación *(opcionales, estándar como en GESCON)*:**
  * Validar credenciales y bloquear temporalmente tras intentos fallidos consecutivos.
  * Solicitar el rol activo tras el login cuando el usuario posee más de un perfil asignado.
  * Enviar enlace temporal de restablecimiento por email ante olvido de contraseña.

---

### WU-19 — Registro de accesos al sistema (Seguridad RGPD)
> *Nota:* Reutiliza el contenedor base del Panel de Administración (**WU-16**).

| Campo | Valor | Campo | Valor |
| :--- | :--- | :--- | :--- |
| **Usuario** | Administrador | **Nombre** | Registro de accesos al sistema (Seguridad RGPD) |
| **Importancia** | Baja | **Urgencia** | Muy Baja |
| **Riesgo** | Medio | **Esfuerzo a priori (en puntos)** | **1** |

* **Descripción:** Consulta cronológica de los accesos al sistema para auditoría de seguridad y cumplimiento RGPD, mostrando fecha-hora de login, `userid` seudonimizado, rol utilizado, dispositivo/IP, fecha-hora de logout y resultado del intento.
* **Mockup Figma:** Página 3 · `18 · WU-19 · Registro de Accesos RGPD (Estado Compartido sobre WU-16)`.
* **Pruebas de Aceptación *(opcionales, estándar como en GESCON)*:**
  * Mostrar listado de accesos filtrable por `userid`, rango de fechas (desde/hasta) y resultado (correcto/fallido).
