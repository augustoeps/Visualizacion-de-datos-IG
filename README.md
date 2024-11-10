# Visualización de Estaciones de Bicicleta y Rutas Activas

Este proyecto utiliza **Three.js** para crear una visualización 3D interactiva de estaciones de bicicleta, representadas como esferas, y sus rutas activas, mostradas con líneas que conectan las estaciones de inicio y fin de cada alquiler en curso.

## Funcionalidad

1. **Carga de Datos**: 
   - **Estaciones**: Se cargan los datos de geolocalización de cada estación de bicicleta a partir de un archivo CSV (`Geolocalización estaciones sitycleta.csv`). Las estaciones incluyen ID, nombre, calle, latitud y longitud.
   - **Alquileres**: Se carga un segundo archivo CSV (`SITYCLETA-2018.csv`) con información de alquileres, incluyendo fecha y hora de inicio, fecha y hora de fin, estación de partida y de retorno.

2. **Visualización de Estaciones**: 
   - Cada estación de bicicleta se representa como una esfera en el mapa 3D. Su posición se calcula mapeando las coordenadas geográficas a coordenadas del espacio 3D.

3. **Destacar Estaciones Activas**:
   - Cuando un alquiler está en curso, se cambia el color de la esfera de la estación:
     - **Verde**: estaciones de inicio.
     - **Amarillo**: estaciones de destino.
     - **Cian**: estaciones que son punto de inicio y de fin de rutas activas.

4. **Visualización de Rutas**:
   - Las rutas de cada bicicleta en alquiler activo se muestran como líneas que conectan la estación de partida con la estación de destino en tiempo real, simulando el tráfico de bicicletas entre estaciones.

5. **Simulación de Tiempo**:
   - Se avanza el tiempo en intervalos definidos para simular el paso de los minutos, lo que permite observar los cambios en las rutas activas y las estaciones en uso.

## Archivos Principales

- **Geolocalización estaciones sitycleta.csv**: Archivo con datos de estaciones de bicicleta (ID, nombre, coordenadas).
- **SITYCLETA-2018.csv**: Archivo con los datos de cada alquiler de bicicleta.
- **script.js**: Contiene la lógica de carga de datos, procesamiento, mapeo de coordenadas y funciones de visualización en Three.js.

