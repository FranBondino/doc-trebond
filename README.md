# 📘 Guía de Uso Oficial & Manual del Cliente — Trebond Inmobiliaria

**Plataforma Integral de Gestión Inmobiliaria**  
**Versión:** 1.0.0 (Producción) | **Fecha:** Julio 2026

---

## 📋 Contenido del Documento

1. [Enlaces de Acceso a Producción](#1-enlaces-de-acceso-a-producción)
2. [Cuentas de Prueba Precargadas](#2-cuentas-de-prueba-precargadas)
3. [Panel de Administración — Los 24 Módulos Operativos](#3-panel-de-administración--los-24-módulos-operativos)
4. [Guía de Uso: Portal del Inquilino y Postulantes](#4-guía-de-uso-portal-del-inquilino-y-postulantes)
5. [Guía de Uso: Portal del Propietario](#5-guía-de-uso-portal-del-propietario)
6. [Novedad: Mapa Interactivo & Integración GPS Google Maps](#6-novedad-mapa-interactivo--integración-gps-google-maps)
7. [Guía de Validación Rápida E2E (5 Minutos)](#7-guía-de-validación-rápida-e2e-5-minutos)

---

## 1. Enlaces de Acceso a Producción

| Servicio / Pantalla | URL Directa | Propósito |
|---|---|---|
| **Portal Web Público** | [https://trebond-frontend.vercel.app](https://trebond-frontend.vercel.app) | Catálogo de inmuebles, landing y accesos. |
| **Mapa Interactivo 全屏** | [https://trebond-frontend.vercel.app/mapa](https://trebond-frontend.vercel.app/mapa) | Mapa panorámico con todos los inmuebles y GPS. |
| **Inicio de Sesión** | [https://trebond-frontend.vercel.app/login](https://trebond-frontend.vercel.app/login) | Formulario de acceso para todos los roles. |
| **Registro de Cuentas** | [https://trebond-frontend.vercel.app/signup](https://trebond-frontend.vercel.app/signup) | Registro de nuevas cuentas. |
| **Servidor API Backend** | [https://trebond-app-production.up.railway.app](https://trebond-app-production.up.railway.app) | API REST en Railway. |

---

## 2. Cuentas de Prueba Precargadas

| Rol de Usuario | Email de Acceso | Contraseña | Alcance de Permisos |
|---|---|---|---|
| 🔴 **Administrador** | `admin@trebond.com` | `admin123` | Control total: configuración de comisiones, aprobación de postulaciones, creación de contratos, cobranzas, liquidaciones y AFIP. |
| 🟠 **Propietario** | `marcelo.rodriguez@owner.com` | `admin123` | Consulta de inmuebles propios, firma digital de alquileres con OTP y recibos de liquidación mensual. |
| 🟢 **Inquilino** | `carlos@tenant.com` | `admin123` | Firma digital de contrato, carga de transferencias de pago de alquiler/expensas y creación de tickets de mantenimiento. |

---

## 3. Panel de Administración (Los 24 Módulos Operativos)

Al iniciar sesión con `admin@trebond.com`, la barra lateral le otorga acceso a los 24 módulos operativos de la agencia:

### ⚙️ 1. Configuración de la Agencia (`/admin/config-agencia`)
Configuración central de la empresa: Nombre comercial, CUIT, dirección, teléfono y correo oficial. Permite definir:
- **Comisión cobrada al propietario** (ej. 5%).
- **Honorarios al inquilino** (ej. 4.5%).
- **Fee inicial de redacción de contrato** (ej. 2 meses o valor fijo).
- **Tasa de interés moratorio diario/mensual por pagos a destiempo** (ej. 2.5%).
- **Días de tolerancia de pago** (ej. del 1 al 10 de cada mes).

### 📊 2. Dashboard Principal & KPIs (`/admin/dashboard`)
Visión ejecutiva del negocio. Muestra tarjetas métricas de Propiedades Totales, Contratos Activos, Cobranza Acumulada del Mes y Porcentaje de Vacancia, acompañados de gráficos de tendencia de ingresos de los últimos 6 meses.

### 👥 3. Gestión de Usuarios & Asignación de Roles (`/admin/usuarios`)
Control de todos los usuarios registrados. Permite buscar por nombre o correo, cambiar el rol de cualquier usuario (convertir un `user` a `owner` o `tenant`), desactivar cuentas o **forzar el cierre de sesión remoto (Force Logout)**.

### 🏠 4. Catálogo de Propiedades (`/admin/propiedades`)
Alta, edición y eliminación de inmuebles. Permite cargar dirección, ciudad, precio, habitaciones, superficie, asignar el propietario del inmueble, cambiar su estado (`available`, `rented`, `maintenance`) y realizar la **carga masiva de fotografías de alta resolución**.

### ✅ 5. Aprobación de Inmuebles de Dueños (`/admin/property-approvals`)
Módulo de control de calidad. Revisa y aprueba las propiedades publicadas por propietarios o vendedores externos antes de hacerlas visibles en el catálogo público y en el mapa.

### 📝 6. Solicitudes de Alquiler & Conversión (`/admin/solicitudes`)
Evaluación de postulantes. Muestra las solicitudes enviadas por interesados con su documentación adjunta (DNI, 3 recibos de sueldo y garantía). Al presionar **"Aprobar y Convertir"**, el sistema transforma al usuario en Inquilino oficial y redacta el borrador del contrato.

### 📅 7. Gestión de Visitas & Agenda (`/admin/turnos`)
Calendario de turnos agendados por clientes interesados para conocer propiedades. Permite asignar el agente inmobiliario que acompañará la visita y confirmar o reprogramar la cita.

### ⏰ 8. Configuración de Horarios de Citas (`/admin/turnos/config`)
Definición de días hábiles de atención (Lunes a Sábados), franjas horarias (ej. 09:00 a 18:00 hs) y duración estimada por visita (30 o 45 min) para habilitar en el turnero automático.

### 🏷️ 9. Solicitudes de Tasación (`/admin/tasaciones`)
Módulo para atender pedidos de vendedores que desean cotizar su propiedad. Permite asignar un tasador oficial, registrar la visita técnica e ingresar la valuación final de mercado.

### 📜 10. Contratos Activos & Firma OTP (`/admin/contratos`)
Módulo central contractual. Redacción de contratos de alquiler especificando valor mensual, depósito en garantía, comisión de la agencia, fecha de inicio/vencimiento y seguimiento de las firmas digitales del Inquilino y Propietario.

### 📈 11. Indexación por Inflación (`/admin/indexacion`)
Reajuste periódico de alquileres. Permite aplicar los índices oficiales de actualización (ICL, IPC, IPIM), calcular automáticamente el nuevo canon locativo e informar por correo a las partes.

### 🔒 12. Depósitos en Garantía (`/admin/depositos`)
Control de los fondos de reserva en custodia. Administra la restitución del depósito al finalizar el contrato o la aplicación de deducciones por deudas o reparaciones.

### 💰 13. Cobranzas & Validación de Pagos (`/admin/pagos`)
Módulo de tesorería. Muestra los comprobantes de transferencia subidos por los inquilinos. Al hacer clic en **"Validar Pago"**, el sistema liquida la cuota, actualiza el estado de cuenta y emite el **Recibo Oficial en PDF**.

### 🏢 14. Control de Expensas (`/admin/expensas`)
Registro de liquidaciones de expensas enviadas por la administración del edificio, control de vencimientos y verificación de pago oportuno por parte del inquilino.

### 💡 15. Control de Servicios de Inquilinos (`/admin/servicios-inquilinos`)
Monitoreo de boletas de servicios públicos (Luz, Gas, Agua, Tasa Municipal) cargadas por el inquilino para garantizar el certificado de libre deuda continuo.

### 🎁 16. Bonificaciones & Descuentos (`/admin/bonificaciones`)
Gestión de créditos o quitas especiales sobre el valor del alquiler (por ejemplo, cuando el inquilino abona arreglos a su cargo o por promociones de la inmobiliaria).

### 💵 17. Liquidaciones a Propietarios (`/admin/liquidaciones`)
Cálculo de rendición mensual al dueña del inmueble. Descuenta la comisión de administración (5%) y retenciones por mantenimiento, emitiendo la orden de pago y comprobante de liquidación PDF.

### 📖 18. Cuenta Corriente (`/admin/cuenta-corriente`)
Libro mayor contable por cliente. Detalla el historial completo de débitos (alquileres, honorarios) y créditos (pagos, transferencias) por contrato.

### 🏦 19. Caja & Bancos (`/admin/caja`)
Flujo de fondos diario de la inmobiliaria. Registra ingresos en efectivo, cobranzas bancarias, pago a proveedores y retiros.

### 🧾 20. Facturación Electrónica AFIP (`/admin/facturacion`)
Integración directa con los servidores de la AFIP. Emisión de Facturas electrónicas A, B y C con código CAE oficial para el cobro de comisiones y servicios.

### 🛠️ 21. Reclamos & Tickets de Mantenimiento (`/admin/mantenimiento`)
Módulo de incidencias. Recibe las solicitudes de reparación enviadas por los inquilinos (ej. filtración, cortocircuito). Asigna el proveedor de la agencia, fija prioridad, sigue el arreglo y carga el gasto.

### 🔧 22. Gestión de Proveedores (`/admin/proveedores`)
Directorio de especialistas de confianza (plomeros, electricistas, gasistas, cerrajeros). Almacena contacto, rubro, historial de trabajos y datos de facturación.

### 📈 23. Reportes de Vacancia & Mercado (`/admin/reportes`)
Informes analíticos sobre tasa de vacancia, tiempo promedio de publicación antes de alquilar y rendimiento porcentual de alquiler por zona.

### 🔐 24. Auditoría & Logs de Seguridad (`/admin/seguridad`)
Registro inalterable de eventos: inicios de sesión, cambios de roles, modificaciones de valores locativos e intentos de ingreso fallidos.

---

## 4. Guía de Uso: Portal del Inquilino y Postulantes

1. **Búsqueda y Navegación:** Explore propiedades en `/propiedades` o en el mapa panorámico `/mapa`.
2. **Visor de Fotos y Ubicación GPS:** Abra fotos a pantalla completa y navegue con flechas. Presione `📍 Ver en Google Maps` para abrir las coordenadas GPS.
3. **Postulación y Carga de Documentación:** Desde el detalle del inmueble presione **"Postularse para Alquilar"** y adjunte su DNI, 3 recibos de sueldo y garantía.
4. **Firma Digital de Contrato:** Una vez aprobado, acceda a `/portal/contratos`, solicite el código OTP e ingréselo para firmar digitalmente.
5. **Carga de Pagos:** En `/portal/pagos` adjunte el comprobante de transferencia para que la administración emita el Recibo PDF.
6. **Tickets de Mantenimiento:** En `/portal/mantenimiento/nuevo` reporte filtraciones o averías indicando categoría (Plomería, Gas, Electricidad), urgencia y fotos del daño.
7. **Mi Perfil & Seguridad:** En `/portal/perfil` actualice sus datos personales o cambie su contraseña.

---

## 5. Guía de Uso: Portal del Propietario

1. **Estado de Inmuebles:** Visualice sus propiedades ocupadas o disponibles con su respectivo valor locativo.
2. **Firma Digital de Alquileres:** Al generarse un nuevo contrato, verifique las cláusulas e ingrese su clave OTP para validar la firma.
3. **Liquidaciones Mensuales:** Consulte la rendición de cobros: Alquiler bruto (-) comisión agencia (5%) (-) retenciones por arreglos = Neto transferido a su cuenta bancaria. Descargue el comprobante PDF.

---

## 6. Novedad: Mapa Interactivo & Integración GPS Google Maps

- **Vista Panorama `/mapa`:** Mapa geográfico interactivo de pantalla completa con todas las propiedades disponibles.
- **Sincronización Panel-Mapa:** Al seleccionar una tarjeta en la lista lateral, el mapa se desplaza suavemente hacia su posición exacta.
- **Botón GPS:** El botón `📍 Ver en Google Maps` en cada pin abre las coordenadas en Google Maps para navegación giro a giro o Street View.

---

## 7. Guía de Validación Rápida E2E (5 Minutos)

1. **Postulación:** Ingrese a [/propiedades](https://trebond-frontend.vercel.app/propiedades), elija un departamento y postúlese subiendo archivos.
2. **Aprobación Admin:** Inicie sesión como Admin (`admin@trebond.com` / `admin123`), vaya a `/admin/solicitudes` y apruebe la postulación.
3. **Firmas Digitales:** Inicie sesión como inquilino y luego como propietario para firmar el contrato usando el sistema OTP.
4. **Pago y Liquidación:** Suba un comprobante como inquilino, valídelo en `/admin/pagos`, descargue el Recibo PDF y emita la liquidación al dueño en `/admin/liquidaciones`.
