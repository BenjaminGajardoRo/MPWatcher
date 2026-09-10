# MPWatcher
# Agente de Monitoreo Inteligente para Mercado Público

Sistema automatizado de exploración, clasificación mediante Inteligencia Artificial y notificación oportuna de licitaciones de Mercado Público orientado a PYMEs en Chile.

---

## Contexto y Problemática

En Chile, **Mercado Público** es la plataforma oficial donde el Estado publica más de **150 mil licitaciones** y **500 mil órdenes de compra** al año. El 83% de los proveedores registrados son micro, pequeñas y medianas empresas. Además, modalidades de compra rápida como **Compra Ágil** crecieron un 81,5% en transacciones durante 2025.

### El Problema
La plataforma no cuenta con un sistema de notificación proactiva:
* Los proveedores dedican entre **2 y 4 horas semanales** a buscar manualmente procesos relevantes.
* En modalidades como Compra Ágil (donde se adjudica el mismo día o al día siguiente), esta demora provoca la **pérdida directa de oportunidades de negocio**.

### La Solución: MPWatcher
MPWatcher es un agente de software que monitorea automáticamente las publicaciones, aplica inteligencia artificial para filtrar oportunidades según el perfil de cada PYME y notifica oportunamente por correo electrónico.

---

## Arquitectura del Sistema

El sistema está organizado en **4 módulos principales** sobre una arquitectura orientada a la nube:

1. **Ingesta de Datos**: Consulta periódicamente la API oficial de Mercado Público y complementa la información extrayendo datos desde bases de licitación en formato PDF.
2. **Procesamiento con IA**: Utiliza un modelo de lenguaje (LLM) para analizar, clasificar y resumir el contenido de cada licitación en tiempo real.
3. **Base de Datos**: Almacena perfiles de usuario, criterios de búsqueda, historial de licitaciones y registros de alertas enviadas.
4. **Notificaciones**: Genera alertas personalizadas por correo electrónico (y opcionalmente otros canales) cuando se detectan oportunidades afines.
