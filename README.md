# Capítulo II: Requirements Elicitation & Analysis

## 2.1. Competidores

El análisis del entorno competitivo de SmartCart se orienta a identificar soluciones digitales que asisten al consumidor en la planificación de compras minoristas, la gestión de despensas domésticas y la supervisión de presupuestos. Se han seleccionado tres competidores representativos del mercado: Bring!, Out of Milk y Listonic.

### 2.1.1. Análisis competitivo

A continuación, se presenta la matriz estructurada del Competitive Analysis Landscape:

| Criterio | SmartCart (Startup) | Bring! | Out of Milk | Listonic |
| :--- | :--- | :--- | :--- | :--- |
| **Overview** | Solución web SaaS para la planificación presupuestaria de compras, control de alacena y cálculo de costos en tiempo real. | Herramienta móvil y web orientada a la creación colaborativa de listas de mercado con enfoque visual en tarjetas. | Aplicación de gestión dual de listas de compras e inventario físico de despensa en el hogar. | Plataforma para compras compartidas con sincronización instantánea y listas recurrentes. |
| **Perfil de Ventaja Competitiva** | Estimación automatizada del costo total previo al pago en caja y clasificación secuencial por pasillos de tienda. | Interfaz estructurada mediante tarjetas visuales e integración directa con asistentes virtuales (Alexa, Google). | Control conjunto de lista de compras y stock actual mediante lector de códigos de barra. | Elevada velocidad de sincronización multiusuario y recomendaciones automáticas de insumos. |
| **Valor ofrecido a los clientes** | Prevención de sobregastos en caja y ahorro de tiempo durante el desplazamiento en el establecimiento. | Selección intuitiva y rápida de productos sin requerir digitación manual extensa. | Disminución de compras repetidas al verificar previamente las existencias en el hogar. | Coordinación ágil del abastecimiento entre varios integrantes de la familia. |
| **Mercado objetivo** | Consumidores independientes, parejas jóvenes y jefes de hogar en zonas urbanas (20-45 años). | Familias y hogares compartidos familiarizados con herramientas de domótica y asistentes de voz. | Administradores del hogar que priorizan el inventario riguroso de alimentos básicos. | Usuarios que demandan agilidad para tachar artículos comprados durante su visita a la tienda. |
| **Perfil de Marketing** | Estrategia de contenidos sobre finanzas del hogar, posicionamiento web (SEO) y alianzas con comercios locales. | Campañas masivas en redes sociales y recetas patrocinadas por marcas de consumo masivo (FMCG). | Posicionamiento orgánico en tiendas de aplicaciones (ASO) y monetización por anuncios display. | Publicidad digital en motores de búsqueda y captación mediante planes grupales familiares. |
| **Perfil de Producto** | Web Application responsiva desarrollada en Angular con servicios RESTful backend en Spring Boot. | Aplicación móvil multiplataforma y portal web con catálogo precargado de productos. | Aplicación móvil centrada en texto, escaneo de códigos de barra y notas. | Aplicación web y móvil ligera orientada al rendimiento y bajo consumo de datos móviles. |
| **Precios y Costos** | Modelo Freemium: Acceso base gratuito; suscripción mensual ($4.99/mes) para analítica avanzada. | Acceso gratuito sustentado en banners publicitarios y productos comerciales patrocinados. | Gratuito con anuncios visuales continuos; pago único opcional para remover la publicidad. | Gratuito con anuncios comerciales; membresía periódica para habilitar modo prémium. |
| **Canales de distribución** | Plataforma Web accesible vía navegadores modernos (Desktop/Mobile) y Landing Page oficial. | Tiendas Google Play Store, App Store y entorno web. | Tiendas Google Play Store y App Store. | Tiendas Google Play Store, App Store y entorno web. |
| **SWOT - Fortalezas** | Arquitectura orientada a servicios escalable, enfoque en ahorro de dinero y diseño inclusivo. | Notoriedad de marca internacional, catálogo visual consolidado y convenios corporativos. | Lector de código de barras para inventariar y panel dual de compras/alacena. | Desempeño veloz, facilidad de aprendizaje y sincronización en la nube estable. |
| **SWOT - Debilidades** | Solución en fase inicial de validación y base de datos de comercios en estructuración. | Nula capacidad para auditar límites presupuestarios monetarios en tiempo real. | Diseño de interfaz visual desactualizado y saturación de anuncios en modalidad gratuita. | Inexistencia de comparativa de costos entre cadenas minoristas competidoras. |
| **SWOT - Oportunidades** | Interés creciente de la población por cuidar el presupuesto ante el alza de costos de alimentos. | Incorporación de compras directas mediante pasarelas de comercio electrónico. | Modernización visual orientada a evitar desperdicio de alimentos e impacto ambiental. | Alianzas estratégicas con billeteras electrónicas locales y programas de fidelidad. |
| **SWOT - Amenazas** | Módulos de listas de compras integrados nativamente por las propias cadenas de supermercados. | Pérdida de interés de usuarios debido al exceso de marcas promocionadas en pantalla. | Desplazamiento hacia soluciones digitales más dinámicas y ligeras. | Empleo extendido de aplicaciones de notas genéricas integradas en el teléfono móvil. |

