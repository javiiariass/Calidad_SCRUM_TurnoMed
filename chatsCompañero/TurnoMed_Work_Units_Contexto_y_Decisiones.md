# Contexto, Historias de Usuario (Work Units) y Justificación de Decisiones — Proyecto TurnoMed

Este documento consolida todo el contexto funcional, metodológico y de estimación del proyecto **TurnoMed**, junto con la justificación de las decisiones tomadas para el catálogo de **19 Historias de Usuario (Work Units)** siguiendo el formato del caso de estudio de referencia (*GESCON*).

---

## 1. Entregables y Documentos Relacionados

* **Documento editable en Google Docs:** [Caso de Estudio TurnoMed - Work Units](https://docs.google.com/document/d/1CU93o89bRjTogy4Qtt-nlEQ8Mu_qkaZQOea5gXflYh8/edit)
* **Documento PDF maquetado (1 WU por página, con espacio reservado para bocetos):** [Caso de Estudio TurnoMed - Work Units.pdf](./Caso%20de%20Estudio%20TurnoMed%20-%20Work%20Units.pdf)
* **Documentación base del proyecto:**
  * [TurnoMed_Memoria.pdf](./TurnoMed_Memoria.pdf) *(Memoria CMEPPS 2026 — Filosofía Lean, MVP, Métricas y Viabilidad)*
  * [TurnoMed.pdf](./TurnoMed.pdf) *(Lean Canvas)*
  * [Caso de Estudio GESCON - Work Units.pdf](./Caso%20de%20Estudio%20GESCON%20-%20Work%20Units.pdf) *(Plantilla metodológica de referencia)*

---

## 2. Contexto del Proyecto (Memoria + Lean Canvas)

**TurnoMed** es una plataforma digital para gestionar y agilizar el intercambio de turnos y la cobertura de guardias entre profesionales sanitarios (enfermeros/as, médicos residentes MIR y médicos adjuntos) y supervisores de planta en hospitales y clínicas.

### Problemas que resuelve (Despilfarros Lean)
1. **Sobreproceso:** Tramitación manual de permutas en papel o Excel impresos.
2. **Tiempo perdido en esperas:** Incertidumbre de 24–48 horas para confirmar un cambio o cobertura de baja.
3. **Movimientos innecesarios:** Desplazamientos continuos al control de enfermería para consultar el tablón físico.
4. **Defectos y errores:** Fatiga clínica derivada de incumplir el descanso legal mínimo de **12 horas ininterrumpidas** entre jornadas.
5. **Talento desperdiciado:** Supervisores dedicando horas administrativas a conciliar cuadrantes en lugar de gestionar la calidad asistencial.

### Flujo del Producto Mínimo Viable (MVP)
```text
1. Oferta P2P  ──▶  2. Aceptación  ──▶  3. Regla 12h Descanso  ──▶  4. Validación 1-Clic
(Sanitario propone)  (Compañero acepta)  (Motor comprueba legalidad)  (Supervisor aprueba y actualiza)
```

### Segmentos y Modelo de Negocio
* **Usuarios Operativos (End Users):** Enfermeros/as, residentes (MIR) y médicos adjuntos + Supervisores de planta (unidades críticas: Urgencias, UCI, Quirófanos).
* **Decisores Institucionales (Clientes B2B):** Dirección de RRHH, Gerencia y Dirección Médica/Enfermería.
* **Monetización:** Modelo dual **Freemium** (gratuito para plantas de hasta 15 usuarios) y **Suscripción B2B SaaS Hospitalario (Plan PRO)** con validación legal completa, exportación a RRHH y soporte prioritario.
* **Cumplimiento RGPD:** Operativa con códigos seudonimizados de empleado y trazabilidad de accesos.

---

## 3. Justificación de las Decisiones Metodológicas

### 3.1. Ampliación de las 8 Funcionalidades Principales a 19 Work Units
Las 8 funcionalidades del enunciado inicial cubren el núcleo operativo del producto (**WU 01 a WU 08**). Sin embargo, al contrastarlas con la **Memoria**, el **Lean Canvas** y la estructura completa del caso de estudio **GESCON**, se detectaron 11 necesidades funcionales y de soporte imprescindibles para que el sistema sea viable y completo:

* **Operativa base sin la cual no hay permutas:**
  * **WU 09 (Carga del cuadrante base mensual):** Sin turnos cargados inicialmente por el supervisor, los sanitarios no tendrían turnos que ofertar ni validar.
  * **WU 10 (Modificación/retirada de oferta):** Equivalente a la WU 2 de GESCON (*Acceso posterior al envío*); permite corregir o cancelar una oferta antes de ser aprobada.
  * **WU 15 (Indisponibilidades, vacaciones y permisos):** Imprescindible en un hospital para no notificar guardias urgentes ni permitir trueques a personal de baja o vacaciones.
* **Ventaja injusta, métricas Lean y clientes B2B (Memoria y Lean Canvas):**
  * **WU 12 (Parametrización de reglas y convenios):** Refleja la *Ventaja Injusta* del Lean Canvas (*"Motor de reglas parametrizado con convenios autonómicos"*).
  * **WU 13 (Dashboard B2B de cumplimiento legal):** Da respuesta al Bloque 6 de la Memoria (*Cuadro de Mandos: tiempo < 2h, > 95% cobertura, 100% cumplimiento legal, WAU/MAU*).
  * **WU 14 (Auditoría y certificados de trazabilidad):** Trazabilidad legal ante Inspección de Trabajo.
  * **WU 17 (Suscripción Freemium / PRO):** Equivalente a la WU 14 de GESCON (*Inscripción con pasarela de pago y recibo PDF*), adaptada al modelo de ingresos del Lean Canvas.
* **Soporte, comunicación y seguridad (equivalentes a GESCON + RGPD):**
  * **WU 11 (Gestión de avisos de planta):** Equivalente a la WU 3 de GESCON (*Gestión de Avisos*).
  * **WU 16 (Gestión de personal y servicios):** Equivalente a la WU 16/17 de GESCON, incorporando categorías sanitarias y seudonimización RGPD.
  * **WU 18 (Autenticación multi-rol):** Equivalente a la WU 18 de GESCON.
  * **WU 19 (Registro de accesos RGPD):** Equivalente a la WU 19 de GESCON.

### 3.2. Síntesis de Descripciones y Formato
* Se replicó la ficha exacta de GESCON (**1 Work Unit por página**, tabla superior con cabecera gris, fila de descripción combinada, espacio central reservado para futuros bocetos/wireframes de interfaz y sección inferior de *Pruebas de Aceptación*).
* Las descripciones se sintetizaron a **3–4 líneas** para transmitir la idea funcional exacta sin sobrecargar la ficha, manteniendo las reglas clave y excepciones en las *Pruebas de Aceptación*.

### 3.3. Criterio de `Importancia` y `Urgencia`
Se mantuvo la escala cualitativa de GESCON (`Muy Alta`, `Alta`, `Media`, `Baja`, `Muy Baja`) para respetar la plantilla original:
* **Importancia** mide el **valor de negocio / diferenciación**: `Muy Alta` para los 4 pilares del MVP (WU 01–04), `Alta` para cobertura urgente y cuadrante (WU 05, 06, 09), `Media` para productividad/B2B (WU 07, 08, 11–15) y `Baja` para administración/soporte (WU 10, 16–19).
* **Urgencia** mide el **orden de necesidad temporal**: `Muy Alta` para el motor de 12h (WU 03), `Alta` para el flujo P2P, aprobación 1-clic, bajas urgentes y carga del cuadrante base (WU 01, 02, 04, 06, 09), bajando progresivamente hasta `Muy Baja` en el registro de accesos (WU 19).

### 3.4. Criterio de Estimación con Planning Poker (Sucesión de Fibonacci)
Para el campo **Esfuerzo a priori (en puntos)** se aplicó **Planning Poker** usando la sucesión de Fibonacci (`1, 2, 3, 5, 8, 13`), evaluando **complejidad algorítmica, integración externa, casos borde, riesgo técnico y esfuerzo de pruebas** de forma relativa:

| Puntos | Nivel de Esfuerzo | Criterio aplicado en TurnoMed | Work Units asignadas |
| :---: | :--- | :--- | :--- |
| **2** | Sencilla | CRUDs básicos, reutilización directa de interfaces previas, formularios simples sin lógica temporal compleja. | WU 10, WU 11, WU 18, WU 19 |
| **3** | Baja-Media | Pantallas con lógica de negocio acotada, cálculos simples (sumas/restas de saldos), exportación de certificados o edición de parámetros. | WU 04, WU 08, WU 12, WU 14 |
| **5** | Media | Flujos completos con notificaciones, filtros por categoría/servicio, generación de cuadrantes PDF/Excel o dashboards con métricas agregadas. | WU 01, WU 02, WU 05, WU 13, WU 15, WU 16 |
| **8** | Alta | Integraciones externas (OAuth/iCal, pasarela de pago + facturación), importación/validación masiva Excel/CSV o notificaciones concurrentes en tiempo real. | WU 06, WU 07, WU 09, WU 17 |
| **13** | Muy Alta (Compleja) | Núcleo algorítmico crítico con múltiples reglas legales simultáneas, casos borde horarios, concurrencia y alto requisito de testing. | **WU 03** |

#### ¿Por qué la WU 03 (Regla de las 12 horas) tiene `13` puntos?
1. **Doble evaluación cruzada:** Simula el cuadrante resultante para **dos sanitarios a la vez**, revisando los turnos inmediatamente anteriores y posteriores de ambos.
2. **Casos borde horarios:** Turnos nocturnos que cruzan de un día a otro (ej. 22:00 a 08:00), guardias de 24 horas y cambios de mes.
3. **Múltiples reglas combinadas:** Descanso de 12h interjornada, solapes horarios, bloqueo por bajas/vacaciones (WU 15), categoría profesional y tope semanal/mensual según convenio (WU 12).
4. **Tiempo real y concurrencia:** Se invoca desde WU 02, WU 06 y WU 09; si un sanitario tiene varias propuestas abiertas, aceptar una puede invalidar legalmente otra en curso.
5. **Riesgo Alto y testing exigente:** La Memoria exige **100 % de cumplimiento legal**; un fallo aquí invalida la propuesta de valor del producto, requiriendo una suite exhaustiva de tests unitarios y de integración.

---

## 4. Product Backlog Completo (19 Work Units)

| # | Nombre de la Work Unit (HU) | Usuario / Rol | Importancia | Urgencia | Riesgo | Esfuerzo (Fibonacci) |
| :- | :--- | :--- | :---: | :---: | :---: | :---: |
| **WU 01** | Publicación de guardia para intercambio | Sanitario | Muy Alta | Alta | Bajo | **5** |
| **WU 02** | Solicitud y acuerdo de cambio entre compañeros (Peer-to-Peer) | Sanitario | Muy Alta | Alta | Medio | **5** |
| **WU 03** | Validación automática del descanso normativo (Regla de las 12 horas) | Sanitario / Sistema Validador | Muy Alta | Muy Alta | Alto | **13** |
| **WU 04** | Panel de aprobación en un clic para el supervisor | Supervisor de Planta | Muy Alta | Alta | Bajo | **3** |
| **WU 05** | Actualización y exportación automática del cuadrante oficial | Supervisor de Planta | Alta | Media | Medio | **5** |
| **WU 06** | Alerta de guardia urgente / Cobertura exprés de bajas | Supervisor de Planta | Alta | Alta | Medio | **8** |
| **WU 07** | Calendario personal interactivo y sincronización externa | Sanitario | Media | Media | Bajo | **8** |
| **WU 08** | Banco de saldos de guardias y turnos (Fair-Play) | Sanitario / Supervisor de Planta | Media | Baja | Bajo | **3** |
| **WU 09** | Carga y gestión del cuadrante base mensual del servicio | Supervisor de Planta | Alta | Alta | Medio | **8** |
| **WU 10** | Modificación o retirada de oferta/propuesta de cambio | Sanitario | Baja | Baja | Bajo | **2** |
| **WU 11** | Gestión de avisos y comunicados de planta | Supervisor de Planta | Media | Baja | Bajo | **2** |
| **WU 12** | Parametrización de reglas normativas y convenios del centro | Dirección de RRHH / Administrador | Media | Media | Medio | **3** |
| **WU 13** | Cuadro de mandos y analítica de cumplimiento legal (Dashboard B2B) | Dirección de RRHH / Gestor Hospitalario | Media | Baja | Bajo | **5** |
| **WU 14** | Auditoría de permutas y certificados de trazabilidad legal | Supervisor de Planta / Dirección de RRHH | Media | Baja | Bajo | **3** |
| **WU 15** | Gestión de indisponibilidades, vacaciones y permisos reglamentarios | Sanitario / Supervisor de Planta | Media | Media | Bajo | **5** |
| **WU 16** | Gestión de personal sanitario y estructura de servicios | Administrador | Baja | Baja | Bajo | **5** |
| **WU 17** | Suscripción de centro hospitalario y gestión de Plan (Freemium / PRO) | Gestor Hospitalario / Visitante | Baja | Baja | Bajo | **8** |
| **WU 18** | Autenticación y control de acceso | Visitante / Usuario Registrado | Baja | Baja | Bajo | **2** |
| **WU 19** | Registro de accesos al sistema (Seguridad RGPD) | Administrador | Baja | Muy Baja | Bajo | **2** |

**Total del Product Backlog:** **92 puntos de historia** (19 Work Units).

---

## 5. Roadmap Sugerido por Iteraciones (Dependencias)

1. **Iteración 1 — Cimientos y MVP Core (41 pts):**
   * `WU 18` (2) + `WU 16` (5) + `WU 09` (8) + `WU 01` (5) + `WU 02` (5) + `WU 03` (13) + `WU 04` (3).
   * *Objetivo:* Tener usuarios, cuadrante inicial y el ciclo completo del MVP funcionando con validación legal de 12h.
2. **Iteración 2 — Operativa de Planta y Reglas (18 pts):**
   * `WU 05` (5) + `WU 06` (8) + `WU 12` (3) + `WU 11` (2).
   * *Objetivo:* Actualización/exportación oficial, cobertura exprés de bajas urgentes, convenios configurables y módulo de avisos.
3. **Iteración 3 — Experiencia del Sanitario y Equidad (18 pts):**
   * `WU 07` (8) + `WU 08` (3) + `WU 15` (5) + `WU 10` (2).
   * *Objetivo:* Calendario por colores + Google Calendar/iCal, banco Fair-Play, gestión de vacaciones/bajas y retirada de ofertas.
4. **Iteración 4 — Capa B2B, Auditoría y Monetización (18 pts):**
   * `WU 13` (5) + `WU 14` (3) + `WU 17` (8) + `WU 19` (2).
   * *Objetivo:* Dashboard ejecutivo de métricas Lean, certificados para Inspección de Trabajo, pasarela Freemium/PRO y auditoría RGPD.

---

## 6. Detalle de Cada Work Unit (Texto Definitivo)

### WU 01 — Publicación de guardia para intercambio
* **Usuario:** Sanitario | **Importancia:** Muy Alta | **Urgencia:** Alta | **Riesgo:** Bajo | **Esfuerzo:** 5
* **Descripción:** El sanitario selecciona un turno propio asignado y lo publica en el tablón de su servicio indicando qué fechas o franjas busca a cambio (o dejándolo abierto a propuestas). La oferta sólo es visible para compañeros de su misma categoría profesional y servicio.
* **Pruebas de Aceptación:**
  * Al publicar, el turno debe pertenecer al sanitario autenticado y estar en una fecha futura.
  * No permitir publicar un turno que ya tenga una oferta activa en el tablón.
  * Permitir indicar turnos preferidos a cambio o marcar 'Abierto a propuestas / Cesión al banco de saldos'.
  * La oferta sólo debe ser visible para sanitarios de la misma categoría profesional y unidad.
  * Al publicar, el turno cambia su estado visual a 'Ofertado' en el calendario personal.

### WU 02 — Solicitud y acuerdo de cambio entre compañeros (Peer-to-Peer)
> *Nota:* Puede resultar interesante que esta WU se implemente después de la WU “Publicación de guardia para intercambio” puesto que opera sobre las ofertas del tablón.
* **Usuario:** Sanitario | **Importancia:** Muy Alta | **Urgencia:** Alta | **Riesgo:** Medio | **Esfuerzo:** 5
* **Descripción:** Un sanitario se postula a una guardia ofertada proponiendo uno de sus turnos a cambio (o asumiéndola contra el banco de saldos). Cuando el ofertante acepta una propuesta, se descartan las demás y el acuerdo cerrado pasa automáticamente a la bandeja del supervisor.
* **Pruebas de Aceptación:**
  * Visualizar las guardias ofertadas por compañeros de la misma categoría y servicio.
  * Permitir postularse seleccionando un turno propio libre de conflictos para ofrecer a cambio.
  * Notificar al ofertante cada propuesta recibida y permitirle aceptarla o rechazarla.
  * Al aceptar una propuesta, cancelar el resto de postulaciones sobre esa guardia y enviarla al supervisor.
  * No permitir postularse a una oferta propia ni proponer un turno ya comprometido en otro acuerdo.

### WU 03 — Validación automática del descanso normativo (Regla de las 12 horas)
> *Nota:* Esta WU constituye el núcleo diferencial del MVP y se invoca en tiempo real durante la WU “Solicitud y acuerdo de cambio entre compañeros”.
* **Usuario:** Sanitario / Sistema Validador | **Importancia:** Muy Alta | **Urgencia:** Muy Alta | **Riesgo:** Alto | **Esfuerzo:** 13
* **Descripción:** Antes de confirmar cualquier propuesta o acuerdo, el sistema comprueba automáticamente los turnos anteriores y posteriores de ambos implicados. Si el cambio supone encadenar jornadas con menos de 12 horas de descanso obligatorio, solapes horarios o exceso de jornada semanal, bloquea la operación indicando el motivo legal.
* **Pruebas de Aceptación:**
  * Bloquear cualquier acuerdo donde alguno de los sanitarios tenga menos de 12 horas de descanso entre jornadas.
  * Bloquear el intercambio si alguno de los dos ya tiene asignado un turno solapado en esa fecha/franja.
  * Bloquear el intercambio si ambos profesionales no pertenecen a la misma categoría requerida.
  * Mostrar un aviso claro indicando qué regla normativa se vulnera y qué turnos entran en conflicto.
  * Marcar el acuerdo como 'Pre-validado legalmente (Cumple 12h)' cuando supere todas las comprobaciones.

### WU 04 — Panel de aprobación en un clic para el supervisor
> *Nota:* Conviene implementar esta WU tras las WUs de acuerdo P2P y validación normativa, ya que recibe las permutas pre-validadas.
* **Usuario:** Supervisor de Planta | **Importancia:** Muy Alta | **Urgencia:** Alta | **Riesgo:** Bajo | **Esfuerzo:** 3
* **Descripción:** Muestra al supervisor todas las solicitudes de cambio ya acordadas entre compañeros y pre-validadas legalmente. El supervisor puede aprobarlas en un solo clic o rechazarlas indicando el motivo, notificándose la decisión al instante a ambos sanitarios.
* **Pruebas de Aceptación:**
  * Visualizar la lista de acuerdos pendientes ordenados por proximidad de la fecha de la guardia.
  * Permitir aprobar un acuerdo en un clic, cambiando su estado a 'Aprobado' y notificando a ambos sanitarios.
  * Permitir rechazar un acuerdo exigiendo un motivo de rechazo que se notificará a los implicados.
  * Al rechazar un acuerdo, mantener sin cambios la titularidad original de los turnos en el cuadrante.
  * Mostrar el historial de solicitudes aprobadas y rechazadas por el supervisor.

### WU 05 — Actualización y exportación automática del cuadrante oficial
* **Usuario:** Supervisor de Planta | **Importancia:** Alta | **Urgencia:** Media | **Riesgo:** Medio | **Esfuerzo:** 5
* **Descripción:** Al aprobarse un cambio o cobertura, el sistema actualiza automáticamente la titularidad de los turnos en el cuadrante general del servicio y genera un registro de auditoría. Permite exportar el cuadrante actualizado en formato PDF o Excel para Dirección y RRHH.
* **Pruebas de Aceptación:**
  * Actualizar de forma inmediata los titulares de los turnos en el cuadrante del servicio tras la aprobación.
  * Registrar automáticamente en auditoría la fecha/hora, los sanitarios implicados y el supervisor aprobador.
  * Exportar el cuadrante mensual o semanal actualizado en formato PDF y Excel (`.xlsx` / `.csv`).
  * Resaltar visualmente en el cuadrante qué turnos han sido permutados respecto a la planificación inicial.

### WU 06 — Alerta de guardia urgente / Cobertura exprés de bajas
> *Nota:* Reutiliza el motor de la WU “Validación automática del descanso normativo” para filtrar candidatos elegibles.
* **Usuario:** Supervisor de Planta | **Importancia:** Alta | **Urgencia:** Alta | **Riesgo:** Medio | **Esfuerzo:** 8
* **Descripción:** Ante una baja imprevista, el supervisor lanza una alerta urgente sobre el turno descubierto. El sistema notifica únicamente a los sanitarios de la misma categoría que estén libres y cumplan las 12 horas de descanso legal, adjudicando la guardia automáticamente al primero que acepte.
* **Pruebas de Aceptación:**
  * Permitir al supervisor declarar un turno como 'Baja urgente' y lanzar la alerta en un clic.
  * Notificar exclusivamente a sanitarios de la misma categoría que estén libres y cumplan la regla de 12 horas.
  * Mostrar al supervisor la lista de candidatos elegibles notificados.
  * Adjudicar automáticamente el turno al primer sanitario elegible que acepte y cerrar la alerta para el resto.
  * Actualizar el cuadrante oficial y el banco de saldos en cuanto la guardia quede cubierta.

### WU 07 — Calendario personal interactivo y sincronización externa
* **Usuario:** Sanitario | **Importancia:** Media | **Urgencia:** Media | **Riesgo:** Bajo | **Esfuerzo:** 8
* **Descripción:** Muestra a cada sanitario una vista mensual y semanal de sus turnos (mañana, tarde, noche y guardia 24h) diferenciados por colores y estado. Permite sincronizar los turnos en tiempo real con calendarios externos (Google Calendar / iCal).
* **Pruebas de Aceptación:**
  * Visualizar el calendario personal en vista mensual y semanal con colores según tipo de turno.
  * Mostrar el estado de cada turno (confirmado, ofertado en tablón, pendiente de aprobación).
  * Generar enlace iCal (`.ics`) o vincular con Google Calendar para sincronizar los turnos automáticamente.
  * Reflejar en el calendario externo cualquier cambio de turno en cuanto sea aprobado por el supervisor.

### WU 08 — Banco de saldos de guardias y turnos (Fair-Play)
* **Usuario:** Sanitario / Supervisor de Planta | **Importancia:** Media | **Urgencia:** Baja | **Riesgo:** Bajo | **Esfuerzo:** 3
* **Descripción:** Registra automáticamente el balance histórico de guardias cedidas y asumidas cuando se cubre un turno sin trueque recíproco inmediato, mostrando un marcador transparente de turnos a favor (`+1`) o pendientes de devolver (`-1`) por sanitario.
* **Pruebas de Aceptación:**
  * Sumar `+1` al saldo del sanitario que asume un turno sin trueque recíproco y restar `-1` al cedente.
  * Mantener el saldo sin cambios cuando el intercambio sea un trueque recíproco equivalente (`1` por `1`).
  * Visualizar el saldo actual y el historial de movimientos que lo justifican.
  * Permitir al supervisor consultar los saldos de la planta para repartir equitativamente las coberturas.

### WU 09 — Carga y gestión del cuadrante base mensual del servicio
> *Nota:* Es recomendable implementar esta WU en las primeras iteraciones ya que carga los turnos iniciales sobre los que operan los cambios.
* **Usuario:** Supervisor de Planta | **Importancia:** Alta | **Urgencia:** Alta | **Riesgo:** Medio | **Esfuerzo:** 8
* **Descripción:** Permite al supervisor crear, editar o importar desde Excel/CSV la planificación mensual inicial de su unidad. El sistema advierte si existen puestos mínimos descubiertos o infracciones de las 12 horas de descanso antes de publicar el cuadrante para todo el servicio.
* **Pruebas de Aceptación:**
  * Permitir importar el cuadrante mensual desde Excel/CSV o asignar turnos sobre la cuadrícula mensual.
  * Resaltar alertas si el cuadrante base contiene solapes o incumple el descanso mínimo de 12 horas.
  * Advertir si alguna franja horaria no alcanza el mínimo de personal requerido en la planta.
  * Permitir guardar el cuadrante como borrador y publicarlo notificando a los sanitarios del servicio.

### WU 10 — Modificación o retirada de oferta/propuesta de cambio
> *Nota:* Puede resultar interesante implementar esta WU después de las WUs de publicación y solicitud P2P puesto que reutiliza su interfaz.
* **Usuario:** Sanitario | **Importancia:** Baja | **Urgencia:** Baja | **Riesgo:** Bajo | **Esfuerzo:** 2
* **Descripción:** Tras publicar una guardia o enviar una propuesta de cambio, el sanitario puede editar las fechas solicitadas o retirar su oferta/propuesta siempre que aún no haya sido aprobada por el supervisor ni haya expirado el plazo límite previo al turno.
* **Pruebas de Aceptación:**
  * Permitir al ofertante editar las preferencias o cancelar su oferta mientras no esté aprobada.
  * Permitir a un candidato retirar su propuesta de trueque antes de que sea aprobada.
  * (Excepción) Si el cambio ya fue aprobado o expiró el plazo previo al turno, NO permitir su modificación.
  * Al retirar una oferta con propuestas pendientes, notificar automáticamente la cancelación a los postulantes.

### WU 11 — Gestión de avisos y comunicados de planta
> *Nota:* Esta WU proporciona el módulo de avisos que también aprovechan las notificaciones de acuerdos y bajas urgentes.
* **Usuario:** Supervisor de Planta | **Importancia:** Media | **Urgencia:** Baja | **Riesgo:** Bajo | **Esfuerzo:** 2
* **Descripción:** Permite al supervisor crear, guardar como borrador, enviar y eliminar (si no han sido enviados) avisos internos dirigidos a toda la planta, a una categoría profesional concreta o a los sanitarios asignados en una fecha determinada.
* **Pruebas de Aceptación:**
  * Enviar avisos por notificación push y email filtrando destinatarios (planta completa, categoría o fecha).
  * Guardar avisos en borrador para modificarlos o enviarlos posteriormente.
  * Permitir eliminar únicamente avisos en preparación que aún no hayan sido enviados.
  * Consultar el registro de avisos enviados indicando fecha, asunto, autor y destinatarios.

### WU 12 — Parametrización de reglas normativas y convenios del centro
* **Usuario:** Dirección de RRHH / Administrador | **Importancia:** Media | **Urgencia:** Media | **Riesgo:** Medio | **Esfuerzo:** 3
* **Descripción:** Permite configurar las reglas del convenio del hospital que aplica el validador automático: horas mínimas de descanso entre jornadas (12h), descanso semanal (36h), tope de horas semanales, antelación mínima de solicitud y catálogo de tipos de turno (horarios y duración).
* **Pruebas de Aceptación:**
  * Editar parámetros normativos (descanso mínimo entre jornadas, tope semanal y antelación mínima).
  * Impedir configurar un descanso entre jornadas inferior a las 12 horas legales.
  * Gestionar los tipos de turno (código, horario, duración y color) sin permitir códigos repetidos.
  * Solicitar confirmación al guardar cambios normativos y actualizar las reglas del validador.

### WU 13 — Cuadro de mandos y analítica de cumplimiento legal (Dashboard B2B)
* **Usuario:** Dirección de RRHH / Gestor Hospitalario | **Importancia:** Media | **Urgencia:** Baja | **Riesgo:** Bajo | **Esfuerzo:** 5
* **Descripción:** Muestra a Dirección y RRHH un panel con las métricas clave del hospital y por unidad: tiempo medio de resolución de cambios (< 2h), porcentaje de bajas urgentes cubiertas, porcentaje de cambios validados sin infracción legal (100% cumplimiento 12h) y usuarios activos (WAU/MAU).
* **Pruebas de Aceptación:**
  * Visualizar las métricas clave filtrando por servicio/planta y rango de fechas.
  * Mostrar el total de intentos de cambio bloqueados por incumplir el descanso legal.
  * Comparar indicadores de rotación y cobertura entre unidades (Urgencias, UCI, Quirófanos, Planta).
  * Exportar el resumen de métricas del cuadro de mandos en formato PDF.

### WU 14 — Auditoría de permutas y certificados de trazabilidad legal
* **Usuario:** Supervisor de Planta / Dirección de RRHH | **Importancia:** Media | **Urgencia:** Baja | **Riesgo:** Bajo | **Esfuerzo:** 3
* **Descripción:** Permite consultar y filtrar el historial completo de cambios de turno y coberturas (solicitante, receptor, fechas, validación de 12h y supervisor que aprobó), así como emitir certificados en PDF para justificar el cumplimiento normativo ante Inspección de Trabajo.
* **Pruebas de Aceptación:**
  * Generar listados de permutas filtrando por sanitario, unidad, fechas o estado (aprobada, rechazada).
  * Permitir seleccionar columnas visibles y ordenar por fecha de guardia o fecha de resolución.
  * Generar fichero PDF con el certificado de trazabilidad legal de una permuta o periodo concreto.

### WU 15 — Gestión de indisponibilidades, vacaciones y permisos reglamentarios
* **Usuario:** Sanitario / Supervisor de Planta | **Importancia:** Media | **Urgencia:** Media | **Riesgo:** Bajo | **Esfuerzo:** 5
* **Descripción:** Permite a los sanitarios solicitar y al supervisor registrar vacaciones, bajas médicas o días de libre disposición. Las fechas aprobadas quedan bloqueadas en el calendario del sanitario, excluyéndolo automáticamente de intercambios y alertas de guardia urgente en ese periodo.
* **Pruebas de Aceptación:**
  * Permitir registrar solicitudes de vacaciones, permisos o bajas indicando fecha de inicio, fin y motivo.
  * Advertir al supervisor si el sanitario tiene guardias asignadas dentro del periodo de ausencia solicitado.
  * Ofrecer lanzar alerta de cobertura o publicar en tablón las guardias afectadas al aprobar una baja/permiso.
  * Excluir automáticamente a los sanitarios de permiso o baja de las notificaciones de guardia urgente.

### WU 16 — Gestión de personal sanitario y estructura de servicios
* **Usuario:** Administrador | **Importancia:** Baja | **Urgencia:** Baja | **Riesgo:** Bajo | **Esfuerzo:** 5
* **Descripción:** El administrador gestiona las altas, bajas, modificaciones y consulta de servicios hospitalarios y usuarios (Sanitario con su categoría: Enfermero/a, MIR, Adjunto; Supervisor; RRHH y Administrador). Un usuario puede tener varios roles y el sistema le envía por email su userid y contraseña inicial.
* **Pruebas de Aceptación:**
  * Visualizar, buscar, filtrar y ordenar usuarios por nombre, código seudonimizado, categoría, servicio o rol.
  * Permitir dar de alta, modificar y eliminar usuarios solicitando confirmación.
  * Impedir eliminar un sanitario que tenga turnos futuros asignados o cambios en curso.
  * Verificar que no existan usuarios duplicados y que cada sanitario tenga categoría y servicio asignados.
  * Notificar automáticamente por email las credenciales al dar de alta o dar de baja un usuario.

### WU 17 — Suscripción de centro hospitalario y gestión de Plan (Freemium / PRO)
* **Usuario:** Gestor Hospitalario / Visitante | **Importancia:** Baja | **Urgencia:** Baja | **Riesgo:** Bajo | **Esfuerzo:** 8
* **Descripción:** Permite registrar una planta u hospital eligiendo entre el Plan Freemium (gratuito hasta 15 sanitarios por planta) o el Plan PRO B2B (plantas ilimitadas, validador legal completo y exportación a RRHH). Calcula el importe según las plantas contratadas, procesa el pago con tarjeta y emite factura en PDF.
* **Pruebas de Aceptación:**
  * Permitir el alta gratuita en modalidad Freemium controlando el límite de 15 usuarios por planta.
  * Advertir respecto de inscripciones repetidas para un mismo centro o unidad.
  * Calcular y mostrar el coste total según el número de plantas o licencias seleccionadas en el Plan PRO.
  * Realizar el pago seguro mediante tarjeta y emitir el recibo/factura en formato PDF.

### WU 18 — Autenticación y control de acceso
* **Usuario:** Visitante / Usuario Registrado | **Importancia:** Baja | **Urgencia:** Baja | **Riesgo:** Bajo | **Esfuerzo:** 2
* **Descripción:** Control de acceso al sistema mediante userid y contraseña. Si el usuario tiene más de un rol asignado (p. ej., Sanitario y Supervisor), solicita con qué perfil desea acceder. Incluye envío de enlace por email para recuperar la contraseña en caso de olvido.
* **Pruebas de Aceptación:**
  * Validar acceso mediante userid y password, bloqueando temporalmente tras varios intentos fallidos.
  * Solicitar el tipo de acceso tras autenticarse en caso de que el usuario posea más de un rol.
  * Enviar email de recuperación de contraseña cuando el usuario lo solicite.

### WU 19 — Registro de accesos al sistema (Seguridad RGPD)
* **Usuario:** Administrador | **Importancia:** Baja | **Urgencia:** Muy Baja | **Riesgo:** Bajo | **Esfuerzo:** 2
* **Descripción:** Consulta de los accesos realizados al sistema incluyendo fecha-hora de login, userid (código seudonimizado), rol utilizado y fecha-hora de logout para auditoría de seguridad y cumplimiento RGPD.
* **Pruebas de Aceptación:**
  * Visualizar el listado de accesos con fecha-hora login, userid, rol y fecha-hora logout.
  * Permitir filtrar los registros por usuario, rango de fechas o intentos de acceso fallidos.

---

## 7. Sistema de Diseño e Interfaz Común (Modo Claro)

Todas las pantallas y prototipos de las Historias de Usuario de **TurnoMed** comparten una misma arquitectura visual en **modo claro**, alineada con la identidad corporativa de la memoria y el Lean Canvas.

### 7.1. Paleta de Colores Oficial (Modo Claro)

| Token / Uso | Código Hex | Aplicación |
| :--- | :---: | :--- |
| **Fondo general (Canvas)** | `#F8FAFC` | Fondo principal de la aplicación (`slate-50`). |
| **Superficie / Tarjetas** | `#FFFFFF` | Contenedores, formularios, modales y tablas (`white`). |
| **Bordes y divisores** | `#E2E8F0` | Contorno de tarjetas, inputs y líneas divisorias (`slate-200`). |
| **Primario (Azul Clínico)** | `#0F4C81` | Banner superior, botones principales, enlaces y elementos activos. |
| **Secundario (Teal Sanitario)** | `#0D9488` | Acentos de marca, badges de turno y resaltado de acciones secundarias. |
| **Texto principal** | `#0F172A` | Títulos, etiquetas y contenido principal (`slate-900`). |
| **Texto secundario / Muted** | `#475569` | Subtítulos, descripciones auxiliares y metadatos (`slate-600`). |
| **Estado Éxito / Validado 12h** | `#16A34A` / `#DCFCE7` | Turno `Ofertado`, acuerdo `Aprobado`, sello `Cumple 12h`. |
| **Estado Aviso / Pendiente** | `#D97706` / `#FEF3C7` | Turnos nocturnos/24h, solicitudes pendientes de aprobación. |
| **Estado Error / Bloqueo Legal** | `#DC2626` / `#FEE2E2` | Incumplimiento regla 12h, solape horario, baja urgente descubierta. |

### 7.2. Banner Superior Común (App Shell)
Todas las vistas heredan la misma cabecera fija superior con fondo `#0F4C81` y texto blanco:
1. **Izquierda (Identidad):** Icono/cruz sanitaria + **TurnoMed** + subtítulo de centro/unidad (ej. *Hospital Universitario · Unidad de Urgencias*).
2. **Centro (Navegación modular):** Pestañas de acceso rápido entre las áreas principales:
   * `Mi Calendario` (WU 07)
   * `Publicar Guardia` (WU 01)
   * `Tablón P2P` (WU 02 / WU 03)
   * `Panel Supervisor` (WU 04 / WU 05 / WU 06)
   * `Fair-Play` (WU 08)
3. **Derecha (Contexto de Usuario):** Indicador de saldo Fair-Play (`+1 turno`), nombre del profesional, categoría/servicio, código seudonimizado RGPD (ej. `ENF-042`) y badge de rol activo.

### 7.3. Reglas de Diseño y Componentes Compartidos
* **Tipografía:** Sans-serif limpia (`Inter` / sistema), tamaño base `14px`, títulos de sección `14px–16px` semibold, textos auxiliares mínimo `12px`.
* **Contenedores:** Tarjetas con fondo `#FFFFFF`, borde `1px solid #E2E8F0`, radio `12px` (`rounded-xl`) y sombra sutil (`shadow-sm`).
* **Código de colores de turnos (consistente en calendario, tablón y cuadrante):**
  * **Mañana (08:00–15:00):** Azul claro (`#DBEAFE` / `#1D4ED8`)
  * **Tarde (15:00–22:00):** Índigo suave (`#E0E7FF` / `#4338CA`)
  * **Noche (22:00–08:00):** Ámbar (`#FEF3C7` / `#B45309`)
  * **Guardia 24h:** Teal (`#CCFBF1` / `#0F766E`)
* **Principio Lean UX:** Máximo **1 clic** para acciones críticas (aprobar cambio, aceptar guardia urgente), mensajes de error normativo explícitos (indicando regla vulnerada y turnos en conflicto) y visibilidad filtrada automáticamente por categoría y servicio.

### 7.4. Índice de Prototipos Interactivos Generados (WU-01 a WU-19)

| WU | Funcionalidad | Prototipo HTML |
| :- | :--- | :--- |
| **WU 01** | Publicación de guardia para intercambio | [wu01_publicacion_guardia.html](file:///C:/Users/jose1/.gemini/antigravity/brain/91448f54-e32c-47d8-8d4f-1008b18b3077/wu01_publicacion_guardia.html) |
| **WU 02** | Solicitud y acuerdo de cambio entre compañeros (P2P) | [wu02_solicitud_acuerdo_p2p.html](file:///C:/Users/jose1/.gemini/antigravity/brain/91448f54-e32c-47d8-8d4f-1008b18b3077/wu02_solicitud_acuerdo_p2p.html) |
| **WU 03** | Validación automática del descanso normativo (Regla 12h) | [wu03_validacion_descanso_12h.html](file:///C:/Users/jose1/.gemini/antigravity/brain/91448f54-e32c-47d8-8d4f-1008b18b3077/wu03_validacion_descanso_12h.html) |
| **WU 04** | Panel de aprobación en un clic para el supervisor | [wu04_panel_aprobacion_supervisor.html](file:///C:/Users/jose1/.gemini/antigravity/brain/91448f54-e32c-47d8-8d4f-1008b18b3077/wu04_panel_aprobacion_supervisor.html) |
| **WU 05** | Actualización y exportación automática del cuadrante oficial | [wu05_actualizacion_exportacion_cuadrante.html](file:///C:/Users/jose1/.gemini/antigravity/brain/91448f54-e32c-47d8-8d4f-1008b18b3077/wu05_actualizacion_exportacion_cuadrante.html) |
| **WU 06** | Alerta de guardia urgente / Cobertura exprés de bajas | [wu06_alerta_guardia_urgente.html](file:///C:/Users/jose1/.gemini/antigravity/brain/91448f54-e32c-47d8-8d4f-1008b18b3077/wu06_alerta_guardia_urgente.html) |
| **WU 07** | Calendario personal interactivo y sincronización externa | [wu07_calendario_personal_sincronizacion.html](file:///C:/Users/jose1/.gemini/antigravity/brain/91448f54-e32c-47d8-8d4f-1008b18b3077/wu07_calendario_personal_sincronizacion.html) |
| **WU 08** | Banco de saldos de guardias y turnos (Fair-Play) | [wu08_banco_saldos_fairplay.html](file:///C:/Users/jose1/.gemini/antigravity/brain/91448f54-e32c-47d8-8d4f-1008b18b3077/wu08_banco_saldos_fairplay.html) |
| **WU 09** | Carga y gestión del cuadrante base mensual del servicio | [wu09_carga_cuadrante_base.html](file:///C:/Users/jose1/.gemini/antigravity/brain/91448f54-e32c-47d8-8d4f-1008b18b3077/wu09_carga_cuadrante_base.html) |
| **WU 10** | Modificación o retirada de oferta/propuesta de cambio | [wu10_modificacion_retirada_oferta.html](file:///C:/Users/jose1/.gemini/antigravity/brain/91448f54-e32c-47d8-8d4f-1008b18b3077/wu10_modificacion_retirada_oferta.html) |
| **WU 11** | Gestión de avisos y comunicados de planta | [wu11_gestion_avisos_planta.html](file:///C:/Users/jose1/.gemini/antigravity/brain/91448f54-e32c-47d8-8d4f-1008b18b3077/wu11_gestion_avisos_planta.html) |
| **WU 12** | Parametrización de reglas normativas y convenios del centro | [wu12_parametrizacion_reglas_convenios.html](file:///C:/Users/jose1/.gemini/antigravity/brain/91448f54-e32c-47d8-8d4f-1008b18b3077/wu12_parametrizacion_reglas_convenios.html) |
| **WU 13** | Cuadro de mandos y analítica de cumplimiento legal (Dashboard B2B) | [wu13_dashboard_cumplimiento_b2b.html](file:///C:/Users/jose1/.gemini/antigravity/brain/91448f54-e32c-47d8-8d4f-1008b18b3077/wu13_dashboard_cumplimiento_b2b.html) |
| **WU 14** | Auditoría de permutas y certificados de trazabilidad legal | [wu14_auditoria_certificados_legales.html](file:///C:/Users/jose1/.gemini/antigravity/brain/91448f54-e32c-47d8-8d4f-1008b18b3077/wu14_auditoria_certificados_legales.html) |
| **WU 15** | Gestión de indisponibilidades, vacaciones y permisos reglamentarios | [wu15_gestion_indisponibilidades_permisos.html](file:///C:/Users/jose1/.gemini/antigravity/brain/91448f54-e32c-47d8-8d4f-1008b18b3077/wu15_gestion_indisponibilidades_permisos.html) |
| **WU 16** | Gestión de personal sanitario y estructura de servicios | [wu16_gestion_personal_servicios.html](file:///C:/Users/jose1/.gemini/antigravity/brain/91448f54-e32c-47d8-8d4f-1008b18b3077/wu16_gestion_personal_servicios.html) |
| **WU 17** | Suscripción de centro hospitalario y gestión de Plan (Freemium / PRO) | [wu17_suscripcion_centro_planes.html](file:///C:/Users/jose1/.gemini/antigravity/brain/91448f54-e32c-47d8-8d4f-1008b18b3077/wu17_suscripcion_centro_planes.html) |
| **WU 18** | Autenticación y control de acceso | [wu18_autenticacion_control_acceso.html](file:///C:/Users/jose1/.gemini/antigravity/brain/91448f54-e32c-47d8-8d4f-1008b18b3077/wu18_autenticacion_control_acceso.html) |
| **WU 19** | Registro de accesos al sistema (Seguridad RGPD) | [wu19_registro_accesos_rgpd.html](file:///C:/Users/jose1/.gemini/antigravity/brain/91448f54-e32c-47d8-8d4f-1008b18b3077/wu19_registro_accesos_rgpd.html) |


