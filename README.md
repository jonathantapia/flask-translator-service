# Servicio de Traducción con Flask y Transformers

Este repositorio contiene un servicio web de traducción de texto utilizando Flask y el modelo de Hugging Face `Helsinki-NLP/opus-mt-en-es`.

## Requisitos

Antes de ejecutar el proyecto, asegúrate de tener instaladas las siguientes dependencias:

```bash
pip install transformers torch flask flask-cors sentencepiece
```

## Ejecución Local

Para ejecutar el servicio en tu máquina local, sigue estos pasos:

1. Clona el repositorio o copia los archivos en tu entorno de trabajo.
2. Instala las dependencias mencionadas anteriormente.
3. Ejecuta el siguiente comando en la terminal:

```bash
python app.py
```

El servidor se iniciará en `http://127.0.0.1:5555/`, donde puedes acceder a la interfaz web o consumir la API.

## Uso del Servicio

### Interfaz Web

Abre tu navegador y accede a `http://127.0.0.1:5555/`. Allí podrás ingresar un texto en inglés y obtener su traducción al español.

### Uso con cURL

También puedes probar el servicio enviando una solicitud `POST` desde la terminal:

```bash
curl -X POST "http://127.0.0.1:5555/translate" -H "Content-Type: application/json" -d '{"text": "Hello, how are you?"}'
```

La respuesta esperada será un JSON con la traducción:

```json
{"translation": "Hola, ¿cómo estás?"}
```

## Estructura del Proyecto

```
/
│── app.py  # Código principal del servicio Flask
│── templates/
│   ├── index.html  # Interfaz web
│── README.md  # Este archivo
```

![Captura de pantalla 2025-03-09 a la(s) 02 49 52](https://github.com/user-attachments/assets/f8fc0296-1294-4b2e-8996-39e2ffed9c86)