### 2.1.2. Estrategias y tácticas frente a competidores

* **Frente a Bring!:** Enfatizar la ventaja financiera de SmartCart, posicionándolo como una herramienta que no solo lista nombres, sino que estima el total a pagar y alerta preventivamente si se sobrepasa el presupuesto fijado.
* **Frente a Out of Milk:** Desarrollar una experiencia de usuario limpia, moderna y accesible sustentada en Material Design, erradicando la fatiga provocada por anuncios intrusivos.
* **Frente a Listonic:** Integrar la clasificación de insumos por categorías de pasillo e inventario de despensa en una sola vista, impidiendo que el consumidor dependa de herramientas separadas para abastecer su hogar.

## 2.2. Entrevistas

### 2.2.1. Diseño de entrevistas

Las entrevistas fueron diseñadas mediante un enfoque semiestructurado, incorporando preguntas demográficas, de hábitos de compra, gestión presupuestaria y experiencia digital, diferenciadas para dos segmentos objetivo: Compradores Independientes (Segmento 1) y Administradores del Hogar Familiar (Segmento 2).

**Preguntas Principales (Segmento 1 - Compradores Independientes):**
1. ¿Con qué periodicidad sueles realizar las compras de alimentos y artículos de primera necesidad para tu hogar?
2. ¿Qué herramientas o métodos utilizas habitualmente para elaborar y revisar tu lista de compras?
3. ¿Estableces un límite monetario previo a la compra y de qué forma controlas no excederte dentro de la tienda?
4. ¿Cuáles consideras que son los principales motivos de demora, confusión o frustración al recorrer el supermercado?
5. ¿Alguna vez has comprado productos duplicados o innecesarios por no recordar con exactitud qué tenías en la despensa?
6. ¿Estarías dispuesto a utilizar una plataforma web que organice tus compras por pasillos y calcule tu presupuesto en tiempo real?

**Preguntas Principales (Segmento 2 - Administradores del Hogar Familiar):**
1. ¿Cómo coordinas y recopilas las solicitudes de compras cuando intervienen múltiples integrantes de la familia?
2. ¿Qué porcentaje aproximado de los ingresos del hogar se destina mensualmente al abastecimiento de despensa y alimentos?
3. ¿Cómo verificas qué productos están próximos a agotarse o vencer en tu alacena antes de ir a comprar?
4. ¿Qué tan importante es para tu economía doméstica comparar precios y ofertas entre distintos supermercados?
5. ¿Qué dificultades experimentas al momento de consolidar y pagar la cuenta total de compras en caja?
6. ¿Qué beneficios clave buscarías en una aplicación web diseñada para el control integral de compras del hogar?

### 2.2.2. Registro de entrevistas

#### Segmento 1: Compradores Independientes

