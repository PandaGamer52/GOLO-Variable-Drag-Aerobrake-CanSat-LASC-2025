# GOLO - Variable Drag Aerobrake CanSat 🛰️

[cite_start]Este repositorio contiene el código fuente, los esquemáticos electrónicos y los modelos mecánicos de **GOLO**, un satélite autónomo (CanSat) de caída libre diseñado para realizar experimentos aerodinámicos durante su descenso[cite: 82, 85]. 

Este proyecto fue desplegado exitosamente en el **Latin American Space Challenge (LASC) 2025**, logrando el 5º lugar general.

## 🚀 Resumen del Proyecto
[cite_start]GOLO es una sonda cilíndrica de 80 mm de diámetro por 300 mm de longitud, con una masa total de 750 gramos[cite: 85]. [cite_start]Su objetivo principal es demostrar una desaceleración controlada mediante un aerofreno de arrastre variable, al mismo tiempo que recopila y transmite datos atmosféricos en tiempo real[cite: 82, 83].

### ⚙️ Mecanismo de Aerofrenado
[cite_start]El sistema transforma el movimiento lineal en una expansión radial controlada[cite: 120, 184]:
* [cite_start]**Actuación Principal:** Utiliza un motor DC acoplado a un tornillo de avance infinito[cite: 108, 185].
* [cite_start]**Cinemática:** El tornillo desplaza una placa base conectada a un mecanismo de cuatro barras[cite: 109, 112, 187].
* [cite_start]**Despliegue:** El movimiento empuja brazos articulados hacia el exterior, desplegando el dosel para aumentar la resistencia aerodinámica y reducir la velocidad de descenso a ~20 m/s[cite: 119, 129, 188, 194].

### 💻 Aviónica y Computadora de Vuelo (Helios PCB)
[cite_start]La sonda opera de manera completamente independiente de la aviónica principal del cohete[cite: 87, 102].
* [cite_start]**Microcontrolador:** Teensy 4.1[cite: 103, 180].
* [cite_start]**Sensores:** IMU MPU6050 y sensor ambiental BME280 (presión y temperatura)[cite: 103, 181].
* [cite_start]**Telemetría:** Módulo LoRa RA-02 independiente para transmisión a la estación terrena[cite: 104, 182].
* [cite_start]**Almacenamiento:** Registro redundante en tarjeta microSD a bordo[cite: 105, 182].

### 📡 Estación Terrena
[cite_start]La comunicación se mantiene mediante una interfaz gráfica de usuario (GUI) personalizada desarrollada en MATLAB y JavaScript[cite: 134, 138]. Permite:
* [cite_start]Visualización en tiempo real de altitud, velocidad, coordenadas GPS y orientación[cite: 137].
* [cite_start]Generación de gráficos y registro de datos para análisis post-vuelo[cite: 139].

## 🗺️ Perfil de Misión (CONOPS)
1. [cite_start]**Despliegue (~1000m AGL):** Expulsión del cohete y despliegue del paracaídas de drogue (descenso a 15 m/s)[cite: 124, 125, 191, 192].
2. [cite_start]**Activación del Aerofreno (~500m AGL):** Liberación de la cápsula y expansión del mecanismo de arrastre variable (descenso a 20 m/s)[cite: 126, 127, 129, 193, 194].
3. [cite_start]**Recuperación (~200m AGL):** Eyección del aerofreno y despliegue del paracaídas principal para un aterrizaje seguro a 5-6 m/s[cite: 130, 131, 132, 195].
