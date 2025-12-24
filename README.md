# 🎙️ Urano - Asistente Virtual con Python

**Urano** es un asistente virtual de escritorio desarrollado en Python que utiliza reconocimiento de voz y síntesis de voz (TTS) para automatizar tareas diarias. El proyecto integra diversas librerías para permitir la navegación web, reproducción multimedia y consultas de información en tiempo real mediante comandos verbales.

## 📋 Características Principales

El asistente escucha a través del micrófono, procesa el lenguaje natural y ejecuta las siguientes acciones:

* **Navegación Web Automatizada:**
    * Abre y busca videos en **YouTube** (`pywhatkit`).
    * Realiza búsquedas en **Google** y abre el navegador automáticamente.
* **Consultas de Información:**
    * Busca definiciones y resúmenes en **Wikipedia** y los lee en voz alta.
    * Informa la **fecha y hora** actual con precisión.
* **Entretenimiento:**
    * Cuenta chistes aleatorios en español utilizando `pyjokes`.
* **Interacción Natural:**
    * Saludo inteligente basado en la hora del día (Buenos días/tardes/noches).
    * Confirmación auditiva de las acciones realizadas.

## 🛠️ Tecnologías Utilizadas

Este proyecto fue construido utilizando las siguientes bibliotecas de Python:

* **`speech_recognition`**: Para la captura de audio y conversión de voz a texto (utilizando la API de Google).
* **`pyttsx3`**: Motor de síntesis de texto a voz (Text-to-Speech) que funciona offline.
* **`pywhatkit`**: Para la automatización de envío de mensajes y reproducción en YouTube.
* **`wikipedia`**: Para la extracción de resúmenes de artículos de Wikipedia.
* **`pyjokes`**: Para la generación de chistes.
* **`yfinance`**: Importado para futuras funcionalidades de consultas bursátiles y financieras.
* **`webbrowser`** y **`datetime`**: Librerías estándar para control del navegador y gestión del tiempo.

## ⚙️ Instalación y Requisitos

Para ejecutar este proyecto en tu máquina local, sigue estos pasos:

1.  **Clonar el repositorio:**
    ```bash
    git clone [https://github.com/tu-usuario/urano-asistente.git](https://github.com/tu-usuario/urano-asistente.git)
    cd urano-asistente
    ```

2.  **Instalar las dependencias:**
    Ejecuta el siguiente comando para instalar todas las librerías necesarias:
    ```bash
    pip install pyttsx3 speechrecognition pywhatkit yfinance pyjokes wikipedia
    ```

    > **Nota sobre PyAudio:** `speech_recognition` depende de PyAudio.
    > * **Windows:** Si tienes problemas instalándolo directamente, usa `pipwin`:
    >     `pip install pipwin` -> `pipwin install pyaudio`
    > * **Linux:** `sudo apt-get install python3-pyaudio`

## ⚠️ Configuración de Voces

El código utiliza IDs de voz específicos del registro de Windows (Microsoft Speech Voices).

En el archivo `main.py`, encontrarás variables como:
```python
id1 = 'HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Speech\Voices\Tokens\TTS_MS_ES-MX_SABINA_11.0'
