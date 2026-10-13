# LNOX v0

*Asistente de voz inteligente (parlante) · hardware del JNOX V3 · carcasa a medida en nylon PA12*

![Carcasa del LNOX en nylon PA12](../assets/img/lnox-carcasa.jpg)

Asistente de voz tipo Alexa, con funciones de agente, que se vincula al reloj JNOX y a la app Android. Reutiliza la placa del [JNOX V3](jnox-watch-v3.md) y añade una salida de audio propia.

## Ficha

| | |
|---|---|
| Hardware base | Placa del JNOX V3 (ESP32-S3 N16R8) |
| Audio | Salida I2S con conversor PCM5102A y etapa de amplificación propia; música desde microSD |
| Conectividad | Wi-Fi, BLE y ESP-NOW (enlace directo con el reloj) |
| Servicio en la nube | Cloudflare Worker que coordina el reconocimiento de voz, el modelo de lenguaje y la síntesis de voz (código y endpoints no públicos) |
| Carcasa | Nylon PA12 a medida, diseñada en Autodesk Inventor, lo más compacta posible y con una salida de audio de geometría compleja |

![Salida de audio de la carcasa del LNOX](../assets/img/lnox-rejilla-audio.jpg)

## Qué hace

- Llamadas y mensajes por voz, a través del teléfono vinculado con la app.
- Lee las notificaciones en voz alta (síntesis de voz con la API de ElevenLabs).
- Responde con personalidad configurable, estilo JARVIS o Alexa.
- Se controla desde el reloj: música y avisos hablados.

## Mi aporte

- Integración del hardware sobre la placa del V3 y diseño de la etapa de audio.
- Diseño y fabricación de la carcasa en PA12: tamaño mínimo, rejilla acústica y montaje de la placa.
- Servicio en la nube, firmware y vinculación con la [JNOX App](jnox-app.md).

## Estado

Prototipo funcional.

[← Volver al portafolio](../README.md)
