# RASTRO-CATASTRO

Herramienta web de consulta y organización de información catastral pública no protegida. RASTRO-CATASTRO permite buscar inmuebles a través de los servicios públicos de la Dirección General del Catastro (DGC) y consultar la ficha oficial correspondiente.

**Acceso a la herramienta:** [https://s3gad3.github.io/rastro-catastro/](https://s3gad3.github.io/rastro-catastro/)

RASTRO-CATASTRO es un proyecto independiente. No es un servicio oficial ni está afiliado, patrocinado o respaldado por la Dirección General del Catastro.

## Funciones

- Búsqueda por referencia catastral de 14, 18 o 20 caracteres.
- Búsqueda por dirección urbana, con sugerencias de provincia, municipio, vía y número procedentes del callejero catastral.
- Búsqueda por coordenadas geográficas WGS84 (EPSG:4326).
- Búsqueda de parcelas rústicas por referencia catastral o por provincia, municipio, polígono y parcela.
- Ficha organizada con la información no protegida que responda el servicio, por ejemplo localización, uso, superficies, antigüedad, unidades constructivas y subparcelas.
- Acceso a la ficha y cartografía oficiales, impresión o guardado en PDF, copia de resumen y exportación voluntaria a JSON.

La información disponible depende de la respuesta de los servicios de la DGC. La herramienta no obtiene datos protegidos de titulares ni valores catastrales individualizados.

## Uso

1. Abre la [herramienta web](https://s3gad3.github.io/rastro-catastro/) con conexión a Internet.
2. Selecciona el tipo de búsqueda: referencia, dirección, coordenadas o parcela rústica.
3. Para buscar por dirección, escribe el comienzo de la provincia y selecciona una sugerencia. Repite el proceso con el municipio y la vía; después introduce el número. Elegir las sugerencias permite enviar al servicio los nombres completos reconocidos por Catastro. Si no aparecen sugerencias, comprueba la conexión o prueba la opción de texto manual.
4. Pulsa el botón de consulta. Revisa los resultados y contrástalos en la ficha oficial enlazada.
5. Usa **Limpiar ficha** al terminar. La exportación JSON y la impresión se generan solo cuando el usuario las solicita.

Los nombres de las vías se presentan con el código oficial de tipo. Por ejemplo, **LG** corresponde a *Lugar*, **PL** a *Polígono* y **PZ** a *Plaza*.

## Publicación en GitHub Pages

Para publicar esta versión como página estática:

1. Crea un repositorio de GitHub llamado `rastro-catastro`.
2. Copia el HTML autónomo de la herramienta en la raíz del repositorio y llámalo `index.html`.
3. Añade este archivo como `README.md` y copia también el archivo `LICENSE` del proyecto.
4. En **Settings → Pages**, configura la publicación desde la rama `main` y la carpeta `/ (root)`.
5. Cuando GitHub Pages termine el despliegue, la página estará disponible en `https://s3gad3.github.io/rastro-catastro/`.

El HTML autónomo contiene los estilos, el código de la aplicación, el logotipo y el favicon. Para que las consultas funcionen, el navegador debe tener JavaScript habilitado y acceso a Internet. La disponibilidad también depende del servicio de Catastro, la red y las políticas de seguridad del navegador.

## Privacidad y flujo de datos

- La aplicación no tiene servidor propio, cuenta de usuario, analítica ni almacenamiento remoto de consultas.
- Las sugerencias se solicitan a la DGC mientras se escriben los campos de dirección. La búsqueda principal se envía cuando se pulsa el botón de consulta. La referencia, dirección, número o coordenadas introducidos se transmiten directamente desde el navegador a los servicios de Catastro; no pasan por un servidor de RASTRO.
- Los resultados permanecen en la memoria de la pestaña abierta y no se guardan automáticamente. Exportar, imprimir o copiar requiere pulsar la acción correspondiente.
- El botón opcional para contrastar una dirección en Google Maps envía esa dirección a Google únicamente cuando se pulsa.
- La web estática se distribuye a través de GitHub Pages, que puede procesar datos técnicos de acceso conforme a sus propias condiciones y políticas.
- Un JSON exportado puede contener referencias, direcciones y otros datos del inmueble. Guárdalo únicamente en sistemas autorizados y no lo subas al repositorio público.

## Fuentes catastrales y condiciones de uso

La licencia MIT de este repositorio cubre únicamente el software y los materiales originales de RASTRO incluidos en él. **No concede derechos sobre datos, cartografía, servicios, marcas ni contenidos de terceros**, y no sustituye las condiciones establecidas por sus titulares.

La DGC ofrece servicios web libres para consultar información no protegida. Sus condiciones y documentación delimitan el uso de esos servicios y de la información resultante; no deben emplearse para barrer sistemáticamente la base de datos. La publicación de esta interfaz no autoriza a republicar, redistribuir o explotar resultados catastrales. Antes de conservar, transformar, compartir o publicar datos, informes, JSON o capturas, revisa las condiciones oficiales vigentes y obtiene las autorizaciones que correspondan.

La herramienta realiza consultas puntuales, no incorpora una base de datos catastral y no está diseñada para búsquedas masivas. Este proyecto no afirma que la presentación o exportación de los resultados constituya por sí misma una transformación autorizada por la DGC.

## Límites

- Una respuesta vacía, un error o una dirección no encontrada no demuestra que el inmueble no exista.
- La información catastral no acredita por sí sola propiedad, ocupación, posesión, estado físico ni situación registral del inmueble.
- RASTRO-CATASTRO no emite certificaciones y no sustituye a la Sede Electrónica del Catastro, al Registro de la Propiedad ni a otras fuentes competentes.
- Los servicios estatales de la DGC no cubren Navarra ni los territorios forales del País Vasco.
- El usuario es responsable de contar con la finalidad, habilitación y base jurídica aplicables y de seguir los procedimientos de su organización.

## Fuentes oficiales

- [Servicios web libres de la Dirección General del Catastro](https://www.catastro.hacienda.gob.es/ws/Webservices_Libres.pdf)
- [Guía de servicios de la Sede Electrónica del Catastro](https://www.catastro.hacienda.gob.es/ayuda/Guia_de_servicios_SEC_ciudadanos.pdf)
- [Licencia de descarga de productos catastrales](https://www.catastro.hacienda.gob.es/pdf/ovc/licdescargaES.pdf)
- [Licencia INSPIRE de acceso y uso](https://www.catastro.hacienda.gob.es/webinspire/documentos/Licencia.pdf)
- [Acceso a la información catastral](https://www.catastro.hacienda.gob.es/es-ES/acceso_infocat.html)
- [Texto refundido de la Ley del Catastro Inmobiliario (BOE)](https://www.boe.es/buscar/act.php?id=BOE-A-2004-4163)

## Licencia

El software original de este proyecto se distribuye bajo la licencia MIT. Consulta [`LICENSE`](LICENSE) para conocer su alcance y las exclusiones relativas a información y servicios de terceros.

## Aviso

Este README y los avisos de la interfaz son informativos. No constituyen asesoramiento jurídico, autorización de la DGC ni garantía de que una modalidad concreta de uso o difusión esté permitida. Comprueba las condiciones oficiales antes de reutilizar información catastral.

**Creado por S3GAD3 · Kit RASTRO**
