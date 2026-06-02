# HydroDrain
Complemento QGIS Análisis hidrológico

# HydroDrain – QGIS Plugin

HydroDrain es un complemento para QGIS que genera redes de drenaje hidrológicas a partir de un MDT y un umbral de acumulación. Utiliza WhiteboxTools para ejecutar una cadena de procesos hidrológicos de forma automatizada.

HydroDrain requiere que WhiteboxTools esté instalado y configurado en QGIS.
El usuario debe instalar WhiteboxTools y activar el provider “WhiteboxTools for QGIS” desde el Administrador de complementos. https://www.whiteboxgeo.com/

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
5. Instala la caja de herramientas WhiteboxTools.

## Uso

1. Abre el panel HydroDrain.
2. Selecciona un MDT desde capa o archivo.
3. Define el umbral de acumulación. El umbral (*Channelization threshold*) es el número mínimo de celdas que deben drenar hacia un punto para que se forme un cauce; depende del tamaño de celda del MDT y controla la densidad de la red.
4. (Opcional) Elige rutas de salida para el raster D8 y la red vectorial.
5. Pulsa **Generar red**.
6. Los resultados se cargan automáticamente en el panel de capas.

## Autor

Roberto Zygmunt Saldaña (v1.2026)
