[English](README.md) | [Español](README.es.md)

# LocalSheet Lite (MIT) — Inspector CSV 100% Offline

**LocalSheet Lite** es una utilidad en un único archivo HTML, 100% offline, para detectar codificaciones en archivos CSV/TSV, inferir delimitadores y encontrar filas duplicadas exactas directamente en tu navegador (`file://`), con **cero subidas, cero instalaciones, cero peticiones de red y CSP estricto (`default-src 'none'` + `script-src 'sha256-...'` sin `'unsafe-inline'`)**.

> ¿Buscas **Lector nativo `.xlsx` multi-hoja**, **Clasificación automática de columnas (`>=70%`)**, **Auditoría de correlatividad multi-serie (`Agrupar serie por`)**, **Presets para Excel (`="00412"`)**, **Guardián pre-exportación**, **Desglose explícito de fechas/montos ambiguos y precisión**, **Totales de control**, **Registro de excepciones CSV** y **Perfiles JSON v2**?
> Esas funciones forman parte de **LocalSheet Auditor (Versión Completa)** *(herramienta técnica de apoyo local en memoria; no reemplaza una auditoría contable o tributaria oficial)*.

---

## Inicio rápido
1. Descarga `localsheet-lite.html` (o clona este repositorio).
2. Haz doble clic en `localsheet-lite.html` para abrirlo en Chrome, Edge, Firefox o Brave (`file://`).
3. Arrastra cualquier archivo `.csv`, `.tsv` o `.txt` (o prueba con `samples/03_inventario_duplicados_latin1.csv`).

## ¿Por qué un único HTML offline?
- **Privacidad verificable:** Tus CSV financieros, contables o de clientes permanecen en la memoria del navegador (`0` peticiones de red, CSP estricto `default-src 'none'` con hashes en `script-src`).
- **Sin instaladores:** Funciona directo en Windows, macOS y Linux sin ejecutables `.exe` ni permisos de administrador.
- **Alcance transparente:** Diseñado para archivos `.csv`, `.tsv` y `.txt`. Los archivos binarios `.xlsx`/`.xls` se rechazan de forma segura con un aviso claro. Motor probado en pruebas automatizadas de Node/Chrome con más de 10,000 filas (sin pruebas de usabilidad humana).

## Qué incluye Lite (MIT)
- Detección automática de codificación (`UTF-8`, `UTF-8 BOM`, `UTF-16LE/BE`, `Windows-1252 / Latin-1`)
- Detección estadística de delimitadores (`,`, `;`, `\t`, `|`) + soporte de directiva `sep=` al importar
- Parser estricto RFC-4180 y neutralización de fórmulas CSV (`=`, `+`, `@`, `-`)
- Detección rápida de duplicados exactos y exportación CSV `UTF-8 BOM` (sin emitir `sep=;`)

## Comparativa: Lite (MIT) vs. Versión Completa

| Capacidad | Lite (MIT) | Versión Completa |
|---|---|---|
| HTML único offline (`file://`, cero red, CSP con hashes) | Sí | Sí |
| Detección de codificación (`UTF-8`, `UTF-8 BOM`, `UTF-16`, `Win-1252`) y bloqueo binario | Sí | Sí |
| Autodetección de delimitadores + `sep=` al importar | Sí | Sí |
| Duplicados exactos y exportación CSV `UTF-8 BOM` | Sí | Sí |
| Neutralización de fórmulas CSV (`=`, `+`, `@`, `-`) | Sí | Sí |
| Lector nativo `.xlsx` (multi-hoja, fechas 1900/1904, celdas combinadas) | — | **Sí** |
| Pegado directo desde Excel (`Ctrl+C` → `Ctrl+V`) y saltar filas superiores | — | **Sí** |
| Clasificación automática de columnas (`>=70%`, resguardo texto/teléfonos, overrides) | — | **Sí** |
| Duplicados por clave compuesta + comparativa lado a lado | — | **Sí** |
| Correlatividad multi-serie + `Agrupar serie por` (`Año de fecha` / `Otra columna`) | — | **Sí** |
| Desglose explícito (`N` fechas ambiguas, `M` montos ambiguos, `K` precisión) + Totales de control | — | **Sí** |
| Presets de Excel (`Excel Inglés`, `Excel Español / LatAm`, `Genérico`) + Guardián pre-exportación | — | **Sí** |
| Grilla virtualizada, panel por fila, deshacer 60s, `.tsv`, `.xls` (tabla HTML), Excepciones CSV, PDF y JSON v2 | — | **Sí** |

## Verificación SHA-256
- `localsheet-lite.html`: `c3e3dcd51f283fcaf62223e197d0683b03fac590b677196fd29c8c7c1df84de`

## Licencia
Licencia MIT — ver [LICENSE](LICENSE).
