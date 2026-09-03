# CITT Stock 📦

> Plataforma Web de Gestión, Control, Trazabilidad e Inventarios para el **Centro de Innovación y Transferencia Tecnológica (CITT)** – Duoc UC Sede San Bernardo.

---

## 📌 Descripción General del Proyecto

**CITT Stock** es un sistema web de gestión de inventarios y trazabilidad diseñado para resolver la desorganización de registros manuales y planillas en el CITT de Duoc UC San Bernardo. 

El CITT es un espacio de trabajo dinámico con múltiples dependencias, estantes y casilleros. A diferencia de un pañol convencional, en el CITT coexisten:
1. **Activos de préstamo** (herramientas y equipos que deben devolverse).
2. **Insumos consumibles** (materiales como filamentos 3D que se entregan de forma definitiva).
3. **Mobiliario y equipos libres** distribuidos por toda la sede.

La solución permite gestionar de forma automatizada los flujos de entradas, salidas, asignaciones, devoluciones y mantenimiento en tiempo real con soporte de lectura y generación de **códigos QR**.

---

## 🔥 Características y Funcionalidades Principales

### 1. Control de Movimientos y Formularios Inteligentes
El sistema gestiona tres flujos operativos clave:
* 🔄 **Préstamo:** Salida temporal de activos. **Exige obligatoriamente una fecha límite/retorno**.
* ↩️ **Devolución:** Registro del retorno del equipo prestado y actualización de su disponibilidad.
* 📦 **Pedido (Entrega Definitiva):** Despacho de insumos consumibles (ej. filamentos 3D). Al seleccionar esta opción, el sistema **deshabilita y oculta automáticamente el campo de fecha de retorno**.

En cada registro se debe seleccionar la **Escuela Solicitante** (Construcción, Mecánica, Administración, Informática, Salud, Turismo, Naturaleza) y contar con **aprobación presencial**.

### 2. Control Especial de Consumibles (Filamento 3D)
* **Unidad de Ingreso y Stock Base:** Kilogramos ($\text{kg}$).
* **Unidad de Descuento/Salida:** Gramos ($\text{g}$).
* **Cálculo Matemático Automático:** La plataforma convierte las salidas en gramos a kilogramos. Por ejemplo, al despachar $50\text{ g}$, el sistema descuenta $0.05\text{ kg}$ de una existencia global de $10\text{ kg}$, dejando el stock saldo en $9.95\text{ kg}$.

### 3. Ubicaciones, Casilleros y Excepciones Físicas
* **Mapeo por Casilleros:** Sustituye la ubicación genérica por una asignación a casilleros estructurados, indicando su estado en tiempo real (**Ocupado / Disponible**).
* **Excepción "Sin Casillero":** Para mobiliario fijo, computadores de libre disposición o sillas plegables/móviles, el sistema permite la etiqueta **"Sin Casillero / Sin ubicación fija"**.

### 4. Codificación Autogenerada y Etiquetas QR
Los códigos se asignan de forma automática asociando un correlativo único según la categoría del activo:
* 🪑 **Mobiliario:** `IM-CITT-[Número]`
* 🖨️ **3D:** `3D-CITT-[Número]`
* 🛠️ **Talleres:** `TA-CITT-[Número]`
* 💻 **Equipamiento:** `EQ-CITT-[Número]`

Al registrar el producto, el sistema autogenera su correspondiente **código QR** para escaneo físico y digital.

### 5. Ficha de Activo (`detalle-activo.html`), Recepción de Stock y Bajas
* **Vista Modal:** Al hacer clic en la acción "ver" (icono del ojo) sobre un activo, se despliega una ventana flotante con especificaciones técnicas, historial de movimientos, observaciones y su código QR.
* **Recepción de Stock:** Permite incrementar las existencias de un activo existente en lugar de duplicar su registro.
* **Baja de Activos:** Opción con confirmación para retirar equipos dañados o fuera de servicio, alimentando un historial de bajas (mensual/anual).

### 6. Órdenes de Trabajo (OT) y Mantenimiento
* **Tipos de Intervención:** *Preventivo* (programado) y *Correctivo / Productivo* (en respuesta a fallas).
* **Flujo de Estados:** Transición dinámicamente entre *En proceso*, *En diagnóstico* y *Finalizada*.

---

## 👥 Matriz de Roles y Permisos

| Rol | Alcance | Permisos y Operaciones |
| :--- | :--- | :--- |
| **Administrador** | Paz Constanza Morales Saavedra | Control total del sistema, parametrización, recepción de stock, aprobación de solicitudes, bajas y reportes. |
| **Alumno Líder (AL)** | Sub-rol Operativo | Gestión operativa en ventanilla: ejecuta préstamos, devoluciones y pedidos. Aprueba solicitudes presenciales. |
| **Usuario Global** | Estudiantes / Docentes (~300 personas) | Perfil de consulta. Sus solicitudes deben ser aprobadas **presencialmente** por un Administrador o Alumno Líder. |

---

## 🏗️ Arquitectura y Enfoque Técnico

* **Enfoque Multi-Tenancy / Parametrizable:** Arquitectura diseñada para ser adaptable y escalable a diferentes contextos (pañoles, instituciones educativas, bodegas).
* **Frontend:** Interfaces modernas desarrolladas en HTML5, CSS3 (Tailwind CSS) y JavaScript.
* **Backend y Base de Datos:** Arquitectura orientada a Servicios / APIs REST con conexión a base de datos relacional para garantizar la integridad de los datos.
* **Control de Versiones:** Git / GitHub con metodología de trabajo colaborativo.

---

## 👥 Perfil y Responsabilidades del Equipo

El desarrollo abarca todo el ciclo de vida del software:
* Levantamiento de requerimientos y lógica de negocio.
* Diseños UI/UX y maquetación de vistas flotantes e interactivas.
* Modelado y estructuración de base de datos relacional.
* Desarrollo Frontend, Backend e integración de APIs REST.
* Pruebas de integración, pruebas de usuario e implementación en producción.

---

## 📌 Representantes del Proyecto

* **Representante de la Contraparte / Cliente:**
  * Paz Constanza Morales Saavedra (`pc.morales@profesor.duoc.cl`)
* **Unidad Ejecutora:**
  * Arianette Pavez (Líder)
  * Tania Gaete
  * Jean García
