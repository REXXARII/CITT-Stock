# CITT Stock 📦

> Plataforma web de gestión, control de inventario y trazabilidad de activos para el **Centro de Innovación y Transferencia Tecnológica (CITT)** – Duoc UC Sede San Bernardo.

---

## 📌 Descripción General

**CITT Stock** es una solución tecnológica desarrollada para optimizar la administración de activos, herramientas e insumos consumibles en el CITT. El sistema centraliza el control de inventario y automatiza los flujos de préstamos, devoluciones y entregas definitivas, integrando lectura y generación de códigos QR para una trazabilidad precisa en tiempo real.

---

## ✨ Características Principales

* 🔄 **Control de Movimientos:** Gestión de tres flujos clave: préstamos (con fecha límite), devoluciones y pedidos o entregas definitivas de consumibles (sin fecha de retorno).
* 🖨️ **Gestión de Consumibles:** Control matemático automatizado para filamentos 3D u otros consumibles (ej. ingreso de stock base en kilogramos y consumo descontado directamente en gramos).
* 📍 **Organización por Casilleros:** Mapeo de disponibilidad de inventario en tiempo real (Ocupado / Disponible). Incluye excepciones para mobiliario categorizado como "Sin Casillero" o de libre disposición.
* 🏷️ **Identificación vía Código QR:** Generación automática de códigos según su categoría (IM-CITT-, 3D-CITT-, TA-CITT-, EQ-CITT-) y escaneo ágil de etiquetas.
* 🛠️ **Módulo de Mantenimiento:** Seguimiento de órdenes de trabajo (OT) de tipo preventivas y correctivas bajo los estados: En proceso, En diagnóstico y Finalizada.
* 📊 **Analítica y Reportes:** Dashboard interactivo, alertas de stock crítico y exportación de datos.

---

## 👥 Roles y Permisos

El sistema opera bajo un modelo de accesos jerárquicos:
* **Administrador (Paz Morales Saavedra):** Control total del sistema, parametrización, reportes y aprobaciones generales.
* **Alumno Líder (AL):** Gestión operativa presencial en ventanilla para registrar préstamos, devoluciones y entregas definitivas.
* **Usuario Global:** Comunidad de la sede (estudiantes y docentes). Pueden consultar el catálogo y solicitar insumos de manera presencial, sujeto a la aprobación de un administrador o alumno líder.

---

## 🛠️ Tecnologías Utilizadas

El proyecto está construido bajo una arquitectura moderna, escalable y con soporte Multi-Tenancy (estrategia Shared Database, Shared Schema):

* **Lenguaje Base:** TypeScript.
* **Frontend:** Next.js (React) para la interfaz de usuario, paneles y lecturas QR.
* **Backend:** NestJS (Node.js) para la estructuración de la API REST y la lógica de negocio.
* **Base de Datos:** PostgreSQL.
* **UI & Estilos:** Tailwind CSS, componentes de Shadcn UI y Lucide React para la iconografía.

---

## 👥 Integrantes y Representantes del Proyecto

* **Representante de la Contraparte / Cliente:**
  * Paz Constanza Morales Saavedra (`pc.morales@profesor.duoc.cl`)

* **Unidad Ejecutora:**
  * Arianette Pavez (Líder)
  * Tania Gaete
  * Jean García
