# HydroDrain – QGIS Plugin

HydroDrain es un complemento para QGIS que genera redes de drenaje hidrológicas a partir de un MDT y un umbral de acumulación. Utiliza algoritmos heredados de WhiteboxTools e integrados dentro del plugin para ejecutar una cadena de procesos hidrológicos de forma automatizada.

## Funcionalidades

- Selección de MDT desde capa o archivo.
- Definición de umbral de acumulación (*Channelization threshold*).
- Eliminación de depresiones (FillDepressions).
- Cálculo de direcciones de flujo (D8).
- Acumulación de flujo.
- Extracción de cauces.
- Vectorización de la red de drenaje.
- Botón de ayuda integrado con explicación del umbral.
- Carga automática de resultados en QGIS.

## Requisitos

- QGIS 3.44 LTR (o compatible).

## Instalación

1. Clona o descarga este repositorio.
2. Copia la carpeta `plugin` en:
   - Windows: `%APPDATA%/QGIS/QGIS3/profiles/default/python/plugins/HydroDrain`
3. Reinicia QGIS.
4. Activa HydroDrain desde el Administrador de complementos.

## Uso

1. Abre el panel HydroDrain.
2. Selecciona un MDT desde capa o archivo.
3. Define el umbral de acumulación. El umbral (*Channelization threshold*) es el número mínimo de celdas que deben drenar hacia un punto para que se forme un cauce; depende del tamaño de celda del MDT y controla la densidad de la red.
4. (Opcional) Elige rutas de salida para el raster D8 y la red vectorial.
5. Pulsa **Generar red**.
6. Los resultados se cargan automáticamente en el panel de capas.

## Licencia

GPL v2 o posterior.

## Autor

Roberto Zygmunt Saldaña (v0.1 2026)

## Créditos y Atribuciones

Este plugin integra componentes de terceros bajo licencias de código abierto y de libre uso con atribución:

### Algoritmos y Motor de Procesamiento (Backend)
* **WhiteboxTools:** El análisis hidrológico y la extracción de la red de drenaje se realizan utilizando el motor de alto rendimiento programado en Rust [WhiteboxTools](https://whiteboxgeo.com), desarrollado por el Dr. John Lindsay (*Geomorphometry and Hydrogeomatics Research Group* de la Universidad de Guelph). El plugin empaqueta su ejecutable y utiliza su API oficial de Python para ejecutar de forma autónoma los siguientes algoritmos:
  * `fill_depressions` (Corrección de depresiones en el MDT)
  * `d8_flow_accumulation` (Acumulación de flujo D8)
  * `d8_pointer` (Direcciones de flujo D8)
  * `extract_streams` (Definición de cauces por umbral)
  * `raster_streams_to_vector` (Vectorización de la red de drenaje)

### Recursos Gráficos
* **Icono de la Interfaz (Delta/Río):** Icono de [Delta](https://flaticon.es) creado por [Freepik](https://flaticon.es) disponible en [Flaticon](https://flaticon.es).

Agradecemos profundamente a los autores por desarrollar y compartir estas potentes herramientas con la comunidad SIG de código abierto.
