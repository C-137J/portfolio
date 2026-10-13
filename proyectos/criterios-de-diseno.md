# Criterios de diseño que aplico

Reglas que uso al diseñar PCB y carcasas, y por qué. Son criterios generales, no los diseños de mis productos.

## PCB

1. **Apilado de 4 capas: señal / masa continua / alimentación / señal.** La capa 2 es un plano de masa sin cortes ni pistas, pegado a la capa 1: así toda señal rápida de la capa 1 tiene su camino de retorno justo debajo.
2. **Lo rápido va en la capa 1**: buses SPI, nodos de conmutación de los reductores, USB y realimentación. Lo lento puede bajar a la capa 4.
3. **El desacoplo lo hacen los condensadores**, no los planos. Con 1 mm de dieléctrico entre masa y alimentación no hay capacidad de plano útil, así que el condensador de entrada de cada reductor va a menos de 2 mm de sus pines VIN y GND.
4. **Ancho de pista según la corriente**, no uno para todo: 0,2 mm para señales digitales, más ancho para 3,3 V y polígonos o pistas de más de 1 mm para 5 V y las cargas de varios amperios.
5. **Varias vías en paralelo** cuando una ruta de potencia cambia de capa, y cosido de masa cada pocos milímetros.
6. **La antena del ESP32-S3 manda sobre el resto**: en el borde, con cobre libre debajo en todas las capas, lejos de piezas metálicas grandes como las baterías cilíndricas.
7. **Separar lo ruidoso de lo sensible**: la zona de conmutación lejos de las medidas analógicas, como el divisor de tensión de la batería.
8. **Cortar la potencia de lo que no se usa**, por ejemplo con un interruptor de carga para los servomotores.
9. **Diseñar para el fabricante**: reglas de pista, separación y vía que el taller hace sin recargo.
10. **Una sola fuente de verdad para los pines en el firmware.** El mismo pin definido en cinco archivos no molesta hasta que cambias de pantalla.

## Carcasa

1. **Empezar por el componente que manda la huella** (en un reloj, la pantalla) y calcular el grosor con una tabla de apilado en Z, capa por capa.
2. **Holguras y paredes explícitas**: por ejemplo, 0,6 mm de holgura alrededor de la pantalla y paredes de 1,5 mm en PA12 sinterizado.
3. **Respetar los flexibles**: la cola de una pantalla AMOLED no admite un radio de doblez menor de unos 1,5 mm, y hay que dejar hueco debajo del vidrio para el pliegue.
4. **Sellar desde el diseño**: sin conector abierto (pogo pines en vez de USB-C), con silicona en la unión y membranas acústicas donde hay sonido.
5. **Elegir el proceso por la pieza**: nylon PA12 sinterizado para la caja, resina SLA para el botón que necesita precisión y poca fricción, PLA en impresora propia para prototipos.
6. **El nylon absorbe humedad**: se barniza si va a recibir salpicaduras.

[← Volver al portafolio](../README.md)
