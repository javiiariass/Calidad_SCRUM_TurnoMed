# Caso de Estudio TurnoMed — Historias de Usuario (Work Units)

* **Documento de Google Docs:** [Caso de Estudio TurnoMed - Work Units](https://docs.google.com/document/d/1CU93o89bRjTogy4Qtt-nlEQ8Mu_qkaZQOea5gXflYh8/edit)
* **Documento PDF Local:** [Caso de Estudio TurnoMed - Work Units.pdf](file:///c:/Users/jose1/Documents/Ingenieria%20Inform%C3%A1tica/CMEPPS/TurnoMed/Caso%20de%20Estudio%20TurnoMed%20-%20Work%20Units.pdf)

---

## Resumen del Product Backlog (19 Work Units)

| # | Nombre de la Work Unit (HU) | Usuario / Rol | Importancia | Urgencia | Riesgo | Esfuerzo (pts) |
| :- | :--- | :--- | :---: | :---: | :---: | :---: |
| **WU 01** | Publicación de guardia para intercambio | Sanitario | Muy Alta | Alta | Bajo | 5 |
| **WU 02** | Solicitud y acuerdo de cambio entre compañeros (Peer-to-Peer) | Sanitario | Muy Alta | Alta | Medio | 5 |
| **WU 03** | Validación automática del descanso normativo (Regla de las 12 horas) | Sanitario / Sistema Validador | Muy Alta | Muy Alta | Alto | 8 |
| **WU 04** | Panel de aprobación en un clic para el supervisor | Supervisor de Planta | Muy Alta | Alta | Bajo | 5 |
| **WU 05** | Actualización y exportación automática del cuadrante oficial | Supervisor de Planta | Alta | Media | Medio | 5 |
| **WU 06** | Alerta de guardia urgente / Cobertura exprés de bajas | Supervisor de Planta | Alta | Alta | Medio | 8 |
| **WU 07** | Calendario personal interactivo y sincronización externa | Sanitario | Media | Media | Bajo | 5 |
| **WU 08** | Banco de saldos de guardias y turnos (Fair-Play) | Sanitario / Supervisor de Planta | Media | Baja | Bajo | 3 |
| **WU 09** | Carga y gestión del cuadrante base mensual del servicio | Supervisor de Planta | Alta | Alta | Medio | 8 |
| **WU 10** | Modificación o retirada de oferta/propuesta de cambio | Sanitario | Baja | Baja | Bajo | 2 |
| **WU 11** | Gestión de avisos y comunicados de planta | Supervisor de Planta | Media | Baja | Bajo | 2 |
| **WU 12** | Parametrización de reglas normativas y convenios del centro | Dirección de RRHH / Administrador | Media | Media | Medio | 3 |
| **WU 13** | Cuadro de mandos y analítica de cumplimiento legal (Dashboard B2B) | Dirección de RRHH / Gestor Hospitalario | Media | Baja | Bajo | 5 |
| **WU 14** | Auditoría de permutas y certificados de trazabilidad legal | Supervisor de Planta / Dirección de RRHH | Media | Baja | Bajo | 3 |
| **WU 15** | Gestión de indisponibilidades, vacaciones y permisos reglamentarios | Sanitario / Supervisor de Planta | Media | Media | Bajo | 5 |
| **WU 16** | Gestión de personal sanitario y estructura de servicios | Administrador | Baja | Baja | Bajo | 5 |
| **WU 17** | Suscripción de centro hospitalario y gestión de Plan (Freemium / PRO) | Gestor Hospitalario / Visitante | Baja | Baja | Bajo | 5 |
| **WU 18** | Autenticación y control de acceso | Visitante / Usuario Registrado | Baja | Baja | Bajo | 2 |
| **WU 19** | Registro de accesos al sistema (Seguridad RGPD) | Administrador | Baja | Muy Baja | Bajo | 3 |

---

## Detalle Sintetizado de las 19 Historias de Usuario

### WU 01 — Publicación de guardia para intercambio
* **Usuario:** Sanitario | **Importancia:** Muy Alta | **Urgencia:** Alta | **Riesgo:** Bajo | **Esfuerzo:** 5
* **Descripción:** El sanitario selecciona un turno propio asignado y lo publica en el tablón de su servicio indicando qué fechas o franjas busca a cambio (o dejándolo abierto a propuestas). La oferta sólo es visible para compañeros de su misma categoría profesional y servicio.
* **Pruebas de Aceptación:**
  * Al publicar, el turno debe pertenecer al sanitario autenticado y estar en una fecha futura.
  * No permitir publicar un turno que ya tenga una oferta activa en el tablón.
  * Permitir indicar turnos preferidos a cambio o marcar 'Abierto a propuestas / Cesión al banco de saldos'.
  * La oferta sólo debe ser visible para sanitarios de la misma categoría profesional y unidad.
  * Al publicar, el turno cambia su estado visual a 'Ofertado' en el calendario personal.

---

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

---

### WU 03 — Validación automática del descanso normativo (Regla de las 12 horas)
> *Nota:* Esta WU constituye el núcleo diferencial del MVP y se invoca en tiempo real durante la WU “Solicitud y acuerdo de cambio entre compañeros”.
* **Usuario:** Sanitario / Sistema Validador | **Importancia:** Muy Alta | **Urgencia:** Muy Alta | **Riesgo:** Alto | **Esfuerzo:** 8
* **Descripción:** Antes de confirmar cualquier propuesta o acuerdo, el sistema comprueba automáticamente los turnos anteriores y posteriores de ambos implicados. Si el cambio supone encadenar jornadas con menos de 12 horas de descanso obligatorio, solapes horarios o exceso de jornada semanal, bloquea la operación indicando el motivo legal.
* **Pruebas de Aceptación:**
  * Bloquear cualquier acuerdo donde alguno de los sanitarios tenga menos de 12 horas de descanso entre jornadas.
  * Bloquear el intercambio si alguno de los dos ya tiene asignado un turno solapado en esa fecha/franja.
  * Bloquear el intercambio si ambos profesionales no pertenecen a la misma categoría requerida.
  * Mostrar un aviso claro indicando qué regla normativa se vulnera y qué turnos entran en conflicto.
  * Marcar el acuerdo como 'Pre-validado legalmente (Cumple 12h)' cuando supere todas las comprobaciones.

---

### WU 04 — Panel de aprobación en un clic para el supervisor
> *Nota:* Conviene implementar esta WU tras las WUs de acuerdo P2P y validación normativa, ya que recibe las permutas pre-validadas.
* **Usuario:** Supervisor de Planta | **Importancia:** Muy Alta | **Urgencia:** Alta | **Riesgo:** Bajo | **Esfuerzo:** 5
* **Descripción:** Muestra al supervisor todas las solicitudes de cambio ya acordadas entre compañeros y pre-validadas legalmente. El supervisor puede aprobarlas en un solo clic o rechazarlas indicando el motivo, notificándose la decisión al instante a ambos sanitarios.
* **Pruebas de Aceptación:**
  * Visualizar la lista de acuerdos pendientes ordenados por proximidad de la fecha de la guardia.
  * Permitir aprobar un acuerdo en un clic, cambiando su estado a 'Aprobado' y notificando a ambos sanitarios.
  * Permitir rechazar un acuerdo exigiendo un motivo de rechazo que se notificará a los implicados.
  * Al rechazar un acuerdo, mantener sin cambios la titularidad original de los turnos en el cuadrante.
  * Mostrar el historial de solicitudes aprobadas y rechazadas por el supervisor.

---

### WU 05 — Actualización y exportación automática del cuadrante oficial
* **Usuario:** Supervisor de Planta | **Importancia:** Alta | **Urgencia:** Media | **Riesgo:** Medio | **Esfuerzo:** 5
* **Descripción:** Al aprobarse un cambio o cobertura, el sistema actualiza automáticamente la titularidad de los turnos en el cuadrante general del servicio y genera un registro de auditoría. Permite exportar el cuadrante actualizado en formato PDF o Excel para Dirección y RRHH.
* **Pruebas de Aceptación:**
  * Actualizar de forma inmediata los titulares de los turnos en el cuadrante del servicio tras la aprobación.
  * Registrar automáticamente en auditoría la fecha/hora, los sanitarios implicados y el supervisor aprobador.
  * Exportar el cuadrante mensual o semanal actualizado en formato PDF y Excel (`.xlsx` / `.csv`).
  * Resaltar visualmente en el cuadrante qué turnos han sido permutados respecto a la planificación inicial.

---

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

---

### WU 07 — Calendario personal interactivo y sincronización externa
* **Usuario:** Sanitario | **Importancia:** Media | **Urgencia:** Media | **Riesgo:** Bajo | **Esfuerzo:** 5
* **Descripción:** Muestra a cada sanitario una vista mensual y semanal de sus turnos (mañana, tarde, noche y guardia 24h) diferenciados por colores y estado. Permite sincronizar los turnos en tiempo real con calendarios externos (Google Calendar / iCal).
* **Pruebas de Aceptación:**
  * Visualizar el calendario personal en vista mensual y semanal con colores según tipo de turno.
  * Mostrar el estado de cada turno (confirmado, ofertado en tablón, pendiente de aprobación).
  * Generar enlace iCal (`.ics`) o vincular con Google Calendar para sincronizar los turnos automáticamente.
  * Reflejar en el calendario externo cualquier cambio de turno en cuanto sea aprobado por el supervisor.

---

### WU 08 — Banco de saldos de guardias y turnos (Fair-Play)
* **Usuario:** Sanitario / Supervisor de Planta | **Importancia:** Media | **Urgencia:** Baja | **Riesgo:** Bajo | **Esfuerzo:** 3
* **Descripción:** Registra automáticamente el balance histórico de guardias cedidas y asumidas cuando se cubre un turno sin trueque recíproco inmediato, mostrando un marcador transparente de turnos a favor (`+1`) o pendientes de devolver (`-1`) por sanitario.
* **Pruebas de Aceptación:**
  * Sumar `+1` al saldo del sanitario que asume un turno sin trueque recíproco y restar `-1` al cedente.
  * Mantener el saldo sin cambios cuando el intercambio sea un trueque recíproco equivalente (`1` por `1`).
  * Visualizar el saldo actual y el historial de movimientos que lo justifican.
  * Permitir al supervisor consultar los saldos de la planta para repartir equitativamente las coberturas.

---

### WU 09 — Carga y gestión del cuadrante base mensual del servicio
> *Nota:* Es recomendable implementar esta WU en las primeras iteraciones ya que carga los turnos iniciales sobre los que operan los cambios.
* **Usuario:** Supervisor de Planta | **Importancia:** Alta | **Urgencia:** Alta | **Riesgo:** Medio | **Esfuerzo:** 8
* **Descripción:** Permite al supervisor crear, editar o importar desde Excel/CSV la planificación mensual inicial de su unidad. El sistema advierte si existen puestos mínimos descubiertos o infracciones de las 12 horas de descanso antes de publicar el cuadrante para todo el servicio.
* **Pruebas de Aceptación:**
  * Permitir importar el cuadrante mensual desde Excel/CSV o asignar turnos sobre la cuadrícula mensual.
  * Resaltar alertas si el cuadrante base contiene solapes o incumple el descanso mínimo de 12 horas.
  * Advertir si alguna franja horaria no alcanza el mínimo de personal requerido en la planta.
  * Permitir guardar el cuadrante como borrador y publicarlo notificando a los sanitarios del servicio.

---

### WU 10 — Modificación o retirada de oferta/propuesta de cambio
> *Nota:* Puede resultar interesante implementar esta WU después de las WUs de publicación y solicitud P2P puesto que reutiliza su interfaz.
* **Usuario:** Sanitario | **Importancia:** Baja | **Urgencia:** Baja | **Riesgo:** Bajo | **Esfuerzo:** 2
* **Descripción:** Tras publicar una guardia o enviar una propuesta de cambio, el sanitario puede editar las fechas solicitadas o retirar su oferta/propuesta siempre que aún no haya sido aprobada por el supervisor ni haya expirado el plazo límite previo al turno.
* **Pruebas de Aceptación:**
  * Permitir al ofertante editar las preferencias o cancelar su oferta mientras no esté aprobada.
  * Permitir a un candidato retirar su propuesta de trueque antes de que sea aprobada.
  * (Excepción) Si el cambio ya fue aprobado o expiró el plazo previo al turno, NO permitir su modificación.
  * Al retirar una oferta con propuestas pendientes, notificar automáticamente la cancelación a los postulantes.

---

### WU 11 — Gestión de avisos y comunicados de planta
> *Nota:* Esta WU proporciona el módulo de avisos que también aprovechan las notificaciones de acuerdos y bajas urgentes.
* **Usuario:** Supervisor de Planta | **Importancia:** Media | **Urgencia:** Baja | **Riesgo:** Bajo | **Esfuerzo:** 2
* **Descripción:** Permite al supervisor crear, guardar como borrador, enviar y eliminar (si no han sido enviados) avisos internos dirigidos a toda la planta, a una categoría profesional concreta o a los sanitarios asignados en una fecha determinada.
* **Pruebas de Aceptación:**
  * Enviar avisos por notificación push y email filtrando destinatarios (planta completa, categoría o fecha).
  * Guardar avisos en borrador para modificarlos o enviarlos posteriormente.
  * Permitir eliminar únicamente avisos en preparación que aún no hayan sido enviados.
  * Consultar el registro de avisos enviados indicando fecha, asunto, autor y destinatarios.

---

### WU 12 — Parametrización de reglas normativas y convenios del centro
* **Usuario:** Dirección de RRHH / Administrador | **Importancia:** Media | **Urgencia:** Media | **Riesgo:** Medio | **Esfuerzo:** 3
* **Descripción:** Permite configurar las reglas del convenio del hospital que aplica el validador automático: horas mínimas de descanso entre jornadas (12h), descanso semanal (36h), tope de horas semanales, antelación mínima de solicitud y catálogo de tipos de turno (horarios y duración).
* **Pruebas de Aceptación:**
  * Editar parámetros normativos (descanso mínimo entre jornadas, tope semanal y antelación mínima).
  * Impedir configurar un descanso entre jornadas inferior a las 12 horas legales.
  * Gestionar los tipos de turno (código, horario, duración y color) sin permitir códigos repetidos.
  * Solicitar confirmación al guardar cambios normativos y actualizar las reglas del validador.

---

### WU 13 — Cuadro de mandos y analítica de cumplimiento legal (Dashboard B2B)
* **Usuario:** Dirección de RRHH / Gestor Hospitalario | **Importancia:** Media | **Urgencia:** Baja | **Riesgo:** Bajo | **Esfuerzo:** 5
* **Descripción:** Muestra a Dirección y RRHH un panel con las métricas clave del hospital y por unidad: tiempo medio de resolución de cambios (< 2h), porcentaje de bajas urgentes cubiertas, porcentaje de cambios validados sin infracción legal (100% cumplimiento 12h) y usuarios activos (WAU/MAU).
* **Pruebas de Aceptación:**
  * Visualizar las métricas clave filtrando por servicio/planta y rango de fechas.
  * Mostrar el total de intentos de cambio bloqueados por incumplir el descanso legal.
  * Comparar indicadores de rotación y cobertura entre unidades (Urgencias, UCI, Quirófanos, Planta).
  * Exportar el resumen de métricas del cuadro de mandos en formato PDF.

---

### WU 14 — Auditoría de permutas y certificados de trazabilidad legal
* **Usuario:** Supervisor de Planta / Dirección de RRHH | **Importancia:** Media | **Urgencia:** Baja | **Riesgo:** Bajo | **Esfuerzo:** 3
* **Descripción:** Permite consultar y filtrar el historial completo de cambios de turno y coberturas (solicitante, receptor, fechas, validación de 12h y supervisor que aprobó), así como emitir certificados en PDF para justificar el cumplimiento normativo ante Inspección de Trabajo.
* **Pruebas de Aceptación:**
  * Generar listados de permutas filtrando por sanitario, unidad, fechas o estado (aprobada, rechazada).
  * Permitir seleccionar columnas visibles y ordenar por fecha de guardia o fecha de resolución.
  * Generar fichero PDF con el certificado de trazabilidad legal de una permuta o periodo concreto.

---

### WU 15 — Gestión de indisponibilidades, vacaciones y permisos reglamentarios
* **Usuario:** Sanitario / Supervisor de Planta | **Importancia:** Media | **Urgencia:** Media | **Riesgo:** Bajo | **Esfuerzo:** 5
* **Descripción:** Permite a los sanitarios solicitar y al supervisor registrar vacaciones, bajas médicas o días de libre disposición. Las fechas aprobadas quedan bloqueadas en el calendario del sanitario, excluyéndolo automáticamente de intercambios y alertas de guardia urgente en ese periodo.
* **Pruebas de Aceptación:**
  * Permitir registrar solicitudes de vacaciones, permisos o bajas indicando fecha de inicio, fin y motivo.
  * Advertir al supervisor si el sanitario tiene guardias asignadas dentro del periodo de ausencia solicitado.
  * Ofrecer lanzar alerta de cobertura o publicar en tablón las guardias afectadas al aprobar una baja/permiso.
  * Excluir automáticamente a los sanitarios de permiso o baja de las notificaciones de guardia urgente.

---

### WU 16 — Gestión de personal sanitario y estructura de servicios
* **Usuario:** Administrador | **Importancia:** Baja | **Urgencia:** Baja | **Riesgo:** Bajo | **Esfuerzo:** 5
* **Descripción:** El administrador gestiona las altas, bajas, modificaciones y consulta de servicios hospitalarios y usuarios (Sanitario con su categoría: Enfermero/a, MIR, Adjunto; Supervisor; RRHH y Administrador). Un usuario puede tener varios roles y el sistema le envía por email su userid y contraseña inicial.
* **Pruebas de Aceptación:**
  * Visualizar, buscar, filtrar y ordenar usuarios por nombre, código seudonimizado, categoría, servicio o rol.
  * Permitir dar de alta, modificar y eliminar usuarios solicitando confirmación.
  * Impedir eliminar un sanitario que tenga turnos futuros asignados o cambios en curso.
  * Verificar que no existan usuarios duplicados y que cada sanitario tenga categoría y servicio asignados.
  * Notificar automáticamente por email las credenciales al dar de alta o dar de baja un usuario.

---

### WU 17 — Suscripción de centro hospitalario y gestión de Plan (Freemium / PRO)
* **Usuario:** Gestor Hospitalario / Visitante | **Importancia:** Baja | **Urgencia:** Baja | **Riesgo:** Bajo | **Esfuerzo:** 5
* **Descripción:** Permite registrar una planta u hospital eligiendo entre el Plan Freemium (gratuito hasta 15 sanitarios por planta) o el Plan PRO B2B (plantas ilimitadas, validador legal completo y exportación a RRHH). Calcula el importe según las plantas contratadas, procesa el pago con tarjeta y emite factura en PDF.
* **Pruebas de Aceptación:**
  * Permitir el alta gratuita en modalidad Freemium controlando el límite de 15 usuarios por planta.
  * Advertir respecto de inscripciones repetidas para un mismo centro o unidad.
  * Calcular y mostrar el coste total según el número de plantas o licencias seleccionadas en el Plan PRO.
  * Realizar el pago seguro mediante tarjeta y emitir el recibo/factura en formato PDF.

---

### WU 18 — Autenticación y control de acceso
* **Usuario:** Visitante / Usuario Registrado | **Importancia:** Baja | **Urgencia:** Baja | **Riesgo:** Bajo | **Esfuerzo:** 2
* **Descripción:** Control de acceso al sistema mediante userid y contraseña. Si el usuario tiene más de un rol asignado (p. ej., Sanitario y Supervisor), solicita con qué perfil desea acceder. Incluye envío de enlace por email para recuperar la contraseña en caso de olvido.
* **Pruebas de Aceptación:**
  * Validar acceso mediante userid y password, bloqueando temporalmente tras varios intentos fallidos.
  * Solicitar el tipo de acceso tras autenticarse en caso de que el usuario posea más de un rol.
  * Enviar email de recuperación de contraseña cuando el usuario lo solicite.

---

### WU 19 — Registro de accesos al sistema (Seguridad RGPD)
* **Usuario:** Administrador | **Importancia:** Baja | **Urgencia:** Muy Baja | **Riesgo:** Bajo | **Esfuerzo:** 3
* **Descripción:** Consulta de los accesos realizados al sistema incluyendo fecha-hora de login, userid (código seudonimizado), rol utilizado y fecha-hora de logout para auditoría de seguridad y cumplimiento RGPD.
* **Pruebas de Aceptación:**
  * Visualizar el listado de accesos con fecha-hora login, userid, rol y fecha-hora logout.
  * Permitir filtrar los registros por usuario, rango de fechas o intentos de acceso fallidos.
