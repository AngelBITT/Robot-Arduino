# Robot-Arduino
Carrito multifuncional con Arduino
Robot Multifuncional con Arduino

1. Descripción del proyecto
    El proyecto consiste en el desarrollo de un robot multifuncional el cual se controla mediante una placa Arduino, tiene dos modos:
    -Modo autónomo: el robot detecta y evita obstáculos utilizando un sensor ultrasónico HC-SR04.
    -Modo teleoperado: el robot permite el control remoto vía Bluetooth HC-06 desde algún smartphone.

2. Requisitos e instalación
    2.1 Requisitos
    -Arduino UNO.
    -Shield de control de motores.
    -Motores DC.
    -Ruedas mecanum.
    -Sensor ultrasónico HC-SR04.
    -Módulo Bluetooth HC-06.
    -Batería Li-Po.
    -Liberías: AFMotor.h y Servo.h

    2.2 Instalación
    1. Instalar Arduino IDE.
    2. Instalar las librerías que se necesitan.
    3. Cargar el código al Arduino IDE.
    4. Conectar el hardware según el diagrama del proyecto.
    5. Encender la batería y verificar.

3. Cómo usarlo
    -Modo autónomo:
        Analizar el entorno con el sensor ultrasónico HC-SR04.
        Compara distancias.
        Decide la dirección más segura.
        Evita colisiones de manera automática.
    
    -Modo teleoperado:
        Comandos:
        F --> Avanzar
        B --> Retroceder
        L --> Giro izquierdo
        R --> Giro derecho
        S --> Detener

4. Estructura del proyecto
    /robot-arduino
│── src/
│   ├── main.ino        
│   ├── autonoma.cpp    
│   ├── bluetooth.cpp   
│   └── sensores.cpp    
│── docs/
│   └── diagramas/           
│── README.md

5. Resumen técnico del sistema
    El robot esta construido de tal forma en la que el Arduino es como la unidad central de procesamiento.
    Aspectos:
    -Control de motores: se controla mediante la librería AFMotor.h para manejar los motores.
    -Percepción del entorno: el sensor ultrasónico HC-SR04 mide las distancias.
    -Comunicación inalámbrica: módulo Bluetooth HC-066 el cual se conecta por serial.
    -Cambiar de modo: si se recibe un comando mediante Bluetooth, el robot cambia del modo autónomo al modo teleoperado.

6. Preguntas frecuentes
    1. El robot no detecta obstáculos.
       Revisar el cableado del sensor ultrásonico HC-SR04.

    2. No se conecta el Bluetooth.
       Verificar el PIN del módulo Bluetooth HC-06.

    3. ¿Se puede utilizar otra batería?
       Sí, siempre y cuando sea 7.4 V a 11.1 V y que pueda alimentar motores.
