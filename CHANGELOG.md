# Cambios

## 0.2.1 — 26-09-2026

- Sustituido el autocompletado nativo por sugerencias visibles del callejero oficial, con selección del nombre canónico completo para provincia, municipio, calle y número.
- Los campos de dirección se habilitan en secuencia para evitar consultas con nombres parciales.
- Añadido el código de vía LG (Lugar), ampliado el catálogo de tipos y corregida la distinción entre PL (Polígono) y PZ (Plaza).
- Las sugerencias ofrecen una alternativa manual y muestran el error de conexión cuando el servicio no responde.


## 0.2.0 — 26-09-2026

- Añadidas sugerencias de provincia, municipio, vía y números próximos a partir de los servicios de callejero de la DGC.
- Corregido el uso de métodos REST actuales para el callejero (`ObtenerProvincias`, `ObtenerMunicipios`, `ObtenerCallejero`, `ObtenerNumerero`).
- Añadida atribución visible de fuente y fecha de consulta en la ficha, resumen y exportación JSON.
- Añadidos avisos sobre privacidad, alcance de MIT, límites de reutilización de datos y enlaces a condiciones oficiales.
- README y LICENSE precisan que MIT cubre el software propio, no respuestas, datos, cartografía ni servicios de Catastro.
- Paquete orientado a carga local como extensión; no incluye base de datos catastral ni propone publicar los resultados en GitHub Pages.
