# RASTRO-CATASTRO v0.2.1

Herramienta local para consultar y organizar datos catastrales **no protegidos** de un inmueble mediante los servicios públicos de la Dirección General del Catastro (DGC). RASTRO es un cliente independiente: no es un servicio oficial ni está afiliado, patrocinado o respaldado por la DGC.

## Qué incluye

- Búsqueda por referencia catastral (14, 18 o 20 caracteres).
- Búsqueda por dirección urbana, con sugerencias oficiales de provincias, municipios, vías y números.
- Consulta por coordenadas geográficas WGS84 / EPSG:4326.
- Búsqueda de parcela rústica por referencia o por provincia, municipio, polígono y parcela.
- Ficha estructurada con los campos no protegidos que devuelva el servicio, como localización, uso, superficies, antigüedad, unidades constructivas y subparcelas.
- Enlaces directos a la ficha y cartografía de la Sede Electrónica del Catastro.
- Copia de resumen, impresión/guardar PDF y exportación voluntaria de un JSON local con fecha, consulta y atribución de la fuente.

Las sugerencias se solicitan después de que el usuario escriba en los campos de dirección. Para una consulta completa, el investigador debe pulsar el botón de búsqueda.

## Instalación en Chrome o Edge

1. Descarga y descomprime el paquete de esta versión.
2. Abre `chrome://extensions` en Chrome o `edge://extensions` en Edge.
3. Activa **Modo de desarrollador**.
4. Pulsa **Cargar descomprimida** y selecciona la carpeta `RASTRO-CATASTRO-v0.2.1` (la que contiene `manifest.json`).
5. Abre RASTRO-CATASTRO desde el icono de la extensión.

No abras `index.html` con doble clic: la consulta requiere el contexto de la extensión. El permiso de red está limitado al dominio del servicio público de Catastro indicado en `manifest.json`.

## Privacidad y flujo de datos

- La extensión no tiene servidor propio, cuenta, telemetría, analítica ni almacenamiento remoto.
- Las consultas y sugerencias se envían directamente desde el navegador a los servicios de la DGC. El texto de provincia, municipio, vía, número, referencia o coordenadas que se use en la consulta se transmite a ese servicio.
- Los resultados permanecen en memoria en la pestaña abierta. No se guardan automáticamente. Imprimir, copiar o exportar crea una salida local solo si el usuario pulsa la acción correspondiente. El enlace opcional «Contrastar en mapa» envía la dirección a Google Maps únicamente cuando se pulsa.
- El JSON exportado puede incluir referencias, direcciones y otros datos del inmueble. Guárdalo en el expediente y sistema autorizados; no lo subas al repositorio público.
- La extensión no solicita ni obtiene nombres de titulares, NIF, domicilio de titulares ni valores catastrales individualizados.

## Condiciones de uso de la información catastral

La licencia MIT de este repositorio cubre exclusivamente el software y los recursos originales de RASTRO identificados en este proyecto. **No concede derechos sobre datos, cartografía, servicios, marcas o contenidos de terceros**, ni sustituye las condiciones publicadas por la DGC.

La DGC ofrece servicios web de consulta de datos no protegidos para automatizar consultas, pero indica que no están destinados al barrido sistemático de la base de datos. La licencia oficial de acceso/descarga establece condiciones para el uso y la difusión: entre ellas, restringe publicar en Internet información catastral original sin transformar, exige atribuir la fuente y la fecha en productos transformados, y contempla la difusión mediante interoperabilidad enlazando a la Sede. La herramienta no incluye una base de datos, no ejecuta búsquedas masivas y enlaza a la ficha oficial; aun así, **este proyecto no declara que el formato de su ficha o de sus exportaciones constituya por sí mismo una transformación autorizada**.

Por ello, esta versión se distribuye como código/extensión para uso local y no se publica como aplicación alojada que redistribuya resultados. No publiques datos consultados, informes o capturas con datos catastrales sin revisar las condiciones vigentes de la DGC y, cuando proceda, obtener la autorización necesaria. Las condiciones pueden cambiar: consulta siempre las fuentes oficiales enlazadas abajo.

## Límites y advertencias

- La herramienta está limitada a datos catastrales no protegidos. El acceso a datos protegidos está sujeto a los supuestos y requisitos legales correspondientes.
- La información catastral no acredita por sí sola propiedad, ocupación, posesión, estado físico ni situación registral del inmueble.
- RASTRO-CATASTRO no expide certificaciones ni sustituye la Sede Electrónica, al Registro de la Propiedad ni a una comprobación oficial.
- Un error, una respuesta vacía o una dirección no encontrada no demuestra que el inmueble no exista. Contrasta el resultado con la ficha oficial.
- Los servicios estatales del Catastro no cubren Navarra ni los territorios forales del País Vasco.
- Para usos profesionales o de investigación, el usuario debe contar con habilitación, finalidad y base jurídica aplicables, respetar necesidad y proporcionalidad, y seguir los procedimientos de su organización.

## Fuentes oficiales

- [Servicios web libres de la Dirección General del Catastro](https://www.catastro.hacienda.gob.es/ws/Webservices_Libres.pdf)
- [Guía de servicios de la Sede Electrónica del Catastro](https://www.catastro.hacienda.gob.es/ayuda/Guia_de_servicios_SEC_ciudadanos.pdf)
- [Licencia de descarga de productos catastrales](https://www.catastro.hacienda.gob.es/pdf/ovc/licdescargaES.pdf)
- [Licencia INSPIRE de acceso y uso](https://www.catastro.hacienda.gob.es/webinspire/documentos/Licencia.pdf)
- [Acceso a la información catastral](https://www.catastro.hacienda.gob.es/es-ES/acceso_infocat.html)
- [Texto refundido de la Ley del Catastro Inmobiliario (BOE)](https://www.boe.es/buscar/act.php?id=BOE-A-2004-4163)

En pantalla e informes se atribuye la fuente como **Dirección General del Catastro**, con la fecha de consulta cuando está disponible.

## Licencia

El software original de este repositorio se ofrece bajo MIT. Consulta `LICENSE` para el alcance de la concesión y las exclusiones relativas a datos/servicios externos.

## Aviso

Este README y la interfaz son avisos informativos, no una autorización de la DGC ni asesoramiento jurídico. La inclusión de un disclaimer no subsana un uso que infrinja la normativa o licencia aplicable. Verifica las condiciones oficiales antes de publicar o redistribuir cualquier resultado.

**Creado por S3GAD3 · Kit RASTRO**

### Versión 0.2.1

El autocompletado de provincia, municipio y calle usa ahora menús de sugerencias visibles conectados al callejero oficial. Selecciona la sugerencia para que la siguiente consulta utilice el nombre completo reconocido por Catastro. Se amplió el catálogo de tipos de vía, incluidos LG (Lugar), PL (Polígono) y PZ (Plaza).
