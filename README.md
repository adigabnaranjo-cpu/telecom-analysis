# telecom-analysis
📊 Análisis Estadístico y Segmentación de Clientes – ConnectaTel

🎯 Objetivo del Proyecto

Analizar el comportamiento de consumo y el perfil demográfico de los clientes de la empresa de telecomunicaciones ConnectaTel, con el fin de identificar patrones de uso, detectar usuarios intensivos (heavy users), evaluar el rendimiento de los planes actuales (Básico vs. Premium) y generar recomendaciones accionables de segmentación, retención y upselling para el negocio.

📁 Datasets Utilizados

El análisis integra dos fuentes de datos principales:

users (4,000 registros): Contiene la información demográfica y contractual de los clientes:

user_id: Identificador único del cliente.

first_name, last_name: Nombre y apellido.

age: Edad del usuario.

city: Ciudad de residencia.

reg_date: Fecha de registro en la plataforma.

plan: Tipo de plan contratado (Basico o Premium).

churn_date: Fecha de cancelación del servicio (NaN si el usuario sigue activo).

usage (40,000 registros): Registra el historial de actividad de llamadas y mensajes:

id: Identificador único del evento.

user_id: Identificador del usuario que realizó la actividad.

type: Tipo de evento (call o message).

date: Fecha del evento.

duration: Duración en minutos (aplica a llamadas).

length: Longitud en caracteres (aplica a mensajes).

🔄 Etapas del Análisis Realizadas

Exploración y Diagnóstico Inicial: Inspección de tipos de datos, estadísticas descriptivas y detección de valores faltantes (NaN) y valores sentinela (-999.0 en edad y '?' en ciudad).

Limpieza y Estandarización: Conversión de valores sentinela a NaN, estandarización de formatos de fecha y validación de integridad referencial entre tablas.

Agregación e Integración de Datos: Agrupación de métricas de uso por usuario (cant_mensajes, cant_llamadas, cant_minutos_llamada) y cruce con la tabla de perfiles mediante LEFT JOIN, imputando con 0 los usuarios sin actividad registrada.

Análisis Exploratorio (EDA) y Detección de Outliers: Evaluación de distribuciones por plan, análisis de correlación entre edad y consumo, e identificación de valores atípicos mediante el rango intercuartílico (IQR).

Segmentación de Clientes y Visualización: Clasificación de la cartera por nivel de actividad (Bajo uso, Uso medio, Alto uso) y grupo etario (Joven, Adulto, Adulto Mayor) acompañada de gráficos de distribución.

Insight Ejecutivo: Traducción de los hallazgos estadísticos en oportunidades comerciales y recomendaciones estratégicas para la oferta de planes.

