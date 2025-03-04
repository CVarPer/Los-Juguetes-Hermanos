# Industria 4.0 en la automatización 

## Propuesta Implementación Industria 4.0


Como propuesta de implementación de nuevas tecnologías de la Industria 4.0, se plantea esta arquitectura de conexiones del sistema, que implica el uso de Ignition para la implementación del sistema SCADA, LOGIX EMULATE para la emulación del PLC y el uso de RSLINX como gateway de comunicaciones para establecer la suscripción a los tags del PLC por medio de comunicación OPC.  

Esta arquitectura permite la integración de sistemas de automatización avanzada con supervisión remota, facilitando la adquisición de datos en tiempo real, la optimización de procesos y la interoperabilidad entre distintos dispositivos y plataformas industriales.  

![Arquitectura de Conexiones](./Figuras/Conexiones.png)


### Tecnologías utilizadas

A continuación, se describen las tecnologías empleadas en esta propuesta:

- **Ignition**: Plataforma SCADA/MES que permite la visualización, control y análisis de datos en tiempo real. Facilita la integración con bases de datos y sistemas empresariales.
- **LOGIX EMULATE**: Herramienta de emulación de Rockwell Automation que permite simular la ejecución de programas en ControlLogix sin necesidad de un hardware físico.
- **RSLINX**: Software de comunicación de Rockwell Automation que actúa como gateway para la conexión entre el PLC y otros sistemas mediante el protocolo OPC.
- **OPC (OLE for Process Control)**: Protocolo de comunicación estándar utilizado para la integración entre dispositivos de automatización y sistemas de supervisión.
- **Ethernet/IP**: Protocolo de comunicación industrial basado en Ethernet, utilizado para la conexión entre PLCs, sensores y sistemas SCADA.
- **Base de Datos SQL**: Se utiliza para almacenar datos históricos del sistema, permitiendo la generación de reportes y análisis de tendencias.



### SCADA e Integración de Datos

El sistema SCADA basado en Ignition permite la supervisión y control de procesos industriales a través de una interfaz gráfica en tiempo real. Algunas de sus funcionalidades clave incluyen:

- Monitoreo remoto de variables del proceso.
- Registro y análisis de datos históricos.
- Configuración de alarmas y notificaciones para eventos críticos.
- Integración con bases de datos SQL para almacenamiento y análisis de datos.
- Paneles de visualización personalizables con indicadores clave de rendimiento (KPIs).

### Lógica de Programación del PLC

La lógica de control del PLC se basa en programación en **Ladder Logic**, desarrollada en **Studio 5000** y emulada en **LOGIX EMULATE**. Se utilizan las siguientes estrategias de control:

- **Estructura modular**: Código organizado en rutinas y subrutinas para facilitar la escalabilidad y mantenimiento.
- **Control por eventos**: Implementación de lógica basada en cambios de estado para optimizar tiempos de respuesta.
- **Optimización de ciclos de escaneo**: Priorización de tareas críticas para mejorar la eficiencia del control.
- **Integración con OPC**: Suscripción de tags del PLC mediante RSLINX para intercambio de datos con el sistema SCADA.
- **Diagnóstico y depuración**: Uso de herramientas de simulación para pruebas previas a la implementación en hardware físico.
