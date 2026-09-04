# 📘 Guía de Uso Oficial & Manual del Cliente — Trebond Inmobiliaria

**Plataforma Integral de Gestión Inmobiliaria**  
**Versión:** 2.0.0 (Producción Hardened) | **Fecha:** Septiembre 2026  
**Portal Web en Vivo:** [https://trebond-frontend.vercel.app](https://trebond-frontend.vercel.app)  
**Guía Renderizada (GitHub Pages):** [https://franbondino.github.io/doc-trebond/](https://franbondino.github.io/doc-trebond/)

---

## 📋 Contenido del Documento

1. [💡 Recomendaciones para Probar la Plataforma (Flujo Rápido de Negocio)](#-recomendaciones-para-probar-la-plataforma-flujo-rápido-de-negocio)
2. [Enlaces Oficiales de Acceso a Producción](#1-enlaces-oficiales-de-acceso-a-producción)
3. [Cuentas de Prueba Precargadas](#2-cuentas-de-prueba-precargadas)
4. [Módulos Estrella & Nuevas Capacidades](#3-módulos-estrella--nuevas-capacidades)
   - 🧾 [Facturación Electrónica AFIP Oficial (CAE & QR)](#-facturación-electrónica-afip-oficial-adminfacturacion)
   - 🏦 [Caja, Arqueo Diario y Tesorería](#-caja-arqueo-diario-y-tesorería-admincaja)
   - 📖 [Cuentas Corrientes y Cálculo de Mora](#-cuentas-corrientes-y-cálculo-de-mora-admincuenta-corriente)
   - 💵 [Liquidaciones a Propietarios](#-liquidaciones-a-propietarios-adminliquidaciones)
   - 📊 [CRM Comercial y Pipeline Kanban de 8 Etapas](#-crm-comercial-y-pipeline-kanban-de-8-etapas-admincrm)
   - 🌐 [Sindicación Multi-Portal (ZonaProp & ArgenProp)](#-sindicación-multi-portal-zonaprop--argenprop-adminpropiedades)
   - 🤳 [Firma de Contratos con Validación Biométrica Facial y OTP](#-firma-de-contratos-con-validación-biométrica-facial-y-otp-portalcontratos)
   - 📱 [Portales de Inquilino y Propietario Mobile-First](#-portales-de-inquilino-y-propietario-mobile-first)
5. [Panel de Administración (Los 27 Módulos Operativos)](#4-panel-de-administración-los-27-módulos-operativos)
6. [Guía de Uso: Portal del Inquilino y Postulantes](#5-guía-de-uso-portal-del-inquilino-y-postulantes)
7. [Guía de Uso: Portal del Propietario](#6-guía-de-uso-portal-del-propietario)
8. [Mapa Interactivo & Integración GPS Google Maps](#7-mapa-interactivo--integración-gps-google-maps)

---

## 💡 Recomendaciones para Probar la Plataforma (Flujo Rápido de Negocio)

Para validar la plataforma de punta a punta en aproximadamente 7 minutos, le sugerimos seguir este circuito guiado:

### 1️⃣ Paso 1: Explorar Propiedades y Postularse
- Ingrese a [https://trebond-frontend.vercel.app/propiedades](https://trebond-frontend.vercel.app/propiedades) o al mapa en `/mapa`.
- Seleccione un departamento y presione **"Postularse para Alquilar"**.
- Suba 3 documentos de prueba (DNI, recibo de sueldo y garantía) y envíe la postulación.

### 2️⃣ Paso 2: Aprobación y Conversión en Inquilino
- Inicie sesión como Administrador (`admin@trebond.com` / `admin123`).
- Ingrese a **Solicitudes (`/admin/solicitudes`)**, revise la postulación y presione **"Aprobar y Convertir en Inquilino"**.
- En `/admin/contratos`, genere el contrato de alquiler confirmando monto, plazos y comisiones.

### 3️⃣ Paso 3: Firma con Validación Biométrica Facial y Clave OTP
- Inicie sesión con el Inquilino recién creado: en `/portal/contratos` el sistema solicitará una captura selfie con detección de vida (anti-spoofing) cotejada al 90% contra el DNI.
- Solicite el código OTP de 6 dígitos e ingréselo para firmar digitalmente.
- Inicie sesión como el Propietario (`marcelo.rodriguez@owner.com` / `admin123`) y confirme la firma con su clave OTP. El contrato pasa a estado **Activo**.

### 4️⃣ Paso 4: Cobranza y Emisión de Factura AFIP con CAE
- Como Admin, ingrese a **Facturación AFIP (`/admin/facturacion`)**.
- Emita la Factura (A, B o C) correspondiente al alquiler o comisión: el sistema asigna el **CAE oficial (14 dígitos)**, genera el **Código QR RG 5003** y permite descargar el **PDF Oficial de AFIP**.

### 5️⃣ Paso 5: Asiento en Caja y Cuenta Corriente
- Verifique en **Caja (`/admin/caja`)** el ingreso asentado de fondos (Efectivo, Transferencia o Cheque).
- Compruebe en **Cuenta Corriente (`/admin/cuenta-corriente`)** el saldo del inquilino actualizado y el historial de débitos/créditos inmutable.

### 6️⃣ Paso 6: Liquidación Neta al Dueño
- Ingrese a **Liquidaciones (`/admin/liquidaciones`)** y emita la liquidación mensual.
- El sistema descuenta de forma automática el % de comisión de administración pactado y genera el comprobante de liquidación neta bancaria en PDF.

### 7️⃣ Paso 7: Verificación en CRM y Portales Móviles
- Ingrese a **CRM (`/admin/crm`)**: compruebe que el prospecto avanzó automáticamente en el Kanban hasta la columna **"Cerrado Ganado"**.
- Abra el portal desde su teléfono móvil para comprobar la experiencia táctil con Bottom Nav y tarjetas colapsables.

---

## 1. Enlaces Oficiales de Acceso a Producción

| Servicio / Pantalla | URL Directa | Propósito |
|---|---|---|
| **Portal Web Público** | [https://trebond-frontend.vercel.app](https://trebond-frontend.vercel.app) | Catálogo de inmuebles, landing y accesos. |
| **Mapa Interactivo Fullscreen** | [https://trebond-frontend.vercel.app/mapa](https://trebond-frontend.vercel.app/mapa) | Mapa panorámico con todos los inmuebles y GPS. |
| **Facturación AFIP** | [https://trebond-frontend.vercel.app/admin/facturacion](https://trebond-frontend.vercel.app/admin/facturacion) | Emisión de Facturas con CAE, QR y descarga PDF. |
| **Caja & Tesorería** | [https://trebond-frontend.vercel.app/admin/caja](https://trebond-frontend.vercel.app/admin/caja) | Libro de ingresos/egresos y arqueo diario. |
| **Cuentas Corrientes** | [https://trebond-frontend.vercel.app/admin/cuenta-corriente](https://trebond-frontend.vercel.app/admin/cuenta-corriente) | Balance por cliente, cobranzas y mora. |
| **Liquidaciones a Dueños** | [https://trebond-frontend.vercel.app/admin/liquidaciones](https://trebond-frontend.vercel.app/admin/liquidaciones) | Liquidación mensual neta con comisión descontada. |
| **CRM Comercial** | [https://trebond-frontend.vercel.app/admin/crm](https://trebond-frontend.vercel.app/admin/crm) | Pipeline Kanban de leads e interacciones. |
| **Portal Inquilino (Mobile)** | [https://trebond-frontend.vercel.app/portal/pagos](https://trebond-frontend.vercel.app/portal/pagos) | Pagos, recibos, facturas PDF y tickets de arreglos. |
| **Portal Propietario** | [https://trebond-frontend.vercel.app/dashboard/owner](https://trebond-frontend.vercel.app/dashboard/owner) | Inmuebles, contratos y liquidaciones netas. |
| **Inicio de Sesión** | [https://trebond-frontend.vercel.app/login](https://trebond-frontend.vercel.app/login) | Formulario de acceso universal. |
| **Registro de Cuentas** | [https://trebond-frontend.vercel.app/signup](https://trebond-frontend.vercel.app/signup) | Registro de nuevas cuentas. |

---

## 2. Cuentas de Prueba Precargadas

| Rol de Usuario | Email de Acceso | Contraseña | Alcance de Permisos |
|---|---|---|---|
| 🔴 **Administrador** | `admin@trebond.com` | `admin123` | Control global: Facturación AFIP, Caja, Liquidaciones, CRM, Sindicación, Contratos y Configuración. |
| 🟠 **Propietario** | `marcelo.rodriguez@owner.com` | `admin123` | Consulta de inmuebles propios, firma digital de alquileres con OTP y recibos de liquidación mensual. |
| 🟢 **Inquilino** | `carlos@tenant.com` | `admin123` | Firma digital de contrato, pago de cuotas, descarga de Facturas Oficiales con CAE y tickets de mantenimiento. |

---

## 3. Módulos Estrella & Nuevas Capacidades

### 🧾 Facturación Electrónica AFIP Oficial (`/admin/facturacion`)
- **Obtención Automática de CAE:** Código de Autorización Electrónico oficial de 14 dígitos con fecha de vencimiento y número correlativo de comprobante.
- **Código QR AFIP RG 5003:** Código QR con payload oficial verificado por la AFIP.
- **Comprobante PDF Oficial:** Factura en formato A4 con membrete inmobiliario, datos completos de emisor y receptor y desglose fiscal.
- **Modo Sandbox / Producción:** Permite probar emisiones sin generar pasivos impositivos mediante simulador de alta fidelidad, o conectar certificados reales (`.crt` y `.key`) desde el modal "Configuración AFIP".

### 🏦 Caja, Arqueo Diario y Tesorería (`/admin/caja`)
- **Multi-Moneda:** Movimientos en Pesos Argentinos (ARS) y Dólares Estadounidenses (USD).
- **Medios de Pago Diversificados:** Efectivo, transferencias bancarias y cheques diferidos.
- **Arqueo y Cierre Diario:** Conciliación del dinero físico en caja versus el saldo asentado en el sistema con reporte de cierre inmutable.
- **Transaccionalidad Atómica:** Todo cobro impacta simultáneamente en caja y en la cuenta corriente del cliente.

### 📖 Cuentas Corrientes y Cálculo de Mora (`/admin/cuenta-corriente`)
- **Libro Mayor por Cliente:** Trazabilidad completa de cuotas devengadas y pagos recibidos.
- **Punitorios Diarios por Mora:** Cálculo de intereses automáticos por mora tras superarse los días de gracia estipulados en el contrato.
- **Inmutabilidad Financiera:** Prohibición de borrado directo de asientos fiscales; se auditan mediante contra-asientos trazables.

### 💵 Liquidaciones a Propietarios (`/admin/liquidaciones`)
- **Rendición Mensual Automática:** Desglose claro de alquiler bruto (+) menos comisión Trebond (-) menos reparaciones y retenciones (-).
- **Neto Bancario:** Determinación del monto exacto a transferir a la cuenta bancaria del dueño con comprobante PDF adjunto.

### 📊 CRM Comercial y Pipeline Kanban de 8 Etapas (`/admin/crm`)
- **Pipeline Visual:** Tablero Kanban con etapas: *Nuevo Lead &rarr; Contactado &rarr; Visita Agendada &rarr; Visita Realizada &rarr; Oferta Hecha &rarr; En Negociación &rarr; Cerrado Ganado &rarr; Cerrado Perdido*.
- **Drag & Drop:** Desplazamiento fluido de tarjetas de prospectos entre etapas.
- **Captura Automática de Leads:** Se generan prospectos automáticamente a partir de solicitudes de alquiler o visitas agendadas desde la web.
- **Bitácora de Interacciones:** Registro cronológico de llamadas, mensajes de WhatsApp, correos y notas internas.

### 🌐 Sindicación Multi-Portal (ZonaProp & ArgenProp) (`/admin/propiedades`)
- **Publicación Simultánea:** Exportación y sincronización de inmuebles hacia ZonaProp y ArgenProp.
- **Toggles Granulares:** Posibilidad de activar o desactivar la sindicación por portal en cada ficha de propiedad.
- **Despublicación Automática:** Al cerrarse el alquiler o venta, el sistema despublica el inmueble en los portales externos automáticamente.

### 🤳 Firma de Contratos con Validación Biométrica Facial y OTP (`/portal/contratos`)
- **Reconocimiento Facial en Tiempo Real:** Captura de selfie frontal con cámara de celular o webcam.
- **Detección de Vida (Liveness):** Previene fraudes por suplantación con fotos impresas o videos en pantallas.
- **Cotejo Facial AWS Rekognition:** Validación biométrica contra el DNI frontal con un umbral mínimo de coincidencia del 90%.
- **Sellado con OTP:** Clave de 6 dígitos de un solo uso para ratificar la firma con constancia legal grabada en el contrato.

### 📱 Portales de Inquilino y Propietario Mobile-First
- **Navegación Táctil con Barra Inferior (Bottom Nav):** Accesos rápidos para el pulgar en celulares (*Inicio, Pagos, Contratos, Arreglos, Perfil*).
- **Cajón Deslizable (Drawer):** Menú lateral fluido para navegación completa en pantallas pequeñas.
- **Tarjetas Colapsables de Cuotas:** Visualización optimizada de vencimientos y estados de pago sin barras de desplazamiento horizontal.
- **Descarga Móvil de Facturas:** Descarga directa de comprobantes y facturas con CAE al celular en un toque.

---

## 4. Panel de Administración (Los 27 Módulos Operativos)

Al iniciar sesión con `admin@trebond.com`, la barra lateral le otorga acceso al panel integral:

1. **Dashboard & Métricas (`/admin/dashboard`):** KPIs ejecutivos, recaudación mensual y tendencias.
2. **Facturación Electrónica AFIP (`/admin/facturacion`):** Comprobantes fiscales con CAE, QR RG 5003 y PDF oficial.
3. **Caja & Tesorería (`/admin/caja`):** Libro de caja diario, efectivo, transferencias, cheques y arqueo de fin de jornada.
4. **Cuentas Corrientes (`/admin/cuenta-corriente`):** Balance por cliente con cálculo automático de mora.
5. **Liquidaciones a Propietarios (`/admin/liquidaciones`):** Rendición mensual con descuento de honorarios y gastos.
6. **CRM Inmobiliario (`/admin/crm`):** Pipeline Kanban de prospectos, historial de llamadas y analítica comercial.
7. **Catálogo de Propiedades & Sindicación (`/admin/propiedades`):** Gestión de inmuebles con publicación en ZonaProp y ArgenProp.
8. **Configuración de Agencia (`/admin/config-agencia`):** Comisiones, tasas de interés moratorio y datos de la empresa.
9. **Gestión de Usuarios (`/admin/usuarios`):** Asignación de roles, activación/desactivación y force logout remoto.
10. **Aprobación de Propiedades (`/admin/property-approvals`):** Moderación de publicaciones externas.
11. **Solicitudes de Alquiler (`/admin/solicitudes`):** Evaluación de documentación y conversión a Inquilino.
12. **Gestión de Visitas & Turnos (`/admin/turnos`):** Agenda de visitas guiadas a inmuebles.
13. **Horarios de Citas (`/admin/turnos/config`):** Días hábiles y franjas de turnos disponibles.
14. **Tasaciones (`/admin/tasaciones`):** Pedidos de cotización de inmuebles.
15. **Contratos Activos (`/admin/contratos`):** Redacción, firma biométrica y seguimiento de estados.
16. **Indexación por Inflación (`/admin/indexacion`):** Reajuste automático por ICL, IPC o IPIM.
17. **Depósitos en Garantía (`/admin/depositos`):** Custodia y restitución de depósitos.
18. **Cobranzas & Validación (`/admin/pagos`):** Aprobación de transferencias y emisión de recibos.
19. **Control de Expensas (`/admin/expensas`):** Liquidaciones de expensas de edificios.
20. **Control de Servicios (`/admin/servicios-inquilinos`):** Boletas de luz, gas y agua con libre deuda.
21. **Bonificaciones & Descuentos (`/admin/bonificaciones`):** Quitas o compensaciones especiales sobre alquileres.
22. **Tickets de Mantenimiento (`/admin/mantenimiento`):** Reclamos de desperfectos y asignación de técnicos.
23. **Gestión de Proveedores (`/admin/proveedores`):** Directorio de profesionales (plomería, electricidad, gas).
24. **Reportes de Vacancia (`/admin/reportes`):** Análisis de ocupación y rendimiento por zona.
25. **Auditoría & Seguridad (`/admin/seguridad`):** Registro inalterable de eventos y accesos.
26. **Centro de Notificaciones (`/admin/notificaciones`):** Avisos de vencimientos, firmas y pagos.
27. **Mensajería Interna (`/admin/mensajes`):** Comunicación directa con inquilinos y propietarios.

---

## 5. Guía de Uso: Portal del Inquilino y Postulantes

1. **Exploración:** Ingrese a `/propiedades` o al mapa panorámico `/mapa`.
2. **Visor de Fotos & GPS:** Galería HD a pantalla completa con navegación por teclado y botón `📍 Ver en Google Maps`.
3. **Postulación Digital:** Suba DNI frontal y dorso, últimos 3 recibos de sueldo y comprobante de garantía.
4. **Firma Biométrica del Contrato:** En `/portal/contratos` capture su selfie en vivo, apruebe el cotejo facial y confirme con su clave OTP.
5. **Pago de Alquiler:** En `/portal/pagos` reporte transferencias bancarias y descargue sus Facturas Oficiales con CAE.
6. **Tickets de Arreglos:** En `/portal/mantenimiento/nuevo` reporte averías con fotografías del daño para que la inmobiliaria envíe un técnico.
7. **Perfil:** Gestione sus datos personales y preferencias de notificación.

---

## 6. Guía de Uso: Portal del Propietario

1. **Mis Inmuebles:** Monitoree el estado de ocupación, inquilino actual y canon locativo de sus propiedades.
2. **Firma de Alquileres:** Valide los contratos de sus inmuebles mediante firma digital segura con OTP.
3. **Liquidaciones Mensuales:** Consulte la liquidación con el desglose del alquiler cobrado menos comisiones y descargue el recibo oficial PDF.
4. **Mantenimiento Aprobado:** Supervise las reparaciones efectuadas sobre su inmueble y las facturas de proveedores deducidas.

---

## 7. Mapa Interactivo & Integración GPS Google Maps

- **Vista Panorama `/mapa`:** Mapa interactivo de pantalla completa con todas las propiedades de la inmobiliaria.
- **Sincronización Panel-Mapa:** Al tocar cualquier propiedad en el listado, el mapa centra de inmediato las coordenadas GPS.
- **Botón `📍 Ver en Google Maps`:** En cada pin de propiedad, abre la ubicación exacta en la aplicación móvil de Google Maps para navegación giro a giro o visualización en Street View.
