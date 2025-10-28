# Taller de Inteligencia Artificial con OpenAI y Jupyter

Este proyecto es un taller práctico para aprender a integrar modelos de lenguaje de OpenAI (GPT) en entornos de desarrollo con Python, utilizando Jupyter Notebooks en Visual Studio Code. El taller cubre desde la configuración inicial hasta la creación de consultas estructuradas y el manejo de parámetros como temperatura y tokens.

## Descripción del Proyecto

El taller proporciona una serie de guías interactivas en formato Jupyter Notebook que enseñan cómo:
- Configurar el entorno de desarrollo para trabajar con la API de OpenAI
- Realizar consultas básicas y avanzadas a modelos GPT
- Estructurar respuestas en formato JSON para automatización
- Experimentar con parámetros como temperatura y max_tokens
- Crear funciones reutilizables para interactuar con modelos de IA

## Comenzando

Estas instrucciones te permitirán obtener una copia del proyecto en funcionamiento en tu máquina local para propósitos de desarrollo y aprendizaje.

### Prerrequisitos

Necesitarás tener instalado lo siguiente:

**1. Python 3.8 o superior**
```bash
python --version
```

**2. Visual Studio Code**
- Descarga desde: https://code.visualstudio.com/

**3. Extensiones de VS Code recomendadas:**
- Python (Microsoft)
- Jupyter (Microsoft)

**4. Una cuenta de OpenAI con acceso a la API**
- Regístrate en: https://platform.openai.com/
- Genera una API key desde tu panel de control

**5. Dependencias de Python:**
```bash
pip install openai python-dotenv
```

### Instalación

Sigue estos pasos para configurar el entorno de desarrollo:

**Paso 1:** Clona este repositorio

```bash
git clone https://github.com/AngieRamosCortes/JupyterGuides.git
cd JupyterGuides
```

**Paso 2:** Crea un entorno virtual (recomendado)

```bash
# En Windows
python -m venv venv
venv\Scripts\activate

# En macOS/Linux
python3 -m venv venv
source venv/bin/activate
```

**Paso 3:** Instala las dependencias

```bash
pip install openai python-dotenv jupyter
```

**Paso 4:** Configura tu API key de OpenAI

Crea un archivo `.env` en la raíz del proyecto:

```bash
echo OPENAI_API_KEY=tu-api-key-aqui > .env
```

O manualmente, crea el archivo `.env` con el siguiente contenido:
```
OPENAI_API_KEY=sk-tu-clave-api-aqui
```

⚠️ **IMPORTANTE:** Nunca compartas tu API key públicamente ni la subas a repositorios.

**Paso 5:** Abre el proyecto en VS Code

```bash
code .
```

**Paso 6:** Abre cualquier notebook y ejecuta las celdas

Comienza con `Guia3.ipynb` para familiarizarte con los conceptos básicos.

## Ejecutando las Guías

### Guía 1

### Guía 2

### Guía 3: Fundamentos de OpenAI API

Esta guía cubre los conceptos básicos:

1. **Instalar dependencias** (primera celda)
2. **Configurar el cliente de OpenAI** (segunda celda)
3. **Hacer tu primera consulta** (tercera celda)
4. **Trabajar con respuestas estructuradas en JSON**
5. **Crear funciones reutilizables**


### Ejercicios Propuestos

El taller incluye ejercicios para experimentar con:

**1. Parámetro de Temperatura:**
```python
for temp in [0.1, 0.5, 0.9]:
    respuesta = ask_model(
        "Describe el impacto de la IA en el arte digital.",
        temperature=temp
    )
    print(f"Temperature = {temp}\n{respuesta}")
```

**2. Respuestas Estructuradas:**
```python
system_rule = "Responde en JSON con las claves 'tema' y 'descripcion'."
respuesta = ask_model(
    "Explica qué es la ciberseguridad en educación.",
    system=system_rule,
    temperature=0.3
)
```

**3. Control de Longitud con max_tokens:**
```python
respuesta = ask_model(
    "Redacta una historia sobre un robot pintor.",
    temperature=0.7,
    max_tokens=30
)
```

### Guía 4

## Estructura del Proyecto

```
hello_ai/
├── .env                      # Configuración de API keys (no incluido en el repo)
├── .gitignore               # Archivos ignorados por Git
├── Guia3.ipynb              # Notebook principal: Fundamentos de OpenAI API
├── Guia4.ipynb              # Notebook avanzado (si aplica)
├── Guia4p.ipynb             # Notebook práctico adicional
├── hello_ai.ipynb           # Notebook inicial
├── hello_ai.py              # Script Python equivalente
├── setup_hello_ai.ipynb     # Configuración inicial del proyecto
├── hello_ai_vscode/         # Recursos adicionales
├── venv/                    # Entorno virtual (no incluido en el repo)
└── README.md                # Este archivo
```

## Construido Con

* [OpenAI API](https://platform.openai.com/docs) - API de modelos de lenguaje GPT-4, GPT-3.5
* [Python 3.x](https://www.python.org/) - Lenguaje de programación
* [Jupyter Notebooks](https://jupyter.org/) - Entorno interactivo de desarrollo
* [Visual Studio Code](https://code.visualstudio.com/) - Editor de código
* [python-dotenv](https://pypi.org/project/python-dotenv/) - Gestión de variables de entorno

## Parámetros Clave de la API

### Temperature (0.0 - 2.0)
- **0.0 - 0.3**: Respuestas más deterministas y consistentes
- **0.4 - 0.7**: Balance entre creatividad y coherencia
- **0.8 - 2.0**: Respuestas más creativas y variadas

### max_tokens
- Controla la longitud máxima de la respuesta
- 1 token ≈ 4 caracteres en inglés, ≈ 2-3 en español

### system messages
- Definen el comportamiento y formato de respuesta del modelo
- Útiles para estructurar salidas en JSON

## Versionado

Este proyecto utiliza [Git](https://git-scm.com/) para el control de versiones. Para ver las versiones disponibles, consulta las [etiquetas en este repositorio](https://github.com/AngieRamosCortes/JupyterGuides/tags).

## Autores

* **Angie Ramos Cortes** - *Trabajo inicial* - [AngieRamosCortes](https://github.com/AngieRamosCortes)

## Licencia

Este proyecto está bajo la Licencia MIT - ver el archivo [LICENSE.md](LICENSE.md) para más detalles.

## Agradecimientos

* Inspirado en la documentación oficial de OpenAI
* Basado en las mejores prácticas de desarrollo con Python y Jupyter
* Recursos educativos sobre IA y aprendizaje automático
* Comunidad de desarrolladores de IA y educadores
