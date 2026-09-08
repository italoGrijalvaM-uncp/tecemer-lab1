Entornos de desarrollo, Github y buenas practicas de desarrollo

El proyecto consiste en un programa que imprime chistes de la base de datos https://official-joke-api.appspot.com/random-joke" abordado con las buenas prácticas de desarrollo en python

1.- clonar el repositorio tecemer_lab1 
2.- ingresar a traves de la terminal de powershell a el directorio tecemer-lab1 
3.- una vez dentro del directorio crear el entorno virtual con el comando "python -m venv .venv"
4.- activar el entorno mediante el comando ".venv\Scripts\activate"
5.- intalar el paquete en modo editable con el comando "pip install -e ."


Ejemplo de uso:
(utiliza el comando dentro del directorio src) "python -m tecemer_lab1.app"


Para formatear el codigo con Black
black --check src/ (verificar el formato sin modificar)
black src/ (formatear automaticamente)

Estructura:

tecemer-lab1/
├── src/
│   └── tecemer_lab1/
│       ├── __init__.py
│       └── app.py
├── .gitignore
├── pyproject.toml
├── README.md
└── requirements.txt

Curso: Tecnologías Emergentes - ISO46B
Autor: Grijalva Martinez Italo Osmar 
Facultad: Facultad de Ingenieria de Sistemas 
