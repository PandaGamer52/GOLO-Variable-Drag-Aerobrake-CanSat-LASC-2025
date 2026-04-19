GOLO - Variable Drag Aerobrake CanSat 🛰️
Este repositorio contiene el código fuente, los esquemáticos electrónicos y los modelos mecánicos de GOLO, un satélite autónomo (CanSat) de caída libre diseñado para realizar experimentos aerodinámicos durante su descenso.

Este proyecto fue desplegado exitosamente en el Latin American Space Challenge (LASC) 2025, logrando el 5º lugar general.

🚀 Resumen del Proyecto
GOLO es una sonda cilíndrica de 80 mm de diámetro por 300 mm de longitud, con una masa total de 750 gramos. Su objetivo principal es demostrar una desaceleración controlada mediante un aerofreno de arrastre variable, al mismo tiempo que recopila y transmite datos atmosféricos en tiempo real.

⚙️ Mecanismo de Aerofrenado
El sistema transforma el movimiento lineal en una expansión radial controlada:

Actuación Principal: Utiliza un motor DC acoplado a un tornillo de avance infinito.

Cinemática: El tornillo desplaza una placa base conectada a un mecanismo de cuatro barras.

Despliegue: El movimiento empuja brazos articulados hacia el exterior, desplegando el dosel para aumentar la resistencia aerodinámica y reducir la velocidad de descenso a ~20 m/s.

💻 Aviónica y Computadora de Vuelo (Helios PCB)
La sonda opera de manera completamente independiente de la aviónica principal del cohete.

Microcontrolador: Teensy 4.1.

Sensores: IMU MPU6050 y sensor ambiental BME280 (presión y temperatura).

Telemetría: Módulo LoRa RA-02 independiente para transmisión a la estación terrena.

Almacenamiento: Registro redundante en tarjeta microSD a bordo.

📡 Estación Terrena
La comunicación se mantiene mediante una interfaz gráfica de usuario (GUI) personalizada desarrollada en MATLAB y JavaScript. Permite:

Visualización en tiempo real de altitud, velocidad, coordenadas GPS y orientación.

Generación de gráficos y registro de datos para análisis post-vuelo.

🗺️ Perfil de Misión (CONOPS)
Despliegue (~1000m AGL): Expulsión del cohete y despliegue del paracaídas de drogue (descenso a 15 m/s).

Activación del Aerofreno (~500m AGL): Liberación de la cápsula y expansión del mecanismo de arrastre variable (descenso a 20 m/s).

Recuperación (~200m AGL): Eyección del aerofreno y despliegue del paracaídas principal para un aterrizaje seguro a 5-6 m/s.
