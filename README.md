# ESCALERA 1.5x - 30 DÍAS

Simulador y seguimiento de cinco caminos (R$1,00, cuota 1.50, reinversión del 100 % durante 30 días). PWA sin dependencias externas: funciona sin internet tras la primera carga.

> Las cifras son proyecciones matemáticas, no ganancias aseguradas. Una cuota de 1.50 no garantiza que una apuesta sea ganadora; una pérdida detiene el camino.

## Ejecutar
1. Descomprime la carpeta.
2. Sirve la carpeta en `localhost` (la instalación y el Service Worker requieren HTTPS o localhost):
   - `python3 -m http.server 8080` y abre `http://localhost:8080`
3. Abre la app una vez con conexión. Después funciona offline.
4. Instalar: en Chrome/Android, menú ⋮ → "Instalar aplicación" o "Añadir a pantalla de inicio". Para usarla desde el teléfono, publícala en un hosting HTTPS (GitHub Pages, Netlify, etc.).
También puedes abrir `index.html` directamente: funcionan los cálculos y el guardado local, pero no la instalación ni el Service Worker.

## Uso
- **Hoy**: elige el día (1–30) con las flechas, el número o el deslizador.
- **Caminos**: marca Ganada / Perdida / Pendiente el día seleccionado, con la fecha indicada. Ganada multiplica el capital real por la cuota. Perdida pone el capital real en 0 y detiene el camino hasta reiniciarlo con un capital nuevo.
- **Tabla**: toca una fila para seleccionar el día; usa ✓ ✗ … para registrar o corregir. Corregir un día borra los resultados posteriores de ese camino.
- **Datos**: cambia capital, cuota y duración; exporta CSV; descarga o restaura una copia JSON.

## Archivos
`index.html`, `style.css`, `app.js`, `manifest.webmanifest`, `service-worker.js`, `icon-192.png`, `icon-512.png`, `icon-maskable-512.png`.
Si cambias archivos, sube la constante `V` de `service-worker.js` para refrescar la caché.
