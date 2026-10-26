# ERP MIPYME

Sistema de gestión integral (ERP) para micro, pequeñas y medianas empresas
cubanas. Diseñado para **trabajar sin conexión a internet** y sincronizar
automáticamente con el servidor central cuando la red vuelve.

## Descargas

| Plataforma | Archivo | Requisitos |
|------------|---------|------------|
| Android | `ErpMipyme-*.apk` | Android 8.0 (API 26) o superior |
| Windows | `ErpMipyme-*.msi` (instalador) / `*.zip` (portátil) | Windows 10/11 x64 |
| Web | Panel de administración en línea (PWA) | Navegador moderno |

Ir a la página de [Releases](https://github.com/ReidelAlcantara/erp-mipyme-releases/releases)
para descargar la última versión.

> Las funciones offline (POS, inventario, impresión de tickets) viven en las
> aplicaciones nativas de Android y Windows. El panel web es el centro de
> administración en línea; su URL se anuncia en cada Release.

## Características principales

- **POS offline**: venta rápida con lector de códigos, varias formas de pago y
  ticket ESC/POS; la cola persistente de ventas garantiza que nada se pierda
  si la red cae a mitad de la jornada.
- **Inventario**: doble depósito (venta / trastienda), kardex con costeo
  promedio ponderado, mínimos y alertas de reposición.
- **Contabilidad cubana**: plan de cuentas según la Resolución 494/2016,
  asientos automáticos por venta, diario, mayor, balance de comprobación y
  cierre de ejercicio.
- **Multi-moneda**: CUP, USD y MLC con tipo de cambio configurable; la
  contabilidad se lleva uniformemente en CUP.
- **RRHH**: empleados, asistencia y cálculo de pago.
- **Sincronización bidireccional** entre dispositivos y el servidor central
  (PostgreSQL en Neon) vía API propia.
- **Usuarios y roles**: cajero, dependiente, contador y administrador.
- **Tema neón oscuro** pensado para pantallas táctiles y uso prolongado.

## Instalación

### Android

1. Descargue el archivo `ErpMipyme-*.apk` del último Release.
2. Abra el archivo; si es la primera vez, permita *Instalar apps desconocidas*
   para su navegador o gestor de archivos.
3. Instale y abra la aplicación.

### Windows

1. Descargue `ErpMipyme-*.msi` (instalador) o `ErpMipyme-*.zip` (portátil).
2. MSI: doble clic y siga el asistente. Portátil: descomprima y ejecute
   `ErpMipyme.UI.exe`.

## Verificación de integridad

Cada Release incluye un archivo `SHA256SUMS.txt`. Verifique antes de instalar:

```bash
# Linux / macOS / Git Bash
sha256sum -c SHA256SUMS.txt
```

```powershell
# Windows (PowerShell)
Get-FileHash ErpMipyme-*.apk -Algorithm SHA256
```

## Primer acceso

Usuario: `admin` — PIN: `1234`. El sistema exige cambiar el PIN en el primer
inicio de sesión.

## Soporte

Abra un [issue](https://github.com/ReidelAlcantara/erp-mipyme-releases/issues) para
reportar errores o solicitar funcionalidades.

---

Publicado por [Reidel Alcantara Castellano](https://github.com/ReidelAlcantara).
