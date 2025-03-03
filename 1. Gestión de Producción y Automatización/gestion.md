# 1. Análisis con Software de Simulación de Planta

En el marco de la mejora continua de los procesos productivos, el **departamento de ingeniería** de la empresa **Los Juguetes Hermanos** ha desarrollado un plan estratégico para la **optimización de su planta de fabricación**. Como primer paso, se llevó a cabo la **modelación del estado actual** de la fábrica en la herramienta de Tecnomatix, identificando ineficiencias y oportunidades de mejora en el flujo de producción.

##  Modelo de la Situación Inicial  

El siguiente esquema representa la **distribución actual** de la planta de producción:

![b78749b6-6aaf-4d20-98c6-121719727126](https://github.com/user-attachments/assets/94e5c501-7bcf-4125-b52f-7952c0f46ce6)

![fe8d665d-fd51-47c2-a37a-ed6a811d3bb9](https://github.com/user-attachments/assets/f17ffe6e-eaa4-4032-9865-bc40e58f6232)

### Problemas Identificados:
- **Cuellos de botella** en múltiples etapas del proceso.
- **Flujo de producción segmentado**, dificultando la integración de las líneas.
- **Aprovechamiento ineficiente del espacio en planta**.
- **Alto consumo energético** debido a la operación simultánea de múltiples inyectoras con baja ocupación.
- **Tiempos de espera prolongados**, afectando la eficiencia global del sistema.

A continuación, se presentan los niveles de **ocupación de los equipos** en cada línea de producción:

#### Línea Propulser  
![4f70c97a-721c-4164-8102-7e4546284dd6](https://github.com/user-attachments/assets/756f2518-0811-4d79-a455-df19b27415b9)

#### Línea Qammar  
![d6e40a6b-5a24-42c7-9a7f-2d20f706c214](https://github.com/user-attachments/assets/100794fd-9ea0-4609-8bc1-84bdcd18393f)

#### Línea TDB (Trompo de Batalla)  
![9af76e86-e705-44e6-9545-35b027ffd6d8](https://github.com/user-attachments/assets/0b687d7e-c53a-4df3-a2c2-3234b70452f4)

##  Propuesta de Optimización del Layout  

Tras un análisis detallado de múltiples alternativas, se seleccionó el siguiente **diseño optimizado de la planta**, el cual maximiza el flujo productivo y reduce desperdicios:

![e0a73841-36ec-4914-883c-5cd0769609cb](https://github.com/user-attachments/assets/769a7ceb-fe93-4d3e-b698-bd3d02912cce)

![faf0b415-ac45-4750-8889-f83526713c13](https://github.com/user-attachments/assets/6ed93f23-6cf3-4709-b643-ca7078fc1a48)

### Beneficios del Nuevo Diseño:
- **Integración de las líneas de producción**, eliminando restricciones de flujo.
- **Reducción de tiempos de espera y transporte de materiales**.
- **Mayor flexibilidad** para la fabricación de distintos modelos de juguetes con cambios mínimos en el sistema.
- **Optimización del consumo energético**, consolidando el uso de equipos.
- **Automatización del cambio de moldes**, permitiendo mayor eficiencia en la inyectora principal.

##  Desempeño del Nuevo Sistema

El siguiente gráfico presenta el desempeño alcanzado tras la optimización:

![image](https://github.com/user-attachments/assets/2a1623c8-997c-48ac-b41a-797bcfe796aa)

Los **tiempos de procesamiento** por operación son los siguientes:

| **Proceso**               | **Tiempo (minutos)** |
|---------------------------|----------------------|
| Registro                  | 0:10                 |
| Inyección                 | 0:11                 |
| Lijado                    | 1:30                 |
| Desbarbado                | 1:00                 |
| Pintado                   | 1:20                 |
| Ensamblaje                | 3:00                 |
| Empaque Individual        | 0:21                 |
| Empaque por Lotes         | 3:30                 |

A continuaciòn se consignan los MTTR para cada proceso:

| **Proceso**              | **Disponibilidad** | **MTTR (mm:ss)** |
|--------------------------|-------------------|------------------|
| Inyección               | 95%               | 1:00             |
| Lijado                  | 90%               | 0:10             |
| Desbarbado              | 95%               | 0:30             |
| Pintado                 | 95%               | 0:30             |
| Ensamblaje              | 85%               | 0:10             |
| Empaque Individual      | 90%               | 1:00             |
| Empaque por Lotes       | 95%               | 1:00             |





## Integración de sistema MES a Los Juguetes Hermanos

### Adquisición de Datos en la Planta

Para optimizar la producción y trazabilidad, se implementará un sistema de adquisición de datos en tiempo real que integrará sensores, PLCs y dispositivos IoT en cada etapa del proceso:

- **Inyección (Gestionada por el IRB 6700)**
  - Sensores de presión y temperatura en la inyectora.
  - Contadores de ciclos de moldeo y tiempo de inactividad.
  - Comunicación OPC UA con el MES.

- **Desbarbado Criogénico:**
  - Monitoreo de temperatura en la cámara de congelación de la màquina.
  - Registro de tiempos de exposición por lote.
  - Control de consumo de nitrógeno líquido.

- **Lijado y Ensamblaje:**
  - Escaneo de códigos de barras o RFID al inicio y fin de cada tarea.
  - Registro de tiempos operativos mediante tablets IoT.
  - Inspección visual con visión artificial en puntos clave.

- **Empacado individual y por lotes:**
  - Pesaje de productos terminados para control de calidad.
  - Registro de lotes mediante código QR.

---

### Infraestructura de Control y Comunicación

Para garantizar la integración fluida entre la planta y el MES, se utilizará una arquitectura basada en:

- **PLCs industriales conectados a un SCADA**, con almacenamiento en bases de datos SQL.
- **Middleware basado en Node-RED o Kepware**, actuando como puente con el MES.
- **Protocolos de comunicación estandarizados**: OPC UA, MQTT y REST API.

El sistema permitirá monitoreo en tiempo real, alertas automáticas y acceso remoto a la información de producción.

---

### Implementación y Desarrollo

La integración con el MES se realizará en **etapas** distribuidas a lo largo de 8 meses para minimizar interrupciones en la producción:

1. **Configuración de Sensores y PLCs (Meses 1-3)**
   - Instalación y calibración de sensores en inyectoras y cámaras criogénicas.
   - Desarrollo del sistema de registro en lijado y ensamblaje.

2. **Desarrollo de Middleware y Conexión con MES (Meses 4-6)**
   - Creación de APIs para transmisión de datos.
   - Configuración de dashboards de productividad y calidad.

3. **Optimización y Validación (Meses 7-8)**
   - Pruebas de precisión de datos y ajuste de alarmas.
   - Capacitación del personal en el uso del sistema.

---

### Valor Agregado y Beneficios Esperados

- **Aumento del OEE** obteniedo datos de eficiencia, disponibilidad y calidad, nos permite identificar cuellos de botella y àreas de mejora en nuestro proceso.

- **Reducciòn de tiempos de inactividad** porque podemos anticipar posibles fallas y programar mantenimientos preventivos que puedan detener completamente el proceso de producciòn.

- **Trazabilidad total** desde la recepciòn del material hasta el empaque.

- **Ajuste en tiempo real de la producciòn** para controlar en tiempo real cuantas unidades queremos producir de cada juguete.

-**Toma de decisiones** basadas eb inbfromaciòn precisa y actualizada sobre el rendimiento de la producciòn, ademàs de poder generar informes y anàlisis de detallas sobre la prioducciòn, identificando tendencias y patrones que permiten mejorar la eficiencia.


- **Cumplimiento normativo** puesto que el MES podrà permitir la documentaciòn y trazabilidad de los procesos, lo que asegura el cumplimiento de las normas de seguridad, dadp que el cumplimiento de estas es primordial para el uso de los juguetes por los niños.