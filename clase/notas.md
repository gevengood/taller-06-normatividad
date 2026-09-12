# 🗒️ Registro de Trabajo en Clase - Taller 6: Checklist de Cumplimiento Normativo

## 📆 Fecha de la sesión
12 de septiembre de 2026 (Sesión presencial / híbrida)

## 👥 Integrantes presentes
- Jorge Steven Doncel Bejarano — Código: 282296 / [jorgedobe@unisabana.edu.co](mailto:jorgedobe@unisabana.edu.co)
- David Santiago Buendia Londoño — Código: 306487 / [davidbulo@unisabana.edu.co](mailto:davidbulo@unisabana.edu.co)

## 🧠 Actividades realizadas en clase

Durante la sesión se abordó el marco de cumplimiento normativo y seguridad de la información aplicado a la arquitectura empresarial, siguiendo la metodología de 5 pasos presentada en la guía de clase:

1. **Revisión teórica y metodológica:**
   - El docente explicó los fundamentos de la Ley 1581 de 2012 (Habeas Data en Colombia), el Decreto 1377 de 2013, los derechos ARCO (Acceso, Rectificación, Cancelación y Oposición), y su interacción con los estándares ISO/IEC 27001:2022 (específicamente controles de acceso, cifrado, copias de seguridad y respuesta a incidentes).
   - Se enfatizó la regla clave de auditoría: *"Cumplir la ley no es marcar una casilla, es sostener una evidencia"*. Un ítem sin evidencia concreta no es evaluable.
   - Se aclaró el concepto de **Brecha**: no es un tercer estado del checklist (solo existen ✅ Cumple y ⚠️ Parcial), sino una tabla derivada que documenta el riesgo y la recomendación priorizada de cada control deficiente.

2. **Evaluación del caso base GobData (Parte 1):**
   - Se analizó el portal estatal de trámites ciudadanos GobData frente a la matriz de 12 ítems del checklist general (`clase/checklist-gobdata.xlsx`).
   - Se revisó el aplicativo interactivo `clase/visualizacion-normatividad.html` para validar cómo los ítems marcados como ⚠️ Parcial (revocatoria de consentimiento por canal físico, ausencia de plan formal BCP/DRP, falta de DLP en exportaciones, carencia de proceso de anonimización de datos sensibles y capacitaciones sin evaluación de efectividad) alimentan la tabla de **Brechas Identificadas**.
   - Se discutió la relación entre la tabla de brechas y la capa de Motivación de ArchiMate, entendiendo cada brecha como una restricción legal u operativa (`Constraint`) que condiciona los procesos de negocio.

3. **Discusión sobre la aplicación al cliente real (Insuclínicos Ltda.):**
   - Se contrastó el escenario de GobData (entidad pública con infraestructura tecnológica y DPO) con la realidad de nuestro cliente **Insuclínicos Ltda.** (empresa manufacturera de 6 empleados, operando con WhatsApp, Excel local, remisiones físicas y facturación electrónica).
   - Se identificó la necesidad de investigar regulaciones sectoriales adicionales propias de la industria de insumos médicos desechables en tela quirúrgica, en particular los decretos y resoluciones del **INVIMA / MinSalud** (Decreto 4725 de 2005 sobre dispositivos médicos y Resolución 4816 de 2008 sobre el Programa Nacional de Tecnovigilancia y trazabilidad de lotes).

## 🧩 Boceto inicial del modelo (Hallazgos preliminares GobData)

A continuación se resume la matriz de trabajo desarrollada en clase para los 12 controles evaluados en GobData:

| N° | Categoría | Criterio de Cumplimiento | Nivel de Cumplimiento | Evidencia / Justificación observada | Recomendación preliminar |
|---|---|---|:---:|---|---|
| 1 | Consentimiento | Consentimiento informado previo | ✅ Cumple | Checkbox de términos en formulario de registro | Especificar finalidades secundarias |
| 2 | Consentimiento | Revocatoria del consentimiento | ⚠️ Parcial | Solo mediante derecho de petición escrito | Implementar módulo digital de revocatoria |
| 3 | Seguridad (ISO 27001) | Política formal de seguridad | ✅ Cumple | Política basada en ISO/IEC 27001:2013 documentada | Actualizar a versión ISO 27001:2022 |
| 4 | Seguridad (ISO 27001) | Cifrado en tránsito y reposo | ✅ Cumple | Certificado TLS v1.3 y AES-256 en BD | Auditoría anual de llaves y algoritmos |
| 5 | Seguridad (ISO 27001) | Plan de continuidad (BCP/DRP) | ⚠️ Parcial | Backups diarios automáticos sin pruebas de restauración | Diseñar y probar protocolo DRP/BCP formal |
| 6 | Protección de Datos | Oficial de Protección de Datos (DPO) | ✅ Cumple | Funcionario asignado según directiva Ley 1581 | Fortalecer independencia y reportes periódicos |
| 7 | Protección de Datos | Logs y auditoría de accesos | ✅ Cumple | Registro automatizado de eventos y consultas | Definir retención inmutable de logs |
| 8 | Prevención de Fugas | Control de exportaciones (DLP) | ⚠️ Parcial | Descargas en Excel sin marcas de agua ni bloqueo | Implementar controles DLP en capas perimetrales |
| 9 | Retención | Política formal de retención | ✅ Cumple | Tabla de retención documental aprobada por AGN | Automatizar purgas periódicas |
| 10 | Retención | Anonimización de datos obsoletos | ⚠️ Parcial | No hay proceso documentado ni algoritmos aplicados | Definir política de seudonimización / borrado |
| 11 | Roles y Permisos | Matriz de roles y accesos | ✅ Cumple | Matriz RBAC documentada en directorio activo | Revisión trimestral de cuentas inactivas |
| 12 | Roles y Permisos | Capacitación en datos personales | ⚠️ Parcial | Charla anual de inducción sin examen ni métricas | Aplicar evaluaciones y pruebas prácticas |

## 🔁 Tareas definidas para la entrega final (Insuclínicos Ltda.)

| Tarea asignada | Responsable | Fecha estimada |
|---|---|---|
| Mapeo de datos sensibles, flujos AS-IS y activos de información de Insuclínicos | Jorge Doncel | 13/09/2026 |
| Diligenciamiento de `entrega/checklist-cliente.xlsx` (Checklist General y Brechas) | Jorge Doncel & David Buendia | 14/09/2026 |
| Redacción del informe técnico (`entrega/informe.md`) con los 5 pasos y análisis | David Buendia | 15/09/2026 |
| Diagramación de la vista ArchiMate de Motivación (`Constraint` y procesos) | Jorge Doncel | 15/09/2026 |
| Investigación complementaria (INVIMA, tecnovigilancia, ISO 27001 en PyMEs) | David Buendia | 16/09/2026 |
| Consolidación de `entrega/referencias.md` en formato APA y verificación final | Todo el equipo | 16/09/2026 |

---

_Este documento resume el trabajo colaborativo realizado durante la sesión del Taller 6 en el curso AREM — Universidad de La Sabana._
