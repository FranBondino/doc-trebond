# 📘 Guía de Uso Oficial — Plataforma Trebond Inmobiliaria

**Documento de Capacitación y Prueba para Usuario Final y Cliente**  
**Versión:** 1.0.0 (Producción) | **Fecha:** Julio 2026

---

## 📋 Contenido del Documento

1. [Bienvenida e Introducción](#1-bienvenida-e-introducción)
2. [Enlaces de Acceso a la Plataforma](#2-enlaces-de-acceso-a-la-plataforma)
3. [Credenciales de Prueba y Cuentas Precargadas](#3-credenciales-de-prueba-y-cuentas-precargadas)
4. [Guía de Uso: Postulantes e Inquilinos](#4-guía-de-uso-postulantes-e-inquilinos)
5. [Guía de Uso: Propietarios](#5-guía-de-uso-propietarios)
6. [Guía de Uso: Panel de Administración Inmobiliaria](#6-guía-de-uso-panel-de-administración-inmobiliaria)
7. [Novedad: Mapa Interactivo de Propiedades y GPS](#7-novedad-mapa-interactivo-de-propiedades-y-gps)
8. [Paso a Paso: Guía de Prueba E2E Recomendada](#8-paso-a-paso-guía-de-prueba-e2e-recomendada)
9. [Preguntas Frecuentes y Soporte](#9-preguntas-frecuentes-y-soporte)

---

## 1. Bienvenida e Introducción

Bienvenido a la **Plataforma Trebond Inmobiliaria**. Esta herramienta integral ha sido diseñada para digitalizar y automatizar por completo la gestión inmobiliaria:

- **Para Inquilinos y Buscadores:** Búsqueda geográfica en mapa, agendamiento de visitas, postulación con carga de documentación, firma digital de contratos y gestión de pagos/mantenimiento online.
- **Para Propietarios:** Consulta del estado de sus inmuebles, firma digital de contratos y recepción de liquidaciones mensuales.
- **Para la Inmobiliaria (Administrador):** Control centralizado de propiedades, aprobación de solicitudes, gestión de contratos, cobranzas, liquidaciones, facturación AFIP y control de mantenimiento.

---

## 2. Enlaces de Acceso a la Plataforma

Para probar la plataforma en producción desde cualquier navegador (computadora, tablet o celular), utilice los siguientes enlaces:

| Servicio | URL de Acceso | Descripción |
|---|---|---|
| 🏠 **Portal Web Principal** | [https://trebond-frontend.vercel.app](https://trebond-frontend.vercel.app) | Plataforma de acceso para todos los usuarios. |
| 🗺️ **Mapa Interactivo de Propiedades** | [https://trebond-frontend.vercel.app/mapa](https://trebond-frontend.vercel.app/mapa) | Exploración geográfica en pantalla completa de todos los inmuebles disponibles. |
| 🔑 **Iniciar Sesión** | [https://trebond-frontend.vercel.app/login](https://trebond-frontend.vercel.app/login) | Formulario de acceso por email y contraseña. |
| 📝 **Registro de Usuarios** | [https://trebond-frontend.vercel.app/signup](https://trebond-frontend.vercel.app/signup) | Registro de nuevas cuentas. |

---

## 3. Credenciales de Prueba y Cuentas Precargadas

> [!IMPORTANT]
> Se han habilitado las siguientes cuentas de prueba precargadas en el servidor de producción. Puede utilizarlas inmediatamente para ingresar con distintos roles sin necesidad de configurar nada previamente:

| Rol | Correo Electrónico | Contraseña | Permisos y Vistas |
|---|---|---|---|
| 🔴 **Administrador** | `admin@trebond.com` | `admin123` | Control total del sistema: aprobación de postulantes, creación de contratos, cobranzas, liquidaciones y balances. |
| 🟠 **Propietario** | `marcelo.rodriguez@owner.com` | `admin123` | Acceso a sus propiedades, firma digital de alquileres y liquidaciones recibidas. |
| 🟢 **Inquilino** | `carlos@tenant.com` | `admin123` | Acceso a su contrato activo, carga de comprobantes de pago de alquiler/expensas y solicitudes de mantenimiento. |

---

## 4. Guía de Uso: Postulantes e Inquilinos

### 4.1 Búsqueda y Selección de Propiedades
1. Ingrese a la plataforma y diríjase al catálogo en `/propiedades` o a la vista panorámica en `/mapa`.
2. Utilice los filtros superiores para acotar la búsqueda por ciudad, tipo de inmueble (*Departamento, Casa, PH, Oficina*), tipo de operación (*Alquiler o Venta*) y rango de precio.
3. Haga clic sobre la tarjeta o sobre el pin del mapa para acceder al **Detalle de la Propiedad**.

### 4.2 Galería de Fotos y Mapa GPS
- **Visor a Pantalla Completa:** Al hacer clic sobre cualquier foto principal o miniatura, se desplegará el visor modal oscuro sin distracciones. Puede pasar de foto con las flechas en pantalla o con las teclas `←` y `→` de su teclado.
- **Navegación GPS:** En la sección de ubicación del detalle o en los pins del mapa, haga clic en el botón **`📍 Ver en Google Maps`** para abrir la ubicación exacta en Google Maps.

### 4.3 Postulación para Alquilar
1. En el detalle del departamento que le interese, presione el botón **"Postularse para Alquilar"**.
2. **Carga de Documentación:** Suba sus archivos requeridos (DNI frontal/dorso, últimos 3 recibos de sueldo y comprobante de garantía).
3. Presione **"Enviar Postulación"**. Recibirá un mensaje de confirmación y el equipo de la inmobiliaria evaluará sus antecedentes.

### 4.4 Firma Digital de Contrato
1. Una vez que la administración apruebe su solicitud, ingrese al portal en `/portal/contratos`.
2. Verifique las condiciones del contrato de alquiler generado.
3. Presione **"Solicitar Código de Firma OTP"** (recibirá el código seguro en pantalla/email).
4. Ingrese los dígitos del código y presione **"Confirmar y Firmar Contrato"**.

### 4.5 Pago de Alquiler y Expensas
1. Desde `/portal/pagos`, consulte el monto a abonar del mes en curso.
2. Realice la transferencia bancaria y presione **"Cargar Comprobante de Pago"**.
3. Adjunte la foto o PDF de su transferencia. Una vez validada por la inmobiliaria, podrá descargar su **Recibo Oficial en PDF**.

---

## 5. Guía de Uso: Propietarios

### 5.1 Gestión de Mis Propiedades
- Ingrese con su cuenta de Propietario (`marcelo.rodriguez@owner.com`).
- En el panel principal visualizará la lista de sus inmuebles, estado de ocupación (*Alquilado / Disponible*) y valor locativo.

### 5.2 Firma Digital de Alquileres
- Cuando un inquilino es aprobado y firma el contrato, recibirá una notificación.
- Diríjase a su sección de Contratos, revise las cláusulas del alquiler, solicite su código OTP de seguridad e ingréselo para dejar el contrato **completamente vigente y firmado por ambas partes**.

### 5.3 Liquidaciones Mensuales
- Desde la sección de Liquidaciones podrá consultar los pagos recibidos por la inmobiliaria.
- Verá el desglose detallado: Alquiler bruto cobrado, deducción de comisión de administración, retenciones por arreglos y el **monto neto transferido a su cuenta bancaria**.

---

## 6. Guía de Uso: Panel de Administración Inmobiliaria

> [!NOTE]
> Para ingresar al panel administrativo, inicie sesión con `admin@trebond.com` / `admin123` y acceda a `/admin/dashboard`.

### 6.1 Control General (Dashboard)
Visualice los indicadores de rendimiento de la oficina en tiempo real:
- **KPIs:** Total de propiedades, Contratos activos, Cobranza acumulada del mes y Porcentaje de vacancia.
- **Gráficos:** Evolución de ingresos y distribución de estados de pago.

### 6.2 Gestión de Solicitudes de Alquiler y Conversión
1. Diríjase a **Solicitudes de Alquiler** (`/admin/solicitudes`).
2. Haga clic en una solicitud pendiente para evaluar la documentación adjuntada por el postulante (DNI, recibos, garantía).
3. Presione **"Aprobar y Convertir en Inquilino"**.
4. El sistema convertirá automáticamente al usuario al rol de Inquilino y abrirá el formulario para confeccionar el nuevo contrato.

### 6.3 Administración de Contratos e Indexación
- **Creación:** Defina el monto inicial de alquiler, porcentaje de comisión de la agencia, fecha de inicio/fin y frecuencia de ajuste.
- **Ajuste por Inflación (Indexación):** Al cumplirse el período de actualización, presione **"Indexar Contrato"**, ingrese el índice (ICL/IPC/IPIM) y el sistema recalculará los nuevos valores locativos notificando a las partes.

### 6.4 Validaciones de Cobro y Facturación
- En **Gestión de Pagos** (`/admin/pagos`), revise los comprobantes subidos por los inquilinos.
- Al hacer clic en **"Validar Pago"**, el sistema emite automáticamente el recibo de cobro y actualiza la cuenta corriente.

---

## 7. Novedad: Mapa Interactivo de Propiedades y GPS

Se ha incorporado una nueva vista geográfica avanzada accesible desde el menú principal haciendo clic en **"Mapa"**:

- **Página `/mapa`:** Visualice en pantalla completa la ubicación de todas las propiedades disponibles en la ciudad.
- **Selección Dinámica:** Al hacer clic en cualquier tarjeta del listado lateral, el mapa se desplazará automáticamente hacia la ubicación del departamento.
- **Filtros Geográficos:** Filtre instantáneamente por zona, tipo de propiedad o rango de precio.
- **Acceso GPS Directo:** En la ventana emergente de cada pin, el botón **`📍 Ver en Google Maps`** permite abrir la posición exacta en la aplicación de Google Maps de su teléfono o navegador para iniciar la navegación guiada por GPS.

---

## 8. Paso a Paso: Guía de Prueba E2E Recomendada

Para validar todo el flujo del sistema en 5 minutos de principio a fin:

1. **Paso 1 (Postulación):** Ingrese a [https://trebond-frontend.vercel.app/propiedades](https://trebond-frontend.vercel.app/propiedades), elija un departamento y postúlese adjuntando archivos de prueba.
2. **Paso 2 (Aprobación Admin):** Inicie sesión como Admin (`admin@trebond.com` / `admin123`), vaya a `/admin/solicitudes`, revise la postulación y presione **Aprobar**.
3. **Paso 3 (Firma Inquilino):** Inicie sesión con la cuenta postulante, vaya a `/portal/contratos`, solicite el código OTP y confirme la firma digital.
4. **Paso 4 (Firma Propietario):** Inicie sesión como Propietario (`marcelo.rodriguez@owner.com` / `admin123`), vaya a su panel de contratos y confirme la firma con su OTP.
5. **Paso 5 (Pago y Recibo):** Desde el portal de inquilino suba un comprobante de pago de prueba, luego como Admin en `/admin/pagos` presione **Validar** y descargue el **Recibo PDF**.

---

## 9. Preguntas Frecuentes y Soporte

- **¿Cómo registro un usuario nuevo con un rol específico?**  
  Cree la cuenta normalmente desde `/signup`. Luego inicie sesión como Admin, vaya a `/admin/usuarios` y cambie el rol de la cuenta registrada a `owner`, `tenant`, etc.
- **¿Qué sucede si un usuario olvida su contraseña?**  
  Puede utilizar la opción "Recuperar Contraseña" en la pantalla de ingreso o el administrador puede forzar el reinicio desde `/admin/usuarios`.
- **Soporte Técnico:** Para consultas o solicitudes adicionales sobre la plataforma, contactar al equipo de desarrollo de Trebond.
