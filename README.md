# Demo: Dataform + Gemini CLI 🚀

Este repositorio es una demostración práctica de cómo integrar y utilizar **Dataform** en Google Cloud junto con **Gemini CLI** para agilizar el modelado, la transformación y la documentación de datos en BigQuery.

## 📌 Sobre este proyecto

El objetivo de esta demo es mostrar un flujo de trabajo moderno para ingenieros y analistas de datos, donde:
1. **Dataform** maneja el linaje de los datos, las dependencias, las pruebas (assertions) y la ejecución de código SQLX en BigQuery.
2. **Gemini CLI** actúa como un asistente de inteligencia artificial directamente en la línea de comandos, ayudando a generar código, explicar modelos complejos, escribir documentación y optimizar consultas.

## 🛠️ Requisitos Previos

Para sacar el máximo provecho de esta demo, necesitas:

* Un proyecto en **Google Cloud Platform (GCP)**.
* Las APIs de **Dataform** y **BigQuery** habilitadas.
* [**Gemini CLI**](https://cloud.google.com/gemini/docs/cli) instalado y autenticado en tu máquina local o en Cloud Shell.
* Dataform CLI instalado localmente si prefieres compilar sin entrar a la consola de GCP.

## 📂 Estructura del Repositorio

El proyecto sigue la estructura estándar de Dataform:

* `dataform.json`: Configuración principal del proyecto (ID del proyecto GCP, dataset de destino, etc.).
* `definitions/`: Directorio principal donde se almacenan los modelos de datos en formato `.sqlx` (tablas, vistas, declaraciones y aserciones).
* `includes/`: Carpeta para scripts y variables reutilizables en JavaScript.
* `package.json`: Archivo para gestionar dependencias y paquetes externos de Dataform.

## 🤖 Ejemplos de uso con Gemini CLI

Una vez que tengas clonado el repositorio, puedes usar Gemini CLI en tu terminal para acelerar tu desarrollo. Aquí tienes algunos ejemplos de *prompts* que puedes probar:

**1. Generar un nuevo modelo:**
```bash
gemini ask "Genera un archivo SQLX de Dataform tipo 'table' que lea de 'raw_users', filtre los usuarios inactivos y estandarice la columna email pasándola a minúsculas."