# Cartography

Cartografía libre hecha en [Espacio Vectorial](https://espaciovectorial.tech) (El Bolsón, Patagonia Argentina): mapas y planificadores para moverse por lugares donde "no hay nada" — hasta que sabés dónde buscar.

**Índice:** https://espaciovectorial.tech/cartography/

## Mapas

| Herramienta | Qué hace | URL |
|---|---|---|
| [Patagonia · Planificador de Ruta](patagonia/) | Mapa de dispersión poblacional de la Patagonia (AR + CL) con armado de recorridos, optimización por vecino más cercano y export a Google Maps. | [`/cartography/patagonia/`](https://espaciovectorial.tech/cartography/patagonia/) |

## Arquitectura

Cada mapa es **un solo archivo HTML autocontenido** en su propia carpeta: estilos, datos y lógica embebidos, sin backend ni build. Las únicas dependencias externas se cargan desde CDN (por ejemplo, Leaflet en el planificador patagónico).

Eso significa que cualquier herramienta se puede correr abriendo su `index.html` en el navegador, y el repo entero se publica tal cual en cualquier hosting estático (GitHub Pages incluido).

```
cartography/
├── index.html        ← índice de mapas
├── patagonia/
│   └── index.html    ← planificador de ruta patagónico
├── LICENSE
└── README.md
```

### Datos del planificador patagónico

Argentina: censo 2022 (INDEC), gobiernos locales jul-2024; localidades menores imputadas desde censo 2010 con factor provincial. Chile: censo 2017 y estimaciones a nivel localidad. Los datos viven embebidos en el HTML como array `D = [nombre, país, región, lat, lon, población]`. El mapa base (costa, frontera, lagos) es GeoJSON vectorial embebido — no usa servidor de tiles.

## Contribuir

Correcciones de datos, altas de localidades e ideas de nuevos mapas: bienvenidos los issues y PRs.

## Licencia

MIT — ver [LICENSE](LICENSE).
