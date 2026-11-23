# Planificación Scrum, Seguimiento Ágil y Medición — Proyecto TurnoMed (Equipo de 2 Personas)

**Proyecto:** TurnoMed — *Plataforma Inteligente de Gestión e Intercambio de Guardias Sanitarias ("El Asana del turno médico")*  
**Autores y Equipo Scrum (2 personas):** Javier Arias Fuentes · José Antonio García Cadenas  
**Asignatura:** Calidad, Medición y Estimación de Productos y Procesos Software (CMEPPS 2026 · ETSI — Universidad de Huelva)  
**Fuentes vinculadas (fuente única de verdad):**
* **Memoria Entregable Maquetada en Google Docs (35 págs. · 8 gráficas + 20 mockups):** [TurnoMed — Memoria Scrum, Historias de Usuario, Mockups y Medición (Google Docs)](https://docs.google.com/document/d/1ZHkfnNMYOtaFF8DL-vyzU8p1XcJS6Bp5340Wi5yr8K0/edit) *(ID: `1ZHkfnNMYOtaFF8DL-vyzU8p1XcJS6Bp5340Wi5yr8K0` · copia PDF en [`TurnoMed_Memoria_SCRUM_GoogleDocs.pdf`](TurnoMed_Memoria_SCRUM_GoogleDocs.pdf))*
* **Hoja de Cálculo Viva en Google Sheets (9 pestañas con fórmulas + 8 gráficas nativas):** [TurnoMed — Planificación Scrum, Burn-Up y Burn-Down (Google Sheets)](https://docs.google.com/spreadsheets/d/1qL701EOC4GaMRSGrcTq-fuIUbtDCPi0PBlGLCfoaxNA/edit) *(ID: `1qL701EOC4GaMRSGrcTq-fuIUbtDCPi0PBlGLCfoaxNA` · copia PDF en [`TurnoMed_SCRUM_GoogleSheets.pdf`](TurnoMed_SCRUM_GoogleSheets.pdf))*
* **Mapa definitivo de Work Units (19 HUs · 94 puntos Fibonacci):** [`Work_Units_TurnoMed.md`](Work_Units_TurnoMed.md)
* **Prototipos completos en Figma (Material 3 Expressive · 20 frames editables):** [TurnoMed — Material 3 Expressive (Figma)](https://www.figma.com/design/7laFRj9vs1fFfJOvPW4M1M)
* **Lean Canvas y Memoria CMEPPS 2026:** [`TurnoMed.pdf`](Lean%20Canvas/TurnoMed.pdf) · [`TurnoMed_Memoria.pdf`](Lean%20Canvas/TurnoMed_Memoria.pdf)

---

## 1. Marco Metodológico, Roles Scrum (Equipo de 2 Personas) y Ceremonias

La gestión de **TurnoMed** aplica el marco ágil **Scrum** apoyado por gestión visual **Kanban** y el ciclo Lean **Construir – Medir – Aprender**. Aunque Scrum plantea como referencia industrial equipos de 4–8 personas, en un proyecto universitario / fase *seed* de **2 integrantes** ambos miembros compaginan sus responsabilidades de gestión (*Product Owner* y *Scrum Master*) con la implementación técnica, tal como recogen las diapositivas 14 (*"He can contribute as a team member"*) y 17 (*"As a responsibility. Performed by a Team-leader..."*) del Tema 4.

### 1.1 Roles Comprometidos (*Engaged*) e Implicados (*Involved*)

| Categoría | Rol Scrum | Responsable | Responsabilidades en TurnoMed |
| :--- | :--- | :--- | :--- |
| **Comprometido** | **Product Owner + Desarrollador Full-Stack** | **Javier Arias Fuentes** | Define la visión y priorización del Product Backlog (19 WUs), fija los cortes de Release y valida cada incremento; desarrolla arquitectura Backend, base de datos, motor legal 12 h (`WU-03`), integraciones (`OAuth/iCal`, Stripe) y pruebas de lógica. |
| **Comprometido** | **Scrum Master + Desarrollador Full-Stack / QA** | **José Antonio García Cadenas** | Vela por el proceso Scrum, facilita las ceremonias, mantiene actualizados los Burn-Down y protege los límites WIP; desarrolla la interfaz móvil y web en **Material 3 Expressive**, flujos UX y validación cruzada de pruebas de aceptación. |
| **Implicado** | **Stakeholders (Clientes y Usuarios)** | Supervisores de Urgencias, Sanitarios piloto, Dirección de RRHH y Gerencia Hospitalaria | Aportan feedback en las *Sprint Reviews*, confirman reglas del convenio sanitario y evalúan los KPIs Lean del piloto. |

### 1.2 Cadencia de Ceremonias y *Definition of Done* (DoD)

El horizonte se divide en **4 Sprints de 2 semanas (10 días laborables cada uno)**, totalizando **8 semanas** (**del 5 de octubre al 27 de noviembre de 2026**), dejando el **Release 1.0 (MVP)** desplegado para el piloto de noviembre–diciembre 2026 reflejado en los mockups:

| Ceremonia | Momento | Duración máx. | Objetivo clave |
| :--- | :--- | :---: | :--- |
| **Sprint Planning** | Día 1 (mañana) | 1,5 h | Selección del *Sprint Goal*, descomposición de WUs en tareas de `4–18 h ideales` repartidas entre Javier y José Antonio y cierre del *Sprint Backlog*. |
| **Daily Scrum** | Días 1–10 (09:15) | 15 min | Sincronización rápida entre ambos (hecho ayer, plan de hoy, bloqueos) y actualización diaria de horas pendientes en Google Sheets. |
| **Sprint Review** | Día 10 (mañana) | 1 h | Demostración informal sobre software funcional (sin diapositivas) y aceptación de historias por el PO. |
| **Sprint Retrospective** | Día 10 (tarde) | 30 min | Análisis de velocidad, bloqueos y acuerdos de mejora para el siguiente Sprint. |

**Definition of Done (DoD):** Una Work Unit solo computa puntos en la velocidad del Sprint cuando cumple: (1) código integrado y revisado de forma cruzada por el compañero, (2) interfaz fiel al sistema **Material 3 Expressive** en Figma, (3) 100 % de las pruebas de aceptación superadas (incluyendo casos límite de la regla de 12 h), (4) tratamiento de datos seudonimizados conforme al **RGPD**, y (5) aceptación del Product Owner.

---

## 2. Estimación Ágil, Capacidad del Equipo (2 Personas) y Velocidad

Siguiendo la descomposición de estimación ágil de Mike Cohn (Tema 4, diap. 32–36) y reflejada con fórmulas vivas en la pestaña **`Resumen_y_Capacidad`** de Google Sheets:

* **Tamaño del Product Backlog (Planning Poker · Fibonacci):** **19 Work Units** estimadas tomando **`WU-01` (Publicación de guardia = `5 SP`)** como referencia:
  $$1(\times 1) + 2(\times 3) + 3(\times 4) + 5(\times 6) + 8(\times 4) + 13(\times 1) = \mathbf{94\text{ Story Points}}$$
* **Tiempo Real vs. Tiempo Ideal (por Sprint de 10 días laborables · 2 personas):**
  * **Tiempo Real disponible:** $2\text{ personas} \times 8\text{ h/día} \times 10\text{ días} = \mathbf{160\text{ horas reales / sprint}}$.
  * **Sobrecarga operativa, ceremonias e imprevistos:** Aplicando un **30 %** (punto medio del rango `25 % – 35 %` de la diapositiva 36), quedan `48 h` de gestión/ceremonias y un **70 % de tiempo ideal efectivo**:
    $$\text{Capacidad Ideal} = 160 \times 0{,}70 = \mathbf{112\text{ horas ideales / sprint}} \quad (11{,}2\text{ h ideales/día} = 5{,}6\text{ h ideales/persona·día})$$
* **Conversión Story Points ↔ Horas Ideales y Velocidad Prevista:**
  * Calibración del equipo de 2 personas: **`1 Story Point = 4 horas ideales`** (media jornada ideal por Story Point; `WU-01 = 5 SP = 20 h ideales`).
  * **Esfuerzo ideal total del proyecto:** $94\text{ SP} \times 4\text{ h/SP} = \mathbf{376\text{ horas ideales}}$ (sobre `640 horas reales` totales en 4 Sprints = 8 semanas).
  * **Velocidad Prevista ($V$):** **`24 Story Points / sprint`** (`96 horas ideales / sprint`, ocupación del **85,7 %** respecto al techo de `112 h`, manteniendo un **colchón de calidad del 14,3 %** / `16 h` para absorber imprevistos y evitar la *Ley de Parkinson*).
* **Escenarios de sensibilidad para el Burn-Up del Plan de Producto (±20 %):**
  * **Velocidad Prevista ($V$):** `24,0 pts/sprint` (`96 h ideales`)
  * **Velocidad Optimista ($V_o = V \times 1{,}20$):** `28,8 pts/sprint` (`115,2 h`)
  * **Velocidad Pesimista ($V_p = V \times 0{,}80$):** `19,2 pts/sprint` (`76,8 h`)

---

## 3. Plan de Entregas (*Release Plan*) y Burn-Up del Plan de Producto

> **Pestaña y Gráfica nativa en Google Sheets:** [`BurnUp_Plan_Producto`](https://docs.google.com/spreadsheets/d/1qL701EOC4GaMRSGrcTq-fuIUbtDCPi0PBlGLCfoaxNA/edit#gid=102) · Gráfica nativa ID **`979463000`** (*Burn-Up del Plan de Producto — Releases 1.0, 1.1 y 1.2*).

| Release / Hito | Sprints | Work Units incluidas | Puntos Acum. | Horas Ideales | Sprint Previsto ($V=24$) | Escenario Optimista ($V_o=28{,}8$) | Escenario Pesimista ($V_p=19{,}2$) | Fecha Objetivo (Plan) |
| :--- | :---: | :--- | :---: | :---: | :---: | :---: | :---: | :---: |
| **Release 1.0 (MVP Piloto Urgencias)** | S1–S2 | `WU-18(2), WU-16(5), WU-09(8), WU-01(5), WU-02(5)` + `WU-12(3), WU-03(13), WU-04(3), WU-05(5)` | **49** | **196** | `2,04` → **Fin S2** (Sem. 4) | `1,70` (Sem. 3,4) | `2,55` (Sem. 5,1) | **30 Oct 2026** |
| **Release 1.1 (Cobertura Exprés y Movilidad)** | S3 | `WU-06(8), WU-07(8), WU-15(5), WU-10(2)` | **72** | **288** | `3,00` → **Fin S3** (Sem. 6) | `2,50` (Sem. 5,0) | `3,75` (Sem. 7,5) | **13 Nov 2026** |
| **Release 1.2 (Suite B2B Completa)** | S4 | `WU-08(3), WU-11(2), WU-13(5), WU-14(3), WU-17(8), WU-19(1)` | **94** | **376** | `3,92` → **Fin S4** (Sem. 8) | `3,26` (Sem. 6,5) | `4,90` (Sem. 9,8) | **27 Nov 2026** |

### 3.1 Tabla Base del Burn-Up del Plan de Producto (`BurnUp_Plan_Producto!A9:G15`)

| Sprint | $V$ Prevista (24/sp) | $V_o$ Optimista (28,8/sp) | $V_p$ Pesimista (19,2/sp) | Release 1.0 (MVP) | Release 1.1 | Release 1.2 (Total) |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: |
| **0 · Inicio (05 Oct)** | 0,0 | 0,0 | 0,0 | 49 | 72 | 94 |
| **Sprint 1 (16 Oct)** | 24,0 | 28,8 | 19,2 | 49 | 72 | 94 |
| **Sprint 2 (30 Oct)** | 48,0 | 57,6 | 38,4 | 49 | 72 | 94 |
| **Sprint 3 (13 Nov)** | 72,0 | 86,4 | 57,6 | 49 | 72 | 94 |
| **Sprint 4 (27 Nov)** | 96,0 | 115,2 | 76,8 | 49 | 72 | 94 |
| **Sprint 5 (11 Dic)** | 120,0 | 144,0 | 96,0 | 49 | 72 | 94 |

---

## 4. Seguimiento Real Simulado: Release Burn-Up (Forecast), Release Burn-Down y Velocidad

> **Pestaña y 3 Gráficas nativas en Google Sheets:** [`Seguimiento_y_Forecast`](https://docs.google.com/spreadsheets/d/1qL701EOC4GaMRSGrcTq-fuIUbtDCPi0PBlGLCfoaxNA/edit#gid=103)
> * Gráfica **`142147379`** — *Release Burn-Up: Seguimiento Real y Forecast (Corte S3 → Cierre S4)*
> * Gráfica **`1987538955`** — *Release Burn-Down Global (94 → 0 Story Points)*
> * Gráfica **`715665129`** — *Velocidad por Sprint: Comprometido vs. Completado (Done)*

| Iteración | Fechas | Alcance Total | Comprometido (SP) | Completado Done (SP) | Acumulado Real (SP) | Pendiente Release (SP) | Burn-Down Ideal (SP) | Forecast Esperado | Forecast Alto ($\mu+\sigma$) | Forecast Bajo ($\mu-\sigma$) |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **Inicio (S0)** | 05 Oct | 94 | 0 | 0 | 0 | **94** | 94,0 | — | — | — |
| **Sprint 1** | 05–16 Oct | 94 | 25 | **25** | **25** | **69** | 70,5 | — | — | — |
| **Sprint 2 (MVP)** | 19–30 Oct | 94 | 24 | **24** | **49** | **45** | 47,0 | — | — | — |
| **Sprint 3 (Corte)** | 02–13 Nov | 94 | 23 | **21** | **70** | **24** | 23,5 | **70,00** | 70,00 | 70,00 |
| **Sprint 4 (Cierre)** | 16–27 Nov | 94 | 24 *(22+2)* | **24** | **94** | **0** | 0,0 | **93,33** | 95,41 | 91,25 |

### 4.1 Estadísticas de Velocidad y *Forecast* (Tema 4, Diap. 50)
* **En el punto de control de fin de Sprint 3 (`70 SP` acumulados, `24 SP` pendientes):**
  * Velocidad media últimos 3 Sprints (`S1–S3: 25, 24, 21`): $\mu_{1..3} = \mathbf{23{,}33\text{ SP/sprint}}$ · Desviación estándar muestral: $\sigma_{1..3} = \mathbf{2{,}08\text{ SP}}$.
  * Proyección de cierre para Sprint 4: Esperado `93,33 SP`, Alto `95,41 SP`, Bajo `91,25 SP` → confirma viabilidad de cerrar el proyecto completo en Sprint 4 priorizando el *carry-over* de `WU-10 (2 SP = 8 h)` desde el Día 1.
* **Al cierre definitivo del proyecto (Fin Sprint 4 · 27 Nov 2026):**
  * Velocidad media global (`S1–S4: 25, 24, 21, 24`): $\mu_{1..4} = \mathbf{23{,}50\text{ SP/sprint}}$ · Desviación estándar $\sigma_{1..4} = \mathbf{1{,}73\text{ SP}}$ · Coeficiente de variación $CV = 7{,}4\%$ (ritmo altamente estable) · Cumplimiento: **`94 / 94 SP (100 %)`**.

---

## 5. Sprint Backlogs Diarios y Burn-Down Diario (Equipo de 2 Personas)

Todas las tablas de los 4 Sprints están implementadas con fórmulas dinámicas en Google Sheets (`=COUNTIF(...)`, `=SUM(...)`, `=$G$5*(10-d)/10`) y verificadas para que **ninguno de los 2 desarrolladores (Javier ni José Antonio) supere nunca las 6–7 horas ideales efectivas en una misma jornada**.

---

### 5.1 Sprint 1 — Base Operativa (`05 Oct – 16 Oct 2026`)
> **Google Sheets:** [`Sprint1_BurnDown`](https://docs.google.com/spreadsheets/d/1qL701EOC4GaMRSGrcTq-fuIUbtDCPi0PBlGLCfoaxNA/edit#gid=104) · Gráfica nativa ID **`904853470`**  
> **Compromiso:** `25 SP = 100 h ideales` (`50 h` Javier + `50 h` José Antonio) · **Velocidad ideal diaria:** `10,0 h/día` · **Resultado:** `25 / 25 SP` (*Done*).

| ID | WU | Descripción de la tarea | Tipo | Estado (D10) | Resp. | D0 | 5 Oct | 6 Oct | 7 Oct | 8 Oct | 9 Oct | 12 Oct | 13 Oct | 14 Oct | 15 Oct | 16 Oct |
| :---: | :---: | :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| — | — | **Tareas pendientes (> 0 h)** | — | — | — | **10** | **10** | **8** | **8** | **6** | **6** | **6** | **4** | **2** | **2** | **0** |
| — | — | **Horas ideales pendientes (Real)** | — | — | — | **100** | **94** | **86** | **76** | **66** | **54** | **42** | **30** | **18** | **8** | **0** |
| — | — | *Referencia Burn-Down Ideal (h)* | — | — | — | *100,0* | *90,0* | *80,0* | *70,0* | *60,0* | *50,0* | *40,0* | *30,0* | *20,0* | *10,0* | *0,0* |
| T1.1 | WU-18 | Modelo usuarios JWT, selector multi-rol y tests auth | Codif. | Terminada | Javier | 4 | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |
| T1.2 | WU-18 | UI móvil Login, recuperación y pruebas de bloqueo | Diseño/UI | Terminada | José Antonio | 4 | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |
| T1.3 | WU-16 | API CRUD personal RGPD, servicios y roles múltiples | Codif. | Terminada | Javier | 10 | 10 | 7 | 2 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |
| T1.4 | WU-16 | Panel Web Personal/Servicios + validación baja segura | Diseño/UI | Terminada | José Antonio | 10 | 10 | 7 | 2 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |
| T1.5 | WU-09 | Parser Excel/CSV y alertas borrador (solapes/dotación) | Análisis | Terminada | Javier | 16 | 16 | 16 | 16 | 13 | 7 | 1 | 0 | 0 | 0 | 0 |
| T1.6 | WU-09 | Cuadrícula editable Web (borrador) y pruebas cobertura | Diseño/UI | Terminada | José Antonio | 16 | 16 | 16 | 16 | 13 | 7 | 1 | 0 | 0 | 0 | 0 |
| T1.7 | WU-01 | Endpoints publicación guardia, antelación y visibilidad | Codif. | Terminada | Javier | 10 | 10 | 10 | 10 | 10 | 10 | 10 | 5 | 0 | 0 | 0 |
| T1.8 | WU-01 | Bottom Sheet móvil Publicar Guardia + tests aceptación | Diseño/UI | Terminada | José Antonio | 10 | 10 | 10 | 10 | 10 | 10 | 10 | 5 | 0 | 0 | 0 |
| T1.9 | WU-02 | Lógica ofertas P2P, candidaturas y descarte automático | Codif. | Terminada | Javier | 10 | 10 | 10 | 10 | 10 | 10 | 10 | 10 | 9 | 4 | 0 |
| T1.10 | WU-02 | Pantalla móvil Tablón P2P, filtros y pruebas E2E | Pruebas | Terminada | José Antonio | 10 | 10 | 10 | 10 | 10 | 10 | 10 | 10 | 9 | 4 | 0 |

* **Análisis Burn-Down S1:** Curva habitual de arranque (*usual behavior*): días D1–D3 ligeramente por encima de la recta ideal (`+6 h`) por la puesta en marcha del proyecto y sistema de diseño M3; a partir de D5 el par de desarrolladores mantiene `12 h/día`, igualando la línea ideal en D7 (`30 h`) y cerrando en `0 h` en D10.

---

### 5.2 Sprint 2 — Release 1.0 MVP (`19 Oct – 30 Oct 2026`)
> **Google Sheets:** [`Sprint2_BurnDown_MVP`](https://docs.google.com/spreadsheets/d/1qL701EOC4GaMRSGrcTq-fuIUbtDCPi0PBlGLCfoaxNA/edit#gid=105) · Gráfica nativa ID **`161294387`**  
> **Compromiso:** `24 SP = 96 h ideales` (`50 h` Javier + `46 h` José Antonio) · **Velocidad ideal diaria:** `9,6 h/día` · **Resultado:** `24 / 24 SP` (**Release 1.0 MVP entregada**).

| ID | WU | Descripción de la tarea | Tipo | Estado (D10) | Resp. | D0 | 19 Oct | 20 Oct | 21 Oct | 22 Oct | 23 Oct | 26 Oct | 27 Oct | 28 Oct | 29 Oct | 30 Oct |
| :---: | :---: | :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| — | — | **Tareas pendientes (> 0 h)** | — | — | — | **10** | **10** | **8** | **7** | **6** | **6** | **5** | **3** | **2** | **1** | **0** |
| — | — | **Horas ideales pendientes (Real)** | — | — | — | **96** | **86** | **76** | **71** | **59** | **47** | **35** | **23** | **13** | **4** | **0** |
| — | — | *Referencia Burn-Down Ideal (h)* | — | — | — | *96,0* | *86,4* | *76,8* | *67,2* | *57,6* | *48,0* | *38,4* | *28,8* | *19,2* | *9,6* | *0,0* |
| T2.1 | WU-12 | Entidad convenios, tope mínimo >=12h y tipos de turno | Codif. | Terminada | Javier | 6 | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |
| T2.2 | WU-12 | Panel Web Convenios y Catálogo Turnos + confirmación | Diseño/UI | Terminada | José Antonio | 6 | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |
| T2.3 | WU-03 | Diseño algoritmo ventanas descanso previo y posterior | Análisis | Terminada | Javier | 8 | 8 | 4 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |
| T2.4 | WU-03 | Motor legal 12h (noches medianoche + guardias 24h) `[+6h]` | Codif. | Terminada | Javier | 18 | 18 | 18 | **22** | 16 | 10 | 4 | 0 | 0 | 0 | 0 |
| T2.5 | WU-03 | Bottom Sheet móvil Bloqueo 12h y escudo legal M3 | Diseño/UI | Terminada | José Antonio | 12 | 12 | 8 | 3 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |
| T2.6 | WU-03 | Batería tests exhaustivos casos límite normativa 12h | Pruebas | Terminada | José Antonio | 14 | 14 | 14 | 14 | 11 | 5 | 0 | 0 | 0 | 0 | 0 |
| T2.7 | WU-04 | API bandeja aprobación 1-clic, lote y rechazo motivado | Codif. | Terminada | Javier | 6 | 6 | 6 | 6 | 6 | 6 | 6 | 4 | 0 | 0 | 0 |
| T2.8 | WU-04 | Panel Web Supervisor 1-Clic + pruebas aceptación | Diseño/UI | Terminada | José Antonio | 6 | 6 | 6 | 6 | 6 | 6 | 5 | 0 | 0 | 0 | 0 |
| T2.9 | WU-05 | Actualización atómica cuadrante, auditoría y export PDF/XLS | Codif. | Terminada | Javier | 12 | 12 | 12 | 12 | 12 | 12 | 12 | 12 | 10 | 4 | 0 |
| T2.10 | WU-05 | UI Cuadrante Oficial, menú Exportar y E2E Release 1.0 | Pruebas | Terminada | José Antonio | 8 | 8 | 8 | 8 | 8 | 8 | 8 | 7 | 3 | 0 | 0 |

* **Análisis Burn-Down S2:** El **Día 3 (21 Oct)**, los casos límite de turnos nocturnos (`22:00–08:00`) cruzando medianoche y guardias 24 h en **`T2.4` (`WU-03`, Riesgo Alto)** añaden `+6 h` de esfuerzo descubierto (`18 h → 22 h`, curva real `71 h vs. 67,2 h` ideal). En la *Daily Scrum* del Día 4, José Antonio aplica el límite **WIP ≤ 2**, frena el arranque de `WU-05` y refuerza en paralelo las pruebas de `WU-03` (`T2.6`), cruzando por debajo de la línea ideal en D5 (`47 h vs. 48,0 h`) y cerrando el MVP a tiempo.

---

### 5.3 Sprint 3 — Release 1.1 (`02 Nov – 13 Nov 2026`)
> **Google Sheets:** [`Sprint3_BurnDown`](https://docs.google.com/spreadsheets/d/1qL701EOC4GaMRSGrcTq-fuIUbtDCPi0PBlGLCfoaxNA/edit#gid=106) · Gráfica nativa ID **`196287044`**  
> **Compromiso:** `23 SP = 92 h ideales` (`48 h` Javier + `44 h` José Antonio) · **Velocidad ideal diaria:** `9,2 h/día` · **Resultado:** `21 / 23 SP` (*Done*: `WU-06, WU-07, WU-15`; **carry-over a S4:** `WU-10 · 2 SP = 8 h`).

| ID | WU | Descripción de la tarea | Tipo | Estado (D10) | Resp. | D0 | 2 Nov | 3 Nov | 4 Nov | 5 Nov | 6 Nov | 9 Nov | 10 Nov | 11 Nov | 12 Nov | 13 Nov |
| :---: | :---: | :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| — | — | **Tareas pendientes (> 0 h)** | — | — | — | **8** | **8** | **8** | **7** | **6** | **6** | **5** | **5** | **5** | **3** | **2** |
| — | — | **Horas ideales pendientes (Real)** | — | — | — | **92** | **82** | **72** | **62** | **52** | **42** | **39** | **30** | **20** | **12** | **8** |
| — | — | *Referencia Burn-Down Ideal (h)* | — | — | — | *92,0* | *82,8* | *73,6* | *64,4* | *55,2* | *46,0* | *36,8* | *27,6* | *18,4* | *9,2* | *0,0* |
| T3.1 | WU-06 | Motor filtrado elegibles 12h + adjudicación atómica | Codif. | Terminada | Javier | 18 | 13 | 8 | 3 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |
| T3.2 | WU-06 | Side Sheet Web Alerta Urgente + pruebas concurrencia | Diseño/UI | Terminada | José Antonio | 14 | 9 | 4 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |
| T3.3 | WU-07 | Feed iCal (.ics) y conector OAuth2 Google Calendar `[+4h]` | Codif. | Terminada | Javier | 16 | 16 | 16 | 16 | 14 | 9 | **11** | 6 | 1 | 0 | 0 |
| T3.4 | WU-07 | Vista Agenda móvil (mensual/semanal) y tests sync | Diseño/UI | Terminada | José Antonio | 16 | 16 | 16 | 15 | 10 | 5 | 0 | 0 | 0 | 0 | 0 |
| T3.5 | WU-15 | API solicitudes permisos/bajas y bloqueo en WU-06 | Codif. | Terminada | Javier | 10 | 10 | 10 | 10 | 10 | 10 | 10 | 10 | 9 | 4 | 0 |
| T3.6 | WU-15 | Pestaña móvil Permisos + aviso guardias y pruebas | Pruebas | Terminada | José Antonio | 10 | 10 | 10 | 10 | 10 | 10 | 10 | 6 | 2 | 0 | 0 |
| T3.7 | WU-10 | Edición/retirada oferta + aviso a postulados *(→ S4)* | Codif. | **Pendiente** | Javier | 4 | 4 | 4 | 4 | 4 | 4 | 4 | 4 | 4 | 4 | **4** |
| T3.8 | WU-10 | Menú contextual Mis Ofertas + bloqueo plazo *(→ S4)* | Diseño/UI | **Pendiente** | José Antonio | 4 | 4 | 4 | 4 | 4 | 4 | 4 | 4 | 4 | 4 | **4** |

* **Análisis Burn-Down S3:** En el **Día 6 (9 Nov)**, la gestión de *refresh tokens* de Google Calendar OAuth2 en **`T3.3` (`WU-07`)** añade `+4 h` (`9 h → 11 h`), desviando la curva sobre la ideal (`39 h vs. 36,8 h`). Al ser un equipo de 2 personas, se prioriza cerrar con 100 % de pruebas las tres historias de mayor valor (`WU-06`, `WU-07`, `WU-15` = `21 SP`) y trasladar limpiamente **`WU-10` (`2 SP = 8 h`)** al arranque del Sprint 4.

---

### 5.4 Sprint 4 — Release 1.2 Suite B2B Completa (`16 Nov – 27 Nov 2026`)
> **Google Sheets:** [`Sprint4_BurnDown`](https://docs.google.com/spreadsheets/d/1qL701EOC4GaMRSGrcTq-fuIUbtDCPi0PBlGLCfoaxNA/edit#gid=107) · Gráfica nativa ID **`2091554835`**  
> **Compromiso ajustado:** `22 + 2 (WU-10) = 24 SP = 96 h ideales` (`48 h` Javier + `48 h` José Antonio) · **Velocidad ideal diaria:** `9,6 h/día` · **Resultado:** `24 / 24 SP` (**94 / 94 SP · Release 1.2 completa**).

| ID | WU | Descripción de la tarea | Tipo | Estado (D10) | Resp. | D0 | 16 Nov | 17 Nov | 18 Nov | 19 Nov | 20 Nov | 23 Nov | 24 Nov | 25 Nov | 26 Nov | 27 Nov |
| :---: | :---: | :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| — | — | **Tareas pendientes (> 0 h)** | — | — | — | **10** | **10** | **8** | **7** | **6** | **5** | **4** | **3** | **3** | **2** | **0** |
| — | — | **Horas ideales pendientes (Real)** | — | — | — | **96** | **86** | **76** | **65** | **55** | **45** | **34** | **23** | **13** | **3** | **0** |
| — | — | *Referencia Burn-Down Ideal (h)* | — | — | — | *96,0* | *86,4* | *76,8* | *67,2* | *57,6* | *48,0* | *38,4* | *28,8* | *19,2* | *9,6* | *0,0* |
| T4.1 | WU-10 | Completar edición/retirada ofertas + menú Mis Ofertas | Codif. | Terminada | José Antonio | 8 | 3 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |
| T4.2 | WU-08 | Contabilidad automática Fair-Play (+1/-1/0) y ranking | Codif. | Terminada | Javier | 6 | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |
| T4.3 | WU-08 | Vista móvil Banco de Saldos + filtros historial | Diseño/UI | Terminada | José Antonio | 6 | 6 | 4 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |
| T4.4 | WU-11 | Panel Web Avisos de Planta, borradores y envío Push/Mail | Diseño/UI | Terminada | José Antonio | 8 | 8 | 8 | 6 | 1 | 0 | 0 | 0 | 0 | 0 | 0 |
| T4.5 | WU-13 | Agregador métricas Lean (<2h, >95%, 100%, WAU/MAU) | Codif. | Terminada | Javier | 10 | 10 | 6 | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |
| T4.6 | WU-13 | Dashboard Web B2B, filtros unidad y exportación PDF | Diseño/UI | Terminada | José Antonio | 10 | 10 | 10 | 10 | 10 | 6 | 1 | 0 | 0 | 0 | 0 |
| T4.7 | WU-14 | Buscador auditoría, sello temporal y certificado PDF | Codif. | Terminada | Javier | 12 | 12 | 12 | 12 | 8 | 3 | 0 | 0 | 0 | 0 | 0 |
| T4.8 | WU-17 | Control límite Freemium (15 usr), CIF y pasarela PCI-DSS | Codif. | Terminada | Javier | 16 | 16 | 16 | 16 | 16 | 16 | 13 | 8 | 3 | 0 | 0 |
| T4.9 | WU-17 | Portal público Onboarding Freemium/PRO + factura PDF | Diseño/UI | Terminada | José Antonio | 16 | 16 | 16 | 16 | 16 | 16 | 16 | 11 | 6 | 1 | 0 |
| T4.10 | WU-19 | Consulta cronológica logs RGPD (filtros fecha/IP) + QA | Pruebas | Terminada | Javier | 4 | 4 | 4 | 4 | 4 | 4 | 4 | 4 | 4 | 2 | 0 |

* **Análisis Burn-Down S4:** Con `WU-10` cerrada el Día 2 y el entorno de pasarela simulado preparado desde la Retrospectiva S3, la curva real se mantiene constantemente por debajo de la línea ideal desde D1 hasta D10 (`0 h`), completando las **19 Work Units (`94 / 94 SP`)**.

---

## 6. Gestión Visual Kanban (WIP ≤ 2) y Marco de Medición (Tema 5)

> **Pestaña en Google Sheets:** [`Kanban_y_Metricas_T5`](https://docs.google.com/spreadsheets/d/1qL701EOC4GaMRSGrcTq-fuIUbtDCPi0PBlGLCfoaxNA/edit#gid=108)

### 6.1 Política Kanban Pull para 2 Personas (Fotografía Sprint 2 · Día 5)
* **`En Curso (WIP máx. = 2)`:** Máximo 1 tarea en curso por desarrollador. El Día 5 del Sprint 2, al aparecer la re-estimación `+6 h` en `T2.4 (WU-03)`, el tope `WIP [2/2]` impide abrir `WU-05` de forma prematura y dirige a José Antonio a realizar *pair testing* con Javier hasta dejar `WU-03` verificada.
* **`En Pruebas (WIP máx. = 2)`:** Revisión cruzada obligatoria (lo desarrollado por Javier lo verifica José Antonio y viceversa).

### 6.2 Clasificación Ontológica y Fichas Operativas de Métricas (Tema 5 · Piattini et al.)

| Código | Métrica / Indicador | Entidad / Atributo | Tipo y Escala | Fórmula de cálculo | Valor simulado | Umbral / Criterio de decisión |
| :---: | :--- | :--- | :---: | :--- | :---: | :--- |
| **`M-01`** | **Cumplimiento de Compromiso (`PCC`)** | Sprint / Predictibilidad | Derivada · Ratio (`%`) | $\frac{SP_{\text{Done}}}{SP_{\text{Plan}}} \times 100$ | **97,8 %** | `≥ 90 %` Óptimo · `80–89 %` Aceptable · `< 80 %` Alerta *(S1:100%, S2:100%, S3:91,3%, S4:100%)* |
| **`M-02`** | **Estabilidad de Velocidad (`CV`)** | Proyecto / Madurez estim. | Indicador · Ratio (`%`) | $\frac{\sigma}{\mu} \times 100$ | **7,4 %** | `< 15 %` Óptimo · `15–25 %` Mejorable · `> 25 %` Inestable *($\mu=23{,}50$, $\sigma=1{,}73$)* |
| **`M-03`** | **Cumplimiento de Releases (`CH`)** | Release / Puntualidad | Derivada · Ratio (`%`) | $\frac{SP_{\text{Acum}}}{SP_{\text{Total}}} \times 100$ | **100,0 %** | `100 %` Conforme *(94/94 SP entregados en fecha · 27 Nov)* |
| **`M-04`** | **Tiempo Medio Resolución (`TMR`)** | Servicio / Agilidad Lean | Base-Deriv. · Ratio (`h`) | $\frac{1}{N}\sum(t_{\text{aprob}}-t_{\text{pub}})$ | **1,4 h** | `< 2,0 h` Objetivo Lean cumplido *(vs. 24–48 h manual)* · `2–6 h` Mejorable · `> 6 h` Deficiente |
| **`M-05`** | **Cumplimiento Regla 12 h (`TCN`)** | Producto / Seguridad legal | Indicador · Ratio (`%`) | $\frac{\text{Permutas }\ge 12\text{h}}{\text{Total aprobadas}} \times 100$ | **100,0 %** | `100 %` Conforme *(0 infracciones · 28 bloqueos preventivos)* · `< 100 %` Fallo Crítico P0 |
