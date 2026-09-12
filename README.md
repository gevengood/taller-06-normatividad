# Taller 06 – Checklist de Cumplimiento Normativo y Seguridad

## Integrantes

- Jorge Steven Doncel Bejarano – Código: 282296 / Usuario GitHub: [gevengood](https://github.com/gevengood) / Correo: [jorgedobe@unisabana.edu.co](mailto:jorgedobe@unisabana.edu.co)
- David Santiago Buendia Londoño – Código: 306487 / Usuario GitHub: [Santiagoob7](https://github.com/Santiagoob7) / Correo: [davidbulo@unisabana.edu.co](mailto:davidbulo@unisabana.edu.co)

---

## Descripción

Repositorio oficial para el **Taller 06 de Arquitectura Empresarial (AREM)**, enfocado en la verificación de aspectos legales, normativos, de privacidad y de seguridad de la información aplicables a la arquitectura de sistemas.

El taller se divide en dos fases metodológicas:
1. **Parte 1 (Trabajo en Clase — Caso Base GobData):** Evaluación de un checklist de 12 ítems frente a la Ley 1581 de 2012 (Habeas Data) e ISO/IEC 27001 para la plataforma estatal de trámites ciudadanos GobData. Los hallazgos y bitácora se registran en `clase/checklist-gobdata.xlsx`, `clase/visualizacion-normatividad.html` y `clase/notas.md`.
2. **Parte 2 (Aplicación al Cliente Real — Insuclínicos Ltda.):** Aplicación de la metodología de 5 pasos al contexto operativo de **Insuclínicos Ltda.**, empresa de confección y comercialización de prendas e insumos médicos desechables en tela quirúrgica. Se analizan 15 criterios de cumplimiento abarcando la Ley 1581 de 2012, ISO/IEC 27001:2022, y normativas sectoriales obligatorias: **Decreto 4725 de 2005** y **Resolución 4816 de 2008 (INVIMA / MinSalud sobre Tecnovigilancia y trazabilidad de insumos médicos)** y la **Resolución DIAN 000165 de 2023** para facturación electrónica.

---

## Estructura del repositorio

```text
taller-06-normatividad/
├── README.md                              # Descripción general, datos de entrega, equipo y cliente
├── clase/
│   ├── guia_paso_a_paso_normatividad.md   # Guía metodológica de 5 pasos y fundamentos teóricos
│   ├── checklist-gobdata.xlsx             # Checklist oficial evaluado para el caso base GobData
│   ├── visualizacion-normatividad.html    # Aplicativo web interactivo del caso base GobData
│   └── notas.md                           # Registro de trabajo colaborativo en clase y asignación de tareas
├── entrega/
│   ├── checklist-cliente.xlsx             # Checklist diligenciado para Insuclínicos (Checklist General y Brechas)
│   ├── informe.md                         # Informe técnico detallado, análisis de brechas, modelo ArchiMate e investigación
│   └── referencias.md                     # Fuentes legales, regulatorias y estándares técnicos en formato APA
└── plantillas/
    ├── plantilla_checklist.xlsx           # Plantilla oficial en blanco del curso
    ├── plantilla_informe_taller.md        # Plantilla base para el informe técnico
    ├── plantilla_notas.md                 # Plantilla base para el registro de clase
    └── plantilla_referencias.md           # Plantilla base para las referencias bibliográficas
```

---

## Contenido de la entrega (Parte 2 – Cliente real)

| Documento | Contenido |
|---|---|
| [`entrega/checklist-cliente.xlsx`](entrega/checklist-cliente.xlsx) | Matriz oficial en Excel con dos hojas: **`Checklist General`** (15 criterios evaluados con evidencia real) y **`Brechas Identificadas`** (13 brechas con análisis de riesgo y recomendación priorizada). |
| [`entrega/informe.md`](entrega/informe.md) | Informe técnico completo: aplicación de los 5 pasos metodológicos, análisis de necesidades de Insuclínicos, vista ArchiMate de Motivación en Mermaid (`Constraint`), tabla de actores y tres investigaciones complementarias (INVIMA, Ley 1581 en PyMEs e ISO 27001 básico). |
| [`entrega/referencias.md`](entrega/referencias.md) | Catálogo de fuentes primarias, normativas colombianas (Congreso, Presidencia, MinSalud, INVIMA, DIAN, SIC), normas ISO y literatura técnica citada formalmente en APA. |

---

## Resumen del Diagnóstico Normativo (Insuclínicos Ltda.)

### 1. Metodología de 5 pasos aplicada
- **Paso 1 (Datos y Procesos Sensibles):** Identificación de datos de contacto de clientes (~40 clínicas y spas), datos de nómina de los 6 trabajadores, trazabilidad de lotes de tela quirúrgica y facturas electrónicas.
- **Paso 2 (Construcción del Checklist):** Organización en 8 categorías (Consentimiento, Seguridad ISO 27001, Protección de Datos, DLP, Retención, Roles/Capacitación, Regulación Sanitaria INVIMA y Tributaria DIAN).
- **Paso 3 (Evaluación con Evidencia):** 2 criterios clasificados como **✅ Cumple** (retención legal contable y facturación electrónica DIAN) y 13 criterios clasificados como **⚠️ Parcial** sustentados en la operación real.
- **Paso 4 (Documentación de Riesgos):** Traslado de cada parcial a la tabla de brechas con valoración de riesgos legales, operativos y comerciales.
- **Paso 5 (Priorización y Recomendaciones):** Definición de 4 brechas de prioridad **Alta**, 6 de prioridad **Media** y 3 de prioridad **Baja**, con acciones viables y proporcionales a una microempresa.

### 2. Brechas de Prioridad Alta identificadas
1. **Seguridad (Continuidad y Backup):** Riesgo crítico de pérdida de datos operativos en Excel por falta de respaldo automatizado fuera de sede.
2. **Seguridad (Control de Accesos):** Falta de autenticación individual por perfiles de usuario en computadores compartidos de oficina.
3. **Regulación Sanitaria (INVIMA / Tecnovigilancia):** Dificultad de trazabilidad ágil lote a lote entre rollos de tela y pedidos despachados ante requerimientos o alertas sanitarias.
4. **Consentimiento (Ley 1581):** Captación de datos de clientes por WhatsApp y correo sin autorización previa, expresa e informada ni aviso de privacidad.

---

## Cliente

**Insuclínicos Ltda.**  
Empresa colombiana con sede en Bogotá (Calle 164 # 19-15), dedicada a la manufactura y comercialización de prendas e insumos médicos desechables en tela quirúrgica para el sector salud y estética.  
**Contacto:** Santiago Martínez — Representante Legal.

---

## Confidencialidad

La información consignada en este repositorio se utiliza exclusivamente con fines académicos en el marco del curso de Arquitectura Empresarial (AREM) de la Universidad de La Sabana, previa autorización del cliente. Los datos comerciales y sensibles han sido tratados respetando los acuerdos de confidencialidad definidos.
