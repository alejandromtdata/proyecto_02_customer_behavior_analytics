# PROYECTO CUSTOMER BEHAVIOR ANALYTICS 

## Contexto del problema

Una empresa digital (ficticia) basada en suscripción quiere entender:

- Quiénes son sus usuarios.
- Cómo utilizan la plataforma.
- Qué usuarios generan ingresos.
- Por qué algunos usuarios abandonan el servicio.

En este análisis buscamos transformar datos de uso y pagos en conclusiones que ayuden a mejorar la retención y los ingresos del producto.

## Enfoque general del proyecto

### Objetivo del proyecto

El objetivo del proyecto es analizar el comportamiento de usuarios y el rendimiento de ingresos de una plataforma digital, utilizando datos de usuarios, sesiones y transacciones, con el fin de identificar patrones de uso, métricas clave de negocio, factores de churn y oportunidades de crecimiento.

## Preguntas de negocio que buscamos responder

- ¿Qué tipo de usuarios utilizan la plataforma?
- ¿Qué usuarios abandonan antes el servicio?
- ¿Existen diferencias claras entre usuarios gratuitos y de pago?
- ¿Influye el canal de adquisición en la calidad del usuario?

Para el analisis disponemos de 4 archivos importados de la propia Web/App. 

1.  users.csv – Perfil, adquisición y ciclo de vida

Este archivo csv representa un usuario único de la plataforma y su estado a lo largo del tiempo.

De este analizamos: 

- Dimensión demográfica y de adquisición.

    - Distribución de usuarios por:

        País.

        Canal de adquisición.

        Dispositivo inicial.

        Plan contratado.

    - Edad y género.

- Ciclo de vida del usuario.

    - Evolución de registros en el tiempo.

    - Análisis de abandono de usuarios (churn), tanto a nivel general como por tipo de usuario.

    - Tiempo hasta churn.

    - Comparación de churn entre planes.

- Segmentación

    - Usuarios free vs paid

    - Impacto del canal de adquisición en:

        - Tipo de plan

        - Churn

    - Diferencias geográficas relevantes

- KPIs derivados

    - Total users

    - % churn

    - Avg lifetime (días)

    - Churn rate por cohort de signup

2. sessions.csv – Engagement y comportamiento

Este csv representa cada interacción (sesión) de un usuario con la plataforma.

Analizamos: 

- Actividad

    - Número de sesiones por usuario

    - Distribución de duración de sesiones

    - Páginas vistas por sesión

    - Usuarios muy activos vs usuarios casuales

- Comportamiento

    - Acciones principales más frecuentes

    - Diferencias de comportamiento por:

        - Plan

        - Dispositivo

        - Canal de tráfico

- Temporalidad

    - Actividad diaria / semanal / mensual

    - Relación entre frecuencia de uso y churn

- KPIs derivados

    - DAU / WAU / MAU

    - Sessions per user

    - Avg session duration

    - Engagement por segmento

3. transactions.csv – Monetización y revenue

Este csv representa cada evento de compra, pago o reembolso.

Analizamos:

- Ingresos

    - Revenue total (neto y bruto)

    - Revenue por:

        - Plan

        - Categoría de producto

        - País

        - Canal de adquisición (vía join con users)

- Monetización

    - ARPU y ARPPU

    - Distribución de precios

    - Impacto de descuentos

    - Peso de suscripciones vs addons

- Calidad del revenue

    - Refund rate

    - Chargeback rate

    - Revenue perdido por reembolsos

- Temporalidad

    - Revenue diario / mensual

    - Estacionalidad

    - Comparativa entre cohortes

- KPIs derivados

    - Total revenue

    - ARPU / ARPPU

    - Refund rate

    - Revenue per user

4. data_dictionary.csv – Soporte y gobernanza

Este archivo csv representa la documentación de los datos.

Su uso, derivara a obtener: 

- Referencia durante el EDA

- Validación de significado de columnas

### Relaciones entre tablas 

users.user_id
            ↳ sessions.user_id
                            ↳ transactions.user_id

A traves de la relación entre tablas nos permitirá:

- Analizar comportamiento antes/después de comprar

- Relacionar engagement con churn

- Medir valor por segmento

- Resultado esperado del proyecto

### Conclusiones del  análisis. 

El proyecto debe responder:

- ¿Qué tipo de usuarios generan más revenue?

- ¿Qué planes tienen mejor retención?

- ¿El engagement reduce el churn?

- ¿Qué canales traen usuarios de mayor valor?

- ¿Dónde se pierde dinero (refunds, churn temprano)?

Debe acabar con:

- Insights claros

- Recomendaciones accionables

- Visualizaciones bien explicadas



### Proyecto creado por Alejandromtdata con Python y VS Code.

📬 Contacto: alejandromtdata@outlook.es

💻 GitHub: https://github.com/alejandromtdata
