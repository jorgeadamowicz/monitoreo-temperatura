# Sistema de Monitoreo de Temperatura

## Descripción
Este proyecto implementa el **Patrón Observador** en un sistema de monitoreo de temperatura. La aplicación simula un sensor de temperatura que notifica automáticamente a distintos observadores cada vez que la temperatura cambia. Entre los observadores, se incluyen:

- **Alarma**: Emite un mensaje cuando la temperatura supera un límite crítico.
- **Pantalla**: Muestra la temperatura actual cuando se actualiza.
- **Alarma por correo**: Envía un correo electrónico de alerta si la temperatura supera el umbral establecido.

## Tecnologías utilizadas
- **Python** (para la lógica del programa).
- **Yagmail** (para el envío automático de correos electrónicos).
- **Programación Orientada a Objetos (POO)**.

## Estructura del Código
El código se organiza en las siguientes clases:

### 1. **SensorTemperatura** (Sujeto observado)
   - Mantiene una lista de observadores.
   - Notifica a los observadores cuando la temperatura cambia.

### 2. **Observador** (Clase base para los observadores)
   - Define el método `update()`, que las subclases deben implementar.

### 3. **Alarma** (Observador concreto)
   - Imprime un mensaje si la temperatura supera el umbral crítico.

### 4. **Pantalla** (Observador concreto)
   - Muestra la temperatura actual en la consola cada vez que cambia.

### 5. **AlarmaCorreo** (Observador concreto)
   - Envía un correo electrónico cuando la temperatura supera el límite crítico.

## Instalación y Uso
1. **Clonar el repositorio**
   ```bash
   git clone https://github.com/tu_usuario/nombre_del_repositorio.git
   cd nombre_del_repositorio
   ```

2. **Instalar dependencias**
   Asegúrate de tener Python instalado y luego ejecuta:
   ```bash
   pip install yagmail
   ```

3. **Configurar credenciales de correo**
   Para enviar correos con Yagmail, define la contraseña en una variable de entorno:
   ```bash
   export EMAIL_PASSWORD="tu_contraseña"
   ```
   También asegúrate de modificar la dirección del remitente en el código.

4. **Ejecutar el programa**
   ```bash
   python monitor_temperatura.py
   ```

## Ejemplo de Salida
```
Sensor de temperatura: la temperatura actual es de 30°C
Alarma!: La temperatura actual es de 30 °C. Está por encima del valor crítico!
Correo enviado a ejemplo@correo.com
Pantalla: la temperatura actual ahora es de 30 °C
```

## Contribuciones
Si deseas mejorar este proyecto, ¡siéntete libre de hacer un **fork** y enviar un **pull request**!

## Licencia
Este proyecto se encuentra bajo la licencia MIT.

---

### Autor

- GitHub: (https://github.com/jorgeadamowicz)
- LinkedIn:(https://www.linkedin.com/in/jorge-adamowicz-048236ba/)

![Python](https://img.shields.io/badge/Python-3.10-blue)