* **Entrevista 1:**
  * **Nombre y Apellidos:** Fernando Justiniano Vega
  * **Edad:** 24 años
  * **Distrito:** San Miguel, Lima
  * **Ocupación:** Ingeniero de Software / Profesional Independiente
  * **Duración:** 04:25
  * **Enlace de Video (Microsoft Stream):** [Ver Entrevista 1 - Fernando Justiniano](https://web.microsoftstream.com/)
  * **Resumen descriptivo:** Fernando vive de manera independiente y realiza compras cada diez o quince días. Utiliza principalmente una nota rápida en su teléfono celular, pero señala que le resulta molesto porque no tiene un orden claro. Admite que con frecuencia compra productos repetidos (como fideos, salsas o condimentos) debido a que no revisa su despensa antes de salir por falta de tiempo. Sobre el presupuesto, intenta fijar un monto aproximado con tarjeta o billeteras digitales, pero suele enterarse del monto real exacto recién en la caja registradora. Afirma que pierde bastante tiempo dando vueltas entre pasillos buscando artículos específicos y considera que una plataforma web que agrupe su lista por zonas del supermercado y le muestre el costo acumulado le ahorraría dinero y tiempo valioso.

![Screenshot Entrevista 1 - Fernando Justiniano](assets/deployment/appandroid/img.png)
*(Reemplazar la imagen por la captura real de la entrevista en video con Fernando ante cámara)*

* **Entrevista 2:**
  * **Nombre y Apellidos:** Andrea Valdivia Cruz `[Dato de muestra - Reemplazar por compañero]`
  * **Edad:** 27 años
  * **Distrito:** Miraflores, Lima
  * **Ocupación:** Diseñadora UX
  * **Duración:** 03:50
  * **Enlace de Video (Microsoft Stream):** [Ver Entrevista 2](https://web.microsoftstream.com/)
  * **Resumen descriptivo:** Realiza compras semanales tras salir del trabajo; fija un presupuesto estricto en su mente pero le frustra desorientarse en pasillos desconocidos; compra por conveniencia y rapidez.

* **Entrevista 3:**
  * **Nombre y Apellidos:** Gonzalo Prieto Sánchez `[Dato de muestra - Reemplazar por compañero]`
  * **Edad:** 25 años
  * **Distrito:** Surquillo, Lima
  * **Ocupación:** Analista Junior
  * **Duración:** 04:10
  * **Enlace de Video (Microsoft Stream):** [Ver Entrevista 3](https://web.microsoftstream.com/)
  * **Resumen descriptivo:** Vive solo y reconoce compras impulsivas; carece de registro de stock doméstico y desearía una herramienta web accesible sin descargas pesadas que le alerte topes de gasto.

---

#### Segmento 2: Administradores del Hogar Familiar

* **Entrevista 4:**
  * **Nombre y Apellidos:** Camila Villavicencio Ramos `[Dato de muestra - Reemplazar por compañero]`
  * **Edad:** 37 años
  * **Distrito:** Magdalena del Mar, Lima
  * **Ocupación:** Coordinadora Administrativa / Madre de familia
  * **Duración:** 05:05
  * **Enlace de Video (Microsoft Stream):** [Ver Entrevista 4](https://web.microsoftstream.com/)
  * **Resumen descriptivo:** Centraliza las compras de su hogar usando mensajes de WhatsApp con su familia; le molesta olvidar insumos esenciales o encontrar alimentos vencidos al fondo de la alacena; compara ofertas de limpieza y abarrotes entre distintas tiendas.

* **Entrevista 5:**
  * **Nombre y Apellidos:** Javier Morales Rivas `[Dato de muestra - Reemplazar por compañero]`
  * **Edad:** 42 años
  * **Distrito:** Jesús María, Lima
  * **Ocupación:** Contador / Padre de familia
  * **Duración:** 04:40
  * **Enlace de Video (Microsoft Stream):** [Ver Entrevista 5](https://web.microsoftstream.com/)
  * **Resumen descriptivo:** Hace compras mensuales grandes y reposiciones semanales de frescos; revisa la despensa manualmente en papel; busca optimizar el gasto familiar total para no sobrepasar el 35% de sus ingresos del mes.

### 2.2.3. Análisis de entrevistas

A partir del análisis cualitativo y cuantitativo de las respuestas recopiladas en las entrevistas registradas para ambos segmentos, se determinaron los siguientes patrones estadísticos representativos:

* **Empleo de medios no estructurados (80%):** 4 de cada 5 entrevistados (80%) elabora sus listas mediante chats de mensajería o blocs de notas genéricos, métodos que no previenen olvidos ni organizan los artículos de forma eficiente.
* **Incidencia de compras repetidas por falta de inventario (60%):** El 60% de los participantes (incluyendo a los compradores independientes como Fernando) confirmó haber comprado artículos duplicados al menos una vez al mes por no verificar con certeza las existencias en casa.
* **Monitoreo presupuestario preventivo como necesidad crítica (80%):** El 100% de los administradores familiares y el 66% de compradores independientes manifestaron preocupación por el aumento de precios en caja y la necesidad de conocer el monto acumulado antes de pagar.
* **Demoras por desorganización de pasillos (80%):** 4 de los 5 entrevistados señalaron que el recorrido desordenado dentro de locales grandes es su principal fuente de pérdida de tiempo y fatiga en horas punta.
* **Preferencia por soluciones Web modernas (100%):** La totalidad de la muestra cuenta con acceso diario a navegadores web en ordenadores y teléfonos inteligentes, expresando apertura total al uso de una plataforma web fluida que no demande almacenamiento local obligatorio.