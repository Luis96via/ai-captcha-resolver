# API Serverless de extracción de texto de imágenes (Gemini Captcha Resolver)

Esta API recibe una imagen (en base64) y devuelve el texto extraído usando Gemini, siguiendo un prompt especializado para captchas.

## Uso rápido

1. **Instala dependencias:**
   ```bash
   npm install
   ```

2. **Prueba localmente con Netlify CLI:**
   ```bash
   npx netlify dev
   ```
   La función estará en: `http://localhost:8888/.netlify/functions/extract-text`

3. **Envía una petición POST:**
   - Content-Type: `application/json`
   - Body:
     ```json
     {
       "imageBase64": "<BASE64_DE_TU_IMAGEN>",
       "mimeType": "image/png",
       "prompt": ""
     }
     ```

4. **Despliega gratis en Netlify:**
   - Sube este proyecto a GitHub.
   - Conéctalo en [Netlify](https://app.netlify.com/) y despliega.

## Respuesta
```json
{
  "text": "Texto extraído o 'Texto no identificable.'"
}
```

## Notas
- Solo acepta imágenes en base64 vía JSON.
- El prompt y la API key están configurados para uso inmediato.
- Puedes usar el archivo `test/test.http` para pruebas rápidas desde VSCode (extensión REST Client).

## Endpoint de la API en producción

https://ai-captcha-resolver-luisvr.netlify.app/.netlify/functions/extract-text
