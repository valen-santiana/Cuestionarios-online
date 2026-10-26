# Repaso Activo

Aplicación web gratuita para estudiar a partir de tus propios apuntes. Funciona en el navegador, sin servidor y sin pagar nada.

## Dos motores

**1. Sin internet (por defecto, 100 % gratis).** La app detecta los conceptos de tus apuntes escritos como `Concepto: definición` (uno por línea) o como oraciones del tipo "El X es…". Descarta referencias, autores y frases cortadas, y te deja revisar la lista de conceptos antes de generar. Con texto corrido (un libro o un PDF largo) usa primero **Crear glosario con Gemini**: una sola consulta convierte el material en un glosario y desde ahí generas preguntas sin internet cuantas veces quieras. Arma:

- Opción múltiple (concepto ↔ descripción)
- Verdadero / falso
- Asociar conceptos
- Preguntas abiertas, comparadas con las ideas clave de tus apuntes
- Completar la oración

**2. Gemini (opcional, con clave gratuita de Google).** Suma lo que necesita inteligencia artificial:

- Casos clínicos y problemas reales de la industria ("¿a qué corresponde?")
- Traducción del material al español o al inglés
- Lectura de fotos de diapositivas, pizarras y PDF escaneados
- Corrección de respuestas abiertas con comentario

Puedes mezclar: por ejemplo, las preguntas de opción múltiple se generan sin internet y los casos reales con Gemini.

## Otras funciones

- Sube PDF, Word (.docx), PowerPoint (.pptx) o texto.
- Elige de 1 a 10, de 10 a 20 o de 20 a 30 preguntas.
- Practica en tiempo real con corrección al instante, o en modo examen.
- Revisa el puntaje por tipo de pregunta y repite solo las que fallaste.
- Descarga el cuestionario en Word (A4) para imprimir, con hoja de respuestas opcional.

## Clave de Gemini (opcional)

1. Entra a https://aistudio.google.com/apikey con tu cuenta de Google y crea una clave.
2. En la app, abre el panel **Gemini (opcional, gratis)**, pégala y pulsa **Conectar**.

La clave se guarda solo en tu navegador y se envía únicamente a Google. El nivel gratuito tiene límites diarios que Google puede cambiar; si se agotan, sigue usando el motor sin internet. En el nivel gratuito Google puede usar lo que envías para mejorar sus modelos, así que no subas datos reales de pacientes ni documentos confidenciales.

## Publicar en GitHub Pages

1. Crea un repositorio nuevo en GitHub (por ejemplo `repaso-activo`).
2. Sube `index.html` y `README.md` a la rama `main`.
3. En el repositorio ve a **Settings → Pages → Source: Deploy from a branch**, elige la rama `main` y la carpeta `/ (root)`, y guarda.
4. En uno o dos minutos la app queda en `https://<tu-usuario>.github.io/repaso-activo/`.

## Detalles técnicos

Un solo archivo HTML. Librerías desde cdnjs: pdf.js (PDF), mammoth (Word) y JSZip (PowerPoint y generación del .docx). Gemini se llama directamente desde el navegador con la API de Google AI Studio, y el modelo se elige de la lista de modelos Flash disponibles para tu clave.
