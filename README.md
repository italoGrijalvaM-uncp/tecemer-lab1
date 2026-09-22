Entornos de desarrollo, Github y buenas practicas de desarrollo

El proyecto consiste en un programa que imprime chistes de la base de datos https://official-joke-api.appspot.com/random-joke" abordado con las buenas prácticas de desarrollo en python

1.- clonar el repositorio tecemer_lab1 
2.- ingresar a traves de la terminal de powershell a el directorio tecemer-lab1 
3.- una vez dentro del directorio crear el entorno virtual con el comando "python -m venv .venv"
4.- activar el entorno mediante el comando ".venv\Scripts\activate"
5.- intalar el paquete en modo editable con el comando "pip install -e ."


EJEMPLO DE USO: 
(utiliza el comando dentro del directorio src) "python -m tecemer_lab1.app"

FORMATEO: 

Para formatear el codigo con Black
black --check src/ (verificar el formato sin modificar)
black src/ (formatear automaticamente)

EXTRACCIÓN y PROCESAMIENTO DE DATOS:

La extracción de los datos y específicamente los parámetros de temperatura mínima, temperatura máxima y precipitación, se realizó de la api "https://api.open-meteo.com/v1/forecast" en forma de archivo json.

Luego guardamos la información con el nombre de "pronostico_huancayo.json" para posteriormente trabajarlo y darle un formato de filas(tiempo,temperatura máxima, temperatura mínima y precipitación) y columnas(fechas) en un archivo csv denominado "pronostico_huancayo.csv" 

Además hacemos un pequeño análisis a el csv creado, primero transformando las fechas a formato datetime, luego agregamos columnas adicionales que agrega información como la amplitud térmica, asi como una clasificación simple sobre si fue un dia lluvioso según la precipitación de la fecha y si fue un dia cálido según la temperatura máxima

Por ultimo hacemos un pequeño resumen que contiene la cantidad de días en la base de datos, la temperatura máxima promedio y la precipitación total


ESTRUCTURA:

tecemer-lab1/
├── src/
│   └── tecemer_lab1/
│       ├── __init__.py
│       └── app.py
├── .gitignore
├── pyproject.toml
├── README.md
└── requirements.txt

## Cierre de la Unidad I — Semana 3 
 
Herramienta de automatización: organizador.py clasifica y mueve archivos 
de una carpeta en subcarpetas por tipo (Documentos, Imagenes, Videos, 
Comprimidos, Otros), con modo de simulacion (--dry-run) mediante argparse. 
 
Uso: 
``` 
python organizador.py <carpeta> [--dry-run] 
``` 
 
Pruebas: test_organizador.py cubre clasificacion, movimiento real y modo 
simulacion, usando la fixture tmp_path de pytest para no afectar el 
sistema de archivos real. Ejecutar con: pytest -v

Curso: Tecnologías Emergentes - ISO46B
Autor: Grijalva Martinez Italo Osmar 
Facultad: Facultad de Ingenieria de Sistemas 

