# Segmentación de empresas en el uso del factoring en Perú (2024)

## Descripción del proyecto
Este proyecto aplica técnicas de clustering y visualización interactiva para segmentar empresas proveedoras que utilizaron factoring en Perú durante 2024. El objetivo es identificar perfiles operativos diferenciados y generar insumos accionables para la gestión estratégica de clientes por parte de entidades financieras y formuladores de políticas públicas.

## Objetivos
- General: Segmentar empresas proveedoras de factoring en Perú mediante clustering y visualización interactiva.

- Específicos:

      1. Realizar análisis exploratorio multivariado y pruebas de estabilidad para seleccionar variables óptimas.
      
      2. Aplicar y comparar algoritmos de agrupamiento (K-means, GMM, jerárquico) con métricas internas (Silhouette, Davies-Bouldin).
      
      3. Derivar indicadores interpretables como monto promedio por factura, monto por trabajador e intensidad de uso para caracterizar cada clúster.

## Dataset
- Fuente: Datos Abiertos del Ministerio de la Producción (datosabiertos.gob.pe in Bing)

- Observaciones: 28,781 registros

- Variables: 14 columnas (9 categóricas, 3 numéricas, 2 fechas)

- Principales atributos:

      ciiu, descripcion_ciiu, sector
      
      ubigeo, departamento, provincia, distrito
      
      tamano_emp, facturas_negociadas, monto_negociado_soles, cantidad_trabajadores

## Metodología
### EDA (Exploratory Data Analysis)

- Histogramas y distribuciones de variables numéricas y categóricas.

- Identificación de redundancias (ej. ciiu vs descripcion_ciiu).

- Eliminación de variables poco relevantes (id_factoring, año, fec_creacion).

### Preprocesamiento

- Escalado de variables numéricas.

- Codificación de variables categóricas.

- Verificación de multicolinealidad (VIF).

### Clustering

- Algoritmos aplicados: K-means, Gaussian Mixture Models (GMM), Jerárquico.

- Validación con métricas internas: Silhouette, Davies-Bouldin.

- Selección final: K-means con 4 clústeres.

### Interpretación

- Indicadores derivados: monto promedio por factura, monto por trabajador, intensidad de uso.

- Visualizaciones: heatmaps de Z-scores, silhouette plots, pairplots.

- Ejemplares cercanos al centroide para storytelling.

## Resultados
- Clúster 1: Empresas grandes, centrales, con alta facturación (robusto).

- Clúster 2: Empresas pequeñas/medianas, localizadas en ciertos departamentos, menor capacidad económica pero cohesión alta.

- Clúster 0: Empresas pequeñas y periféricas, baja cohesión.

- Clúster 3: Definidas por sector económico (CIIU), menor consistencia interna.

## Reflexión crítica
- Limitaciones: ausencia de datos cualitativos, sesgos geográficos (Lima concentra 80% del factoring).

- Ética: segmentación debe promover inclusión financiera, no exclusión.

- Valor para el negocio:

      - Estrategias diferenciadas por perfil.
      
      - Reducción de riesgos en entidades de factoring.
      
      - Insumos para políticas públicas focalizadas.

## Deployment conceptual
- Integración: modelo en sistemas de gestión de clientes (CRM).

- Monitoreo: métricas internas (Silhouette, distribución de clústeres, indicadores económicos).

- Actualización: reentrenamiento anual + revisión semestral.

- Roadmap: validación inicial → dashboards interactivos → retroalimentación cualitativa → optimización algorítmica → escalamiento estratégico.

## Autor
Bryan Villasante López – Proyecto Integrador de Saberes (2025)

Universidad: TECSUP – Big Data y Ciencia de Datos
