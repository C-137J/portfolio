# VRNOx

*Realidad virtual casera para SteamVR · mandos propios con hardware del JNOX V3*

![Mandos del sistema VRNOx](../assets/img/vrnox-mandos.jpg)

Sistema para jugar en SteamVR con un celular como visor, dos mandos basados en la placa del [JNOX V3](jnox-watch-v3.md) y seguimiento de posición con cámaras PS3 Eye. Con él ya jugué Half-Life: Alyx.

## Cómo funciona

| Parte | Qué hace |
|---|---|
| Visor | Un celular con la app PhoneVR (pantalla y rotación de la cabeza) |
| Mandos | Dos placas basadas en el V3 con IMU; mandan su orientación y sus botones por ESP-NOW |
| Dongle | Una placa V3 conectada por USB al PC que recibe por ESP-NOW a 250 Hz y entrega los datos a SteamVR |
| Posición | Tres cámaras PS3 Eye que siguen esferas de color |

## Mi aporte

- Hardware de los mandos y del dongle sobre la placa del V3, y su firmware con enlace ESP-NOW.
- Integración del sistema con proyectos de código abierto (PhoneVR, HadesVR y PSMoveServiceEx): instalador, calibración y parche de posición 6DOF.

## Estado

Funcional: se leen correctamente los mandos y la cabeza. Falta afinar el seguimiento de posición.

[← Volver al portafolio](../README.md)
