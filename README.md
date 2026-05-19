# Informe Técnico de Auditoría

Página Web a analizar [**https://www.mk2cines.es/es/nervion-plaza-sevilla/**](https://www.mk2cines.es/es/nervion-plaza-sevilla/) 

<img width="484" height="487" alt="image" src="https://github.com/user-attachments/assets/555ee654-60ef-4687-ab8b-1b5188d040ee" />

## Fase 1: Inventario y Dimensión Ambiental (A)
### **Medición inicial.**
<img width="1293" height="254" alt="image" src="https://github.com/user-attachments/assets/7ef0a2c0-1ac4-4f4b-98f8-c94f5d6cbe19" />

-  Es más contaminante que el 98% de las páginas a nivel global
  
-  Tiene una pesima optimizacion
  
-  Genera hasta un 3,06g de CO2e por visita
  
-  Basado en 5000 visitas a la página al mes de promedio en una página web, esta web produce 184 kg de carbono cada año 

Para conseguir estos datos usamos páginas de análisis ecológico como: [Website Carbon Calculator](https://www.websitecarbon.com/) y  [Website emissions](https://websiteemissions.com/) <br> Hicimos la division de permiso en una sola tabla dividida en roles/sectores, manteniendo el Principio de Mínimo Privilegio para garantizar la seguridad al usuario. 

### **Identificación de Bloatware**
| Nombre del Archivo | tipo de archivo | tamaño | 
 | :---- | :---- | :---- | 
 | https://www.mk2cines.es/data/fotos/captura-de-pantalla-2026-05-06-a-la69.png |  png  | 1,64 MB |
 | https://www.mk2cines.es/data/fotos/captura-de-pantalla-2026-05-06-a-la.png | png  |  1,48 MB |  
 |  https://www.mk2cines.es/data/fotos/tadc-poster-2x3-es-4-7jun10.jpg|  jpeg | 1,35 MB  |  
 
-  Para conseguir estas medidas se ha usado la herramienta de desarrollador del navegador Firefox,
ya que otras herramientas como la de Chrome no mostraba el tamaño de los archivos al estar guardado en la caché
<img width="1189" height="133" alt="image" src="https://github.com/user-attachments/assets/e0d10960-4d93-4315-91f9-9eee2296f63d" />

## Fase 2: Dimensión Social y Equidad (S)
### Test de Accesibilidad
Usando la herramienta de chrome *“Lighthouse“*,sabemos que la accesibilidad de la página es de 62
<p align="center">
<img width="202" height="143" alt="image" src="https://github.com/user-attachments/assets/7c48e1ef-caef-4fba-b5b0-a8128ded1e1a" />
 </p>
 
### Identificación de barreras

-  Las áreas táctiles no tienen un tamaño o un espaciado suficientes: Disponer de objetivos de tamaño suficiente (o en su defecto, de suficiente espacio entre ellos) puede ayudar a todos los usuarios que puedan tener dificultades para apuntar o utilizar controles pequeños con seguridad
-  Los elementos de imagen no tienen ningún atributo [alt] : los usuarios ciegos deben poder obtener tanta información del texto alternativo como un usuario vidente obtiene de la imagen misma. El texto alternativo debe indicar la intención, el propósito y el significado de la imagen. [2]

## Fase 3: Dimensión de Gobernanza y Ética (G)
### **Trasparencia**
<p align="justify">
 
-  La web tiene un menú con cookies que te permite Rechazar y Aceptar, o configurarlas. La página avisa que el usuario puede configurar o rechazar las cookies que quiere que se presenten. Además de como siempre, asegurar la privacidad del usuario y que se usarán para un buen uso. Aun con eso, el mensaje insiste en que primero se acepten y después se configure para gestionar el consentimiento.
</p>
<p align="center">
<img width="670" height="150" alt="image" src="https://github.com/user-attachments/assets/bd6b1bd4-d091-41fd-a569-89a50ea68f9a" />
</p>

### **Datos innecesarios**
<p align="justify">
 
-  El formulario se realiza en Newsletter y solo solicita el correo electrónico y un nombre por el cual dirigirse al usuario, además del consentimiento para que se les envíen correos con publicidad, No pide datos personales más que esos. Además de esto se pide aceptar los términos y condiciones y la política de la empresa, bastante adecuado para una empresa de cines
 </p>
<p align="center">
<img width="500" height="350" alt="image" src="https://github.com/user-attachments/assets/d44b7364-50f8-4a81-b17d-c009ddb29b7b" />
</p>

## Fase 4: Propuesta de Refactorización (Green Coding)
### Optimización de activos

- Respecto a las imágenes, sería muy beneficioso que fueran refactorizadas para pasar ser a formato WebP ya que es un formato muy estandarizado,
  sencillo y con el que se reduciría el tamaño alrededor de un 30% respecto a los actuales usados.
  
- En adición, sería recomendable implementar el lazy loading. Al tener tantas imágenes esto reduciría el 
procesamiento y uso de red inicial que hay que hacer al descargar todas las imágenes al principio.

### Reducción de peticiones

-  Se han podido identificar la librerías que requieren de la biblioteca jQuery de Javascript que se podría sustituir por alternativas más modernas y ligeras. Además se ha identificado el uso de Bootstrap que con un poco de trabajo y adaptación podría ser sustituido por CSS.

### Reflexión sobre la Paradoja de Jevons
-  Teniendo en cuenta la Paradoja de Jevons y lo que significa, la web tendrá mucho tráfico, así que tanto sí es por la implementación de publicidad en la web y su monetización o el crecimiento del negocio, se alcanzarán beneficios económicos. <br> <br> Ahora, referenciando otra expresión, “*un gran poder conlleva una responsabilidad*”, así que con la responsabilidad y nuestra conciencia respecto a la sostenibilidad lo más beneficioso sería invertir esas ganancias en cosas como servidores de alojamiento más sostenibles, buenos profesionales que actualicen la página web con las últimas tecnologías más eficientes y en concienciar a la empresa y los trabajadores para que se adopten medidas y se tomen decisiones responsables sosteniblemente en todos los aspectos que la rodean.

## Referencias
[1]
“Axe rules”, Dequeuniversity.com. [En línea]. Disponible en: https://dequeuniversity.com/rules/axe/4.11/target-size. [Consultado: 19-may-2026].

[2]
“Axe rules”, Dequeuniversity.com. [En línea]. Disponible en: https://dequeuniversity.com/rules/axe/4.11/image-alt. [Consultado: 19-may-2026].


