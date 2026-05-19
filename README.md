# Informe Técnico de Auditoría

Página Web a analizar [**https://www.mk2cines.es/es/nervion-plaza-sevilla/**](https://www.mk2cines.es/es/nervion-plaza-sevilla/) 

<img width="484" height="487" alt="image" src="https://github.com/user-attachments/assets/555ee654-60ef-4687-ab8b-1b5188d040ee" />

## Fase 1: Inventario y Dimensión Ambiental (A)
**1. Medición inicial.**
<img width="1293" height="254" alt="image" src="https://github.com/user-attachments/assets/7ef0a2c0-1ac4-4f4b-98f8-c94f5d6cbe19" />
- Es más contaminante que el 98% de las páginas a nivel global
- Tiene una pesima optimizacion 
- Genera hasta un 3,06g de CO2e por visita
- Basado en 5000 visitas a la página al mes de promedio en una página web, esta web produce 184 kg de carbono cada año 

Para conseguir estos datos usamos páginas de análisis ecológico como: [Website Carbon Calculator](https://www.websitecarbon.com/) y  [Website emissions](https://websiteemissions.com/)


Hicimos la division de permiso en una sola tabla dividida en roles/sectores, manteniendo el Principio de Mínimo Privilegio para garantizar la seguridad al usuario. 

**2.Identificación de Bloatware**
| Nombre del Archivo | tipo de archivo | tamaño | 
 | :---- | :---- | :---- | 
 | https://www.mk2cines.es/data/fotos/captura-de-pantalla-2026-05-06-a-la69.png |  png  | 1,64 MB |
 | https://www.mk2cines.es/data/fotos/captura-de-pantalla-2026-05-06-a-la.png | png  |  1,48 MB |  
 |  https://www.mk2cines.es/data/fotos/tadc-poster-2x3-es-4-7jun10.jpg|  jpeg | 1,35 MB  |  
 
Para conseguir estas medidas se ha usado la herramienta de desarrollador del navegador Firefox,
ya que otras herramientas como la de Chrome no mostraba el tamaño de los archivos al estar guardado en la caché
<img width="1189" height="133" alt="image" src="https://github.com/user-attachments/assets/e0d10960-4d93-4315-91f9-9eee2296f63d" />

## Fase 2: Dimensión Social y Equidad (S)

## Fase 3: Dimensión de Gobernanza y Ética (G)
### **Trasparencia**
La web tiene un menú con cookies que te permite Rechazar y Aceptar, o configurarlas. La página avisa que el usuario puede configurar o rechazar las cookies que quiere que se presenten. Además de como siempre, asegurar la privacidad del usuario y que se usarán para un buen uso

Aun con eso, el mensaje insiste en que primero se acepten y después se configure para gestionar el consentimiento.
<img width="670" height="137" alt="image" src="https://github.com/user-attachments/assets/bd6b1bd4-d091-41fd-a569-89a50ea68f9a" />

## Fase 4: Propuesta de Refactorización (Green Coding)
### **Optimización de activos**

- Respecto a las imágenes, sería muy beneficioso que fueran refactorizadas para pasar ser a formato WebP ya que es un formato muy estandarizado,
  sencillo y con el que se reduciría el tamaño alrededor de un 30% respecto a los actuales usados.
  
- En adición, sería recomendable implementar el lazy loading. Al tener tantas imágenes esto reduciría el 
procesamiento y uso de red inicial que hay que hacer al descargar todas las imágenes al principio.
