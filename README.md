# Cartografía

Mapas libres hechos en [Espacio Vectorial](https://espaciovectorial.tech) (El Bolsón, Patagonia Argentina). Herramientas autocontenidas — un solo archivo HTML, sin backend — para entender y recorrer el territorio.

## Proyectos

**[Dispersión Poblacional Patagónica](https://espaciovectorial.tech/patagonia_dispersion.html)** — primer proyecto del repo. Mapa interactivo de la Patagonia argentina y chilena donde cada localidad aparece con radio proporcional a √población. Incluye buscador, filtros por país y población mínima, y permite armar un recorrido tocando localidades y abrirlo en Google Maps.

Población: Argentina, censos INDEC 2022 y 2010 (parajes y comunas rurales); Chile, censo 2017 INE a nivel entidad (servicios cartográficos oficiales del INE); Islas Malvinas, censo 2021 realizado por la administración de las islas. Coordenadas: georef/BAHRA (Argentina), INE (Chile) y [GeoNames](https://www.geonames.org/). El dataset cubre ~380 localidades, de ciudades a parajes de decenas de habitantes; el filtro de población mínima arranca en cero.

Mapa base (costa, límites, lagos): [Natural Earth](https://www.naturalearthdata.com/) (dominio público), vectorizado y embebido en el HTML. Renderizado con [Leaflet](https://leafletjs.com/) (BSD-2), única dependencia externa, cargada desde CDN.

## Participar

Correcciones de datos, altas de localidades, ideas y nuevos mapas son bienvenidos — abrí un issue o mandá un PR.
