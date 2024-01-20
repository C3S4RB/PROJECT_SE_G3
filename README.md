# Sistema de seguridad remoto de bajo costo

## Descripción del proyecto

El proyecto consiste en un pequeño sistema de seguridad remoto de bajo costo.

Los componentes principales son:

- ESP32-CAM
- Sensor PIR
- Módulo USB-TTL
- Bot de Telegram

## Funcionamiento

El sistema funciona de la siguiente manera:

1. La ESP32-CAM permanece en modo sleep la mayor parte del tiempo para ahorrar energía.

2. Cuando el bot de Telegram recibe el comando para activar el sensor PIR, despierta a la ESP32-CAM.

3. La ESP32-CAM activa el sensor PIR para detectar movimiento.

4. Cuando el sensor PIR detecta movimiento, envía la señal a la ESP32-CAM.

5. La ESP32-CAM captura una foto con la cámara integrada y la envía al bot de Telegram.

6. El proceso se repite cada vez que se detecta movimiento.

7. Para desactivar, se envía el comando correspondiente al bot de Telegram.

## Componentes

- **ESP32-CAM**: incluye el microcontrolador ESP32, conectividad WiFi y una cámara integrada. Permite capturar y enviar las fotos.

- **Sensor PIR**: detecta movimiento mediante infrarrojos. Sirve como disparador de las fotos.

- **Módulo USB-TTL**: permite programar la ESP32-CAM y monitorizar la depuración por serial.

- **Bot de Telegram**: recibe comandos y envía alertas e imágenes. Sirve como interfaz de control remoto.

## Conclusiones

El proyecto demuestra que es posible crear un sistema de vigilancia de bajo costo usando componentes como la ESP32-CAM. El uso de Telegram como interfaz remota es muy útil para recibir alertas y fotos al instante. El sistema es fácilmente expandible agregando más sensores y lógica en el lado del servidor.
