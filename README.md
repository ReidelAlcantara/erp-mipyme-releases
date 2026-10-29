# ERP MIPYME — Descargas

Sistema de gestión integral (ERP) para micro, pequeñas y medianas empresas
cubanas: **mayorista + minorista**, con POS que funciona **sin conexión a
internet** y sincronización automática bidireccional (PowerSync + Neon
PostgreSQL) cuando la red vuelve.

## Descargas

| Plataforma | Archivo del Release | Requisitos |
|------------|--------------------|------------|
| Android | `ERP-MIPYME-v*.*.*.apk` (firmado) | Android 8.0 (API 26)+, permisos de impresora Bluetooth/USB |
| Windows | `ERP-MIPYME_*.msi` / `*.exe` (NSIS, WebView2 embebido) | Windows 10/11 x64 |
| Web/PWA | Enlace en cada Release (Vercel) | Navegador moderno (Chrome/Edge) |

Ir a la página de [**Releases**](https://github.com/ReidelAlcantara/erp-mipyme-releases/releases)
y descargar el archivo de tu plataforma desde el último release publicado.

> La versión **Web/PWA** se instala desde el propio navegador: abre el enlace,
> menú de Chrome → «Instalar aplicación». Funciona offline tras la primera
> carga (los datos viven en SQLite local dentro del navegador/dispositivo).

## Características

- 🔐 **Roles**: Administrador, Dependiente (POS), Económico (contabilidad),
  Almacenero (inventario) — inicio de sesión con usuario + PIN.
- 🧾 **POS offline**: ventas a mayor y menor con impresión de tickets
  térmicos ESC/POS (USB/TCP en Windows, Bluetooth/USB en Android).
- 📊 **Contabilidad cubana** según Resolución 494/2016: nomenclador de
  cuentas, libro diario, asientos con partida doble y cierre de ejercicio.
- 📦 **Inventario multi-almacén** con mínimos, trazabilidad de movimientos
  y ajustes.
- 👥 **RRHH**: ficha de empleados y control de asistencia.
- 🏷️ **Branding configurable**: nombre y logo del negocio en la app y en
  todos los tickets impresos.
- 🔄 **Sincronización offline-first**: todos los dispositivos del negocio
  comparten los mismos datos vía PowerSync; las ventas hechas sin internet
  se encolan y suben automáticamente al reconectar.

## Instalación

**Android**: descarga el `.apk` y ábrelo (permite «Instalar apps desconocidas»
si el sistema lo pide). Conecta la impresora térmica por Bluetooth o USB OTG.

**Windows**: ejecuta el `.msi` (o el `.exe` del instalador NSIS) y sigue el
asistente. Las impresoras USB/TCP se detectan desde la propia aplicación.

**Soporte**: el código fuente y la documentación técnica viven en el
repositorio privado del proyecto.
