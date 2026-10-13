# VACHI v0

*PCB de 4 capas con etapa de potencia para servomotores · proyecto de emprendimiento*

![PCB de 4 capas del VACHI v0](../assets/img/vachi-placa.jpg)

Hardware de un dispositivo con pantalla y tres servomotores que se comunican entre sí por radio ESP-NOW. La idea y los requisitos son de un compañero; yo diseñé la PCB y el mecanismo de montaje de los servos. Participa en Equipu, el laboratorio de emprendimientos universitarios.

## Ficha

| | |
|---|---|
| PCB | 4 capas (apilado estándar de 1,6 mm de JLCPCB), diseñada en EasyEDA Pro y fabricada en JLCPCB |
| Procesador | ESP32-S3-WROOM-1 |
| Pantalla | 240×240 (ST7789) |
| Potencia | Reductor de 5 V (TPS54302) para los servomotores, con interruptor de carga (TPS22918) que corta su alimentación; reductor de 3,3 V (TPS54202) para la lógica |
| Sensores y datos | IMU BMI160 y microSD |
| Comunicación | ESP-NOW, con detección de cercanía por la intensidad de la señal |
| Mecánica | Soporte de montaje de los servomotores, diseñado por mí |

![Soporte mecánico de los servomotores del VACHI](../assets/img/vachi-servos.jpg)

## Mi aporte

- Requisitos a partir de lo que pedía el equipo, selección de componentes, esquemático y layout de la PCB de 4 capas.
- Etapa de potencia: reductores, interruptor de carga para los servos y reglas de ruteo para 2 A.
- Diseño mecánico del montaje de los servomotores.
- Armado de 2 placas funcionales.

## Criterios que apliqué en el layout

- Plano de masa continuo en la capa 2, sin cortes ni pistas, y todo lo rápido (SPI, nodos de conmutación, USB) en la capa 1, justo encima.
- Alimentación en polígonos en la capa 3, con varias vías en paralelo en las rutas de 5 V.
- Antena del ESP32-S3 en el borde, lejos de las celdas de batería (que la desintonizan) y sin cobre debajo.
- Condensadores de entrada de los reductores pegados a sus pines, porque en 4 capas el desacoplo lo hacen los cerámicos.

Más detalle en [criterios de diseño](criterios-de-diseno.md).

## Estado

2 placas armadas y funcionales, en uso en el concurso.

[← Volver al portafolio](../README.md)
