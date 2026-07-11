# Control de Depósito

App de un solo sitio (PWA) para llevar stock, ventas propias y tercerizadas,
finanzas y horas trabajadas. Funciona sin instalar nada, guarda los datos en
el navegador, y se puede instalar como app en el celular.

## Archivos

- `index.html` — la aplicación completa (HTML + CSS + JS).
- `manifest.json` — metadatos para que se pueda instalar como app.
- `sw.js` — service worker, permite que abra aunque no haya internet.
- `icon-192.png`, `icon-512.png`, `icon-512-maskable.png`, `apple-touch-icon.png` — íconos de la app.

## Publicar en GitHub Pages

1. Creá un repositorio en GitHub (puede ser privado) y subí estos archivos
   a la raíz (no dentro de una subcarpeta).
2. Andá a **Settings → Pages**.
3. En "Source" elegí la rama `main` (o `master`) y la carpeta `/ (root)`.
4. Guardá. En un par de minutos vas a tener una URL del tipo:
   `https://tu-usuario.github.io/tu-repo/`
5. Abrí esa URL desde el celular. El navegador va a ofrecer "Agregar a
   pantalla de inicio" / "Instalar app", o podés usar el botón
   **Instalar app** que aparece en la barra lateral de la propia app.

## Sincronizar entre varios dispositivos (opcional)

Por defecto todo se guarda solo en el navegador donde la uses. Si querés
ver los mismos datos desde el celular y la computadora, configurá la
sincronización con Supabase desde la pestaña **Ajustes** dentro de la app
(ahí están las instrucciones y el SQL necesario).

## Actualizar la app ya instalada

Cuando subas cambios nuevos al repo, los dispositivos que ya la tengan
instalada los van a descargar solos la próxima vez que abran la app con
internet (el service worker se actualiza automáticamente en segundo plano).
