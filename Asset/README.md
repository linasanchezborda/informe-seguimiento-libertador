# Asset — Plantilla de Reporte VP Sponsor El Libertador

Esta carpeta contiene la plantilla base para generar reportes semanales de seguimiento ejecutivo.

## Estructura del repo

```
/
├── index.html                    ← Reporte actual (siempre el mas reciente)
├── Asset/
│   ├── template-reporte.html     ← Plantilla con placeholders
│   └── README.md                 ← Este archivo
├── versiones/
│   ├── reporte-2026-05-08.html   ← Historial de versiones
│   ├── reporte-2026-05-15.html
│   └── ...
├── logo-libertador-white.svg     ← Logo blanco para header
└── logo-libertador.svg           ← Logo rojo para otros usos
```

## Como generar un nuevo reporte

1. Entregar al agente los datos actualizados (Excel o texto) con la fecha de corte
2. El agente genera el HTML usando la plantilla
3. Se publica como `index.html` (reporte actual)
4. La version anterior se mueve a `versiones/reporte-YYYY-MM-DD.html`

## Placeholders en la plantilla

| Placeholder | Descripcion |
|-------------|-------------|
| `{{FECHA_CORTE}}` | Fecha de corte del reporte (ej: 8 de Mayo 2026) |
| `{{CARRILES_ACTIVOS}}` | Numero de carriles |
| `{{EQUIPO_TOTAL}}` | Total de devs unicos |
| `{{ALERTAS_ACTIVAS}}` | Numero de alertas |
| `{{CARRIL_N_*}}` | Datos por carril (KPIs, estado, backlog, capacidades) |

## Semaforos

| Clase CSS | Significado |
|-----------|-------------|
| `semaforo verde` | Cumplimiento >= 90% |
| `semaforo amarillo` | Cumplimiento 70-89% |
| `semaforo rojo` | Cumplimiento < 70% |
| `semaforo gris` | Sin dato / Pendiente |

## Badges de estado

| Clase CSS | Significado |
|-----------|-------------|
| `badge-prod` | En produccion |
| `badge-pruebas` | En pruebas |
| `badge-dev` | En desarrollo |
| `badge-estab` | En estabilizacion |
