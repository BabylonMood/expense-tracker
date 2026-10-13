# Expense Tracker

Tracker de gastos en un solo archivo (`index.html`), pensado para un viaje:
cargás los gastos a mano o los importás desde una captura de pantalla (OCR),
y ves totales, ranking de categorías y estadísticas por tracker.

Corre 100% en el navegador y guarda todo en `localStorage` (con sincronización
en la nube **opcional** vía JSONBin).

## Funcionalidades

- **Multi-tracker**: varios trackers en paralelo (un viaje, una etapa, etc.),
  con uno activo a la vez.
- **Multi-moneda**: BRL / ARS / USD, con cotizaciones configurables
  (`1 R$ = ? ARS`, `1 USD = ? R$`) y una moneda principal para el hero.
- **OCR**: subís una captura o foto de tus movimientos (extractos de ARQ,
  bancos, tarjetas) y [Tesseract.js](https://tesseract.io/) detecta los
  renglones. Después los revisás en un modal (importe, categoría, lugar,
  nota, split) y elegís cuáles importar.
- **Hero y ranking**: total en la moneda principal, desglose por otras
  monedas, cantidad de movimientos y ranking de categorías.
- **Nube opcional**: sincronización con JSONBin (Bin ID + API key propias).
  Si no configurás nada, queda solo local.
- **Respaldo**: export/import de todos los trackers en un archivo JSON.

## Cómo usarlo

Abrí `index.html` con doble clic o servilo local:

```bash
python3 -m http.server
# http://localhost:8000
```

1. Creá un tracker y elegí su moneda principal.
2. Cargá gastos a mano o subí una captura para el OCR.
3. Revisá el ranking y los totales; ajustá cotizaciones en Ajustes.
4. (Opcional) Configurá JSONBin para sincronizar; o descargá el respaldo JSON.

> El OCR carga Tesseract.js desde CDN con los idiomas español y portugués, así
> que la primera vez necesita conexión a internet.

## Archivos

| Archivo | Qué hace |
|---|---|
| `index.html` | Toda la app: estructura, estilos y lógica |
