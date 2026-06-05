# Quantum Key Distribution (QKD) & Hybrid Cryptography Engine

Este repositorio contiene un proyecto de ingeniería avanzada enfocado en la **Ciberseguridad y Computación Cuántica**. El sistema simula la ejecución del protocolo cuántico **BB84** utilizando el framework **Cirq** para generar y distribuir llaves criptográficas de forma segura, integrándolas posteriormente con algoritmos de cifrado simétrico clásico (**AES**) mediante capas criptográficas de nivel de producción.

## 🚀 Características y Capacidades Técnicas

* **Simulación Cuántica con Cirq:** Modelado y ejecución de circuitos cuánticos para la preparación de estados, elección aleatoria de bases de medición (rectilíneas y diagonales) y colapso de funciones de onda.
* **Protocolo BB84 End-to-End:** Implementación completa del flujo cuántico: transmisión de qubits, reconciliación de bases, detección de espías (*Eve*) mediante control de tasa de error de bits cuánticos (QBER).
* **Cifrado Híbrido Avanzado (AES):** Integración de la llave cuántica generada en un motor de cifrado clásico utilizando `cryptography` (AES en modo CBC/GCM), garantizando el secreto perfecto (*Perfect Forward Secrecy*).
* **Gestión de Datos y Padding:** Manejo seguro de bytes, codificación en Base64 para el transporte de datos y formateo criptográfico estricto mediante `PKCS7`.

## 🛠️ Stack Tecnológico

* **Lenguaje Core:** Python 3.x
* **Framework Cuántico:** Google Cirq
* **Librería Criptográfica:** `cryptography` (Hazmat primitives)
* **Soporte Matemático:** `NumPy`

## ⚙️ Arquitectura del Sistema y Seguridad

El proyecto resuelve el problema de la distribución segura de claves combinando la física cuántica con la criptografía tradicional:

1. **El Canal Cuántico (Generación de Llave):** Alice genera fotones (qubits) en estados aleatorios a través de compuertas cuánticas ($X$, $H$). Bob los mide utilizando bases aleatorias. Tras comparar las bases públicamente, extraen una clave compartida secreta.
2. **Inviolabilidad Cuántica:** Aprovechando el **Teorema de No Clonación** y el principio de incertidumbre, cualquier intento de interceptación en el circuito cuántico altera los estados de los qubits, elevando el error y alertando al sistema para descartar la clave.
3. **Capa de Cifrado Clásico:** La clave cuántica purificada se transforma en una secuencia de bytes usada por el algoritmo `Cipher(algorithms.AES(key), modes.CBC(iv))` para encriptar el mensaje real de manera indestructible para computadoras convencionales.

## 📌 Flujo del Algoritmo Implementado

$$\text{Alice (Qubits)} \longrightarrow \text{Canal Cuántico} \longrightarrow \text{Bob (Medición)} \longrightarrow \text{Clave BB84} \longrightarrow \text{Cifrado AES-256}$$

## 🔧 Configuración y Ejecución Local

Para ejecutar la simulación cuántica y probar el cifrado híbrido en tu máquina local, sigue estos pasos:

### Prerrequisitos
Disponer de un entorno de Python 3.8 o superior.

### Instalación
1. Clonar el repositorio:
   ```bash
   git clone [https://github.com/longaresf/quantum-key-distribution-bb84.git](https://github.com/longaresf/quantum-key-distribution-bb84.git)
    ```
2. Ingresar al directorio:
  Bash
  cd quantum-key-distribution-bb84

3. Instalar las dependencias del entorno:
  Bash
  pip install cirq cryptography numpy

Ejecución
1. Corre el script o notebook principal para iniciar la simulación del circuito cuántico y el posterior cifrado de datos:
  Bash
  python main.py  # O inicia tu entorno de Jupyter/Colab según corresponda

✒️ Reconocimientos y Contexto

  Francisco Longares - Especialista en Automatización, Datos y Soluciones de Vanguardia - longaresf
  
  Proyecto desarrollado como trabajo final (Capstone Project) en la especialización de Computación Cuántica de Qubit by Qubit (QxQ).
