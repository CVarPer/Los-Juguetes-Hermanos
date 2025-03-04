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

A continuación, se presenta el desempeño en cada línea de producción:

#### Línea Propulser  
![4f70c97a-721c-4164-8102-7e4546284dd6](https://github.com/user-attachments/assets/756f2518-0811-4d79-a455-df19b27415b9)

**Información General**

| UNIDADES | T. DISPONIBLE | T. OPTVO | CALIDAD |
|----------|--------------|----------|---------|
| 17       | 28800        | 28644    | 0,93    |



**Procesos: Propulser**

| PROCESO   | REGISTRO | INYECCIÓN | M. CHASIS | M. MOTOR | M. VIDRIOS | CALIDAD | DESPACHO |
|-----------|---------|-----------|-----------|----------|------------|---------|----------|
| **T. DE CICLO** | 300 | 30 | 5 | 180 | 120 | 10 | 10 |
| **T. DISPONIBLE** | 23040 | 18720 | 27360 | 27360 | 27360 | 24480 | 27360 |
| **DISPONIBILIDAD** | 0,8 | 0,65 | 0,95 | 0,95 | 0,95 | 0,85 | 0,95 |



**Métricas Finales**

| DISPONIBILIDAD | EFICIENCIA | FFT  |
|---------------|-----------|------|
| 0,8833        | 0,3615    | 0,93 |

Esto deja a la línea con un desastroso OEE de 29%.

#### Línea Qammar  
![d6e40a6b-5a24-42c7-9a7f-2d20f706c214](https://github.com/user-attachments/assets/100794fd-9ea0-4609-8bc1-84bdcd18393f)

**Información General**

| UNIDADES | T. DISPONIBLE | T. OPTVO | CALIDAD |
|----------|--------------|----------|---------|
| 22       | 28800        | 28644    | 0,95    |

**Procesos: Qammar**

| PROCESO   | REGISTRO | CORTE | CALIDAD 1 | PINTURADO | ENSAMBLE | CALIDAD 2 | E. INDIVIDUAL |
|-----------|---------|-------|-----------|-----------|---------|-----------|--------------|
| **T. DE CICLO** | 10 | 10 | 10 | 60 | 10 | 10 | 210 |
| **T. DISPONIBLE** | 25920 | 23040 | 25920 | 24480 | 21600 | 24480 | 25920 |
| **DISPONIBILIDAD** | 0,90 | 0,80 | 0,90 | 0,85 | 0,75 | 0,85 | 0,90 |

**Métricas Finales**

| DISPONIBILIDAD | EFICIENCIA | FFT  |
|---------------|-----------|------|
| 0,85         | 0,2335    | 0,95 |

Con ello se calcula que esta línea de producción tiene un OEE del 18%.


#### Línea TDB (Trompo de Batalla)  
![9af76e86-e705-44e6-9545-35b027ffd6d8](https://github.com/user-attachments/assets/0b687d7e-c53a-4df3-a2c2-3234b70452f4)

**Información General**

| UNIDADES | T. DISPONIBLE | T. OPTVO | CALIDAD |
|----------|--------------|----------|---------|
| 232      | 28800        | 28644    | 0,85    |

**Procesos: TDB**

| PROCESO   | REGISTRO | INYECCIÓN | FUNDICIÓN | TROQUELADO | PINTURADO | ENSAMBLAJE | CALIDAD | DESPACHO |
|-----------|---------|-----------|-----------|------------|----------|------------|---------|----------|
| **T. DE CICLO** | 10 | 3 | 5 | 1 | 2 | 10 | 5 | 15 |
| **T. DISPONIBLE** | 23040 | 24480 | 27360 | 27936 | 24480 | 20160 | 25920 | 24480 |
| **DISPONIBILIDAD** | 0,8 | 0,85 | 0,95 | 0,97 | 0,85 | 0,7 | 0,9 | 0,85 |

**Métricas Finales**

| DISPONIBILIDAD | EFICIENCIA | FFT  |
|---------------|-----------|------|
| 0,85875      | 0,3511    | 0,85 |


Presentando un OEE de 25%.

Como puede observar, gran parte del tiempo que la maquinaria estaba funcionando era consumido por las fallas de los equipos, reduciendo la productividad de los mismos.



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


Con estos datos es posible entonces hacer el cálculo del OEE de la planta actualizada, para ello, asuminedo que la planta va operar en dos turnos de 8 horas cada uno de lunes a viernes, y asuminedo una tasa de calidad del 95% en nuestros productos, tenemos las siguientes consideraciones par la operación diaria de la plana:


| UNIDADES | T. DISPONIBLE | T. OPTVO | CALIDAD |
|----------|--------------|----------|---------|
| 640      | 57600       | 57444    | 0.95    |


Ahora, consignando la información de forma más precisa sobre cada etapa del proceso de producción, estos datos nos permitirán calcular el OEE de la fábrica más adelante:

| PROCESO      | REGISTRO | INYECCIÓN | LIJADO | DESBARBADO | PINTADO | ENSAMBLAJE | E. INDIVIDUAL | E. LOTES |
|-------------|---------|-----------|--------|------------|---------|------------|--------------|---------|
| **T. DE CICLO (s)** | 10  | 11        | 90     | 60         | 80      | 180        | 21           | 210     |
| **T. DISPONIBLE (s)** | 51840 | 54720     | 51840  | 54720      | 54720   | 48960      | 51840        | 54720   |
| **DISPONIBILIDAD** | 0.90 | 0.95      | 0.90   | 0.95       | 0.95    | 0.85       | 0.90         | 0.95    |

Con las siguientes ecuaciones:

![image](https://github.com/user-attachments/assets/257c9de8-171f-490b-b41b-4e3093b749f4)

![image](https://github.com/user-attachments/assets/7d1bdea3-95be-4e48-834b-da892a2c82b0)

![image](https://github.com/user-attachments/assets/5dfb9163-9b41-46dc-9f4c-175b50f9740b)

Reemplazando los datos de la tabla de consideraciones generales tenemos que:

| MÉTRICA        | VALOR      |
|---------------|------------|
| DISPONIBILIDAD | 0.92       |
| EFICIENCIA    | 0.875844301 |
| FTT          | 0.95       |

Con los datos de la tabla anterior, se puede hacer el cálculo del OEE de la propuesta de mejora de automatización, de esta forma, reemplazando en la ecuación:

![image](https://github.com/user-attachments/assets/44626dc9-6682-4d1b-8831-335584504c41)

Con ello, obtenemos que el OEE de la actualización es de 76%, lo cual es una mejora significativa partiendo de la situación inicial que tenía la empresa. Con esta distribución se alcanza una producción de 640 unidades diarias repartidas entre los juguetes del catálogo. La mayor o menor producción de uno u otro dependerá de la demanda del mercado en el momento de producción.


## VSM del proceso actual y el mejorado:

El proceso actual de la empresa presenta el siguiente Value Stream Mapping:

![image](https://github.com/user-attachments/assets/3715923b-83b5-4056-9ce9-cce61668e519)





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
