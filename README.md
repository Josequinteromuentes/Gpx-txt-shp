# Gpx-txt-shp
Script de R para convertir archivos GPX a SHP
# Instalar los paquetes necesarios si no lo has hecho ya
install.packages("sf")
install.packages("rgdal")

# Cargar los paquetes
library(sf)
library(rgdal)

# Ruta al archivo GPX de entrada
input_gpx <- "ruta/al/archivo.gpx"

# Leer el archivo GPX
gpx_data <- st_read(input_gpx, layer = "tracks")

# Ruta para el archivo SHP de salida
output_shp <- "ruta/al/archivo_salida.shp"

# Exportar a formato SHP
st_write(gpx_data, output_shp)
