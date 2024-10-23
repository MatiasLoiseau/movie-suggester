# Movie Suggester

Este proyecto es un sistema de recomendación de películas. Utiliza datos almacenados en cinco DataFrames que contienen información de personas, usuarios, trabajadores, películas y puntuaciones.

## Instalación

Para instalar el entorno y todas las dependencias necesarias, asegúrate de tener **Conda** instalado en tu sistema. Luego, ejecuta los siguientes comandos:

1. Clona el repositorio:

   ```bash
   git clone https://github.com/MatiasLoiseau/movie-suggester.git
   cd movie-suggester
   ```

2. Instalar MLFlow

    ```bash
    conda install -c conda-forge mlflow
    ```

3. Instalar y ejecutar el entorno:

   ```bash
   mlflow run . --experiment-name EDA
   ```

## Estructura de los Datos

Los datos serán almacenados en memoria en cinco DataFrames distintos, cada uno representando una parte clave del sistema de recomendación:

1. **Personas**: Información de las personas, incluyendo:
    - Id
    - Fecha de Nacimiento
    - Género
    - Código Postal

2. **Usuarios (Personas)**: Información sobre los usuarios que son personas:
    - Id (relación con Personas)
    - Ocupación
    - Fecha de Alta

3. **Trabajadores (Personas)**: Información de los trabajadores (que también son personas):
    - Id (relación con Personas)
    - Fecha de Alta
    - Puesto
    - Categoría
    - Horario de Trabajo

4. **Películas**: Información de las películas:
    - Nombre
    - Año
    - Género(s)
    - Id

5. **Scores**: Puntuaciones dadas por los usuarios a las películas:
    - Usuario (Id)
    - Película (Id)
    - Puntuación
    - Timestamp

## Archivos CSV

El repositorio contiene cinco archivos CSV en la carpeta `data/` que se utilizan para inicializar los DataFrames mencionados anteriormente:

1. `personas_o.csv`
2. `usuarios_o.csv`
3. `trabajadores_o.csv`
4. `peliculas_o.csv`
5. `scores_o.csv`
