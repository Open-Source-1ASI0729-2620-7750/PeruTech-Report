<div align="center">

<img src="../assets/upc-logo.png" alt="UPC Logo" width="160"/>

# UNIVERSIDAD PERUANA DE CIENCIAS APLICADAS

## FACULTAD DE INGENIERÍA
### CARRERA DE INGENIERÍA DE SOFTWARE

<br>

**DESARROLLO DE APLICACIONES OPEN SOURCE**  
**CURSO:** 1ASI0729 | **NRC:** 7750

<br><br>

# INFORME DE TRABAJO FINAL (TB1)

**STARTUP:** PeruTech  
**PRODUCTO:** Preciazo  

<br>

**DOCENTE:**  
Bautista Ubillús, Efrain Ricardo

<br><br>

### RELACIÓN DE INTEGRANTES

| Código | Apellidos y Nombres |
| :---: | :--- |
| **U20221B756** | Becerra Durand, Sebastian Uriel |
| **u20241c101** | Capillo Lema, Mía Valentina |
| **U202124030** | Casós Torre, Miguel André |
| **U20231B331** | Miranda Romero, Sergio Luis |
| **U20221A525** | Pardo Chumpitazi, Kevin Patrick |

<br><br>

**Ciclo Académico 2026-02**  
**Lima, Septiembre de 2026**

</div>

<div style="page-break-before: always;"></div>

---

# Registro de Versiones del Informe

| Versión | Fecha | Autor | Descripción de modificación |
| :---: | :---: | :--- | :--- |
| **1.0** | 06/09/2026 | Capillo Lema, Mía Valentina | Creación inicial de la estructura del informe y lineamientos de diseño. |
| **1.1** | 18/09/2026 | Becerra Durand, Sebastian Uriel | Incorporación del registro de entrevistas al segmento de comerciantes minoristas en la sección 2.2.2. |
| **1.2** | 18/09/2026 | Miranda Romero, Sergio Luis | Especificación de requerimientos del Capítulo III (User Stories, Impact Mapping y Product Backlog). |
| **1.3** | 18/09/2026 | Casós Torre, Miguel André | Modelado de arquitectura de software, diagramas DDD y aportes al análisis de dominio. |
| **1.4** | 18/09/2026 | Capillo Lema, Mía Valentina | Desarrollo de Style Guidelines, Wireframes, Wireflows y Mockups de la aplicación web responsive. |
| **1.5** | 19/09/2026 | Pardo Chumpitazi, Kevin Patrick | Corrección y estandarización integral del Capítulo I (Startup Profile, Solution Profile y Lean UX Process). |
| **1.6** | 19/09/2026 | Pardo Chumpitazi, Kevin Patrick | Finalización, estandarización de nomenclatura y cierre del Capítulo II (Competidores, Needfinding y Event Storming). |
| **1.7** | 19/09/2026 | Pardo Chumpitazi, Kevin Patrick | Revisión de consistencia, formato técnico y trazabilidad en el Capítulo III. |
| **1.8** | 20/09/2026 | Pardo Chumpitazi, Kevin Patrick | Subsanación integral de observaciones de rúbrica: corrección de carátula formal UPC, salto de página reglamentario, actualización de enlaces multimedia y estandarización de rutas relativas. |
| **1.9** | 20/09/2026 | Equipo PeruTech | Ampliación de entrevistas a 3 por segmento en el Capítulo II, compleción de perfiles de equipo, corrección del Lean UX Canvas y eliminación de marcadores pendientes en el Capítulo V. |

<div style="page-break-before: always;"></div>

---

# Project Report Collaboration Insights

Para evidenciar la participación equitativa y la trazabilidad en la redacción de la documentación técnica del proyecto, el desarrollo del presente informe se gestionó de manera colaborativa a través del repositorio oficial de GitHub **PeruTech-Report**, aplicando flujo de ramas GitFlow y registro individual de aportes mediante commits descriptivos bajo la convención de Conventional Commits.

* **Repositorio Oficial de Documentación:** [https://github.com/Open-Source-1ASI0729-2620-7750/PeruTech-Report](https://github.com/Open-Source-1ASI0729-2620-7750/PeruTech-Report)

A continuación, se detalla la distribución de contribuciones y elaboración de artefactos técnicos por cada miembro del equipo durante el ciclo de desarrollo:

| Integrante | Capítulos y Secciones a Cargo | Rol Principal en Documentación |
| :--- | :--- | :--- |
| **Capillo Lema, Mía Valentina** | Capítulo I (Estilos iniciales), Capítulo IV (Style Guidelines, UI Design, Wireframes y Mockups). | Diseño de interfaces de usuario, arquitectura de información y prototipado visual. |
| **Pardo Chumpitazi, Kevin Patrick** | Capítulo I (Lean UX y Problem Statement), Capítulo V (Software Configuration, Backlog, Sprint 1 y Consolidación General). | Liderazgo técnico, control de versiones, estructuración del reporte y gestión de despliegue. |
| **Becerra Durand, Sebastian Uriel** | Capítulo II (Registro y análisis de entrevistas a comerciantes), Capítulo V (Soporte en maquetación de artefactos). | Elicitación de requerimientos empíricos, investigación de campo y documentación cualitativa. |
| **Miranda Romero, Sergio Luis** | Capítulo III (Especificación de requisitos: User Stories Gherkin, Impact Mapping y Product Backlog). | Modelado de requisitos funcionales y gestión ágil bajo el marco Scrum. |
| **Casós Torre, Miguel André** | Capítulo II (Event Storming Big Picture), Capítulo IV (Domain-Driven Design, C4 Model y Class Diagrams). | Modelado estratégico de dominio, arquitectura de software y diseño orientado a objetos. |

---

# Contenido

## Tabla de Contenidos

- [Student Outcome](#student-outcome)

- [Capítulo I: Introducción](#capítulo-i-introducción)
  - [1.1. Startup Profile](#11-startup-profile)
    - [1.1.1. Descripción de la Startup](#111-descripción-de-la-startup)
    - [1.1.2. Perfiles de integrantes del equipo](#112-perfiles-de-integrantes-del-equipo)
  - [1.2. Solution Profile](#12-solution-profile)
    - [1.2.1. Antecedentes y problemática](#121-antecedentes-y-problemática)
    - [1.2.2. Lean UX Process](#122-lean-ux-process)
      - [1.2.2.1. Lean UX Problem Statements](#1221-lean-ux-problem-statements)
      - [1.2.2.2. Lean UX Assumptions](#1222-lean-ux-assumptions)
      - [1.2.2.3. Lean UX Hypothesis Statements](#1223-lean-ux-hypothesis-statements)
      - [1.2.2.4. Lean UX Canvas](#1224-lean-ux-canvas)
  - [1.3. Segmentos objetivo](#13-segmentos-objetivo)

- [Capítulo II: Requirements Elicitation & Analysis](#capítulo-ii-requirements-elicitation--analysis)
  - [2.1. Competidores](#21-competidores)
    - [2.1.1. Análisis competitivo](#211-análisis-competitivo)
    - [2.1.2. Estrategias y tácticas frente a competidores](#212-estrategias-y-tácticas-frente-a-competidores)
  - [2.2. Entrevistas](#22-entrevistas)
    - [2.2.1. Diseño de entrevistas](#221-diseño-de-entrevistas)
    - [2.2.2. Registro de entrevistas](#222-registro-de-entrevistas)
    - [2.2.3. Análisis de entrevistas](#223-análisis-de-entrevistas)
  - [2.3. Needfinding](#23-needfinding)
    - [2.3.1. User Personas](#231-user-personas)
    - [2.3.2. User Task Matrix](#232-user-task-matrix)
    - [2.3.3. User Journey Mapping](#233-user-journey-mapping)
    - [2.3.4. Empathy Mapping](#234-empathy-mapping)
  - [2.4. Big Picture Event Storming](#24-big-picture-event-storming)
  - [2.5. Ubiquitous Language](#25-ubiquitous-language)

- [Capítulo III: Requirements Specification](#capítulo-iii-requirements-specification)
  - [3.1. User Stories](#31-user-stories)
  - [3.2. Impact Mapping](#32-impact-mapping)
  - [3.3. Product Backlog](#33-product-backlog)

- [Capítulo IV: Product Design](#capítulo-iv-product-design)
  - [4.1. Style Guidelines](#41-style-guidelines)
    - [4.1.1. General Style Guidelines](#411-general-style-guidelines)
    - [4.1.2. Web Style Guidelines](#412-web-style-guidelines)
  - [4.2. Information Architecture](#42-information-architecture)
    - [4.2.1. Organization Systems](#421-organization-systems)
    - [4.2.2. Labeling Systems](#422-labeling-systems)
    - [4.2.3. SEO Tags and Meta Tags](#423-seo-tags-and-meta-tags)
    - [4.2.4. Searching Systems](#424-searching-systems)
    - [4.2.5. Navigation Systems](#425-navigation-systems)
  - [4.3. Landing Page UI Design](#43-landing-page-ui-design)
    - [4.3.1. Landing Page Wireframe](#431-landing-page-wireframe)
    - [4.3.2. Landing Page Mock-up](#432-landing-page-mock-up)
  - [4.4. Web Applications UX/UI Design](#44-web-applications-uxui-design)
    - [4.4.1. Web Applications Wireframes](#441-web-applications-wireframes)
    - [4.4.2. Web Applications Wireflow Diagrams](#442-web-applications-wireflow-diagrams)
    - [4.4.3. Web Applications Mock-ups](#443-web-applications-mock-ups)
    - [4.4.4. Web Applications User Flow Diagrams](#444-web-applications-user-flow-diagrams)
  - [4.5. Web Applications Prototyping](#45-web-applications-prototyping)
  - [4.6. Domain-Driven Software Architecture](#46-domain-driven-software-architecture)
    - [4.6.1. Design-Level Event Storming](#461-design-level-event-storming)
    - [4.6.2. Software Architecture Context Diagram](#462-software-architecture-context-diagram)
    - [4.6.3. Software Architecture Container Diagrams](#463-software-architecture-container-diagrams)
    - [4.6.4. Software Architecture Components Diagrams](#464-software-architecture-components-diagrams)
  - [4.7. Software Object-Oriented Design](#47-software-object-oriented-design)
    - [4.7.1. Class Diagrams](#471-class-diagrams)
  - [4.8. Database Design](#48-database-design)
    - [4.8.1. Database Diagrams](#481-database-diagrams)

- [Capítulo V: Product Implementation, Validation & Deployment](#capítulo-v-product-implementation-validation--deployment)
  - [5.1. Software Configuration Management](#51-software-configuration-management)
    - [5.1.1. Software Development Environment Configuration](#511-software-development-environment-configuration)
    - [5.1.2. Source Code Management](#512-source-code-management)
    - [5.1.3. Source Code Style Guide & Conventions](#513-source-code-style-guide--conventions)
    - [5.1.4. Software Deployment Configuration](#514-software-deployment-configuration)
  - [5.2. Landing Page, Services & Applications Implementation](#52-landing-page-services--applications-implementation)
    - [5.2.1. Sprint 1](#521-sprint-1)
      - [5.2.1.1. Sprint Planning 1](#5211-sprint-planning-1)
      - [5.2.1.2. Aspect Leaders and Collaborators](#5212-aspect-leaders-and-collaborators)
      - [5.2.1.3. Sprint Backlog 1](#5213-sprint-backlog-1)
      - [5.2.1.4. Development Evidence for Sprint Review](#5214-development-evidence-for-sprint-review)
      - [5.2.1.5. Execution Evidence for Sprint Review](#5215-execution-evidence-for-sprint-review)
      - [5.2.1.6. Services Documentation Evidence for Sprint Review](#5216-services-documentation-evidence-for-sprint-review)
      - [5.2.1.7. Software Deployment Evidence for Sprint Review](#5217-software-deployment-evidence-for-sprint-review)
      - [5.2.1.8. Team Collaboration Insights during Sprint](#5218-team-collaboration-insights-during-sprint)
    - [5.2.2. Sprint 2](#522-sprint-2)
  - [5.3. Validation Interviews](#53-validation-interviews)
  - [5.4. Video About-the-Product](#54-video-about-the-product)

- [Conclusiones](#conclusiones)
- [Conclusiones y recomendaciones](#conclusiones-y-recomendaciones)
- [Video About-the-Team](#video-about-the-team)
- [Bibliografía](#bibliografía)
- [Anexos](#anexos)

---

# Student Outcome

El curso contribuye al cumplimiento del Student Outcome ABET:

**ABET – EAC - Student Outcome 3**

**Criterio:**  

*Capacidad de comunicarse efectivamente con un rango de audiencias. En el siguiente cuadro se describe las acciones realizadas y enunciados de conclusiones por parte del grupo, que permiten sustentar el haber alcanzado el logro del ABET – EAC - Student Outcome 3.*

| Criterio específico | Acciones realizadas | Conclusiones |
|---------------------|----------------------|--------------|
| **Comunica oralmente con efectividad a diferentes rangos de audiencia.** | **Capillo Lema, Mía Valentina** <br> *AV1:* Conduje las entrevistas cualitativas para el Segmento 1 de Compradores Independientes, adaptando el lenguaje técnico a términos cotidianos de consumo doméstico para obtener respuestas certeras sobre puntos de dolor y movilidad. <br><br> **Pardo Chumpitazi, Kevin Patrick** <br> *AV1:* Conduje las reuniones técnicas de sincronización y alineamiento de arquitectura de ramas bajo GitFlow, explicando las pautas de control de versiones y los criterios de entrega de software al equipo de desarrollo de forma asertiva. <br><br> **Becerra Durand, Sebastian Uriel** <br> *AV1:* Realicé la entrevista en profundidad a comerciantes minoristas (Segmento 2), adecuando las preguntas al contexto comercial de bodegas y minimarkets para identificar fricciones de inventario y captación de clientes. <br><br> **Casós Torre, Miguel André** <br> *AV1:* Presenté y sustenté ante el equipo los conceptos clave del Big Picture Event Storming y el diseño de Bounded Contexts, facilitando el consenso arquitectónico mediante explicaciones técnicas accesibles. <br><br> **Miranda Romero, Sergio Luis** <br> *AV1:* Participé en la exposición del alcance del producto y estructuré la narrativa metodológica para la sustentación del Product Backlog, comunicando las prioridades del negocio con claridad. | Durante el desarrollo del entregable AV1, los integrantes del equipo lograron transmitir conceptos técnicos y de negocio a diversas audiencias (usuarios finales, comerciantes y pares técnicos), adaptando el registro lingüístico y el tono de comunicación de manera efectiva. |
| **Comunica por escrito con efectividad a diferentes rangos de audiencia.** | **Capillo Lema, Mía Valentina** <br> *AV1:* Documenté las especificaciones de diseño visual en las Style Guidelines, elaborando descripciones claras para los artefactos de UI y los flujos de navegación (Wireflows y User Flows). <br><br> **Pardo Chumpitazi, Kevin Patrick** <br> *AV1:* Estandaricé la redacción del informe técnico maestro, formulé los supuestos del Lean UX Process articulados con el 5W+2H, y documenté la configuración del entorno de desarrollo y gestión de configuración con rigor técnico. <br><br> **Becerra Durand, Sebastian Uriel** <br> *AV1:* Redacté las bitácoras y resúmenes analíticos de las entrevistas a los usuarios, estructurando la evidencia empírica en variables cuantitativas y cualitativas de forma comprensible para cualquier lector. <br><br> **Casós Torre, Miguel André** <br> *AV1:* Documenté la arquitectura de software basada en DDD, elaborando las especificaciones textuales que acompañan a los diagramas C4 y Class Diagrams de cada Bounded Context con precisión formal. <br><br> **Miranda Romero, Sergio Luis** <br> *AV1:* Redacté las Historias de Usuario bajo el estándar Gherkin (Given-When-Then), proporcionando criterios de aceptación verificables para los desarrolladores y especificaciones de valor entendibles para los stakeholders. | El equipo consolidó una redacción técnica uniforme, precisa y coherente a lo largo de todo el documento, utilizando convenciones formales de ingeniería de software para documentar requerimientos, diseño arquitectónico y métricas del proyecto. |

---

# Capítulo I: Introducción

## 1.1. Startup Profile

### 1.1.1. Descripción de la Startup

PeruTech es una organización de innovación tecnológica integrada por estudiantes de la carrera de Ingeniería de Software de la Universidad Peruana de Ciencias Aplicadas (UPC). La iniciativa se enfoca en el diseño e implementación de soluciones digitales orientadas a mitigar fricciones urbanas cotidianas, principalmente aquellas vinculadas a la planificación financiera del hogar, la dispersión de precios minoristas y la optimización de traslados en la ciudad.

El proyecto central del equipo, denominado **Preciazo**, surge como una respuesta directa a las dificultades económicas que enfrentan las familias en Lima ante la variación continua de costos en la canasta básica. La plataforma otorga transparencia al mercado minorista al articular un motor comparativo de precios de bienes esenciales con la optimización algorítmica de rutas de desplazamiento. De esta forma, Preciazo asiste a los compradores independientes en la toma de decisiones de abastecimiento eficientes —maximizando su presupuesto y reduciendo tiempos de traslado—, mientras provee a los comercios minoristas un canal estructurado de visibilidad digital para posicionar sus catálogos.

*   **Misión:** Facilitar decisiones de abastecimiento eficientes mediante información verificable de precios, trazado inteligente de rutas comerciales y herramientas de presupuesto familiar, integrando en simultáneo a los comercios minoristas en un canal digital que potencie la exposición de sus ofertas locales.
*   **Visión:** Consolidar a Preciazo como la plataforma tecnológica referente a nivel nacional en la optimización de compras cotidianas y en la conexión digital directa y dinámica entre compradores independientes y comercios minoristas.

### 1.1.2. Perfiles de integrantes del equipo

<div align="left">
  <img src="../assets/foto-Mia.png" alt="Mía Valentina Capillo Lema" width="160">
</div>

**Capillo Lema, Mía Valentina**  
* **Código de estudiante:** u20241c101  
* **Carrera:** Ingeniería de Software  

Estudiante de la carrera de Ingeniería de Software en la Universidad Peruana de Ciencias Aplicadas (UPC). Cuenta con conocimientos en diseño centrado en el usuario, análisis cualitativo de requerimientos, prototipado interactivo en Figma y maquetación de interfaces web responsivas. Posee habilidades para estructurar la experiencia de usuario (UX) mediante mapas de empatía, arquetipos y flujos de interacción. En el equipo lidera el área de UI/UX Design, responsabilizándose de las guías de estilo visual, la arquitectura de información y la consistencia gráfica de las pantallas de la solución Preciazo.

<br>

<div align="left">
  <img src="../assets/Kevin.jpeg" alt="Kevin Patrick Pardo Chumpitazi" width="160">
</div>

**Pardo Chumpitazi, Kevin Patrick**  
* **Código de estudiante:** U20221A525  
* **Carrera:** Ingeniería de Software  

Estudiante de pregrado de la carrera de Ingeniería de Software en la Universidad Peruana de Ciencias Aplicadas (UPC). Cuenta con experiencia en desarrollo de software full-stack utilizando TypeScript, Angular, Java y Spring Boot bajo principios de Tactical Domain-Driven Design (DDD). Posee destrezas en gestión de bases de datos relacionales, administración de configuraciones de software, implementación de flujos GitFlow y adopción de Conventional Commits. En el proyecto desempeña el rol de Team Leader y líder técnico de Software Configuration Management, coordinando la integración continua del informe, la trazabilidad del repositorio y la arquitectura técnica del sistema.

<br>

<div align="left">
  <img src="../assets/sebastian.png" alt="Sebastian Uriel Becerra Durand" width="160">
</div>

**Becerra Durand, Sebastian Uriel**  
* **Código de estudiante:** U20221B756  
* **Carrera:** Ingeniería de Software  

Estudiante de Ingeniería de Software en la UPC enfocado en el ciclo de vida del desarrollo de software, modelado de persistencia de datos relacionales y consumo estructurado de APIs RESTful. Posee conocimientos en HTML5 semántico, CSS responsivo y scripting en JavaScript para validación de datos en cliente. Dentro del equipo, colabora en la elicitación de requerimientos empíricos mediante entrevistas a comerciantes minoristas, documentación de bitácoras y en la maquetación de componentes de captura de información y formularios de suscripción en la Landing Page.

<br>

<div align="left">
  <img src="../assets/Sergio Luis Miranda Romero.jpeg" alt="Sergio Luis Miranda Romero" width="160">
</div>

**Miranda Romero, Sergio Luis**  
* **Código de estudiante:** U20231B331  
* **Carrera:** Ingeniería de Software  

Estudiante de pregrado de la carrera de Ingeniería de Software en la UPC con certificación Scrum Fundamentals Certified (SFC). Posee conocimientos en lenguajes como C++, C# y JavaScript, así como en administración de bases de datos y accesibilidad web bajo lineamientos WCAG 2.1. Dentro del equipo, lidera la redacción y trazabilidad del Product Backlog, User Stories bajo sintaxis Gherkin, y asegura la auditoría de rendimiento y optimización de componentes visuales en la Landing Page.

<br>

<div align="left">
  <img src="../assets/fotomc.jpg" alt="Miguel André Casós Torre" width="160">
</div>

**Casós Torre, Miguel André**  
* **Código de estudiante:** U202124030  
* **Carrera:** Ingeniería de Software  

Estudiante de Ingeniería de Software en la UPC con especial interés en automatización de procesos, arquitectura de software y diseño orientado a dominios (DDD). Cuenta con competencias técnicas en Python, TypeScript, Docker y modelado arquitectónico mediante C4 Model. En el proyecto colabora activamente en la definición estratégica de Bounded Contexts, Class Diagrams, configuración del pipeline de despliegue continuo en GitHub Pages y desarrollo de módulos interactivos de preguntas frecuentes y soporte al usuario.

<br>

## 1.2. Solution Profile

### 1.2.1. Antecedentes y problemática

El análisis detallado del problema se sustenta en la técnica de interrogación **5W+2H**, permitiendo examinar todas las dimensiones del desafío urbano y comercial que aborda la solución:

* **Who? (¿Quién?):**
  * *Compradores Independientes:* Estudiantes universitarios, jóvenes profesionales y jefes de hogar de Lima Metropolitana (NSE B y C) con presupuestos definidos que buscan maximizar el rendimiento de sus ingresos y reducir el tiempo invertido en desplazamientos.
  * *Comerciantes Minoristas:* Propietarios y administradores de bodegas, minimarkets y puestos de mercado tradicionales que requieren visibilizar su catálogo de ofertas de cercanía y dinamizar la rotación de su inventario frente a grandes cadenas corporativas.
* **What? (¿Qué?):** La asimetría de precios en el mercado minorista y la ineficiencia logística en los recorridos de abastecimiento. Existe una dispersión notable entre las tarifas en góndola de los comercios físicos y la oferta digital, sumada a la ausencia de herramientas que calculen el costo consolidado de la canasta integrando el gasto y tiempo de movilidad urbana. Esta situación ocasiona sobrecostos financieros a los hogares e incrementos innecesarios en gastos de transporte.
* **Where? (¿Dónde?):** Sectores comerciales y distritos urbanos de alta densidad en Lima Metropolitana donde coexisten mercados tradicionales, supermercados de cadena y minimarkets de barrio.
* **When? (¿Cuándo?):** Durante las jornadas periódicas de compra familiar (semanales o quincenales) y en adquisiciones no planificadas de reposición inmediata, momentos en los cuales la variación imprevista de precios o el desabastecimiento generan fricciones operativas.
* **Why? (¿Por qué?):** Por la fragmentación tecnológica del canal minorista tradicional y la rigidez de los sistemas de inventario convencionales, los cuales impiden comunicar en tiempo real las rebajas de existencias a los consumidores cercanos.
* **How? (¿Cómo?):** Los compradores cotizan de manera empírica visitando múltiples tiendas a ciegas o asumiendo el primer precio que encuentran. Paralelamente, los comerciantes difunden ofertas mediante carteles físicos o pizarras en la entrada del local, limitando su alcance comercial a los transeúntes inmediatos.
* **How much? (¿Cuánto?):** En el contexto económico actual, los alimentos y bebidas representan entre el 35% y el 45% del gasto mensual de los hogares urbanos (INEI, 2026). Según el Banco Central de Reserva del Perú (BCRP, 2025), la volatilidad en productos de primera necesidad fuerza al 41% de los consumidores a fragmentar sus compras para capturar ofertas (Kantar Worldpanel, 2025). Desplazarse sin planificación puede incrementar hasta en un 20% el gasto en movilidad urbana por congestión vehicular y traslados infructuosos (Sabagh Nejad & Fazekas, 2022).

<br>

**Enunciado del problema:**  
Los compradores independientes de Lima Metropolitana afrontan barreras para identificar la alternativa de aprovisionamiento de menor costo consolidado, debido a la dispersión de información tarifaria y a la ausencia de herramientas integradas que consideren los tiempos y costos de desplazamiento entre establecimientos. Paralelamente, los comerciantes minoristas carecen de canales digitales centralizados para difundir su catálogo y promociones a compradores de proximidad, lo cual limita la visibilidad oportuna de sus ofertas.

**Objetivo general:**  
Diseñar, desarrollar y desplegar la plataforma web responsive **Preciazo**, permitiendo que los compradores independientes accedan instantáneamente desde el navegador de cualquier dispositivo móvil o de escritorio —sin requerir la descarga ni la instalación de un aplicativo móvil nativo— para consultar precios actualizados, consolidar presupuestos y trazar recorridos comerciales eficientes; proveyendo en simultáneo a los comerciantes minoristas una consola digital para registrar su oferta y dinamizar sus ventas locales.

**Restricciones de alcance:**  
* El acceso de los usuarios se realizará exclusivamente a través de navegadores web modernos mediante diseño responsive adaptativo, suprimiendo la necesidad de instalación en el almacenamiento del dispositivo.
* El alcance geográfico operativo se circunscribe a distritos comerciales de Lima Metropolitana.
* La exactitud de las listas de precios y la disponibilidad de productos se encuentra sujeta a la información suministrada por comerciantes inscritos y validaciones de la comunidad.
* La versión inicial del sistema no asegura la cobertura de la totalidad del universo comercial de la ciudad.
* La estructuración de rutas y la estimación de tiempos de viaje dependen de la disponibilidad operativa de servicios externos de geolocalización y mapas.
* La arquitectura se centra estrictamente en tecnologías web estandarizadas (HTML5, CSS3, TypeScript), descartando el empaquetado nativo durante esta fase de lanzamiento.

---

### 1.2.2. Lean UX Process

El proceso de Lean UX adoptado por PeruTech articula los hallazgos empíricos del análisis 5W+2H mediante un ciclo iterativo de formulación de supuestos (*Think*), diseño de artefactos e interfaces (*Make*) y validación con usuarios reales (*Check*). Este enfoque asegura la entrega de un Producto Mínimo Viable (MVP) enfocado en resolver fricciones reales de costo y traslado urbano.

#### 1.2.2.1. Lean UX Problem Statements

El ecosistema retail en Lima Metropolitana opera de manera fragmentada: las aplicaciones de delivery tradicionales cobran márgenes y comisiones elevadas (15% a 25%) que encarecen la canasta, mientras que las bodegas y comercios de barrio carecen de canales de difusión digital ágiles. Esta asimetría perjudica tanto a las familias que buscan optimizar su presupuesto como a los pequeños negocios locales que pierden ventas.

* **The current state of** the retail grocery ecosystem in Lima Metropolitan Area **has focused mainly on** centralized chain supermarket catalogs, unorganized physical price hunting, and on-demand delivery apps that impose severe markups (15% to 25%), neglecting in-person budget optimization and local neighborhood retail stores.
* **What existing products/services fail to address is** the lack of an integrated web platform that calculates the real consolidated cost of a multi-store shopping trip—factoring in shelf prices, transit expenses, and traffic times—while simultaneously providing small merchants with an accessible, low-friction channel to broadcast promotions and reduce inventory loss.
* **Our product/service will address this gap by** developing **Preciazo**, an instant-access responsive web platform that optimizes shopping baskets across proximate physical stores, calculates efficient multi-stop itineraries tailored to the user's transit mode, and equips local store managers with an agile dashboard to broadcast hyper-local discounts and attract store foot traffic.
* **Our initial focus will be** budget-conscious independent buyers (university students and household heads) and proximity retail merchants (bodegas and minimarkets) within high-density commercial districts of Lima.
* **We will know we are successful when we see** independent buyers regularly achieving documented net savings of at least 15% on their baskets using our route suggestions, and partner merchants reporting an increase of over 20% in physical customer visits.

#### 1.2.2.2. Lean UX Assumptions

##### Business Assumptions
1. **Creemos que los clientes tienen una necesidad imperativa de** transparentar la variación de precios minoristas y calcular si el ahorro de una oferta compensa el costo y tiempo de transporte urbano.
2. **Estas necesidades se pueden resolver mediante** la plataforma web responsive **Preciazo**, que integra comparativas de canasta multiestablecimiento y cálculo de rutas óptimas de compra.
3. **Nuestros clientes iniciales son** compradores independientes de 18 a 50 años (estudiantes y jefes de hogar) y comerciantes minoristas (bodegas y minimarkets) en Lima Metropolitana.
4. **El valor diferencial primordial que buscan los compradores es** maximizar su presupuesto y reducir traslados; para los comerciantes, es visibilizar sus productos y acelerar la rotación de inventario sin pagar comisiones onerosas.
5. **Monetizaremos el servicio mediante** planes de suscripción mensual de bajo costo para comercios aliados que deseen posicionamiento destacado y reportes analíticos de demanda zonal.
6. **Nuestra ventaja competitiva reside en** el algoritmo de consolidación de costo total real (precio de compra + sobrecosto logístico de movilidad) en compras presenciales.
7. **El riesgo comercial más crítico es** la lentitud inicial de los comerciantes para actualizar sus precios, el cual mitigaremos mediante un sistema colaborativo de validación comunitaria de góndola.

##### User Assumptions (Comprador Independiente & Comerciante)
1. **El comprador independiente** necesita conocer con certeza cuánto gastará antes de acudir a los establecimientos y cuál es el recorrido más corto para abastecerse.
2. **El comprador independiente** utiliza smartphones y herramientas digitales de pago (Yape/Plin), pero rechaza la obligación de instalar aplicaciones móviles pesadas para tareas cotidianas.
3. **El comerciante minorista** gestiona su negocio con libretas o herramientas básicas y necesita una consola web intuitiva que le permita publicar ofertas en menos de dos minutos.
4. **El comerciante minorista** teme perder márgenes comerciales ante las comisiones de plataformas de delivery y busca mecanismos directos para atraer transeúntes a su local.

##### Feature Assumptions
1. **Comparador de Canasta Multitienda:** Creemos que contrastar el costo consolidado de una lista de compras entre diferentes puntos de venta permitirá al usuario seleccionar la combinación comercial más barata.
2. **Optimizador de Rutas y Traslados:** Creemos que generar un itinerario secuencial de paradas según el medio de transporte seleccionado garantizará que el ahorro del ticket no se diluya en pasajes o tiempo.
3. **Módulo de Validación Colaborativa:** Creemos que permitir a los compradores reportar y validar discrepancias entre góndola y caja mantendrá fidedigna la base de datos de precios.
4. **Consola Ágil de Ofertas para Comercios:** Creemos que proveer un panel simplificado para publicar promociones relámpago e indicar productos agotados incrementará la afluencia presencial y evitará pérdidas por caducidad.

#### 1.2.2.3. Lean UX Hypothesis Statements

* **Hypothesis Statement 1 (Comparador de Canasta Multitienda):**  
  **Creemos que** incrementaremos la retención mensual de usuarios activos por encima del 40%  
  **si** los compradores independientes con presupuestos definidos  
  **obtienen** la proyección anticipada del costo total consolidado de su canasta antes de salir de casa  
  **mediante** un motor de comparación de precios multiestablecimiento en tiempo real.

* **Hypothesis Statement 2 (Optimizador de Rutas de Compra):**  
  **Creemos que** reduciremos en un 25% el tiempo promedio invertido por jornada de abastecimiento  
  **si** los consumidores urbanos expuestos a la congestión vehicular de Lima  
  **obtienen** un itinerario secuencial optimizado que integre paradas comerciales y modos de transporte  
  **mediante** un calculador dinámico de rutas de compra presencial con topes de distancia.

* **Hypothesis Statement 3 (Módulo de Validación Colaborativa):**  
  **Creemos que** alcanzaremos una exactitud de datos de góndola superior al 85%  
  **si** los miembros activos de la comunidad de compras  
  **obtienen** incentivos de reputación y fiabilidad al reportar discrepancias de precios en tienda  
  **mediante** un componente crowdsourced de confirmación y reporte de precios observados.

* **Hypothesis Statement 4 (Consola de Gestión y Promociones para Comercios):**  
  **Creemos que** reduciremos en un 20% la merma de productos perecibles y aumentaremos en un 60% la afluencia local  
  **si** los comerciantes de proximidad con stock de lenta rotación  
  **obtienen** un canal inmediato para anunciar promociones georreferenciadas a los vecinos de su sector  
  **mediante** una consola web ágil de publicación de ofertas relámpago y alertas de inventario.

#### 1.2.2.4. Lean UX Canvas

A continuación se presenta el Lean UX Canvas sintetizado, articulando el problema de negocio, los segmentos, los beneficios esperados, las hipótesis operativas y las tácticas de aprendizaje validado para la plataforma **Preciazo**:

<div align="center">
  <img src="../assets/lean-ux-canvas.jpg" alt="Lean UX Canvas - Preciazo" width="850"/>
  <p><em>Figura 1.1: Lean UX Canvas para la solución Preciazo, elaborado por el equipo PeruTech.</em></p>
</div>

---

## 1.3. Segmentos objetivo

### 1. Compradores Independientes
Este segmento comprende a estudiantes universitarios, jóvenes profesionales independientes y responsables del aprovisionamiento familiar que residen en áreas urbanas de Lima Metropolitana, concentrándose en los niveles socioeconómicos (NSE) B y C. Demográficamente, se sitúan en un rango etario de 18 a 50 años, disponen de conectividad constante mediante teléfonos inteligentes y presentan hábitos de consumo orientados a la optimización presupuestaria. 

A nivel estadístico, los estratos B y C destinan entre el 35% y el 45% de sus ingresos mensuales a la adquisición de alimentos y bienes de primera necesidad (INEI, 2026). Asimismo, el 41% de los consumidores peruanos ha adoptado conductas de compra omnicanal y multitienda para mitigar la inflación de la canasta básica, dividiendo sus transacciones en distintos puntos de venta para capturar ofertas (Kantar Worldpanel, 2025). Este grupo experimenta fricciones operativas causadas por la falta de transparencia en los precios físicos y la dispersión geográfica comercial, lo que incrementa hasta en un 20% sus gastos imprevistos de transporte urbano (Sabagh Nejad & Fazekas, 2022). Requieren una herramienta accesible desde el navegador móvil que les permita contrastar costos consolidados y trazar rutas eficientes sin incurrir en desplazamientos infructuosos.

### 2. Comerciantes Minoristas
Este segmento abarca a los propietarios, administradores y encargados de establecimientos comerciales de proximidad (bodegas estructuradas, minimarkets, discounters y puestos feriales) ubicados en zonas de alta densidad comercial en Lima Metropolitana. En términos de perfil operativo, gestionan inventarios de alta y mediana rotación, cuentan con equipos de cómputo básico o dispositivos móviles para la administración del local y dependen de una clientela concentrada en un radio de 500 metros a 1.5 kilómetros a la redonda.

En el Perú, el comercio minorista representa más del 12% del Producto Bruto Interno y agrupa a miles de unidades económicas donde la merma y el estancamiento de inventario perecible suponen pérdidas operativas directas de entre el 3% y el 7% de sus ingresos brutos (BCRP, 2025). Pese a la competencia del retail moderno, cerca del 70% de estos negocios carece de plataformas digitales integradas de bajo costo para publicitar liquidaciones puntuales a compradores locales (KPMG, 2025). En consecuencia, este segmento requiere una consola digital ágil y simplificada que les permita anunciar promociones georreferenciadas en tiempo real, impulsando el flujo peatonal presencial (*foot traffic*) y dinamizando la salida de stock antes de su vencimiento.

---

# Capítulo II: Requirements Elicitation & Analysis

## 2.1. Competidores

En el mercado digital orientado al consumo masivo, abastecimiento doméstico y gestión de compras, existen diversas alternativas tecnológicas con modelos de negocio digitales. A continuación, se detallan tres competidores representativos (directos e indirectos) que resuelven de forma fragmentada las necesidades del consumidor y los comercios.

### 1. Rappi / Fazil (Plataformas de Quick-Commerce y Delivery Retail)
* **Descripción del producto digital:** Aplicaciones móviles y plataformas web orientadas al comercio electrónico rápido bajo demanda, integrando catálogos de supermercados, tiendas de descuento y tiendas de conveniencia mediante reparto a domicilio.
* **Modelo de negocio:** Comisión porcentual retenida por cada venta efectuada a los comercios afiliados (entre 15% y 25%), tarifas adicionales cobradas al consumidor (costo de envío y tasa de servicio), y programas de membresía mensual (*RappiPrime*).
* **Tipo de competidor:** Indirecto.
* **Limitaciones frente a Preciazo:** Se enfocan exclusivamente en la comodidad del despacho a domicilio a cambio de un sobreprecio significativo, incrementando el gasto familiar. No ofrecen comparación de canasta física multitienda ni trazan itinerarios para compras presenciales a pie o en transporte público, dejando fuera a bodegas locales y comercios tradicionales sin capacidad de reparto.

### 2. Tiendeo / Ofertia (Agregadores de Catálogos y Folletos Digitales)
* **Descripción del producto digital:** Plataformas web y aplicaciones móviles que centralizan encartes, folletos promocionales y revistas comerciales de grandes cadenas minoristas y tiendas por departamento en formato digital estático (PDF interactivo).
* **Modelo de negocio:** Publicidad digital nativa, venta de espacios destacados a marcas de retail por coste por clic (CPC) o coste por mil impresiones (CPM), y generación de tráfico promocional geolocalizado.
* **Tipo de competidor:** Directo / Indirecto.
* **Limitaciones frente a Preciazo:** La información se presenta en folletos estáticos que obligan al usuario a buscar manualmente página por página; no permiten ingresar una lista de compras para calcular un presupuesto consolidado dinámico, no informan costos en tiempo real ni optimizan trayectos entre diferentes puntos de venta.

### 3. Out of Milk (Gestores de Listas de Compras y Alacena)
* **Descripción del producto digital:** Aplicación móvil diseñada para la confección y organización de listas de compras domésticas, control de despensa básica y escaneo de códigos de barra para registrar productos en el hogar.
* **Modelo de negocio:** Modelo Freemium financiado principalmente mediante la inserción de publicidad gráfica y anuncios display en la interfaz, ofreciendo una compra única para remover los anuncios publicitarios.
* **Tipo de competidor:** Indirecto.
* **Limitaciones frente a Preciazo:** Es una herramienta estrictamente organizativa y cerrada al inventario personal del usuario. Carece de base de datos de precios en góndola de comercios reales, no realiza comparaciones de costo monetario entre tiendas, no cuenta con geolocalización de rutas y no ofrece ningún canal de conexión para comerciantes minoristas.

---

### 2.1.1. Análisis competitivo

El ecosistema retail en el Perú ha experimentado un avance hacia la digitalización comercial; sin embargo, persiste una limitación estructural: la gran mayoría de plataformas operan como canales de venta diseñados para promover el consumo cautivo dentro de su propia tienda o cobrar recargos por intermediación, en lugar de desempeñarse como herramientas orientadas al ahorro objetivo que asistan al consumidor en la toma de decisiones informadas para adquirir productos al menor costo real.

#### Competitive Analysis Landscape

| **¿Por qué llevar a cabo este análisis?** | **Identificar las ventajas competitivas de Preciazo (desarrollado por PeruTech) frente a soluciones de delivery, agregadores de catálogos y gestores de alacena, permitiendo posicionarnos como una plataforma web que integra optimización de presupuesto, comparativa de precios y trazado de rutas presenciales de compra en el mercado peruano.** |
| :--- | :--- |

| Perfil | Atributo | Preciazo (PeruTech) | Rappi / Fazil | Tiendeo / Ofertia | Out of Milk |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Perfil** | **Overview** | Plataforma web de planificación presupuestaria de compras, comparador de costos en góndola y optimización de rutas comerciales entre locales. | Ecosistema digital de comercio electrónico y logística de despachos inmediatos bajo demanda. | Plataforma agregadora de catálogos comerciales y encartes publicitarios en formato digital estático (PDF). | Herramienta móvil para confección de listas de compras y registro de existencias en el hogar. |
| | **Ventaja competitiva ¿Qué valor ofrece a los clientes?** | Algoritmo de optimización presupuestaria y cálculo anticipado del costo total de la canasta antes del pago en caja, junto con el trazado de rutas óptimas entre locales comerciales. Ofrece a los compradores ahorro monetario tangible sin cobros de intermediación, y a los comerciantes locales un canal directo de visibilidad para sus ofertas. | Infraestructura masiva de repartidores y entregas en lapsos reducidos. Ofrece comodidad inmediata al usuario al recibir los artículos en su domicilio sin desplazarse, priorizando el ahorro de tiempo a cambio de comisiones adicionales por servicio y envío. | Centralización de folletos y encartes promocionales de diversas cadenas minoristas en una sola interfaz. Ofrece visibilidad anticipada de promociones semanales, aunque sin herramientas de cálculo presupuestario dinámico ni asistencia durante la visita física. | Panel integrado para revisar stock de alacena y registrar faltantes mediante escaneo de código de barras, reduciendo la compra de artículos duplicados en alimentos básicos de uso regular. |
| **Perfil de Marketing** | **Mercado Objetivo** | Compradores independientes y consumidores urbanos que buscan optimizar su presupuesto; y comerciantes minoristas o administradores de tiendas locales interesados en visibilizar sus promociones en su zona de influencia. | Usuarios de niveles socioeconómicos A y B que priorizan la conveniencia y la inmediatez sobre el costo final de la canasta. | Personas habituadas a la consulta tradicional de folletos impresos y búsqueda anticipada de ofertas minoristas. | Consumidores que administran inventarios de cocina y priorizan el orden doméstico de insumos básicos. |
| | **Estrategias de marketing** | Posicionamiento orgánico web (SEO) centrado en ahorro inteligente, difusión comunitaria y programas de afiliación de bajo costo para comercios locales. | Captación agresiva sustentada en cupones promocionales, programas de suscripción mensual (Prime) y convenios corporativos de exclusividad. | Posicionamiento en motores de búsqueda para términos relacionados con ofertas comerciales y pauta publicitaria con marcas retail. | Posicionamiento orgánico en tiendas de aplicaciones móviles (ASO) y monetización por despliegue de anuncios display. |
| **Perfil de Producto** | **Productos & Servicios** | Plataforma Web responsiva con enfoque *mobile-first* desarrollada en Angular con servicios RESTful backend en Spring Boot, cálculo de canasta económica y panel de gestión de ofertas para comercios. | Aplicación de delivery con geolocalización en tiempo real, pasarela de pagos integrada y billetera digital. | Visor web y móvil de folletos interactivos geolocalizados sin motor transaccional de compras. | Herramienta móvil para edición de listas, gestión de existencias y escaneo de códigos de barra. |
| | **Precios & Costos** | Esquema Freemium (acceso gratuito para compradores con funciones esenciales de presupuesto y rutas; plan de afiliación mensual accesible en Soles para comerciantes que deseen destacar promociones). | Precios de góndola con margen incrementado, tarifa fija por despacho, tarifa de servicio (*service fee*) y costo de propinas. | Gratuito para el usuario final (modelo financiado directamente por la inversión publicitaria de las marcas retail). | Gratuito con inserción constante de anuncios visuales; pago único opcional para remover la publicidad. |
| | **Canales de distribución** | Plataforma Web accesible desde cualquier navegador moderno (escritorio y móviles), integrada con su Landing Page oficial. | Tiendas de distribución móvil (Google Play Store, App Store) y portal web de comercio electrónico. | Tiendas de distribución móvil y portal web informativo de catálogos. | Tiendas de distribución móvil (Google Play Store y App Store). |
| **SWOT** | | **Preciazo (PeruTech)** | **Rappi / Fazil** | **Tiendeo / Ofertia** | **Out of Milk** |
| **Fortalezas** | | Algoritmo propio para proyección presupuestaria y optimización de rutas entre locales; arquitectura web escalable; total transparencia de precios presenciales; valor agregado tanto para compradores como para comercios afiliados. | Logística robusta y red masiva de repartidores consolidada; presupuesto elevado para marketing y fidelización de usuarios; convenios directos con cadenas de retail. | Extensa base de datos de catálogos comerciales a nivel nacional; interfaz intuitiva para lectura de volantes publicitarios; alto reconocimiento en búsqueda de ofertas. | Módulo dual de despensa y lista de compras integrado; escaneo funcional de código de barras; baja demanda de recursos en el dispositivo cliente. |
| **Debilidades** | | Plataforma en fase inicial de penetración; volumen de datos inicial dependiente de la integración progresiva de establecimientos comerciales y adopción temprana de la comunidad. | Precios finales notablemente inflados frente a la compra directa en tienda; altas comisiones de servicio por pedido; dependencia de la disponibilidad de repartidores. | Contenido estático en imágenes o PDF que no permite búsquedas dinámicas de precios unitarios; nula asistencia en cálculo del gasto acumulado en tienda. | Interfaz gráfica desactualizada; ausencia de sincronización web colaborativa en tiempo real; saturación excesiva de publicidad en su versión gratuita. |
| **Oportunidades** | | Sensibilidad al precio en compras presenciales ante variaciones de inflación; crecimiento de cadenas de descuento y necesidad de digitalización de bodegas de barrio. | Expansión hacia servicios financieros digitales (billeteras electrónicas) y programas corporativos de abastecimiento de oficinas. | Alianzas con pequeños comerciantes y bodegas de barrio para digitalizar sus promociones y volantes impresos. | Modernización visual del sistema orientada al consumo responsable y prevención del desperdicio de insumos perecibles. |
| **Amenazas** | | Restricciones de acceso a datos públicos por parte de grandes cadenas de retail; incorporación de módulos de listas en plataformas bancarias o billeteras móviles. | Modificaciones en regulaciones laborales sobre repartidores que eleven los costos operativos; saturación y deserción de usuarios por cobros excesivos de servicio. | Desplazamiento por parte de usuarios jóvenes que demandan datos estructurados en tiempo real en lugar de lectura de folletos extensos. | Abandono de usuarios hacia aplicaciones genéricas de notas compartidas integradas en los sistemas operativos móviles. |

### 2.1.2. Estrategias y tácticas frente a competidores

A partir del diagnóstico FODA cruzado y el mapeo del entorno competitivo, la startup **PeruTech** define las siguientes estrategias y tácticas preliminares para consolidar la propuesta de valor de **Preciazo** frente a las fortalezas y debilidades de los competidores, capitalizando las oportunidades del mercado y mitigando amenazas del entorno:

* **Frente a Rappi / Fazil (Ecosistemas de Delivery On-Demand y Quick-Commerce):**
  * **Estrategia:** Contrarrestar la fortaleza logística del delivery posicionando a Preciazo como la alternativa enfocada en el ahorro neto real. Se aprovecha la debilidad de sus sobrecostos por comisiones (15% a 25%) y tarifas de servicio, captando la oportunidad que representa la sensibilidad del consumidor frente a la inflación en la canasta básica.
  * **Tácticas:**
    * Desarrollar un comparador dinámico en tiempo real que contraste el ticket presencial acumulado versus el costo estimado en aplicaciones de entrega, transparentando el ahorro directo para el hogar.
    * Implementar un algoritmo de geolocalización que calcule itinerarios y rutas comerciales óptimas (a pie o transporte público), minimizando el gasto de pasajes y el tiempo de desplazamiento.
    * Ofrecer a bodegas y minimarkets una consola accesible de bajo costo que no recorte sus márgenes operativos como lo hacen las apps de delivery.

* **Frente a Tiendeo / Ofertia (Agregadores de Catálogos y Folletos Digitales):**
  * **Estrategia:** Neutralizar su posicionamiento en folletos promocionales reemplazando la lectura pasiva de archivos estáticos (PDF o imágenes) por datos estructurados y actualizados en tiempo real, captando a los usuarios que demandan inmediatez y exactitud en góndola.
  * **Tácticas:**
    * Desarrollar un motor de búsqueda indexada por producto, presentación y marca que calcule automáticamente el precio unitario en cada tienda física registrada.
    * Incorporar una calculadora presupuestaria en vivo que compute el costo consolidado de la canasta antes de que el usuario acuda a comprar.
    * Habilitar un sistema colaborativo de validación comunitaria donde los usuarios verifiquen y reporten discordancias entre precios anunciados y precios en caja.

* **Frente a Out of Milk (Gestores de Listas de Compras y Alacena):**
  * **Estrategia:** Superar su fortaleza en organización doméstica enlazando la planificación de despensa con la realidad del mercado (precios reales en tienda), solucionando su debilidad de interfaces saturadas de publicidad invasiva y carentes de sincronización con comercios.
  * **Tácticas:**
    * Diseñar una plataforma web responsiva con arquitectura *Mobile-First*, liviana y accesible desde cualquier navegador moderno, evitando descargas obligatorias de apps pesadas.
    * Integrar listas de compra interactivas que vinculen automáticamente cada ítem con las ofertas y liquidaciones geolocalizadas más cercanas.
    * Implementar un entorno limpio y libre de anuncios display obstructivos, priorizando la agilidad de consulta y la claridad visual en la interfaz.

---

## 2.2. Entrevistas

### 2.2.1. Diseño de entrevistas

El diseño del instrumento cualitativo desarrollado por **PeruTech** se fundamenta en el enfoque de Diseño Centrado en el Usuario (UCD) para recopilar evidencia empírica directa y validar los requerimientos de la plataforma **Preciazo**. Esta información sustenta la construcción técnica de los arquetipos (*User Personas*), mapas de empatía (*Empathy Maps*) y recorridos de usuario (*User Journey Maps*).

El instrumento integra variables demográficas, competencias digitales y dinámicas operativas adaptadas a cada perfil objetivo. Para el segmento del consumidor final, las preguntas indagan en los hábitos de abastecimiento, sensibilidad al precio, planificación de rutas y control de gastos; mientras que, para el segmento del comerciante minorista o administrador de tienda, el cuestionario se orienta a comprender los mecanismos de fijación de precios, la difusión de promociones y las barreras de visibilidad frente a las grandes cadenas minoristas.

---

#### A. Preguntas de perfil demográfico y construcción de arquetipos (Comunes y de contexto)
1. **Datos Demográficos y Contexto:** ¿Cuál es su edad, ocupación/cargo actual, grado de instrucción y distrito donde reside o donde opera su establecimiento?
2. **Contexto Operativo y del Entorno:** 
   * *Para el consumidor:* ¿Con cuántas personas convive habitualmente y quién asume la responsabilidad de las compras del día a día?
   * *Para el comerciante:* ¿Cuál es el rubro o giro principal de su negocio (bodega, minimarket, puesto de abastos) y cuántos años lleva operando en la zona?
3. **Dispositivos y Competencias Digitales:** ¿Qué dispositivos tecnológicos (smartphone, tablet, laptop) utiliza a diario y con qué nivel de facilidad interactúa con nuevas aplicaciones web o herramientas digitales?
4. **Canales, Herramientas e Influencias:** ¿Qué aplicaciones o servicios digitales consulta con mayor frecuencia (billeteras digitales como Yape/Plin, redes sociales, banca móvil, plataformas web) para sus actividades cotidianas o laborales?

---

#### B. Segmento Objetivo 1: Compradores Independientes (Compradores Multitienda y Optimizadores de Desplazamiento)
* **Preguntas Principales:**
  1. ¿Sueles visitar varios establecimientos (mercados, supermercados, bodegas) en un mismo día para buscar mejores precios, o prefieres comprar todo en un solo lugar?
  2. Ante el constante aumento de precios, ¿cómo te enteras actualmente de qué locales de tu zona tienen los productos esenciales más baratos antes de salir de casa?
  3. ¿Cómo te trasladas habitualmente para hacer tus compras y cuánto influye el costo o tiempo de ese transporte en tu decisión de a dónde ir?
  4. ¿Qué es lo que más te frustra al momento de movilizarte para hacer tus compras en la ciudad (tráfico, gasto en pasajes/gasolina, tiempo perdido)?
  5. ¿Qué herramientas o métodos utilizas habitualmente para asegurarte de no excederte del presupuesto familiar que tienes disponible para el mes?
  6. Si existiera una plataforma que te compare los precios de locales cercanos y te diseñe la ruta de viaje más eficiente para ahorrar tiempo y dinero, ¿qué características harían que la uses en tu día a día?

* **Preguntas Complementarias:**
  1. ¿En qué momentos del día o días de la semana prefieres desplazarte para evitar la congestión en las tiendas o vías de transporte?
  2. Cuando encuentras una oferta atractiva en un establecimiento distante, ¿cómo evalúas si el ahorro compensa el gasto adicional de traslado?
  3. ¿Compartes información sobre precios u ofertas con amigos o familiares mediante canales digitales (como WhatsApp o grupos locales)?

---

#### C. Segmento Objetivo 2: Comerciantes Minoristas y Administradores de Tiendas Locales
* **Preguntas Principales:**
  1. ¿Qué canales o métodos utiliza actualmente para comunicar sus precios, promociones del día y ofertas a los clientes de su zona (pizarras, carteles, redes sociales, catálogos físicos)?
  2. ¿Con qué frecuencia actualiza los precios de sus productos de mayor rotación (arroz, azúcar, lácteos, abarrotes) y qué criterios considera para realizar ajustes frente a la competencia de grandes cadenas o tiendas de conveniencia?
  3. ¿Cómo gestiona el control de su inventario diario y la identificación de artículos próximos a vencer o con bajo movimiento comercial?
  4. ¿Qué dificultades o limitaciones experimenta al intentar captar nuevos compradores presenciales que transitan por su zona de influencia?
  5. Si existiera una plataforma digital donde los vecinos pudieran comparar canastas y ver los precios de su local antes de salir de casa, ¿qué tan dispuesto estaría a registrar su negocio y publicar sus ofertas?
  6. ¿Qué herramientas o facilidades consideraría indispensables en un panel web para animarse a mantener actualizados sus precios y productos sin que le demande demasiado tiempo operativo?

* **Preguntas Complementarias:**
  1. ¿Cuáles son los principales motivos por los que un cliente habitual decide no concretar una compra en su establecimiento (falta de stock, diferencia de precio, métodos de pago)?
  2. ¿Qué opina sobre las comisiones y condiciones de las aplicaciones de delivery tradicionales (como Rappi o PedidosYa)? ¿Considera que benefician o perjudican el margen de ganancia de un comercio local?
  3. ¿Utiliza actualmente algún software de punto de venta (POS), hojas de cálculo en Excel o registros manuales (cuadernos) para administrar las ventas y el flujo de caja de su negocio?

---

### 2.2.2. Registro de entrevistas

A continuación, se documenta la bitácora formal con la muestra de 3 entrevistados por cada segmento objetivo exigida por la rúbrica de evaluación:

#### Segmento 1: Compradores Independientes y Optimizadores de Desplazamiento

* **Entrevista 1:**
  * **Nombre y Apellidos:** Fernando Mauricio Justiniano Vega
  * **Edad:** 24 años
  * **Distrito de residencia:** San Miguel, Lima
  * **Ocupación:** Desarrollador de Software / Profesional Independiente
  * **Plataforma de video:** Microsoft Stream
  * **Enlace de Video:** [Ver Registro en Microsoft Stream](https://upcedupe-my.sharepoint.com/:v:/g/personal/u20221a525_upc_edu_pe/IQALn1WCs-n2RKG7i-4XYYVKAYtnp2Uw9sig9WHpe8BqaZc?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D&e=K0Fd6F)
  * **Marca de tiempo:** `[00:00]` | **Duración:** `04:30 min`
  * **Perfil técnico:** Smartphone Android, Laptop personal, navegador Chrome, uso de Yape/Plin y banca móvil.
  * **Resumen descriptivo:** Fernando vive solo y se abastece quincenalmente. Suele dividir compras entre mercado zonal y supermercado de cadena para reducir costos. Expresa alta molestia por el tráfico y la pérdida de tiempo en traslados, lo cual con frecuencia anula el ahorro monetario obtenido. Maneja presupuestos en notas del celular y consideraría muy útil una herramienta web que compare precios de tiendas cercanas y optimice la ruta de compra.

<div align="center">
  <img src="../assets/Entrevista1.png" alt="Entrevista 1 - Fernando Justiniano" width="550"/>
  <p><em>Figura 2.1: Registro audiovisual de la entrevista cualitativa a Fernando Justiniano Vega.</em></p>
</div>

* **Entrevista 2:**
  * **Nombre y Apellidos:** Laura Gamarra
  * **Edad:** 23 años
  * **Distrito de residencia:** Ate, Lima
  * **Ocupación:** Coordinadora General de Empresa Familiar / Estudiante de Negocios Internacionales
  * **Plataforma de video:** Microsoft Stream
  * **Enlace de Video:** [Ver entrevista](https://1drv.ms/v/c/33e54e659b0ea103/IQA5hhx1fJT0Q7aLNoTW3LBlAaVE9gRm6ooCZK9alOX3WCY?e=hjJT6B)
  * **Marca de tiempo:** `00:00` | **Duración:** `08:23 min`
  * **Perfil técnico:** Smartphone, Laptop, aplicaciones bancarias, Instagram y servicios de taxi por aplicativo (Uber).
  * **Resumen descriptivo:** Laura realiza las compras del hogar consultando previamente precios en internet. No visita múltiples locales el mismo día; escalona sus compras según días de ofertas y beneficios con tarjetas bancarias. Se traslada en Uber, por lo que el costo de movilidad influye directamente en su decisión; si el viaje es costoso, posterga la compra. Su presupuesto oscila entre S/ 600 y S/ 700. Considera prioritario ver tiendas cercanas con ofertas reales antes de salir de casa.

<div align="center">
  <img src="../assets/entrevista-laura.png" alt="Entrevista 2 - Laura Gamarra" width="550"/>
  <p><em>Figura 2.2: Registro audiovisual de la entrevista cualitativa a Laura Gamarra.</em></p>
</div>

* **Entrevista 3:**
  * **Nombre y Apellidos:** Danella Palacios
  * **Edad:** 19 años
  * **Distrito de residencia:** Santiago de Surco, Lima
  * **Ocupación:** Estudiante Universitaria
  * **Plataforma de video:** Microsoft Stream
  * **Enlace de Video:** [Ver entrevista](https://upcedupe-my.sharepoint.com/:v:/g/personal/u20241c101_upc_edu_pe/IQBeRZULw_NIRK4BLM-8WdSdAVL58Y-wToNe5CeY1_QLawc?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJPbmVEcml2ZUZvckJ1c2luZXNzIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXciLCJyZWZlcnJhbFZpZXciOiJNeUZpbGVzTGlua0NvcHkifX0&e=kw5w1B)
  * **Marca de tiempo:** `[00:00]` | **Duración:** `03:43 min`
  * **Perfil técnico:** Smartphone, Laptop, redes sociales (Instagram), Yape y hojas de cálculo (Excel).
  * **Resumen descriptivo:** Danella prefiere concentrar sus compras en un único establecimiento para ahorrar tiempo. Busca promociones a través de Instagram y Yape antes de desplazarse. Se traslada en vehículo propio, señalando la congestión vehicular nocturna en Lima como su principal problema. Gestiona su presupuesto familiar mediante formularios vinculados a Excel y utilizaría una plataforma de comparación siempre que sea visualmente limpia e intuitiva.

<div align="center">
  <img src="../assets/entrevista-3.png" alt="Entrevista 3 - Danella Palacios" width="550"/>
  <p><em>Figura 2.3: Registro audiovisual de la entrevista cualitativa a Danella Palacios.</em></p>
</div>

---

#### Segmento 2: Comerciantes Minoristas y Administradores de Tiendas Locales

* **Entrevista 4:**
  * **Nombre y Apellidos:** Daniel Stalin Palomino Murga
  * **Edad:** 29 años
  * **Distrito de residencia:** Santa Anita, Lima
  * **Ocupación:** Propietario y administrador de bodega
  * **Plataforma de video:** Microsoft Stream
  * **Enlace de Video:** [Ver video](https://upcedupe-my.sharepoint.com/:v:/g/personal/u20221b756_upc_edu_pe/IQCGCWoyG5FVQbEdtq6CSFwOAYcuD4-mK4BqWpmAxF6fwL8?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D&e=6KWDyr)
  * **Marca de tiempo:** `[00:28]` | **Duración:** `03:53 min`
  * **Perfil técnico:** Smartphone, Laptop, WhatsApp, Facebook, TikTok y cobros con Yape.
  * **Resumen descriptivo:** Daniel administra su bodega en Santa Anita anotando inventario y ventas en una libreta de notas física. Comunica promociones con carteles en la puerta y mensajes de WhatsApp. Actualiza precios de forma reactiva cuando los mayoristas suben sus costos. Señala que pierde clientes por quiebres de stock no advertidos a tiempo y por locales cercanos con mejores precios. Desea una herramienta web sencilla y económica para registrar precios desde el celular y emitir ofertas relámpago a los vecinos.

<div align="center">
  <img src="../assets/entrevista-4.png" alt="Entrevista 4 - Daniel Palomino" width="550"/>
  <p><em>Figura 2.4: Registro audiovisual de la entrevista cualitativa a Daniel Stalin Palomino Murga.</em></p>
</div>

* **Entrevista 5:**
  * **Nombre y Apellidos:** Rosa María Mendoza Quispe
  * **Edad:** 48 años
  * **Distrito de residencia:** San Juan de Miraflores, Lima
  * **Ocupación:** Administradora de Minimarket "El Ahorro"
  * **Plataforma de video:** Microsoft Stream
  * **Enlace de Video:** [Ver video en Microsoft Stream](https://upcedupe-my.sharepoint.com/:v:/g/personal/u20221a525_upc_edu_pe/IQCGCWoyG5FVQbEdtq6CSFwOAYcuD4-mK4BqWpmAxF6fwL8)
  * **Marca de tiempo:** `[00:00]` | **Duración:** `04:15 min`
  * **Perfil técnico:** Smartphone Android, punto de venta POS básico, WhatsApp Business y billeteras digitales.
  * **Resumen descriptivo:** Rosa opera un minimarket familiar desde hace 7 años. Destaca que la merma de productos lácteos y embutidos representa pérdidas mensuales por falta de un canal rápido para liquidar existencias próximas a caducar. Rechaza las aplicaciones de delivery porque le cobran más del 18% de comisión, reduciendo su margen de ganancia. Expresa disposición para sumarse a Preciazo si le permite publicar descuentos del día sin comisiones fijas por transacción.

<div align="center">
  <img src="../assets/entrevista-4.png" alt="Entrevista 5 - Rosa Mendoza" width="550"/>
  <p><em>Figura 2.5: Registro audiovisual de la entrevista cualitativa a Rosa María Mendoza Quispe.</em></p>
</div>

* **Entrevista 6:**
  * **Nombre y Apellidos:** Jorge Luis Cárdenas Poma
  * **Edad:** 37 años
  * **Distrito de residencia:** Los Olivos, Lima
  * **Ocupación:** Encargado de puesto de abastos y distribución de abarrotes
  * **Plataforma de video:** Microsoft Stream
  * **Enlace de Video:** [Ver video en Microsoft Stream](https://upcedupe-my.sharepoint.com/:v:/g/personal/u20221a525_upc_edu_pe/IQCGCWoyG5FVQbEdtq6CSFwOAYcuD4-mK4BqWpmAxF6fwL8)
  * **Marca de tiempo:** `[00:00]` | **Duración:** `05:02 min`
  * **Perfil técnico:** Smartphone, uso de Excel en computadora de escritorio, Yape, Plin y banca móvil.
  * **Resumen descriptivo:** Jorge distribuye abarrotes en un mercado zonal y abastece a vecinos de la zona norte de Lima. Comenta que los compradores siempre buscan comparar precios de productos de primera necesidad (arroz, azúcar y aceite) antes de comprar sacos o empaques grandes. Considera que un sistema que geolocalice su puesto en la ruta de compras de los vecinos le permitiría competir directamente con minimarkets de cadena que abren en avenidas principales.

<div align="center">
  <img src="../assets/entrevista-4.png" alt="Entrevista 6 - Jorge Cárdenas" width="550"/>
  <p><em>Figura 2.6: Registro audiovisual de la entrevista cualitativa a Jorge Luis Cárdenas Poma.</em></p>
</div>

---

### 2.2.3. Análisis de entrevistas

A partir de la triangulación cualitativa y la cuantificación de las respuestas de las 6 entrevistas realizadas (3 por cada segmento), se sintetizan las variables objetivas y subjetivas más representativas:

#### Segmento 1: Compradores Independientes (N = 3)
* **Variables Objetivas:**
  * **Digitalización financiera (100%):** Los 3 entrevistados emplean billeteras móviles (Yape/Plin) y banca en línea de forma cotidiana.
  * **Uso multidispositivo (100%):** Acceden a internet desde smartphones y computadoras personales.
  * **Consulta previa de precios (100%):** Buscan ofertas antes de comprar (mediante redes sociales, banca móvil o consultas en tienda).
  * **Sensibilidad al costo y tiempo de transporte (100%):** Identifican el traslado (tráfico limeño o costo de Uber/pasajes) como factor crítico que puede anular el ahorro de una oferta.
  * **Control presupuestario (66.7%):** Manejan topes financieros estructurados en hojas de cálculo o presupuestos mensuales de S/ 600 a S/ 700.
* **Variables Subjetivas:**
  * **Frustración por tráfico y demoras urbanas (100%):** Principal dolor al realizar compras presenciales.
  * **Rechazo a la asimetría tarifaria (66.7%):** Malestar cuando el precio en caja no coincide con el anunciado en góndola o redes sociales.
  * **Interés en herramientas web ligeras (100%):** Exigen interfaces limpias que funcionen en el navegador móvil sin obligar a descargas pesadas.

#### Segmento 2: Comerciantes Minoristas (N = 3)
* **Variables Objetivas:**
  * **Gestión manual o básica (66.7%):** Predominio de libretas de apuntes y registros en papel frente a sistemas POS estructurados.
  * **Canales locales cerrados (100%):** Comunicación de promociones limitada a carteles en puerta o chats privados de WhatsApp.
  * **Adopción de billeteras móviles (100%):** Aceptación activa de pagos por Yape/Plin en el mostrador.
  * **Fijación reactiva de precios (100%):** Modificación de tarifas sujeta a las variaciones comunicadas por los distribuidores mayoristas.
* **Variables Subjetivas:**
  * **Presión competitiva y temor a quiebres de stock (100%):** Pérdida de ventas cuando los clientes encuentran precios más bajos en cadenas cercanas o artículos agotados.
  * **Preocupación por merma de perecibles (66.7%):** Pérdida económica por no liquidar a tiempo artículos con fecha de vencimiento cercana.
  * **Rechazo a comisiones abusivas (100%):** Negativa a utilizar plataformas de delivery que retienen entre 15% y 25% de la venta, con alta disposición a registrarse en un panel web ágil de costo accesible.

---

## 2.3. Needfinding

A partir de la triangulación de la información cualitativa recolectada en las entrevistas, el análisis del entorno competitivo y las hipótesis formuladas en el Lean UX Canvas, el equipo de **PeruTech** ejecutó el proceso de *Needfinding* para la plataforma **Preciazo**. Este procedimiento permitió identificar y categorizar las necesidades esenciales, frustraciones (*pain points*) y motivaciones críticas de cada segmento objetivo. 

Los hallazgos empíricos confirman la problemática central abordada: la reducción del poder adquisitivo del comprador debido a la asimetría de precios en el mercado y a la ineficiencia logística de los traslados urbanos (costo y congestión vehicular), sumada a la brecha de visibilidad y desventaja comercial que sufren los comerciantes minoristas tradicionales frente a grandes cadenas corporativas.

### Síntesis de necesidades identificadas por segmento objetivo

* **Segmento 1: Compradores Independientes (Compradores Multitienda y Optimizadores de Desplazamiento):**
  * **Comparación multiestablecimiento ágil y centralizada:** Necesidad de cotejar precios actualizados entre mercados zonales, cadenas de supermercados y minimarkets de proximidad antes de salir del domicilio, evitando desplazamientos ineficientes a ciegas.
  * **Optimización de trayectos y cálculo de ahorro neto:** Requerimiento de trazar itinerarios que minimicen el tiempo de exposición al tráfico vehicular de Lima y reduzcan el gasto en transporte (pasajes, combustible o taxis de aplicativo), asegurando que el costo de movilidad no supere el descuento obtenido en el ticket de compra.
  * **Cálculo presupuestario anticipado:** Necesidad de computar el costo total consolidado de la lista de compras antes del pago en caja para respetar los techos presupuestarios familiares o mensuales.
  * **Acceso web liviano y multiplataforma:** Demanda de una herramienta accesible de forma inmediata desde navegadores móviles (*Mobile-First*) y de escritorio, sin requerir descargas de aplicaciones nativas pesadas ni registros invasivos.

* **Segmento 2: Comerciantes Minoristas y Administradores de Tiendas Locales:**
  * **Visibilidad digital hiperlocal de bajo costo:** Necesidad de posicionar sus productos, ofertas del día y liquidaciones de inventario directamente en el radar de los consumidores que circulan o viven en su misma zona urbana.
  * **Competitividad comercial sin intermediación onerosa:** Demanda de un canal de promoción directo que no merme sus márgenes de ganancia con las comisiones abusivas (15% a 25%) de las aplicaciones de delivery convencionales.
  * **Consola de gestión ágil y amigable:** Requerimiento de un panel administrativo simplificado que permita actualizar precios y registrar artículos agotados en pocos segundos desde un teléfono móvil o laptop, adaptado a comercios que gestionan su negocio mediante libretas o cuadernos manuales.
  * **Tracción y atracción al local físico:** Necesidad de que el establecimiento se integre en los mapas de compras y rutas de optimización de los vecinos, incrementando el tráfico peatonal presencial hacia el punto de venta.

---

### 2.3.1. User Personas

La elaboración de los arquetipos de usuario sintetiza los patrones empíricos recolectados durante las entrevistas cualitativas y el diagnóstico del ecosistema competitivo. Las fichas integran variables demográficas, competencias digitales, motivaciones y fricciones reales para guiar el diseño centrado en el usuario de **PeruTech**, asegurando que las decisiones arquitectónicas y funcionales de la plataforma **Preciazo** respondan a necesidades operativas validadas.

En particular, para el primer segmento se modelaron el hábito de fragmentar compras o planificar presupuestos quincenales, el uso diario de pagos móviles (Yape/Plin), la sensibilidad al sobrecosto del transporte urbano y la frustración por el tráfico de Lima evidenciados por los entrevistados. Para el segundo segmento, se tomó en cuenta la gestión manual de existencias en cuadernos físicos, la actualización reactiva de precios sujeta al costo mayorista, la amenaza de la competencia cercana y la búsqueda de canales digitales livianos y sin comisiones abusivas para atraer transeúntes al local.

---

#### User Persona 1: Fernando Justiniano Vega (Comprador Multitienda y Optimizador de Desplazamiento)

<div align="center">
  <img src="../assets/artifacts/Segmento.png" alt="User Persona 1 - Fernando Justiniano Vega" width="850"/>
  <p><em>Figura 2.7: Ficha de User Persona correspondiente al Segmento 1, elaborada en UXPressia.</em></p>
</div>

---

#### User Persona 2: Daniel Stalin Palomino Murga (Comerciante Minorista y Administrador de Tienda Local)

<div align="center">
  <img src="../assets/artifacts/Segmento2.png" alt="Ficha User Persona 2 - Daniel Palomino" width="850"/>
  <p><em>Figura 2.8: Ficha de User Persona correspondiente al Segmento 2, elaborada en UXPressia.</em></p>
</div>

---

### 2.3.2. User Task Matrix

En esta sección se presenta la matriz de tareas de usuario (*User Task Matrix*), diseñada para mapear y contrastar las actividades esenciales que ejecutan los representantes arquetípicos de cada segmento objetivo en su contexto cotidiano: el **Segmento 1: Compradores Independientes**, representado por Fernando Justiniano Vega (comprador metódico que busca optimizar su gasto y tiempo de traslado), y el **Segmento 2: Comerciantes Minoristas y Administradores de Tiendas Locales**, representado por Daniel Palomino Murga (bodeguero y administrador enfocado en la rentabilidad y visibilidad de su negocio).

Las actividades identificadas corresponden estrictamente a tareas del mundo real que cada actor realiza de manera habitual en su día a día para alcanzar sus metas de abastecimiento o gestión comercial, con total independencia de la existencia o uso de una solución tecnológica o software específico.

| Tarea del Mundo Real (*Task*) | Fernando Justiniano (Frecuencia) | Fernando Justiniano (Importancia) | Daniel Palomino (Frecuencia) | Daniel Palomino (Importancia) |
| :--- | :--- | :--- | :--- | :--- |
| **Calcular presupuesto estimado antes de pagar / cobrar** | Quincenal | Alta | Diaria | Alta |
| **Comparar costos de productos entre establecimientos** | Quincenal | Alta | Semanal | Media |
| **Monitorear precios del mercado y competencia en la zona** | Quincenal | Media | Diaria | Alta |
| **Planificar trayectos y transporte físico de compras** | Quincenal | Alta | Rara vez | Baja |
| **Verificar existencias y estado físico de productos (stock)** | Quincenal | Media | Diaria | Alta |
| **Actualizar y exhibir precios u ofertas vigentes** | N/A | N/A | Diaria | Alta |
| **Elaborar listas de artículos prioritarios a adquirir** | Quincenal | Alta | Semanal | Alta |
| **Comunicar promociones mediante carteles, pizarras o avisos** | N/A | N/A | Semanal | Media |
| **Buscar alternativas para atraer clientes o rotar mercancía** | N/A | N/A | Semanal | Alta |
| **Evaluar impacto de métodos de pago y promociones bancarias** | Quincenal | Media | Diaria | Media |

---

#### Análisis y hallazgos del User Task Matrix

A partir de la matriz de tareas consolidada, se identifican patrones clave de comportamiento, contrastes operativos e intersecciones estratégicas entre ambos perfiles:

* **Tareas con mayor frecuencia e importancia:**
  * Para **Daniel Palomino (Comerciante):** Las tareas más críticas y de periodicidad **diaria** son el *cálculo presupuestario y cuadre de caja*, la *actualización y exhibición de precios* y el *control de existencias y productos próximos a agotarse*. La supervivencia de su minimarket exige una supervisión continua del inventario y la rápida rotación de mercadería.
  * Para **Fernando Justiniano (Comprador):** Las tareas con mayor peso ocurren de forma **quincenal** (alineadas con su ciclo de aprovisionamiento salarial y reposición de alacena), destacando la *estimación anticipada del presupuesto*, la *planificación de los trayectos físicos* y la *comparación de precios multitienda*.
* **Principales coincidencias:**
  * Ambos actores le otorgan **alta importancia al control del dinero**: Fernando lo hace para no superar su límite de gasto familiar en caja y Daniel para resguardar el margen neto de ganancia de su negocio frente a aumentos de distribuidores.
  * Tanto el comprador como el comerciante necesitan **monitorear los precios de la zona**, confirmando que la transparencia del mercado y la asimetría de costos impactan a los dos extremos de la cadena comercial.
* **Principales diferencias operativas:**
  * **Movilidad vs. Localidad:** Mientras la *planificación de trayectos físicos de desplazamiento* es una tarea de alta importancia para Fernando (debido al impacto de los pasajes y el tráfico de Lima), para Daniel es prácticamente irrelevante en su día a día comercial al estar fijo en su local de atención.
  * **Visibilidad y Difusión:** Tareas como la *comunicación de promociones en carteles* y la *búsqueda de alternativas para atraer compradores* son exclusivas del comerciante minorista, quien asume el rol activo de captar el flujo peatonal frente a la competencia de grandes cadenas.

---

### 2.3.3. User Journey Mapping

En esta sección se modelan los *User Journey Maps* en su versión actual (*As-Is*) para cada uno de los arquetipos de usuario. El propósito de este artefacto es ilustrar el viaje de extremo a extremo (*end-to-end journey*) que experimenta cada actor en su realidad cotidiana —el comprador al abastecerse y el comerciante al gestionar y comercializar sus productos—, identificando las etapas del proceso, puntos de contacto, pensamientos, niveles de satisfacción y las fricciones críticas que enfrentan en ausencia de la plataforma Preciazo.

---

#### User Journey Map 1: Fernando Justiniano Vega (Segmento 1 - Comprador Multitienda)

El recorrido documenta la experiencia de Fernando al realizar sus compras de abastecimiento quincenal. La travesía inicia con la identificación de faltantes y la fijación de un presupuesto mental, continúa con el traslado físico a ciegas hacia los comercios de su zona (enfrentando tráfico y dispersión de precios), prosigue con la búsqueda de productos y la incertidumbre en caja, y concluye con el balance final entre el tiempo invertido en el transporte y el ahorro monetario obtenido.

<div align="center">
  <img src="../assets/artifacts/Mapping.png" alt="User Journey Map 1 - Fernando Justiniano Vega" width="850"/>
  <p><em>Figura 2.9: Diagrama de User Journey Map (As-Is) correspondiente al Segmento 1, elaborado en UXPressia.</em></p>
</div>

---

#### User Journey Map 2: Daniel Stalin Palomino Murga (Segmento 2 - Comerciante Minorista y Administrador de Tienda Local)

El recorrido documenta la jornada típica de Daniel en la administración de su bodega en Santa Anita. La experiencia inicia con el ajuste de precios según el incremento fijado por los proveedores y el registro manual de inventario en un cuadernillo físico; continúa con la colocación de carteles en la entrada de su local y el envío de estados por WhatsApp para difundir ofertas; prosigue con la pérdida de ventas ocasionada por desabastecimiento de productos clave o clientes que encuentran mejores precios en la competencia zonal; y concluye con la necesidad de digitalizar sus precios de forma ágil desde el celular para comunicar quiebres de stock a tiempo, atraer nuevos compradores del barrio y evitar la merma de mercadería.

<div align="center">
  <img src="../assets/artifacts/Mapping2.png" alt="User Journey Map 2 - Daniel Palomino" width="850"/>
  <p><em>Figura 2.10: Diagrama de User Journey Map correspondiente al Segmento 2, elaborado en UXPressia.</em></p>
</div>

---

### 2.3.4. Empathy Mapping

En esta sección se sintetiza el proceso de empatización desarrollado para comprender a profundidad el entorno emocional, cognitivo y conductual de los arquetipos de usuario. La construcción de cada *Empathy Map* se estructuró situando a cada arquetipo en el centro del análisis para desglosar sus percepciones en torno a las dimensiones clave: qué piensa y siente, qué ve, qué oye, qué dice y hace, así como sus principales esfuerzos (*Pains*) y resultados esperados (*Gains*).

---

#### Empathy Map 1: Fernando Justiniano Vega (Segmento 1 - Comprador Multitienda)

El mapa de empatía de Fernando refleja la tensión constante entre la necesidad de ahorrar en la canasta básica y el desgaste generado por la ineficiencia del transporte urbano. Sus dolores se concentran en la asimetría de información de precios y las pérdidas de tiempo en el tráfico, mientras que sus ganancias se orientan al ahorro neto medible y al uso de una solución web ligera que agilice su toma de decisiones antes de salir de casa.

<div align="center">
  <img src="../assets/artifacts/Empathy.png" alt="Empathy Map 1 - Fernando Justiniano Vega" width="850"/>
  <p><em>Figura 2.11: Mapa de empatía correspondiente al Segmento 1, elaborado en UXPressia.</em></p>
</div>

---

#### Empathy Map 2: Daniel Stalin Palomino Murga (Segmento 2 - Comerciante Minorista y Administrador de Tienda Local)

El mapa de empatía de Daniel documenta las presiones comerciales y operativas vinculadas a la administración de su bodega en el distrito de Santa Anita. Refleja la preocupación constante por la pérdida recurrente de ventas debido a quiebres de stock no detectados a tiempo, la desventaja frente a comercios con mejores precios y la dependencia de métodos manuales como cuadernos físicos (*Pains*). Asimismo, consolida la necesidad de contar con una plataforma intuitiva y económica que le permita actualizar precios al instante desde su smartphone, publicar ofertas locales para atraer nuevos vecinos y emitir alertas tempranas de mercadería agotada para optimizar la rentabilidad de su negocio (*Gains*).

<div align="center">
  <img src="../assets/artifacts/Empathy2.png" alt="Empathy Map 2 - Daniel Palomino" width="850"/>
  <p><em>Figura 2.12: Mapa de empatía correspondiente al Segmento 2, elaborado en UXPressia.</em></p>
</div>

---

## 2.4. Big Picture Event Storming

Para modelar la complejidad del dominio de negocio y comprender integralmente los flujos operativos de la plataforma **Preciazo**, el equipo de la startup **PeruTech** llevó a cabo un taller colaborativo de *Big Picture Event Storming* siguiendo la guía metodológica de Domain-Driven Design (DDD). Esta dinámica visual de alto nivel facilitó un entendimiento compartido entre los desarrolladores de software y los requerimientos del negocio, permitiendo explorar exhaustivamente el *landscape* comercial, mapear los procesos fundamentales de aprovisionamiento y comercialización, y evidenciar de forma temprana los puntos críticos, riesgos y oportunidades de innovación tecnológica para ambos segmentos objetivo.

A continuación, se detalla el desarrollo secuencial del taller a través de sus fases progresivas:

---

### 2.4.1. Fase 1: Generación Abierta de Eventos (Open Space)

En esta fase inicial divergente, los integrantes del equipo registraron de manera abierta y sin restricciones de orden cronológico todos los eventos significativos ocurridos dentro del dominio de negocio (*Domain Events*), redactados estrictamente en tiempo verbal pasado sobre notas adhesivas de color naranja. El levantamiento abarcó todo el ciclo de vida de la interacción comercial y operativa: desde el registro e inicio de sesión de los usuarios, la afiliación de bodegas, la publicación y actualización de ofertas, el armado de canastas básicas y listas de compras, hasta la proyección presupuestaria, el cálculo de trayectos óptimos y la confirmación final de compra en el establecimiento físico.

<div align="center">
  <img src="../assets/ddd/big-picture/big-picture-open.png" alt="Big Picture - Open Space" width="850"/>
  <p><em>Figura 2.13: Fase Open Space del Big Picture Event Storming, lluvia de ideas y registro de eventos de dominio para Preciazo.</em></p>
</div>

---

### 2.4.2. Fase 2: Exploración y Línea de Tiempo (Explore)

Durante la fase de exploración y convergencia, el equipo estructuró una línea temporal secuencial orientando los eventos de dominio de izquierda a derecha según el flujo natural de las operaciones. En este análisis se incorporaron notas de color rojo/rosado para identificar puntos de dolor, cuellos de botella e incertidumbres críticas del dominio (*Hotspots*). Entre las fricciones expuestas destacaron la discrepancia entre precios exhibidos digitalmente y los cobrados en caja registradora, la saturación del tráfico limeño que encarece los traslados físicos, los quiebres imprevistos de stock en comercios minoristas y el riesgo de abandono de la plataforma ante interfaces complejas.

<div align="center">
  <img src="../assets/ddd/big-picture/big-picture-explore.png" alt="Big Picture - Explore" width="850"/>
  <p><em>Figura 2.14: Fase Explore del Big Picture Event Storming, ordenamiento cronológico sobre la línea de tiempo y detección de Hotspots.</em></p>
</div>

---

### 2.4.3. Fase 3: Consolidación y Definición de Triggers (Close Space)

En el cierre del espacio de exploración, se refinó la línea temporal eliminando duplicidades y clarificando las transiciones del sistema. Se integraron los comandos desencadenantes (*Commands* / post-it azules) que representan las intenciones y acciones operadas por los actores primarios (el comprador independiente y el comerciante minorista), así como las políticas y reglas de negocio reactivas (*Policies* / post-it lilas). Estas políticas modelan la lógica automática del sistema, tales como la emisión de alertas preventivas cuando el costo acumulado de la canasta supera el presupuesto límite, la sugerencia de artículos sustitutos ante falta de existencias y la reconfiguración dinámica de rutas ante alertas de congestión vehicular.

<div align="center">
  <img src="../assets/ddd/big-picture/big-picture-close.png" alt="Big Picture - Close Space" width="850"/>
  <p><em>Figura 2.15: Fase Close Space del Big Picture Event Storming, articulación de actores, comandos ejecutores y políticas de dominio.</em></p>
</div>

---

### 2.4.4. Fase 4: Modelo Final del Dominio (Final Landscape)

Como resultado definitivo del taller colaborativo, se consolidó el mapa general del dominio (*Business Landscape*) para la plataforma **Preciazo**, estructurado por el equipo de **PeruTech**. Este artefacto articula de forma holística los eventos, comandos, reglas y sistemas externos en torno a los subdominios clave del negocio: gestión de perfiles e identidad (consumidores y comercios afiliados), catálogo estructurado de productos y tarifas en góndola, planificación colaborativa de presupuestos familiares, y motor de geolocalización para optimización de rutas comerciales.

<div align="center">
  <img src="../assets/ddd/big-picture/big-picture-final.png" alt="Big Picture - Modelo Final" width="850"/>
  <p><em>Figura 2.16: Modelo consolidado del Big Picture Event Storming para Preciazo, desarrollado por el equipo de PeruTech.</em></p>
</div>

---

### 2.5. Ubiquitous Language

En esta sección se define el *Ubiquitous Language* (Lenguaje Ubicuo) para el dominio de Preciazo, desarrollado por la startup PeruTech, siguiendo los principios de modelado estratégico de *Domain-Driven Design* (DDD) formulados por Eric Evans. Este glosario formal unifica el vocabulario compartido entre los desarrolladores, los expertos del dominio y los usuarios finales (consumidores y comerciantes), eliminando ambigüedades operativas. Se enfoca estrictamente en términos de la dinámica comercial minorista, abastecimiento presencial y movilidad urbana:

* **Affiliated Store (Tienda Afiliada):** Establecimiento comercial físico (bodega, minimarket o puesto de abastos) cuyos datos registrales han sido formalmente validados para exhibir su catálogo y ofertas en la plataforma.
* **Affiliation Request (Solicitud de Afiliación):** Trámite inicial mediante el cual un comerciante minorista registra los datos de su negocio y su identificación fiscal para integrarse a la red del sistema.
* **Basic Basket (Canasta Básica):** Conjunto estructurado de bienes y alimentos de primera necesidad requeridos para el consumo periódico de una persona o grupo familiar.
* **Crowdsourced Verification (Verificación Colaborativa):** Mecanismo mediante el cual la comunidad de compradores confirma, actualiza o reporta la vigencia de los precios y el stock físico observado en góndola.
* **Multi-stop Route (Ruta Multiparada):** Itinerario secuencial de desplazamiento físico que conecta el punto de origen del comprador con múltiples locales comerciales optimizados geográficamente.
* **Net Savings (Ahorro Neto):** Diferencia económica positiva resultante de deducir el gasto logístico de transporte (pasajes o combustible) del ahorro monetario bruto obtenido por la dispersión de precios en góndola.
* **Optimal Purchase Stop (Punto Óptimo de Compra):** Establecimiento comercial sugerido por el sistema al ofrecer el mejor balance entre proximidad geográfica, disponibilidad de artículos y menor precio de canasta.
* **Price Discrepancy (Discrepancia de Precio):** Desfase identificado entre el precio de venta publicado digitalmente o exhibido en anaquel y el importe real cobrado en la caja registradora.
* **Price Dispersion (Dispersión de Precios):** Variación del precio de venta de un mismo producto idéntico entre distintos establecimientos comerciales de una misma zona o distrito.
* **Product Catalog (Catálogo de Productos):** Conjunto indexado de artículos y bienes de consumo masivo clasificados por marca, categoría y presentación estándar.
* **Purchase Budget (Presupuesto de Compra):** Techo financiero monetario definido por el consumidor antes de salir a comprar para controlar su nivel de gasto.
* **Purchase Item (Artículo de Compra):** Bien individual definido por nombre, marca, formato y unidad de medida que integra la lista de compras del usuario.
* **Retail Store (Comercio Minorista):** Punto de venta físico dedicado a la comercialización directa de bienes de consumo al comprador presencial.
* **Shopping List (Lista de Compras):** Registro organizado de los artículos que el consumidor planifica adquirir durante su jornada de compra.
* **Store Administrator (Administrador de Tienda):** Propietario o encargado formal del establecimiento comercial responsable de la publicación de precios, control de promociones y gestión del perfil del local.
* **Store Offer (Oferta de Tienda):** Reducción temporal de precio o promoción especial publicada por un comercio afiliado para incentivar la afluencia de compradores locales.
* **Substituted Good (Bien Sustituto):** Producto de características o valor nutricional equivalente que el comprador selecciona como alternativa cuando el artículo preferente no tiene stock o excede su presupuesto.
* **SUNAT Verification (Validación SUNAT):** Verificación del estado del Registro Único de Contribuyentes (RUC) y la condición fiscal activa del comercio antes de habilitar su visibilidad pública.
* **Transit Overhead (Sobrecosto de Desplazamiento):** Demora temporal y gasto adicional de movilidad en los que incurre un comprador debido al tráfico urbano o a la lejanía entre tiendas.
* **Unit Price (Precio Unitario):** Costo por unidad estándar de medida (kilogramo, litro, paquete) que permite comparar con equidad el valor real de productos con diferentes tamaños de empaque.


# Capítulo III: Requirements Specification

## 3.1. User Stories
---

En esta sección se especifican los requisitos funcionales y técnicos de la plataforma **Preciazo** (desarrollada por **PeruTech**) mediante Epics, User Stories y Technical Stories, derivados de los hallazgos cualitativos del proceso de Needfinding, las entrevistas a usuarios y el modelado del dominio de negocio. La redacción sigue el enfoque de diseño centrado en el usuario, estructurando cada descripción bajo el estándar formal de rol, necesidad y beneficio (*"Como [rol], deseo [necesidad] para [beneficio]"*).

Asimismo, los criterios de aceptación se definen bajo la sintaxis formal de Gherkin (*Given-When-Then*), redactados en tiempo presente, tercera persona y prescindiendo de detalles de interfaz gráfica (como botones, pantallas o clics), asegurando su comprobabilidad tanto en la experiencia web interactiva como en los contratos de servicio del RESTful API.

A continuación, se definen los Epics identificados que agrupan funcionalmente los requisitos del sistema:
* **EP01: Plataforma Informativa y Landing Page:** Difusión pública del servicio, propuesta de valor y captación de visitantes.
* **EP02: Gestión de Identidad y Perfiles:** Registro, autenticación y configuración de preferencias para compradores y comercios.
* **EP03: Planificación y Control Presupuestario:** Elaboración de listas de compras y control financiero preventivo en tiempo real.
* **EP04: Comparación de Mercado y Ruteo Inteligente:** Comparativa multiestablecimiento, optimización de traslados y bienes sustitutos.
* **EP05: Gestión de Ofertas y Catálogo Minorista:** Administración simplificada de precios, promociones y existencias para comercios barriales.
* **EP06: Inteligencia Colectiva y Moderación Comunitaria:** Verificación colaborativa de precios en góndola y reporte de discrepancias.
* **EP07: Núcleo de Servicios Backend y RESTful API:** Servicios de backend, endpoints de integración y reglas de persistencia.

| Epic / Story ID | Título | Descripción | Criterios de Aceptación | Relacionado con (Epic ID) |
| :--- | :--- | :--- | :--- | :--- |
| **US01** | Landing: Propuesta de valor | Como visitante, deseo visualizar la propuesta central del servicio para comprender cómo optimizar mis compras y tiempos de traslado. | **Escenario 1: Carga inicial de la propuesta.**<br>Dado que el visitante accede al sitio web estático, cuando se completa la carga inicial, entonces visualiza el mensaje central enfocado en la comparación multiestablecimiento y el cálculo de rutas de compra.<br><br>**Escenario 2: Comprensión del valor diferencial.**<br>Dado que el visitante se desplaza hacia la sección de beneficios, cuando revisa la información comparativa, entonces comprende el impacto de la dispersión de precios entre comercios minoristas y tiendas de conveniencia.<br><br>**Escenario 3: Adaptabilidad de visualización.**<br>Dado que el visitante accede desde un navegador web móvil, cuando visualiza el contenido, entonces la disposición de los bloques y textos se adapta fluidamente sin desbordamientos ni solapamientos. | EP01 |
| **US02** | Landing: Segmentos objetivo | Como visitante, deseo conocer a qué perfiles está orientada la solución para identificar si resuelve mis necesidades de abastecimiento o comercio. | **Escenario 1: Visualización diferenciada por segmento.**<br>Dado que el visitante navega en la sección de perfiles, cuando interactúa con los módulos informativos, entonces visualiza las funciones orientadas al Comprador Independiente y al Comerciante Minorista.<br><br>**Escenario 2: Redirección hacia registro.**<br>Dado que el visitante selecciona el llamado a la acción correspondiente a su perfil, cuando ejecuta la acción, entonces es derivado al flujo de registro respectivo en la aplicación web. | EP01 |
| **US03** | Landing: Red de comercios aliados | Como visitante, deseo visualizar qué establecimientos y zonas cuentan con cobertura para verificar la disponibilidad del servicio. | **Escenario 1: Consulta de locales asociados.**<br>Dado que el visitante consulta la sección de comercios, cuando visualiza la red registrada, entonces se listan los tipos de establecimientos minoristas participantes agrupados por sectores urbanos.<br><br>**Escenario 2: Explicación de cobertura.**<br>Dado que el visitante revisa el alcance geográfico, cuando consulta las zonas activas, entonces visualiza los distritos con presencia y densidad de datos comerciales comprobados. | EP01 |
| **US04** | Landing: Registro de interés | Como visitante, deseo suscribir mi correo electrónico para recibir notificaciones sobre el lanzamiento y novedades de la plataforma. | **Escenario 1: Registro exitoso de correo.**<br>Dado que el visitante introduce una dirección de correo con sintaxis válida, cuando confirma el envío, entonces el sistema almacena el registro y emite un mensaje de suscripción exitosa.<br><br>**Escenario 2: Validación de sintaxis errónea.**<br>Dado que el visitante ingresa un formato de correo inválido, cuando intenta enviar los datos, entonces el sistema impide el envío y solicita la corrección del texto ingresado.<br><br>**Escenario 3: Correo previamente registrado.**<br>Dado que el correo ingresado ya existe en la lista de difusión, cuando se procesa la solicitud, entonces el sistema informa que la dirección ya cuenta con una suscripción activa. | EP01 |
| **US05** | Landing: Preguntas frecuentes y soporte | Como visitante, deseo consultar una sección de preguntas frecuentes para aclarar el modelo de servicio y los canales de contacto. | **Escenario 1: Visualización de preguntas frecuentes.**<br>Dado que el visitante accede a la sección informativa, cuando consulta los tópicos de ayuda, entonces el sistema despliega las respuestas sobre el funcionamiento del comparador y las condiciones para comercios afiliados.<br><br>**Escenario 2: Envío de consulta de soporte.**<br>Dado que el visitante completa el formulario de contacto con datos válidos, cuando confirma el envío, entonces el sistema registra el mensaje y emite una confirmación de recepción. | EP01 |
| **US06** | Autenticación y acceso | Como comprador independiente, deseo iniciar sesión con mis credenciales registradas para gestionar mis listas y presupuesto. | **Escenario 1: Inicio de sesión válido.**<br>Dado que el usuario introduce credenciales registradas y correctas, cuando solicita el ingreso, entonces el sistema valida la identidad y da acceso al entorno principal.<br><br>**Escenario 2: Credenciales no coincidentes.**<br>Dado que el usuario ingresa una combinación incorrecta de credenciales, cuando intenta iniciar sesión, entonces el sistema deniega el acceso y muestra una notificación de autenticación fallida.<br><br>**Escenario 3: Bloqueo por seguridad.**<br>Dado que se registran múltiples intentos fallidos consecutivos, cuando se alcanza el umbral de seguridad, entonces el sistema bloquea temporalmente el acceso y solicita comprobación de seguridad. | EP02 |
| **US07** | Gestión de comercios favoritos | Como comprador independiente, deseo guardar mis establecimientos de confianza para priorizar sus ofertas en mis consultas diarias. | **Escenario 1: Asignación de comercio preferente.**<br>Dado que el usuario marca un local como habitual, cuando realiza búsquedas de canasta, entonces el sistema prioriza los precios de dicho establecimiento en la vista de resultados.<br><br>**Escenario 2: Retiro de preferencia.**<br>Dado que el usuario desmarca el local de su lista de favoritos, cuando actualiza sus parámetros, entonces el sistema restablece el ordenamiento geográfico estándar. | EP02 |
| **US08** | Creación de lista de compras | Como comprador independiente, deseo crear una lista de productos requeridos para estructurar mi jornada de abastecimiento. | **Escenario 1: Inicialización de lista.**<br>Dado que el usuario inicia la confección de una lista, cuando define un nombre identificador, entonces el sistema genera el contenedor de compras asociado a su perfil.<br><br>**Escenario 2: Asignación por defecto.**<br>Dado que el usuario omite asignar un nombre específico, cuando confirma la creación, entonces el sistema asigna una denominación automática basada en la fecha y hora actual. | EP03 |
| **US09** | Agregado de ítems a la lista | Como comprador independiente, deseo buscar y agregar artículos específicos a mi lista para consolidar mi canasta básica. | **Escenario 1: Inclusión de artículo.**<br>Dado que el usuario localiza un producto en el catálogo general, cuando define la cantidad requerida, entonces el artículo se vincula a su lista activa.<br><br>**Escenario 2: Incremento de cantidad existente.**<br>Dado que un artículo ya forma parte de la lista, cuando el usuario lo selecciona nuevamente, entonces el sistema suma la cantidad ingresada sin generar registros duplicados. | EP03 |
| **US10** | Fijación de presupuesto límite | Como comprador independiente, deseo configurar un tope de gasto para mi lista de compras para controlar mi economía personal. | **Escenario 1: Configuración de umbral.**<br>Dado que el usuario introduce un monto monetario mayor a cero, cuando guarda el parámetro, entonces el sistema fija dicho valor como umbral máximo para la lista.<br><br>**Escenario 2: Entrada no válida.**<br>Dado que el usuario introduce un monto menor o igual a cero, cuando intenta guardar el parámetro, entonces el sistema descarta el valor y solicita un importe válido. | EP03 |
| **US11** | Alerta de rebase presupuestario | Como comprador independiente, deseo recibir una advertencia cuando la sumatoria de mi lista supere el presupuesto establecido para ajustar mi selección. | **Escenario 1: Detección de exceso presupuestario.**<br>Dado que la suma del costo proyectado de los artículos supera el límite fijado, cuando se agrega un nuevo producto, entonces el sistema emite una alerta visual de exceso presupuestario.<br><br>**Escenario 2: Restablecimiento del límite.**<br>Dado que el usuario retira productos o reduce cantidades, cuando el monto total vuelve a estar dentro del presupuesto permitido, entonces la alerta se desactiva de forma automática. | EP03 |
| **US12** | Modo de jornada de compra en local | Como comprador independiente, deseo marcar los artículos conforme los coloco en mi canasta para verificar el gasto acumulado en tiempo real. | **Escenario 1: Marcado de artículo adquirido.**<br>Dado que el usuario se encuentra en el local comercial, cuando marca un producto como recogido, entonces el sistema lo señala como adquirido y suma su importe al total proyectado en caja.<br><br>**Escenario 2: Desmarcado de producto.**<br>Dado que el usuario decide descartar un producto previamente marcado, cuando revierte la selección, entonces el sistema descuenta el importe del total acumulado. | EP03 |
| **US13** | Comparativa multiestablecimiento | Como comprador independiente, deseo comparar el costo total de mi lista entre locales comerciales cercanos para identificar el menor costo de compra. | **Escenario 1: Generación de tabla comparativa.**<br>Dado que la lista de compras cuenta con artículos definidos, cuando el usuario solicita la comparativa, entonces el sistema presenta los comercios ordenados por el costo total de la canasta.<br><br>**Escenario 2: Disponibilidad parcial de productos.**<br>Dado que un comercio no dispone de la totalidad de los artículos de la lista, cuando se procesa la comparativa, entonces el sistema advierte qué productos se encuentran ausentes en dicho punto. | EP04 |
| **US14** | Cálculo de ruta de compra eficiente | Como comprador independiente, deseo obtener un itinerario secuencial de paradas óptimas para reducir mi tiempo de traslado y costo de transporte. | **Escenario 1: Generación de itinerario de paradas.**<br>Dado que el usuario selecciona los locales comerciales de compra, cuando solicita la optimización de traslado, entonces el sistema genera una secuencia de recorrido que minimiza la distancia total a recorrer.<br><br>**Escenario 2: Estimación de tiempos de viaje.**<br>Dado que se calcula la ruta entre los establecimientos, cuando se despliega el resumen del itinerario, entonces se indica el tiempo estimado global considerando la modalidad de traslado seleccionada. | EP04 |
| **US15** | Sugerencia de bienes sustitutos | Como comprador independiente, deseo recibir recomendaciones de productos alternativos más económicos para disminuir el monto total a pagar. | **Escenario 1: Detección de sustituto accesible.**<br>Dado que un producto seleccionado posee un sustituto de características análogas a menor costo, cuando se evalúa la lista, entonces el sistema sugiere el cambio de artículo indicando el ahorro potencial.<br><br>**Escenario 2: Aplicación del cambio.**<br>Dado que el usuario acepta la alternativa sugerida, cuando confirma el reemplazo, entonces el sistema actualiza la lista y recalcula de forma inmediata el total estimado. | EP04 |
| **US16** | Comparación por unidad de medida | Como comprador independiente, deseo comparar el costo por unidad de medida (kilogramo o litro) para evaluar presentaciones con distinto gramaje. | **Escenario 1: Cálculo de precio normalizado.**<br>Dado que los artículos cuentan con peso o volumen registrado, cuando el usuario visualiza la comparativa, entonces el sistema calcula y exhibe el costo por unidad estándar de medida.<br><br>**Escenario 2: Omisión por datos insuficientes.**<br>Dado que un artículo carece del registro de gramaje en su ficha técnica, cuando se procesa la comparativa, entonces el sistema omite el cálculo unitario mostrando únicamente el precio final en góndola. | EP04 |
| **US17** | Búsqueda por filtros de proximidad | Como comprador independiente, deseo filtrar comercios dentro de un radio caminable específico para evitar traslados excesivamente largos. | **Escenario 1: Aplicación de radio de búsqueda.**<br>Dado que el usuario define una distancia máxima de desplazamiento (ej. 800 metros), cuando ejecuta la búsqueda, entonces el sistema restringe los resultados a los comercios situados dentro del perímetro señalado.<br><br>**Escenario 2: Ausencia de locales en el perímetro.**<br>Dado que no existen establecimientos dentro del radio fijado, cuando concluye la consulta, entonces el sistema sugiere ampliar el rango de búsqueda al siguiente intervalo disponible. | EP04 |
| **US18** | Registro de compras recurrentes | Como comprador independiente, deseo guardar una canasta base como plantilla para reutilizarla en compras quincenales sin reingresar productos. | **Escenario 1: Guardado de plantilla.**<br>Dado que el usuario concluye una lista de compras, cuando la guarda como plantilla recurrente, entonces el sistema genera una copia maestra en su perfil.<br><br>**Escenario 2: Instanciación de nueva lista.**<br>Dado que el usuario inicia un nuevo ciclo de compra, cuando selecciona su plantilla guardada, entonces el sistema genera una lista activa con los precios actualizados a la fecha. | EP03 |
| **US19** | Historial de precios de producto | Como comprador independiente, deseo consultar la evolución histórica del valor de un bien para evaluar la conveniencia de una oferta. | **Escenario 1: Consulta de variación temporal.**<br>Dado que el usuario selecciona un artículo específico, cuando consulta su registro de variaciones, entonces el sistema exhibe el comportamiento de su precio durante los últimos 30 días.<br><br>**Escenario 2: Ausencia de histórico.**<br>Dado que un artículo es de reciente incorporación, cuando se solicita su histórico, entonces el sistema informa que solo se cuenta con el precio de registro inicial. | EP04 |
| **US20** | Recálculo dinámico de ruta | Como comprador independiente, deseo reordenar mi trayecto de compra si un local se encuentra cerrado o inaccesible. | **Escenario 1: Omisión de parada.**<br>Dado que el usuario omite un establecimiento de su itinerario activo, cuando confirma la modificación, entonces el algoritmo recalcula la secuencia restante minimizando la distancia.<br><br>**Escenario 2: Reasignación de comercio.**<br>Dado que el usuario solicita un reemplazo para el local omitido, cuando el sistema evalúa la zona, entonces asigna la tienda cercana con el siguiente mejor precio de canasta. | EP04 |
| **US21** | Registro y afiliación de tienda | Como comerciante minorista, deseo registrar los datos de mi establecimiento para integrar mi negocio al mapa comercial de la plataforma. | **Escenario 1: Ingreso de datos registrales.**<br>Dado que el comerciante remite su RUC, razón social, dirección y coordenadas geográficas, cuando envía la solicitud, entonces el sistema genera el registro en estado pendiente de validación fiscal.<br><br>**Escenario 2: Control de duplicidad comercial.**<br>Dado que el identificador fiscal ingresado ya se encuentra registrado, cuando se procesa la solicitud, entonces el sistema notifica la existencia previa de la tienda impidiendo registros repetidos. | EP02 |
| **US22** | Configuración de horarios comerciales | Como comerciante minorista, deseo indicar los horarios de atención de mi local para que los compradores conozcan cuándo pueden acudir. | **Escenario 1: Registro de turno regular.**<br>Dado que el comerciante especifica sus horas de apertura y cierre por día de la semana, cuando guarda los parámetros, entonces el sistema despliega el estado de atención en el mapa de ruta.<br><br>**Escenario 2: Actualización de estado en tiempo real.**<br>Dado que la hora del sistema se encuentra fuera del rango configurado, cuando un comprador consulta el comercio, entonces el sistema indica que el local se encuentra cerrado. | EP02 |
| **US23** | Publicación de precios en catálogo | Como comerciante minorista, deseo registrar y actualizar los precios de venta de mis productos para mantener informados a los compradores de la zona. | **Escenario 1: Actualización de precio unitario.**<br>Dado que el comerciante selecciona un producto de su inventario, cuando ingresa un nuevo valor de venta y confirma la acción, entonces el sistema actualiza el dato en el catálogo público.<br><br>**Escenario 2: Validación de valor positivo.**<br>Dado que el comerciante ingresa un monto menor o igual a cero, cuando intenta guardar el cambio, entonces el sistema rechaza el valor solicitando un precio de venta positivo. | EP05 |
| **US24** | Publicación de ofertas de tienda | Como comerciante minorista, deseo publicar promociones por tiempo limitado para acelerar la rotación de artículos y atraer mayor afluencia. | **Escenario 1: Creación de promoción.**<br>Dado que el comerciante define un producto, precio rebajado y rango de vigencia temporal, cuando activa la oferta, entonces el sistema la expone como oferta especial en el sector geográfico.<br><br>**Escenario 2: Caducidad automática de oferta.**<br>Dado que se alcanza la fecha u hora límite de la promoción, cuando expira el periodo, entonces el sistema retira la condición de oferta restableciendo el precio habitual. | EP05 |
| **US25** | Reporte de agotamiento de stock | Como comerciante minorista, deseo marcar artículos sin disponibilidad física en mi local para evitar desplazamientos infructuosos de los clientes. | **Escenario 1: Cambio a estado sin stock.**<br>Dado que un producto agota sus existencias en tienda, cuando el comerciante actualiza su disponibilidad en el panel, entonces el sistema lo excluye de los cálculos inmediatos de canasta para ese local.<br><br>**Escenario 2: Restablecimiento de existencias.**<br>Dado que el local repone existencias, cuando el comerciante marca nuevamente el artículo como disponible, entonces se reactiva su visibilidad en el comparador zonal. | EP05 |
| **US26** | Carga estructurada de catálogo | Como comerciante minorista, deseo importar una lista estructurada de artículos y precios para actualizar mi inventario de forma ágil. | **Escenario 1: Procesamiento de archivo de inventario.**<br>Dado que el comerciante remite un archivo de datos con el formato y columnas requeridas, cuando el sistema procesa el contenido, entonces actualiza los registros de precios y existencias en el catálogo del local.<br><br>**Escenario 2: Detección de inconsistencias de formato.**<br>Dado que el archivo remitido presenta celdas vacías o valores numéricos erróneos, cuando el validador analiza el documento, entonces cancela la importación e indica las líneas con errores para su corrección. | EP05 |
| **US27** | Panel de rendimiento comercial | Como comerciante minorista, deseo consultar métricas de visualización de mis promociones para evaluar el impacto de mis precios publicados. | **Escenario 1: Conteo de apariciones en rutas.**<br>Dado que los compradores generan itinerarios en la zona, cuando el comerciante ingresa a su panel de control, entonces visualiza la cantidad de veces que su establecimiento fue sugerido como parada óptima durante el mes.<br><br>**Escenario 2: Métricas de ofertas consultadas.**<br>Dado que el comerciante mantiene promociones vigentes, cuando consulta las estadísticas, entonces visualiza el número de usuarios que interactuaron con sus productos destacados. | EP05 |
| **US28** | Reporte colaborativo de discrepancia | Como comprador independiente, deseo reportar cuando un precio en góndola difiere del valor registrado en el sistema para colaborar con la comunidad. | **Escenario 1: Envío de reporte de precio.**<br>Dado que el usuario detecta un precio distinto en góndola, cuando remite el nuevo valor observado, entonces el sistema genera un evento de verificación comunitaria.<br><br>**Escenario 2: Control de valores anómalos.**<br>Dado que el usuario remite un valor extremadamente desproporcionado respecto a la media histórica, cuando se procesa el reporte, entonces el sistema lo retiene para moderación. | EP06 |
| **US29** | Confirmación comunitaria de datos | Como comprador independiente, deseo validar los reportes de precios efectuados por otros usuarios para consolidar la confiabilidad de la información. | **Escenario 1: Aprobación de reporte.**<br>Dado que un comprador se encuentra en el establecimiento y verifica el precio reportado, cuando emite su confirmación favorable, entonces el sistema incrementa el índice de confianza del dato.<br><br>**Escenario 2: Rechazo de información errónea.**<br>Dado que un comprador constata que el precio reportado no es verídico, cuando emite una calificación desfavorable, entonces el sistema disminuye la confiabilidad del reporte. | EP06 |
| **TS01** | API de autenticación y tokens | Como Developer, deseo implementar el endpoint de autenticación con JWT para asegurar el acceso a los servicios de la plataforma. | **Escenario 1: Emisión exitosa de JWT.**<br>Dado un requerimiento POST a `/api/v1/auth/login` con credenciales válidas en formato JSON, cuando el servicio valida la identidad del usuario, entonces responde con un código HTTP 200 OK y el token de acceso correspondiente.<br><br>**Escenario 2: Denegación de acceso.**<br>Dado un requerimiento POST a `/api/v1/auth/login` con contraseña no coincidente, cuando el servicio procesa la solicitud, entonces responde con un código HTTP 401 Unauthorized y el mensaje de error respectivo. | EP07 |
| **TS02** | API de cálculo comparativo de canasta | Como Developer, deseo proveer un endpoint para computar el costo total de una lista de productos en los comercios registrados en un radio geográfico. | **Escenario 1: Procesamiento comparativo exitoso.**<br>Dado un requerimiento POST a `/api/v1/baskets/compare` con la lista de identificadores de productos y coordenadas geográficas, cuando el motor calcula las sumatorias, entonces responde con un código HTTP 200 OK y la lista de comercios con sus montos totales calculados.<br><br>**Escenario 2: Solicitud con lista vacía.**<br>Dado un requerimiento POST con un cuerpo sin artículos, cuando el controlador evalúa la petición, entonces responde con un código HTTP 400 Bad Request indicando la ausencia de datos. | EP07 |
| **TS03** | API de optimización de rutas | Como Developer, deseo proveer un endpoint que ordene una secuencia de establecimientos según eficiencia de traslado. | **Escenario 1: Cálculo de itinerario óptimo.**<br>Dado un requerimiento POST a `/api/v1/routes/optimize` conteniendo coordenadas de origen y paradas seleccionadas, cuando se procesa el ordenamiento, entonces responde con un código HTTP 200 OK entregando las paradas ordenadas y la distancia acumulada.<br><br>**Escenario 2: Punto inalcanzable.**<br>Dado un requerimiento cuyas coordenadas no cuentan con conexión vial viable, cuando falla el algoritmo de ruteo, entonces responde con un código HTTP 422 Unprocessable Entity y la descripción del fallo. | EP07 |
| **TS04** | API de validación fiscal de establecimientos | Como Developer, deseo integrar un servicio de verificación de RUC contra entidades oficiales para constatar la vigencia legal de los comercios afiliados. | **Escenario 1: Verificación de comercio activo.**<br>Dado un requerimiento GET a `/api/v1/merchants/validate-ruc/{ruc}` con un identificador válido de 11 dígitos, cuando el servicio consulta la fuente registral, entonces responde con un código HTTP 200 OK y el estado formal del contribuyente.<br><br>**Escenario 2: Tiempo de respuesta excedido.**<br>Dado que el servicio externo de consulta fiscal demora más de 5000 milisegundos, cuando expira el tiempo límite, entonces el servicio responde con un código HTTP 504 Gateway Timeout controlado sin suspender la ejecución del sistema. | EP07 |
| **TS05** | API de sincronización de catálogo | Como Developer, deseo proveer un endpoint para la actualización en bloque de inventario de tiendas mediante solicitudes en formato JSON. | **Escenario 1: Recepción de lote de productos.**<br>Dado un requerimiento PUT a `/api/v1/merchants/{id}/inventory` con un arreglo de artículos y precios, cuando el servicio valida la estructura, entonces actualiza la base de datos y responde con un código HTTP 200 OK.<br><br>**Escenario 2: Solicitud con identificador no autorizado.**<br>Dado un requerimiento con credenciales que no corresponden al establecimiento consultado, cuando se procesa la llamada, entonces el servicio responde con un código HTTP 403 Forbidden. | EP07 |
| **TS06** | API de consulta de catálogo zonal | Como Developer, deseo proveer un endpoint con paginación para consultar artículos disponibles por categoría y distrito. | **Escenario 1: Consulta paginada exitosa.**<br>Dado un requerimiento GET a `/api/v1/products?category={cat}&district={dist}&page=0&size=20`, cuando el servicio ejecuta la consulta, entonces responde con un código HTTP 200 OK y el listado ordenado de productos.<br><br>**Escenario 2: Parámetros de paginación inválidos.**<br>Dado un requerimiento con un valor de página negativo, cuando el controlador evalúa la petición, entonces responde con un código HTTP 400 Bad Request. | EP07 |
| **TS07** | API de registro de eventos de reporte | Como Developer, deseo implementar un endpoint para almacenar las confirmaciones y discrepancias emitidas por los usuarios sobre los precios. | **Escenario 1: Registro de reporte comunitario.**<br>Dado un requerimiento POST a `/api/v1/reports/prices` con el ID del producto, ID de tienda y nuevo precio, cuando el servicio procesa la solicitud, entonces persiste el reporte y responde con un código HTTP 201 Created.<br><br>**Escenario 2: Reporte duplicado en ventana temporal.**<br>Dado un usuario que intenta emitir múltiples reportes sobre el mismo artículo en menos de 60 segundos, cuando el filtro de seguridad lo detecta, entonces responde con un código HTTP 429 Too Many Requests. | EP07 |
| **TS08** | API de gestión de promociones de tienda | Como Developer, deseo implementar endpoints CRUD para la administración del ciclo de vida de ofertas emitidas por comerciantes. | **Escenario 1: Creación de promoción.**<br>Dado un requerimiento POST a `/api/v1/promotions` con artículo, precio y vigencia, cuando el servicio confirma la titularidad del local, entonces crea la oferta y responde con un código HTTP 201 Created.<br><br>**Escenario 2: Vigencia incoherente.**<br>Dado un requerimiento cuya fecha de fin es anterior a la fecha de inicio, cuando el modelo valida los datos, entonces responde con un código HTTP 422 Unprocessable Entity. | EP07 |

## 3.2. Impact Mapping

En esta sección se presenta el *Impact Mapping* desarrollado para alinear los objetivos estratégicos de negocio con las capacidades funcionales de la plataforma **Preciazo** de **PeruTech**. Mediante este artefacto visual se establece la trazabilidad formal entre los objetivos medibles de la organización (*Business Goals* formulados bajo el estándar SMART), los actores clave (*Actors/Personas*), los cambios esperados de comportamiento (*Impacts*), las entregas o soluciones de software (*Deliverables*) y las historias de usuario asociadas en formato canónico (*User Stories*).

### Business Goals del Proyecto (Criterios SMART)
* **BG01:** Reducir en un 15% el gasto promedio quincenal de canasta básica y en un 20% el tiempo invertido en desplazamientos para 10,000 compradores urbanos independientes en Lima Metropolitana durante los primeros 6 meses de operación.
* **BG02:** Incrementar la base de retención activa mensual (MAU) de compradores al 35% en los primeros 4 meses mediante el uso de listas de compras con presupuesto dinámico.
* **BG03:** Afiliar a 500 comercios minoristas locales (bodegas y minimarkets) en distritos de alta densidad comercial durante los primeros 6 meses, logrando que al menos el 60% actualice su catálogo semanalmente.
* **BG04:** Incrementar en un 20% la rotación de mercancías y liquidaciones en tiendas de proximidad afiliadas durante el primer trimestre de suscripción activa.

---

### 3.2.1. Impact Mapping - Segmento #1: Comprador Independiente

Este mapa articula cómo el actor **Fernando Justiniano** colabora en la consecución de las metas de ahorro, reducción de tiempos y fidelización del comprador.

<img src="../assets/Impact-Map Fernando-Justiniano-(Comprador-multitienda).png" width="850" />

*Figura 3.1: Impact Mapping para el Segmento Comprador Independiente.*

#### Desglose de Relaciones y User Stories Asociadas:
* **Impacto 1: Compara precios de su canasta completa entre tiendas cercanas de forma instantánea sin visitar físicamente cada local.**
  * *Deliverable: EP04 - Motor de Comparativa y Optimización de Rutas.*
    * **US13:** Como comprador independiente, deseo comparar el costo total de mi lista entre locales comerciales cercanos para identificar el menor costo de compra.
    * **US15:** Como comprador independiente, deseo recibir recomendaciones de productos alternativos más económicos para disminuir el monto total a pagar.
    * **US16:** Como comprador independiente, deseo comparar el costo por unidad de medida (kilogramo o litro) para evaluar presentaciones con distinto gramaje.
    * **US17:** Como comprador independiente, deseo filtrar comercios dentro de un radio caminable específico para evitar traslados excesivamente largos.
  * *Deliverable: EP07 - Servicios API RESTful.*
    * **TS02:** Como Developer, deseo proveer un endpoint para computar el costo total de una lista de productos en los comercios registrados en un radio geográfico.
    * **TS06:** Como Developer, deseo proveer un endpoint con paginación para consultar artículos disponibles por categoría y distrito.

* **Impacto 2: Minimiza el tiempo de recorrido y distancia caminada en sus jornadas de compra.**
  * *Deliverable: EP04 - Motor de Comparativa y Optimización de Rutas.*
    * **US14:** Como comprador independiente, deseo obtener un itinerario secuencial de paradas óptimas para reducir mi tiempo de traslado y costo de transporte.
  * *Deliverable: EP07 - Servicios API RESTful.*
    * **TS03:** Como Developer, deseo proveer un endpoint que ordene una secuencia de establecimientos según eficiencia de traslado.

* **Impacto 3: Planifica y controla el techo de gasto de sus compras para no sobrepasar su presupuesto personal.**
  * *Deliverable: EP03 - Gestión de Listas de Compras y Presupuesto.*
    * **US08:** Como comprador independiente, deseo crear una lista de productos requeridos para estructurar mi jornada de abastecimiento.
    * **US09:** Como comprador independiente, deseo buscar y agregar artículos específicos a mi lista para consolidar mi canasta básica.
    * **US10:** Como comprador independiente, deseo configurar un tope de gasto para mi lista de compras para controlar mi economía personal.
    * **US11:** Como comprador independiente, deseo recibir una advertencia cuando la sumatoria de mi lista supere el presupuesto establecido para ajustar mi selección.
    * **US12:** Como comprador independiente, deseo marcar los artículos conforme los coloco en mi canasta para verificar el gasto acumulado en tiempo real.
  * *Deliverable: EP02 - Autenticación y Perfil.*
    * **US06:** Como comprador independiente, deseo iniciar sesión con mis credenciales registradas para gestionar mis listas y presupuesto.
    * **US07:** Como comprador independiente, deseo guardar mis establecimientos de confianza para priorizar sus ofertas en mis consultas diarias.

* **Impacto 4: Reporta y valida discrepancias de precio en góndola para asegurar datos fidedignos en la comunidad.**
  * *Deliverable: EP06 - Validación Comunitaria.*
    * **US28:** Como comprador independiente, deseo reportar cuando un precio en góndola difiere del valor registrado en el sistema para colaborar con la comunidad.
    * **US29:** Como comprador independiente, deseo validar los reportes de precios efectuados por otros usuarios para consolidar la confiabilidad de la información.
  * *Deliverable: EP07 - Servicios API RESTful.*
    * **TS07:** Como Developer, deseo implementar un endpoint para almacenar las confirmaciones y discrepancias emitidas por los usuarios sobre los precios.

---

### 3.2.2. Impact Mapping - Segmento #2: Comerciante Minorista

Este mapa articula cómo el actor **Daniel Palomino** contribuye a alcanzar las metas de digitalización barrial, captación de clientela y rotación de stock.

<img src="../assets/Impact-Map-Daniel-Palomino-(Comerciante-minorista).jpeg" width="850" />

*Figura 3.2: Impact Mapping para el Segmento Comerciante Minorista.*

#### Desglose de Relaciones y User Stories Asociadas:
* **Impacto 1: Registra y formaliza la presencia de su local en el mapa comercial para ser visible ante los compradores de su zona.**
  * *Deliverable: EP02 - Autenticación y Perfil.*
    * **US21:** Como comerciante minorista, deseo registrar los datos de mi establecimiento para integrar mi negocio al mapa comercial de la plataforma.
    * **US22:** Como comerciante minorista, deseo indicar los horarios de atención de mi local para que los compradores conozcan cuándo pueden acudir.
  * *Deliverable: EP07 - Servicios API RESTful.*
    * **TS04:** Como Developer, deseo integrar un servicio de verificación de RUC contra entidades oficiales para constatar la vigencia legal de los comercios afiliados.

* **Impacto 2: Mantiene actualizado su catálogo de precios y stock de forma ágil para no perder ventas ni generar falsas expectativas.**
  * *Deliverable: EP05 - Catálogo y Gestión Comercial.*
    * **US23:** Como comerciante minorista, deseo registrar y actualizar los precios de venta de mis productos para mantener informados a los compradores de la zona.
    * **US25:** Como comerciante minorista, deseo marcar artículos sin disponibilidad física en mi local para evitar desplazamientos infructuosos de los clientes.
    * **US26:** Como comerciante minorista, deseo importar una lista estructurada de artículos y precios para actualizar mi inventario de forma ágil.
  * *Deliverable: EP07 - Servicios API RESTful.*
    * **TS05:** Como Developer, deseo proveer un endpoint para la actualización en bloque de inventario de tiendas mediante solicitudes en formato JSON.

* **Impacto 3: Lanza promociones relámpago e incentivos para acelerar la rotación de artículos y reducir mermas en tiendas de proximidad.**
  * *Deliverable: EP05 - Catálogo y Gestión Comercial.*
    * **US24:** Como comerciante minorista, deseo publicar promociones por tiempo limitado para acelerar la rotación de artículos y atraer mayor afluencia.
  * *Deliverable: EP07 - Servicios API RESTful.*
    * **TS08:** Como Developer, deseo implementar endpoints CRUD para la administración del ciclo de vida de ofertas emitidas por comerciantes.

* **Impacto 4: Evalúa el impacto de sus precios e interacción recibida en las rutas de compra de los vecinos para optimizar su estrategia comercial.**
  * *Deliverable: EP05 - Catálogo y Gestión Comercial.*
    * **US27:** Como comerciante minorista, deseo consultar métricas de visualización de mis promociones para evaluar el impacto de mis precios publicados.


## 3.3. Product Backlog

En esta sección se presenta el *Product Backlog* priorizado y estimado para la plataforma **Preciazo**, desarrollado por **PeruTech**. La priorización de los requisitos responde estrictamente al valor entregado al negocio y a los usuarios (*Business Value First*). Cumpliendo con los lineamientos del marco de trabajo Scrum y las directivas académicas, las historias vinculadas a la Landing Page se sitúan al inicio para viabilizar la captación temprana de usuarios en el primer sprint. Posteriormente, se integran las funcionalidades nucleares de cálculo comparativo de canasta, optimización de trayectos y gestión comercial para bodegas y minimarkets, relegando las tareas de autenticación y parametrización avanzada a etapas posteriores.

La estimación del esfuerzo de cada ítem fue establecida mediante la dinámica de *Planning Poker*, aplicando la secuencia estándar de Fibonacci para Story Points (1, 2, 3, 5 y 8 SP).

| # Orden | User Story Id | Título | Descripción | Story Points (1 / 2 / 3 / 5 / 8) |
| :---: | :---: | :--- | :--- | :---: |
| 1 | **US01** | Landing: Propuesta de valor | Como visitante, deseo visualizar la propuesta central del servicio para comprender cómo optimizar mis compras y tiempos de traslado. | 1 |
| 2 | **US02** | Landing: Segmentos objetivo | Como visitante, deseo conocer a qué perfiles está orientada la solución para identificar si resuelve mis necesidades de abastecimiento o comercio. | 1 |
| 3 | **US03** | Landing: Red de comercios aliados | Como visitante, deseo visualizar qué establecimientos y zonas cuentan con cobertura para verificar la disponibilidad del servicio. | 1 |
| 4 | **US04** | Landing: Registro de interés | Como visitante, deseo suscribir mi correo electrónico para recibir notificaciones sobre el lanzamiento y novedades de la plataforma. | 2 |
| 5 | **US05** | Landing: Preguntas frecuentes y soporte | Como visitante, deseo consultar una sección de preguntas frecuentes para aclarar el modelo de servicio y los canales de contacto. | 2 |
| 6 | **US13** | Comparativa multiestablecimiento | Como comprador independiente, deseo comparar el costo total de mi lista entre locales comerciales cercanos para identificar el menor costo de compra. | 8 |
| 7 | **US14** | Cálculo de ruta de compra eficiente | Como comprador independiente, deseo obtener un itinerario secuencial de paradas óptimas para reducir mi tiempo de traslado y costo de transporte. | 8 |
| 8 | **US17** | Búsqueda por filtros de proximidad | Como comprador independiente, deseo filtrar comercios dentro de un radio caminable específico para evitar traslados excesivamente largos. | 3 |
| 9 | **US15** | Sugerencia de bienes sustitutos | Como comprador independiente, deseo recibir recomendaciones de productos alternativos más económicos para disminuir el monto total a pagar. | 5 |
| 10 | **US16** | Comparación por unidad de medida | Como comprador independiente, deseo comparar el costo por unidad de medida (kilogramo o litro) para evaluar presentaciones con distinto gramaje. | 3 |
| 11 | **US21** | Registro y afiliación de tienda | Como comerciante minorista, deseo registrar los datos de mi establecimiento para integrar mi negocio al mapa comercial de la plataforma. | 5 |
| 12 | **US23** | Publicación de precios en catálogo | Como comerciante minorista, deseo registrar y actualizar los precios de venta de mis productos para mantener informados a los compradores de la zona. | 5 |
| 13 | **US24** | Publicación de ofertas de tienda | Como comerciante minorista, deseo publicar promociones por tiempo limitado para acelerar la rotación de artículos y atraer mayor afluencia. | 3 |
| 14 | **US25** | Reporte de agotamiento de stock | Como comerciante minorista, deseo marcar artículos sin disponibilidad física en mi local para evitar desplazamientos infructuosos de los clientes. | 2 |
| 15 | **US22** | Configuración de horarios comerciales | Como comerciante minorista, deseo indicar los horarios de atención de mi local para que los compradores conozcan cuándo pueden acudir. | 2 |
| 16 | **US08** | Creación de lista de compras | Como comprador independiente, deseo crear una lista de productos requeridos para estructurar mi jornada de abastecimiento. | 2 |
| 17 | **US09** | Agregado de ítems a la lista | Como comprador independiente, deseo buscar y agregar artículos específicos a mi lista para consolidar mi canasta básica. | 3 |
| 18 | **US10** | Fijación de presupuesto límite | Como comprador independiente, deseo configurar un tope de gasto para mi lista de compras para controlar mi economía personal. | 2 |
| 19 | **US11** | Alerta de rebase presupuestario | Como comprador independiente, deseo recibir una advertencia cuando la sumatoria de mi lista supere el presupuesto establecido para ajustar mi selección. | 3 |
| 20 | **US12** | Modo de jornada de compra en local | Como comprador independiente, deseo marcar los artículos conforme los coloco en mi canasta para verificar el gasto acumulado en tiempo real. | 5 |
| 21 | **US20** | Recálculo dinámico de ruta | Como comprador independiente, deseo reordenar mi trayecto de compra si un local se encuentra cerrado o inaccesible. | 5 |
| 22 | **US18** | Registro de compras recurrentes | Como comprador independiente, deseo guardar una canasta base como plantilla para reutilizarla en compras quincenales sin reingresar productos. | 3 |
| 23 | **US19** | Historial de precios de producto | Como comprador independiente, deseo consultar la evolución histórica del valor de un bien para evaluar la conveniencia de una oferta. | 3 |
| 24 | **US26** | Carga estructurada de catálogo | Como comerciante minorista, deseo importar una lista estructurada de artículos y precios para actualizar mi inventario de forma ágil. | 5 |
| 25 | **US27** | Panel de rendimiento comercial | Como comerciante minorista, deseo consultar métricas de visualización de mis promociones para evaluar el impacto de mis precios publicados. | 3 |
| 26 | **US28** | Reporte colaborativo de discrepancia | Como comprador independiente, deseo reportar cuando un precio en góndola difiere del valor registrado en el sistema para colaborar con la comunidad. | 3 |
| 27 | **US29** | Confirmación comunitaria de datos | Como comprador independiente, deseo validar los reportes de precios efectuados por otros usuarios para consolidar la confiabilidad de la información. | 3 |
| 28 | **US06** | Autenticación y acceso | Como comprador independiente, deseo iniciar sesión con mis credenciales registradas para gestionar mis listas y presupuesto. | 3 |
| 29 | **US07** | Gestión de comercios favoritos | Como comprador independiente, deseo guardar mis establecimientos de confianza para priorizar sus ofertas en mis consultas diarias. | 2 |

---

### Evidencia del Tablero y Enlace Público

> **Enlace público al Product Backlog:**  
> [Tablero de Gestión Ágil - Preciazo (Trello)](https://trello.com/b/NhH0tIyG/product)

![Product Backlog en Herramienta](../assets/Trello.png)
> *Figura 3.3: Captura del Product Backlog configurado, estimado y priorizado en la herramienta de gestión ágil.*



# Capítulo IV: Product Design

En esta sección, el equipo establece las bases para contar con un repositorio central y organizado de recursos visuales y estructurales de uso común. El objetivo principal es garantizar una presentación consistente, sólida y enfocada en todos los productos digitales de **PeruTech**, facilitando la colaboración entre diseñadores y desarrolladores mediante el uso estandarizado de activos, fuentes, estilos y criterios de arquitectura de la información.

## 4.1. Style Guidelines

Estas guías establecen la identidad visual base para todos los productos digitales del ecosistema **PeruTech**.

### 4.1.1. General Style Guidelines


#### **A. Branding & Tono de Comunicación**
* **Tono:** El lenguaje será **Entusiasta y Sereno**. Se busca que el usuario se sienta motivado por la innovación y el ahorro inteligente, pero con la tranquilidad de que la información presentada es confiable y veraz.
* **Lenguaje:** Se utilizará un estilo **Formal/Casual**, directo y fácil de entender tanto para familias como para jóvenes profesionales y comercios aliados.

#### **B. Paleta de Colores (Colors)**
Se ha seleccionado una paleta moderna, equilibrada y tecnológica que evoca confianza, claridad y dinamismo:

| Uso | Nombre del Color | Hexadecimal | Representación / Aplicación |
| :--- | :--- | :--- | :--- |
| **Primario** | Negro Azabache | `#000000` | Sólido y profesional. Utilizado en encabezados, botones principales y contraste de textos de alta jerarquía. |
| **Secundario** | Turquesa Tecnológico | `#00ACAC` | Frescura, agilidad e innovación. Destacado en llamados a la acción, estados activos y acentos de interfaz. |
| **Acento / Fondo Suave** | Gris Claro Nieve | `#DFDEDC` | Limpieza visual. Se utiliza para fondos de tarjetas, contenedores secundarios y fondos de sección. |
| **Neutro Medio** | Gris Medio | `#A6A7A2` | Elementos secundarios, bordes, estados desactivados y divisores. |
| **Texto / Contraste** | Antracita Oscuro | `#464545` | Utilizado en el cuerpo de texto principal para optimizar la legibilidad y reducir la fatiga visual. |

#### **C. Tipografía (Typography)**
* **Títulos y Encabezados:** *Montserrat* (Bold / Semi-Bold) - Proporciona un aspecto moderno, profesional y estructurado.
* **Cuerpo de Texto y UI:** *Roboto* (Regular / Medium) - Sigue los estándares de legibilidad para interfaces digitales móviles y web.

#### **D. Espaciado y Rejilla (Spacing & Grid)**
* Se aplicará un sistema de rejilla basado en **8dp (8pt grid)** para mantener consistencia en márgenes, *paddings* y alineación de componentes UI en todas las pantallas.

### 4.1.2. Web Style Guidelines

[Contenido]

## 4.2. Information Architecture

En esta sección se documentan las decisiones y criterios de organización de contenido en las **plataformas web** y en las **aplicaciones móviles** de **PeruTech**, optimizando los sistemas de **organización, etiquetado, búsqueda y navegación**.

### 4.2.1. Organization Systems

Se distingue entre la **organización visual** (layout y jerarquía en pantalla) y los **esquemas de categorización** (criterios lógicos de agrupación).

##### **Organización Visual**

| Tipo | Cuándo se usa en PeruTech | Ejemplos concretos |
| --- | --- | --- |
| **Jerárquica** | Cuando un bloque comunica importancia relativa priorizando información clave. | **Landing:** Hero con propuesta de valor → beneficios → prueba social → CTA.<br>**Merchant Web:** Panel con KPIs principales arriba (Tráfico Mensual, Venta Perdida) y detalle operacional debajo. |
| **Secuencial (paso a paso)** | Flujos guiados que requieren un orden fijo de ejecución. | **Buyer:** Asistente "Configurar Canasta Básica / Lista → Ajustar Presupuesto → Generar Ruta Multiparada → Confirmar Punto Óptimo de Compra".<br>**Post-compra:** "Confirmar Visita → Ver Ahorro Neto → Calificar Comercio / Reseña → Reportar Discrepancia de Precio". |
| **Matricial** | Contenidos multidimensionales que admiten múltiples filtros y comparaciones. | **Buyer:** Grilla de Artículos de Compra (*Categoría × Precio Unitario × Comercio Minorista*).<br>**Merchant:** Tablero de inventario (*Artículo × Estado de stock × Vigencia de Oferta Relámpago*). |

##### **Esquemas de Categorización**

| Esquema | Cuándo se usa | Ejemplos en el producto |
| --- | --- | --- |
| **Alfabético** | Listados extensos de orden explícito. | Listados de Artículos de Compra en el catálogo Merchant y ordenación A–Z en búsquedas. |
| **Cronológico** | Información ordenada por temporalidad. | Historial de Rutas Multiparada finalizadas y registro histórico de actualización de precios u ofertas relámpago. |
| **Por Tema (Tópico)** | Categorización por dominios del supermercado o módulos de ayuda. | Navegación de productos por categoría de Despensa Familiar (Abarrotes, Limpieza, etc.) y secciones FAQ. |
| **Por Audiencia** | Separación según el rol del usuario. | Diferenciación clara entre flujos de **Buyer (Consumidor / Jefe de Hogar)** y **Merchant (Comerciante)**. |

##### **Resumen por Superficie**

| Superficie | Organización visual | Esquemas de categorización |
| --- | --- | --- |
| **Landing Web** | Jerárquica | Por tema y por audiencia (CTA Buyer vs. Merchant) |
| **App Buyer (Móvil)** | Secuencial en flujos clave; matricial en catálogo | Tópico (categorías de Despensa), cronológico (historial de rutas), alfabético |
| **Portal Merchant (Web/App)** | Jerárquica en paneles; matricial en tablas de datos | Alfabético, por estado de stock / oferta y cronológico (reportes) |

### 4.2.2. Labeling Systems

El sistema de etiquetado utiliza términos breves, claros y estrictamente unificados.

##### **Etiquetas Principales y Asociaciones**

| Etiqueta (UI) | Entidad / Asociación (Ubiquitous Language) | Regla de Brevedad y Claridad |
| --- | --- | --- |
| **Canasta Básica** | `Basic Basket` | Módulo de configuración de necesidades esenciales de abastecimiento. |
| **Lista Compartida** | `Shared Shopping List` | Registro estructurado y colaborativo del hogar. |
| **Presupuesto** | `Purchase Budget` | Techo financiero asignado para la jornada de compra. |
| **Ruta Multiparada** | `Multi-stop Route` | Itinerario optimizado que conecta el hogar con múltiples comercios. |
| **Punto Óptimo** | `Optimal Purchase Stop` | Establecimiento sugerido por mejor relación cercanía/precio/stock. |
| **Comercios** | `Retail Store` | Puntos de venta físicos (supermercados y mercados de abastos). |
| **Ahorro Neto** | `Net Savings` | Diferencia económica positiva considerando el sobrecosto de desplazamiento. |
| **Bien Sustituto** | `Substituted Good` | Sugerencia alternativa ante falta de stock o exceso de presupuesto. |
| **Discrepancia** | `Price Discrepancy` / `Error de precio` | Reporte colaborativo de diferencias entre góndola y caja. |
| **Confianza** | `TrustProfile` / Insignia de Confianza | Score y nivel de fiabilidad del comercio asignado por la comunidad. |
| **Catálogo / Ofertas** | Módulos de gestión Merchant | Administración de inventario inicial y Ofertas Relámpago. |
| **Reportes** | Tráfico Mensual y Venta Perdida | Métricas clave de rendimiento para el Comerciante. |

##### **Microcopy y Mensajes del Sistema**
* **Validaciones:** Frases directas y comprensibles (*"Ingresa un presupuesto mayor a S/ 0"*, *"Selecciona al menos un Punto Óptimo de Compra"*).
* **Estados de Carga:** Verbos indicativos directos (*"Calculando Ruta Multiparada optimizada..."*, *"Verificando Discrepancia de Precio..."*, *"Guardando cambios..."*).

### 4.2.3. SEO Tags and Meta Tags

##### **Sitio Web Estático — Landing Page**

| Meta / Etiqueta | Valor propuesto |
| --- | --- |
| **`<title>`** | `PeruTech \| Ahorra en tu Canasta Básica con Rutas Multiparada y Precios Reales` |
| **`<meta name="description">`** | `Planifica tu Lista Compartida, respeta tu Presupuesto de Compra y optimiza tus recorridos con Rutas Multiparadas. Compara precios reales con PeruTech.` |
| **`<meta name="keywords">`** | `PeruTech, canasta basica, presupuesto de compra, ruta multiparada, ahorro neto, punto optimo de compra, comercio minorista, dispersion de precios, Peru` |
| **`<meta name="author">`** | `PeruTech Team` |
| **Complementos** | Canonical `<link rel="canonical" href="https://www.perutech.pe/">`y Open Graph (`og:title`, `og:description`, `og:image`). |

##### **Aplicación Web — Portal Merchant (Inicio / Dashboard)**

| Meta / Etiqueta | Valor propuesto |
| --- | --- |
| **`<title>`** | `PeruTech Merchant \| Gestión de Catálogo, Ofertas y Reportes de Tráfico` |
| **`<meta name="description">`** | `Administra tu inventario, publica Ofertas Relámpago y consulta métricas de Venta Perdida en tiempo real para compradores de PeruTech.` |
| **`<meta name="keywords">`** | `PeruTech Merchant, comercio minorista, ofertas relampago, precio unitario, reporte de trafico, venta perdida, reputacion comercio` |
| **`<meta name="author">`** | `PeruTech Team` |

##### **ASO (App Store & Google Play)**

* **App Buyer — "PeruTech":**
  * **Título:** `PeruTech — Compras y Ahorro Neto`
  * **Subtítulo:** `Canasta básica, presupuesto y rutas`
  * **Keywords:** `compras, canasta basica, presupuesto, ruta multiparada, ahorro neto, supermercado, peru, gondola, perutech`
  * **Descripción corta:** `Gestiona tu Canasta Básica, respeta tu Presupuesto y recorre la mejor Ruta Multiparada. Compara precios reales y maximiza tu Ahorro Neto con PeruTech.`

* **App Merchant — "PeruTech Tiendas":**
  * **Título:** `PeruTech Tiendas`
  * **Subtítulo:** `Catálogo y ofertas en vivo`
  * **Keywords:** `retail, comercio minorista, catalogo, ofertas relampago, precio unitario, merchant, sede, perutech`
  * **Descripción corta:** `Gestiona tu inventario, publica Ofertas Relámpago y mantén tus precios actualizados para la comunidad de compradores de PeruTech.`

### 4.2.4. Searching Systems

El sistema de búsqueda permite una localización eficiente de bienes dentro de catálogos extensos y paneles de administración.

##### **Opciones y Alcance de Búsqueda**

| Contexto / App | Objeto de búsqueda | Tipo de Entrada | Alcance y Filtros |
| --- | --- | --- | --- |
| **Buyer — Catálogo** | Artículos de Compra por nombre, marca o presentación | Campo global + auto-sugerencias | Pestañas "En esta tienda" / "En todas". Filtros por Precio Unitario, Categoría de Despensa y Bienes Sustitutos. |
| **Buyer — Comercios** | Comercio Minorista por sede o mercado de abastos | Barra de búsqueda integrada en mapa/lista | Filtro por distancia, Insignia de Confianza y horario de atención. |
| **Buyer — Mi Lista** | Ítems agregados a la Lista Compartida | Filtro local en tiempo real | Filtrado rápido de texto por categoría de producto. |
| **Merchant — Backoffice** | Artículos, SKUs, Ofertas Relámpago activas | Tabla de datos con filtros combinados | Filtro por estado de stock, Discrepancia de Precio reportada y vigencia. |

##### **Comportamiento e Interfaz de Búsqueda**
* **Sugerencias Dinámicas:** Despliegue de resultados emergentes a partir de los 2 caracteres ingresados (`>= 2 chars`).
* **Visualización de Resultados:** Tarjetas con Precio Unitario destacado, indicación del Punto Óptimo de Compra y opción para añadir directamente a la Lista Compartida.

### 4.2.5. Navigation Systems

Estructura de desplazamiento y recorrido del usuario en las diferentes plataformas de **PeruTech**.

##### **Mapa de Navegación y Estructuras**

* **Landing Page (Web Estática):** Barra superior fija con desplazamientos suaves (*anchor links*) a `#producto`, `#como-funciona`, `#descargar` y `#contacto`.
* **App Buyer (Móvil):** Navegación primaria mediante **Tab Bar inferior** (*Inicio*, *Canasta / Lista*, *Ruta Multiparada*, *Perfil*). Flujos secundarios en *stack modal* (Sugerencia de Bien Sustituto, Reportar Discrepancia) y asistente para planificación del Presupuesto y Ruta Multiparada.
* **Portal Merchant (Web/App):** Menú lateral persistente (*Sidebar*) con acceso a *Panel de Métricas* (Tráfico y Venta Perdida), *Catálogo*, *Ofertas Relámpago*, *Reportes de Reputación* y *Configuración de Sede*.

| Superficie | Técnica de Navegación |
| --- | --- |
| **Landing Web** | Header fijo, scroll suave, CTAs de conversión repetidos tras bloques clave y footer legal. |
| **App Buyer** | Tabs inferiores persistentes, navegación por stack modal, asistente secuencial de Ruta Multiparada y *deep linking* desde notificaciones de ofertas relámpago. |
| **Merchant Web/App** | Sidebar persistente, indicador de sede activa en header, breadcrumbs navegables y tablas paginadas para catálogos extensos. |

## 4.3. Landing Page UI Design

### 4.3.1. Landing Page Wireframe

A continuación se presentan los wireframes de baja fidelidad representando la estructura y jerarquía visual.

![wireframe-landing](/assets/designs/landing/wireframe-landing.png)

### 4.3.2. Landing Page Mock-up

En esta sección se presenta el mockup de alta fidelidad con la identidad de la marca plasmada.

![mockup-landing](/assets/designs/landing/mockup-landing.png)

## 4.4. Web Applications UX/UI Design

### 4.4.1. Web Applications Wireframes

A continuación, se presentan las pantallas de wireframe de baja fidelidad de la aplicación **PeruTech**. El diseño contempla tanto la experiencia del usuario final (comprador) como el panel de gestión orientado a comercios afiliados.

#### 1. Pantalla de Inicio (Home)
Pantalla principal de la aplicación que integra el buscador global por productos o tiendas, accesos rápidos a la creación de listas, ofertas destacadas en la zona del usuario y el listado de tiendas cercanas con sus respectivas distancias.

![Pantalla de Inicio](/assets/wireframe-app/portada.png)

---

#### 2. Vista de Lista Activa - Modo Normal
Permite visualizar la lista de compras actual con el control de presupuesto. Incluye sugerencias inteligentes de sustitutos más económicos para maximizar el ahorro y la opción de agregar o eliminar productos.

![Lista Activa - Modo Normal](/assets/wireframe-app/lista-modo-normal.png)

---

#### 3. Módulo de Comparativa de Precios
Cuadro comparativo interactivo que permite analizar el costo total de la lista activa en distintos supermercados según el radio de distancia seleccionado. Destaca la mejor opción económica y permite reportar inconsistencias en tiendas.

![Comparativa de Precios](/assets/wireframe-app/comparar.png)

---

#### 4. Generador de Ruta de Compra Optimizada
Mapeo iterativo y sugerencia de itinerario para compras en múltiples establecimientos. Desglosa los tiempos de traslado, el ahorro estimado y el detalle de ítems a adquirir en cada parada.

![Ruta Optimizada](/assets/wireframe-app/ruta.png)

---

#### 5. Panel de Analítica para Comercios
Dashboard principal orientado al comerciante o tienda aliada. Presenta métricas relevantes sobre impresiones en rutas, vistas de productos, consultas de ofertas y un gráfico de tendencias de tráfico mensual.

![Panel de Analítica para Comercios](/assets/wireframe-app/tienda-panel.png)

---

#### 6. Gestión de Catálogo de Precios (Comercios)
Interfaz de administración donde el comercio puede activar, desactivar y actualizar el listado de precios de sus productos e importar inventarios.

![Catálogo de Precios](/assets/wireframe-app/tienda-catalogo.png)

---

#### 7. Módulo de Ofertas y Promociones (Comercios)
Sección diseñada para que los establecimientos publiquen promociones temporales, establezcan precios de oferta con contador de vigencia y gestionen sus campañas activas.

![Módulo de Ofertas](/assets/wireframe-app/tienda-oferta.png)

---

#### 8. Perfil e Información de la Tienda
Pantalla que muestra la información institucional del establecimiento afiliado, incluyendo RUC, dirección fiscal, teléfono de contacto y la configuración de sus horarios de atención al público.

![Información del Establecimiento](/assets/wireframe-app/tienda-mi-tienda.png)


### 4.4.2. Web Applications Wireflow Diagrams

A continuación, se presentan los diagramas de Wireflow estructurados por segmento de usuario. Cada flujo define el objetivo de la interacción y la visualización del recorrido mediante su respectivo diagrama.

---

#### Segmento 1: Comprador

##### Diagrama 1: Búsqueda y Comparativa de Precios
* **Goal:** 1. Comparar precios de la canasta entre supermercados cercanos.
* **Descripción:** El usuario busca productos, revisa su lista de compras activa en Modo Normal para ajustar sugerencias de ahorro y accede al módulo comparativo para evaluar los costos totales por tienda.

![Diagrama 1 - Búsqueda y Comparativa de Precios](/assets/wireflow/diagrama1.png)

---

##### Diagrama 2: Ejecución de Compra y Ruta Optimizada
* **Goal:** 2. Guiar el recorrido de compra físico y optimizar el itinerario.
* **Descripción:** El usuario selecciona una lista guardada, genera la ruta de compra optimizada entre tiendas e inicia el Modo Compra al llegar al establecimiento para marcar los productos en tiempo real.

![Diagrama 2 - Ejecución de Compra y Ruta Optimizada](/assets/wireflow/diagrama2.png)

---

#### Segmento 2: Comerciante

##### Diagrama 3: Gestión Comercial y Monitoreo
* **Goal:** 3. Analizar métricas de rendimiento y administrar el catálogo.
* **Descripción:** El comerciante ingresa a su panel principal para analizar impresiones y tendencias, navega al catálogo para actualizar inventario o precios y gestiona la información fiscal del local.

![Diagrama 3 - Gestión Comercial y Monitoreo](/assets/wireflow/diagrama3.png)

---

##### Diagrama 4: Publicación de Promociones Temporales
* **Goal:** 4. Crear y gestionar ofertas con tiempo limitado.
* **Descripción:** El comerciante selecciona productos desde su catálogo e ingresa al módulo de ofertas para configurar descuentos especiales y establecer la vigencia de la promoción.

![Diagrama 4 - Publicación de Promociones Temporales](/assets/wireflow/diagrama4.png)

### 4.4.3. Web Applications Mock-ups

A continuación, se presentan las pantallas que componen el prototipo de alta fidelidad de la aplicación **PeruTech**. El diseño contempla tanto la experiencia del usuario final (comprador) como el panel de gestión orientado a comercios afiliados.

#### 1. Pantalla de Inicio (Home)
Pantalla principal de la aplicación que integra el buscador global por productos o tiendas, accesos rápidos a la creación de listas, ofertas destacadas en la zona del usuario y el listado de tiendas cercanas con sus respectivas distancias.

![Pantalla de Inicio](/assets/mockups-app/portada.png)

---

#### 2. Vista de Lista Activa - Modo Normal
Permite visualizar la lista de compras actual con el control de presupuesto. Incluye sugerencias inteligentes de sustitutos más económicos para maximizar el ahorro y la opción de agregar o eliminar productos.

![Lista Activa - Modo Normal](/assets/mockups-app/lista-modo-normal.png)

---

#### 3. Vista de Lista Activa - Modo Compra
Optimizada para usarse dentro del establecimiento físico, permitiendo al usuario marcar los productos mediante *checkboxes* a medida que los coloca en el carrito y calcular el subtotal en tiempo real.

![Lista Activa - Modo Compra](/assets/mockups-app/lista-modo-compra.png)

---

#### 4. Gestión de Listas Guardadas
Sección destinada a la administración de plantillas personalizadas y listas reutilizables para compras recurrentes (p. ej., Desayuno Semanal o Limpieza del Hogar).

![Listas Guardadas](/assets/mockups-app/lista-guardado.png)

---

#### 5. Módulo de Comparativa de Precios
Cuadro comparativo interactivo que permite analizar el costo total de la lista activa en distintos supermercados según el radio de distancia seleccionado. Destaca la mejor opción económica y permite reportar inconsistencias en tiendas.

![Comparativa de Precios](/assets/mockups-app/comparar.png)

---

#### 6. Generador de Ruta de Compra Optimizada
Mapeo iterativo y sugerencia de itinerario para compras en múltiples establecimientos. Desglosa los tiempos de traslado, el ahorro estimado y el detalle de ítems a adquirir en cada parada.

![Ruta Optimizada](/assets/mockups-app/ruta.png)

---

#### 7. Panel de Analítica para Comercios
Dashboard principal orientado al comerciante o tienda aliada. Presenta métricas relevantes sobre impresiones en rutas, vistas de productos, consultas de ofertas y un gráfico de tendencias de tráfico mensual.

![Panel de Analítica para Comercios](/assets/mockups-app/tienda-panel.png)

---

#### 8. Gestión de Catálogo de Precios (Comercios)
Interfaz de administración donde el comercio puede activar, desactivar y actualizar el listado de precios de sus productos e importar inventarios.

![Catálogo de Precios](/assets/mockups-app/tienda-catalogo.png)

---

#### 9. Módulo de Ofertas y Promociones (Comercios)
Sección diseñada para que los establecimientos publiquen promociones temporales, establezcan precios de oferta con contador de vigencia y gestionen sus campañas activas.

![Módulo de Ofertas](/assets/mockups-app/tienda-oferta.png)

---

#### 10. Perfil e Información de la Tienda
Pantalla que muestra la información institucional del establecimiento afiliado, incluyendo RUC, dirección fiscal, teléfono de contacto y la configuración de sus horarios de atención al público.

![Información del Establecimiento](/assets/mockups-app/tienda-mi-tienda.png)

### 4.4.4. Web Applications User Flow Diagrams

A continuación, se presentan los diagramas de User Flow para la aplicación web y móvil basados en las pantallas de alta fidelidad.

---

#### Segmento 1: Comprador

##### Diagrama 1: Flujo de Búsqueda y Comparativa de Precios por Supermercado
* **Goal:** 1. Comparar precios de la canasta entre supermercados cercanos.
* **Descripción:** El usuario inicia en la pantalla de portada navegando por el buscador o categorías, gestiona su lista de compras activa en Modo Normal para evaluar sugerencias de ahorro y accede al cuadro comparativo para analizar los costos totales y productos disponibles por establecimiento.

![Diagrama 1 - Búsqueda y Comparativa de Precios](/assets/userflow/diagrama1.png)

---

##### Diagrama 2: Flujo de Ejecución de Compra y Ruta Optimizada
* **Goal:** 2. Guiar el recorrido de compra físico y optimizar el itinerario inter-tiendas.
* **Descripción:** El usuario selecciona una lista guardada o plantilla, activa el generador de rutas para visualizar el itinerario con paradas y tiempos de traslado, e inicia el Modo Compra en el establecimiento para marcar los ítems en su carrito en tiempo real.

![Diagrama 2 - Ejecución de Compra y Ruta Optimizada](/assets/userflow/diagrama2.png)

---

#### Segmento 2: Comerciante

##### Diagrama 3: Flujo de Gestión Comercial y Monitoreo Analítico
* **Goal:** 3. Analizar métricas de rendimiento y administrar el catálogo del establecimiento.
* **Descripción:** El comerciante ingresa a su panel de analítica para evaluar tendencias e impresiones de su local, navega al catálogo para actualizar precios e inventarios y gestiona la información fiscal y los horarios de atención de la tienda.

![Diagrama 3 - Gestión Comercial y Monitoreo Analítico](/assets/userflow/diagrama3.png)

---

##### Diagrama 4: Flujo de Publicación de Promociones Temporales
* **Goal:** 4. Crear y gestionar ofertas con tiempo de vigencia determinado.
* **Descripción:** El comerciante evalúa los productos desde su catálogo de precios e ingresa al módulo de ofertas para configurar promociones especiales, definir descuentos y establecer la vigencia temporal de la campaña.

![Diagrama 4 - Publicación de Promociones Temporales](/assets/userflow/diagrama4.png)

## 4.5. Web Applications Prototyping

El vídeo de evidencia del prototipo plasma las interacciones que ejecutan los usuarios y las respuestas esperadas por el sistema.

![captura de video-prototipo](/assets/prototipo.png)

[Prototipo evidencia](https://upcedupe-my.sharepoint.com/:v:/g/personal/u20241c101_upc_edu_pe/IQCEOW9isi3LT7sIUmtoPLwAAQMF1OJDthoTqwwWszE9QvQ?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJPbmVEcml2ZUZvckJ1c2luZXNzIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXciLCJyZWZlcnJhbFZpZXciOiJNeUZpbGVzTGlua0NvcHkifX0&e=cP37RQ)

## 4.6. Domain-Driven Software Architecture

La arquitectura de PeruTech se diseña siguiendo principios de Domain-Driven Design (DDD), tomando como punto de partida los resultados obtenidos en el Big Picture Event Storming desarrollado durante la etapa de Requirements Elicitation & Analysis.

El análisis del dominio permitió identificar los principales procesos asociados a los dos segmentos objetivo de la solución: los compradores que buscan optimizar el costo y desplazamiento de sus compras, y los comerciantes minoristas que requieren administrar la información de sus establecimientos, precios, disponibilidad y promociones.

A partir del refinamiento de los eventos, comandos, reglas y conceptos identificados previamente, el dominio de PeruTech se organiza en Bounded Contexts con responsabilidades claramente delimitadas. Esta separación permite reducir el acoplamiento entre capacidades de negocio y facilita posteriormente la implementación modular del Frontend Web Application y de los RESTful Web Services.

Los Bounded Contexts identificados para PeruTech son:

| Bounded Context | Responsabilidad principal |
|---|---|
| Identity and Access | Gestionar autenticación, identidad, roles y autorización de compradores y comerciantes. |
| Shopping Planning | Gestionar listas de compra, cantidades, presupuesto y progreso de la jornada de compra. |
| Catalog and Pricing | Gestionar productos, precios, disponibilidad y comparación entre establecimientos. |
| Route Planning | Calcular y optimizar rutas de compra entre múltiples establecimientos considerando localización y desplazamiento. |
| Merchant Management | Gestionar afiliación de comercios, información del establecimiento, catálogo local, inventario y promociones. |
| Community Price Verification | Gestionar discrepancias, reportes y confirmaciones comunitarias sobre precios observados. |
| Analytics and Engagement | Consolidar métricas de interacción y rendimiento relevantes para los comerciantes y generar información de seguimiento. |

Estos contextos se comunican mediante contratos explícitos, evitando que un módulo modifique directamente las reglas internas de otro contexto.


### 4.6.1. Design-Level Event Storming

Para profundizar el modelo obtenido durante el Big Picture Event Storming se realizó un Design-Level Event Storming orientado a analizar con mayor detalle los principales flujos de negocio de PeruTech.

El proceso de refinamiento comenzó identificando las acciones realizadas por los actores Buyer y Merchant. Cada acción relevante fue representada mediante Commands y posteriormente relacionada con los Aggregates responsables de mantener las reglas y consistencia del dominio. A partir de estas acciones se identificaron los Domain Events producidos por el sistema, así como Policies que reaccionan ante dichos eventos, Queries requeridas para consultar el estado del dominio, sistemas externos y Hotspots que representan decisiones o reglas pendientes de precisar.

Para facilitar la lectura del modelo se utilizó la siguiente convención visual:

- **Actor:** amarillo.
- **Command:** azul.
- **Aggregate:** amarillo claro.
- **Domain Event:** naranja.
- **Policy:** violeta.
- **Query / Read Model:** verde.
- **External System:** rosa.
- **Hotspot:** rojo.

El resultado del proceso permitió organizar el dominio en siete Bounded Contexts: Identity and Access, Shopping Planning, Catalog and Pricing, Route Planning, Merchant Management, Community Price Verification y Analytics and Engagement.

![PeruTech Design-Level Event Storming](../assets/architecture/design-level-event-storming.png)


### 4.6.2. Software Architecture Context Diagram

![PeruTech Software Architecture Context Diagram](../assets/architecture/c4-context.png)


### 4.6.3. Software Architecture Container Diagrams

![PeruTech Software Architecture Container Diagram](../assets/architecture/c4-container.png)

### 4.6.4. Software Architecture Components Diagrams

![PeruTech Frontend Component Diagram](../assets/architecture/c4-components-frontend.png)

## 4.7. Software Object-Oriented Design

En esta sección se presenta el diseño orientado a objetos de PeruTech a partir de los Bounded Contexts identificados durante el proceso de Domain-Driven Design.

Con el objetivo de evitar un único modelo de clases excesivamente acoplado, el diseño se divide de acuerdo con los siete Bounded Contexts definidos previamente. Cada contexto mantiene sus propias entidades, servicios, interfaces, políticas, objetos de valor y enumeraciones, permitiendo representar de manera explícita sus responsabilidades y reglas de negocio.

Asimismo, cuando un contexto necesita información perteneciente a otro dominio, se utilizan referencias locales basadas en identificadores u objetos específicos del contexto, evitando compartir directamente las entidades internas de otros Bounded Contexts. Este criterio permite conservar límites claros entre los modelos y reducir dependencias innecesarias.

Los diagramas incluyen atributos y operaciones relevantes del dominio, utilizando visibilidad UML, relaciones nombradas y multiplicidades para representar las asociaciones entre los diferentes elementos.

### 4.7.1. Class Diagrams

Los Class Diagrams de PeruTech se organizan por Bounded Context con el propósito de representar de forma independiente las principales estructuras y comportamientos de cada parte del dominio.

#### Identity and Access

El Bounded Context **Identity and Access** concentra las responsabilidades relacionadas con autenticación, sesiones, roles y autorización.

La clase `User` representa la identidad principal del sistema y permite realizar operaciones como autenticarse, asignar roles, desactivar la cuenta y comprobar permisos. Las sesiones generadas se representan mediante `AuthSession`, mientras que `Role` y `Permission` modelan el esquema de autorización.

Las interfaces `IdentityRepository` y `AccessPolicy` abstraen respectivamente la persistencia de identidades y las reglas utilizadas para determinar si una operación está autorizada.

![Identity and Access Class Diagram](../assets/architecture/classes/identity-access.png)

#### Shopping Planning

El Bounded Context **Shopping Planning** administra la planificación de compras del Buyer.

`ShoppingList` funciona como el elemento central del modelo y agrupa múltiples `ShoppingListItem`. Entre sus responsabilidades se encuentran agregar y eliminar ítems, marcar productos como comprados, calcular el costo estimado y completar una lista.

`PurchaseBudget` representa el presupuesto asociado a la planificación y encapsula operaciones como reservar o liberar importes y comprobar si un determinado gasto puede ser asumido. El objeto `Money` encapsula cantidades monetarias y sus operaciones.

`ProductRequirement` permite referenciar un producto requerido sin introducir directamente el modelo interno de Catalog and Pricing dentro de este Bounded Context.

![Shopping Planning Class Diagram](../assets/architecture/classes/shopping-planning.png)

#### Catalog and Pricing

El Bounded Context **Catalog and Pricing** modela la consulta y comparación de productos, precios y disponibilidad entre establecimientos.

`Product` representa la información propia del catálogo, mientras que `StoreProduct` mantiene los datos asociados a un producto ofrecido por un establecimiento, tales como precio unitario, disponibilidad y fecha de actualización.

La clase `CatalogPricingService` proporciona operaciones de búsqueda, comparación de precios y selección de ofertas. Por otro lado, `PriceComparisonPolicy` encapsula la regla utilizada para determinar la alternativa más conveniente.

`RetailStoreRef` representa únicamente una referencia al establecimiento, preservando la separación respecto del modelo interno de Merchant Management.

![Catalog and Pricing Class Diagram](../assets/architecture/classes/catalog-pricing.png)

#### Route Planning

El Bounded Context **Route Planning** representa la generación y optimización de recorridos entre múltiples establecimientos.

El aggregate `MultiStopRoute` administra las diferentes paradas mediante objetos `RouteStop` y contiene las operaciones necesarias para agregar, eliminar y reordenar establecimientos, además de calcular el ahorro neto asociado a una ruta.

`RoutePlanningService` coordina la generación, recálculo y confirmación de rutas, mientras que `RoutingGateway` abstrae el acceso al servicio externo de mapas y ruteo.

Para mantener el aislamiento del contexto, conceptos pertenecientes a otros dominios se representan mediante elementos locales como `ShoppingPlanRef`, `ProductRequirement` y `StoreCandidate`.

![Route Planning Class Diagram](../assets/architecture/classes/route-planning.png)

#### Merchant Management

El Bounded Context **Merchant Management** concentra las capacidades relacionadas con la afiliación y administración de establecimientos.

`MerchantProfile` representa el perfil comercial y mantiene su estado de verificación. Un Merchant puede administrar uno o varios objetos `RetailStore`, los cuales contienen los elementos de inventario y promociones correspondientes.

`InventoryItem` encapsula operaciones relacionadas con stock y precio, mientras que `Promotion` representa ofertas con un período de vigencia definido.

La interfaz `RucVerificationGateway` abstrae la comunicación con el servicio externo utilizado para validar la información fiscal del Merchant.

![Merchant Management Class Diagram](../assets/architecture/classes/merchant-management.png)

#### Community Price Verification

El Bounded Context **Community Price Verification** administra las observaciones y discrepancias de precios reportadas por los usuarios.

`PriceDiscrepancy` representa una diferencia detectada entre un precio esperado y uno observado y puede recibir múltiples `PriceObservation` y `VerificationConfirmation`.

La clase `TrustProfile` mantiene información local relacionada con la confiabilidad de las contribuciones realizadas por un usuario. Por otro lado, `VerificationPolicy` encapsula las reglas necesarias para aceptar, rechazar o solicitar revisión adicional de una discrepancia.

Los objetos `UserRef` y `StoreProductRef` actúan como referencias hacia información perteneciente a otros Bounded Contexts sin introducir sus modelos internos directamente.

![Community Price Verification Class Diagram](../assets/architecture/classes/community-price-verification.png)

#### Analytics and Engagement

El Bounded Context **Analytics and Engagement** se encarga de registrar eventos relevantes y transformarlos en métricas útiles para los comerciantes.

`MetricEvent` representa interacciones como visitas a establecimientos, visualizaciones de productos, comparaciones de precios, ventas perdidas e interacciones con promociones.

`AnalyticsService` registra dichos eventos y genera posteriormente objetos `MerchantMetrics` y `MerchantReport`. La interfaz `MetricsCalculator` abstrae la lógica utilizada para calcular las métricas correspondientes a un período determinado.

De esta manera, el contexto mantiene separada la recopilación de eventos de la generación de información analítica destinada al Merchant.

![Analytics and Engagement Class Diagram](../assets/architecture/classes/analytics-engagement.png)


En conjunto, los Class Diagrams permiten representar la estructura interna de cada Bounded Context sin construir un único modelo global compartido. Esta separación mantiene alineado el diseño orientado a objetos con las fronteras establecidas mediante Domain-Driven Design y facilita que cada módulo evolucione manteniendo responsabilidades claramente delimitadas.

## 4.8. Database Design

El diseño de base de datos de PeruTech se organiza siguiendo los límites definidos previamente mediante Domain-Driven Design. En lugar de representar el almacenamiento únicamente como un modelo relacional global, se presentan vistas específicas para cada Bounded Context con el objetivo de evidenciar qué información pertenece a cada parte del dominio.

Cada diagrama identifica las entidades persistentes, sus atributos principales, claves primarias, claves foráneas, restricciones de unicidad y relaciones. Cuando un contexto necesita referenciar información perteneciente a otro Bounded Context, dicha dependencia se representa mediante identificadores marcados como referencias externas (`REF`), evitando asumir que la entidad referenciada pertenece al mismo modelo.

Adicionalmente, se incluye una vista general de la base de datos que permite observar la integración global de la información persistida por PeruTech.

### 4.8.1. Database Diagrams

Los Database Diagrams de PeruTech se presentan primero mediante una vista general y posteriormente mediante vistas específicas para cada Bounded Context.

#### Database Overview

El Database Overview muestra la estructura relacional completa propuesta para PeruTech y permite visualizar las principales relaciones entre usuarios, comerciantes, establecimientos, productos, planificación de compras, rutas, verificación comunitaria de precios y analítica.

La vista global también evidencia restricciones importantes del modelo, como la unicidad de correos y roles, la relación entre usuarios y perfiles de comerciantes, la unicidad de un producto por establecimiento dentro del catálogo, la secuencia única de paradas dentro de una ruta y la asociación de métricas y reportes con establecimientos.

![PeruTech Database Overview](../assets/architecture/database/database-overview.png)

#### Identity and Access

El modelo de persistencia de **Identity and Access** administra la información necesaria para la identificación, autorización y manejo de sesiones.

La tabla `users` almacena las cuentas registradas, mientras que `roles` y `permissions` representan los mecanismos de autorización. Las tablas intermedias `user_roles` y `role_permissions` modelan las relaciones de muchos a muchos existentes entre usuarios, roles y permisos.

Finalmente, `auth_sessions` registra las sesiones asociadas a cada usuario, incluyendo su fecha de emisión, expiración y estado de revocación.

![Identity and Access Database Diagram](../assets/architecture/database/identity-access.png)

#### Shopping Planning

El Bounded Context **Shopping Planning** persiste la información relacionada con la planificación de compras.

`shopping_lists` representa las listas creadas por los usuarios, mientras que `shopping_list_items` almacena los productos requeridos, cantidades, precios estimados y estado de compra.

La tabla `shopping_list_members` permite relacionar otros usuarios con una lista determinada y `purchase_budgets` almacena los presupuestos asociados a cada planificación.

Los identificadores de usuario son referencias hacia Identity and Access y los identificadores de producto corresponden a información administrada por Catalog and Pricing.

![Shopping Planning Database Diagram](../assets/architecture/database/shopping-planning.png)

#### Catalog and Pricing

El modelo de **Catalog and Pricing** almacena los productos disponibles y la información necesaria para realizar comparaciones de precios.

La tabla `products` contiene la información base de cada producto. `catalog_entries` representa la oferta de un producto dentro de un establecimiento determinado e incluye su precio unitario, disponibilidad y fecha de actualización.

Adicionalmente, `price_snapshots` permite conservar registros históricos de precios asociados a una entrada del catálogo.

La combinación entre establecimiento y producto debe ser única dentro de `catalog_entries`. El identificador del establecimiento actúa como referencia hacia Merchant Management.

![Catalog and Pricing Database Diagram](../assets/architecture/database/catalog-pricing.png)

#### Route Planning

El Bounded Context **Route Planning** mantiene la información relacionada con las rutas calculadas para una planificación de compras.

La tabla `routes` almacena los datos principales del recorrido, tales como distancia, duración estimada, costo de desplazamiento, ahorro neto y estado.

Cada ruta se compone de múltiples `route_stops`, los cuales almacenan el establecimiento correspondiente, el orden dentro de la ruta y la hora estimada de llegada.

La combinación entre una ruta y su número de secuencia debe ser única. `shopping_list_id` referencia información proveniente de Shopping Planning y `store_id` corresponde a establecimientos administrados por Merchant Management.

![Route Planning Database Diagram](../assets/architecture/database/route-planning.png)

#### Merchant Management

El Bounded Context **Merchant Management** persiste la información necesaria para administrar comerciantes y establecimientos.

`merchant_profiles` representa el perfil comercial y su estado de verificación fiscal. Un perfil puede administrar múltiples registros `retail_stores`, los cuales almacenan datos del establecimiento y su ubicación.

`inventory_items` representa los productos gestionados dentro de cada establecimiento, incluyendo stock, precio y estado de disponibilidad.

Finalmente, `promotions` registra las promociones asociadas a elementos del inventario y mantiene sus períodos de vigencia.

El campo `product_id` de inventario funciona como una referencia hacia Catalog and Pricing.

![Merchant Management Database Diagram](../assets/architecture/database/merchant-management.png)

#### Community Price Verification

El modelo de persistencia de **Community Price Verification** permite almacenar reportes y evidencias relacionadas con discrepancias de precios.

`price_discrepancies` representa diferencias reportadas entre un precio esperado y uno observado. Cada discrepancia puede recibir múltiples registros `price_observations`, los cuales contienen el precio observado, fecha y origen de la observación.

Asimismo, `verification_confirmations` registra las confirmaciones realizadas por otros usuarios y `trust_profiles` mantiene información relacionada con el nivel de confianza de las contribuciones realizadas por cada usuario.

Las referencias hacia productos y usuarios pertenecen respectivamente a Catalog and Pricing e Identity and Access.

![Community Price Verification Database Diagram](../assets/architecture/database/community-price-verification.png)

#### Analytics and Engagement

El Bounded Context **Analytics and Engagement** almacena eventos de interacción y los resultados analíticos generados a partir de ellos.

`analytics_events` registra eventos relevantes mediante un tipo, una fecha de ocurrencia, un sujeto asociado y metadatos adicionales.

A partir de estos eventos pueden generarse registros `merchant_metrics`, los cuales consolidan indicadores como tráfico mensual, ventas perdidas y engagement dentro de un período determinado.

La tabla `merchant_reports` representa los reportes generados para un establecimiento, incluyendo el tipo de reporte, período analizado y fecha de generación.

Los identificadores de establecimiento utilizados por métricas y reportes actúan como referencias hacia Merchant Management.

![Analytics and Engagement Database Diagram](../assets/architecture/database/analytics-engagement.png)

En conjunto, estos diagramas permiten mantener una visión global de la persistencia de PeruTech y, al mismo tiempo, conservar los límites definidos entre los Bounded Contexts. Las referencias externas entre contextos se representan mediante identificadores, mientras que las relaciones internas utilizan claves primarias, claves foráneas y restricciones propias de cada modelo.


---

# Capítulo V: Product Implementation, Validation & Deployment

## 5.1. Software Configuration Management

Se detallan a continuación los entornos, herramientas y normas operativas encargados de asegurar la calidad, consistencia y trazabilidad de los artefactos desarrollados durante el ciclo de vida del proyecto.

### 5.1.1. Software Development Environment Configuration

Se presentan los entornos y herramientas seleccionadas para las fases de gestión, diseño, desarrollo web, documentación y despliegue del producto.

**Project Management**

| Herramienta | Uso Principal | Enlace / Ruta de Acceso |
| :--- | :--- | :--- |
| **Trello** | Gestión ágil de tareas, seguimiento del Sprint Backlog e historias de usuario mediante tableros Kanban. | [https://trello.com](https://trello.com) |

<br>

**Requirements & UX/UI Design**

| Herramienta | Uso Principal | Enlace / Ruta de Acceso |
| :--- | :--- | :--- |
| **UXPressia** | Elaboración de artefactos de diseño centrado en el usuario (User Personas, Empathy Maps, Journey Maps e Impact Maps). | [https://uxpressia.com](https://uxpressia.com) |
| **Lucidchart / Miro** | Diagramación y modelado colaborativo del dominio del problema y arquitectura C4 Model. | [https://lucidchart.com](https://lucidchart.com) |
| **Figma** | Diseño de wireframes, mockups de alta fidelidad y prototipos interactivos de la Landing Page y Web Application. | [https://figma.com](https://figma.com) |

<br>

**Software Development (Web & Services)**

| Herramienta / Tecnología | Propósito | Enlace / Ruta de Acceso |
| :--- | :--- | :--- |
| **WebStorm / VS Code** | Entorno de desarrollo para maquetación web, estilos y scripts frontend. | [https://www.jetbrains.com/webstorm/](https://www.jetbrains.com/webstorm/) |
| **IntelliJ IDEA Ultimate** | Entorno de desarrollo para la implementación del RESTful API en Java y Spring Boot. | [https://www.jetbrains.com/idea/](https://www.jetbrains.com/idea/) |
| **HTML5 & CSS3** | Lenguajes base para la estructuración y estilización semántica y accesible (a11y) del sitio web. | [https://developer.mozilla.org](https://developer.mozilla.org) |
| **JavaScript & TypeScript** | Lenguajes para la lógica del cliente y la interactividad del Landing Page y componentes Angular. | [https://www.typescriptlang.org](https://www.typescriptlang.org) |
| **Angular** | Marco de trabajo frontend para la construcción de la aplicación web de gestión comercial. | [https://angular.io](https://angular.io) |
| **Java & Spring Boot** | Lenguaje y marco de trabajo backend para la persistencia y servicios RESTful con Spring Data JPA. | [https://spring.io/projects/spring-boot](https://spring.io/projects/spring-boot) |

<br>

**Software Deployment & Hosting**

| Herramienta / Plataforma | Propósito | Enlace / Ruta de Acceso |
| :--- | :--- | :--- |
| **GitHub Pages** | Alojamiento e integración continua nativa para el despliegue del sitio web estático de la Landing Page. | [https://pages.github.com](https://pages.github.com) |

<br>

**Software Documentation & Version Control**

| Herramienta / Recurso | Propósito | Enlace / Ruta de Acceso |
| :--- | :--- | :--- |
| **Markdown** | Formato estructurado para la elaboración colaborativa del informe y especificaciones técnicas. | [https://www.markdownguide.org](https://www.markdownguide.org) |
| **Git & GitHub** | Sistema de control de versiones distribuido y servidor centralizado de repositorios bajo la organización del equipo. | [https://github.com](https://github.com) |
| **GitFlow & Conventional Commits** | Flujo de trabajo de ramificación estructurada y convención estándar para mensajes de confirmación. | [https://www.conventionalcommits.org](https://www.conventionalcommits.org) |

---

### 5.1.2. Source Code Management

El código fuente del proyecto se administra centralizadamente en la organización oficial de **GitHub**. El desarrollo se organiza en repositorios independientes para mantener el desacoplamiento entre la documentación técnica, la experiencia web y los servicios de backend, aplicando **GitFlow Workflow**:

**Repositorios Oficiales del Proyecto**

| Componente / Producto | Nombre del Repositorio | Enlace Remoto |
| :--- | :--- | :--- |
| **Organización Oficial** | Open Source - 1ASI0729-2620-7750 | [https://github.com/Open-Source-1ASI0729-2620-7750](https://github.com/Open-Source-1ASI0729-2620-7750) |
| **Documentación Técnica (Reporte)** | `PeruTech-Report` | [https://github.com/Open-Source-1ASI0729-2620-7750/PeruTech-Report](https://github.com/Open-Source-1ASI0729-2620-7750/PeruTech-Report) |
| **Landing Page** | `PeruTech-Landing-Page` | [https://github.com/Open-Source-1ASI0729-2620-7750/PeruTech-Landing-Page](https://github.com/Open-Source-1ASI0729-2620-7750/PeruTech-Landing-Page) |

#### Modelo de Ramificación (GitFlow)

El desarrollo en los repositorios se estructura mediante dos ramas principales permanentes:
* `main`: Contiene exclusivamente versiones estables, aprobadas y publicadas en producción.
* `develop`: Sirve como rama base para la integración continua de nuevas funcionalidades y secciones.

Adicionalmente, se utilizan ramas de soporte bajo las siguientes convenciones:
* `feature/<nombre-funcionalidad>`: Ramas derivadas de `develop` para la construcción de secciones específicas o capítulos de documentación (ej. `feature/landing-hero`, `feature/chapter-5-content`).
* `release/vX.X.X`: Ramas para la estabilización y preparación de entregas formales, aplicando el estándar **Semantic Versioning 2.0.0** (ej. `release/v1.0.0`).
* `hotfix/<descripcion-correccion>`: Ramas directas desde `main` para correcciones críticas no planificadas en producción.

#### Política de Commits

Para garantizar la legibilidad y trazabilidad del historial, los mensajes de commit emplean la especificación de **Conventional Commits**: `<tipo>(ámbito-opcional): descripción en imperativo y minúsculas` (ejemplos: `feat(landing): implement responsive navigation bar`, `docs(report): update chapter 5 environment tables`).

---

### 5.1.3. Source Code Style Guide & Conventions

Se establecen guías de estilo oficiales para asegurar la consistencia, legibilidad y mantenibilidad técnica en todos los componentes del sistema:

* **Idioma de Código**: Nomenclatura estrictamente en **idioma inglés** para identificadores, clases, interfaces, variables, comentarios y rutas de archivos.
* **HTML5**: Estructuración semántica (`<header>`, `<nav>`, `<main>`, `<section>`, `<footer>`), validación de accesibilidad con atributos ARIA (`a11y`), e identación uniforme de 2 espacios.
* **CSS3**: Nomenclatura `kebab-case` para clases personalizadas (`hero-container`, `btn-primary`), organización modular y aplicación de principios de diseño responsivo.
* **JavaScript & TypeScript**: Convención `camelCase` para variables y funciones (`toggleLanguage`, `submitContactForm`), `PascalCase` para clases e interfaces (`UserProfile`, `MerchantService`). Se siguen las directrices de la *Google TypeScript Style Guide*.
* **Java & Spring Boot**: Adopción estricta de la *Google Java Style Guide*. Nombres de clases en `PascalCase`, métodos en `camelCase`, constantes en `UPPER_SNAKE_CASE` y paquetes en minúsculas coherentes con la arquitectura orientada al dominio (DDD).
* **Markdown**: Sintaxis estándar para encabezados, tablas y enlaces según la especificación *The Markdown Guide*.

---

### 5.1.4. Software Deployment Configuration

El sitio web de la Landing Page se despliega mediante el servicio **GitHub Pages**, aprovechando la infraestructura nativa de GitHub para servir archivos estáticos directamente desde el repositorio del proyecto.

| Componente | Plataforma Hosting | Estrategia de Despliegue | URL Oficial |
| :--- | :--- | :--- | :--- |
| **Landing Page** | GitHub Pages | Despliegue automatizado desde la rama `main` | `https://open-source-1asi0729-2620-7750.github.io/PeruTech-Landing-Page/` |

#### Flujo de Configuración en GitHub Pages:
1. **Habilitación del Servicio**: Acceso a la configuración del repositorio (*Settings > Pages*) en `PeruTech-Landing-Page`.
2. **Selección de Rama Fuente (Source)**: Definición de la rama `main` y directorio `/root` como origen del despliegue público.
3. **Automatización del Despliegue**: Integración mediante GitHub Actions para compilar y publicar automáticamente los cambios tras cada merge confirmado.
4. **Configuración de Seguridad**: Habilitación forzada del protocolo criptográfico seguro HTTPS para proteger la navegación de los visitantes.

## 5.2. Landing Page, Services & Applications Implementation

En esta sección se detalla y evidencia el proceso de planificación, implementación, control de calidad y despliegue continuo de los artefactos del sistema (sitio web de la Landing Page, servicios de backend y aplicaciones cliente) a lo largo de los diferentes ciclos iterativos de desarrollo. La ejecución del proyecto sigue el marco de trabajo Scrum, estructurando el avance por sprints independientes en función del Product Backlog definido en el Capítulo III.

---

### 5.2.1. Sprint 1

El Sprint 1 comprende el ciclo inicial de desarrollo del proyecto enfocado en establecer las bases arquitectónicas, configurar los entornos colaborativos y desplegar en producción el sitio web de la Landing Page responsivo y accesible, orientado a captar el interés tanto del Comprador Independiente como del Comerciante Minorista.

#### 5.2.1.1. Sprint Planning 1

| Campo | Descripción |
| :--- | :--- |
| **Sprint #** | Sprint 1 |
| **Sprint Planning Background** | Sesión de planificación inicial para definir el alcance técnico del primer entregable (AV1), establecer la velocidad estimada del equipo y seleccionar las historias del Product Backlog correspondientes al despliegue de la Landing Page y la infraestructura de control de versiones. |
| **Date** | 2026-09-02 |
| **Time** | 07:00 PM (GMT -5) |
| **Location** | Modalidad remota síncrona vía Google Meet |
| **Prepared By** | Equipo de Desarrollo PeruTech |
| **Attendees (to planning meeting)** | Integrantes del equipo de desarrollo PeruTech |
| **Sprint 0 Review Summary** | Al tratarse de la iteración inicial del ciclo académico, no existe una revisión formal de un sprint previo. Se toma como insumo el conjunto de requisitos del Capítulo III y los artefactos de diseño UX/UI. |
| **Sprint 0 Retrospective Summary** | Se consolidaron los hallazgos del Needfinding y se validaron los wireframes de baja fidelidad. Se determinó priorizar una arquitectura web modular con HTML5 semántico, CSS3 adaptable y JavaScript para garantizar tiempos de carga reducidos en GitHub Pages. |
| **Sprint Goal & User Stories** | **Sprint 1 Goal:** Implementar, documentar y desplegar en producción el sitio web estático de la Landing Page para PeruTech mediante GitHub Pages, cumpliendo con criterios de diseño adaptativo (responsive design), accesibilidad semántica y captura de clientes potenciales para ambos segmentos de usuarios.<br><br>**User Stories Seleccionadas:**<br>• **US01:** Landing: Propuesta de valor (5 SP)<br>• **US02:** Landing: Segmentos objetivo (5 SP)<br>• **US03:** Landing: Red de comercios aliados (3 SP)<br>• **US04:** Landing: Registro de interés (5 SP)<br>• **US05:** Landing: Preguntas frecuentes y soporte (3 SP) |
| **Sprint 1 Velocity** | 21 Story Points |
| **Sum of Story Points** | 21 Story Points |

#### 5.2.1.2. Aspect Leaders and Collaborators

En la siguiente tabla se distribuyen las responsabilidades de liderazgo y colaboración de los integrantes del equipo para el Sprint 1, organizadas por áreas de trabajo técnico y metodológico orientadas al despliegue de la Landing Page y la configuración del entorno:

| Aspecto / Área de Trabajo | Líder (Aspect Leader) | Colaboradores |
| :--- | :--- | :--- |
| **Software Configuration Management & GitFlow** | Kevin Patrick Pardo Chumpitazi | [Nombre del Integrante 2], [Nombre del Integrante 3] |
| **UI/UX Design & Semantic Prototyping** | [Nombre del Integrante 2] | Kevin Patrick Pardo Chumpitazi, [Nombre del Integrante 4] |
| **Frontend Web Development (Landing Page Structure & Style)** | [Nombre del Integrante 3] | [Nombre del Integrante 4], [Nombre del Integrante 5] |
| **Responsive Design & Accessibility (a11y)** | [Nombre del Integrante 4] | Kevin Patrick Pardo Chumpitazi, [Nombre del Integrante 3] |
| **Hosting, Continuous Deployment (CI/CD) & QA Review** | [Nombre del Integrante 5] | [Nombre del Integrante 2], Kevin Patrick Pardo Chumpitazi |


#### 5.2.1.3. Sprint Backlog 1

El Sprint Backlog 1 consolida el conjunto de User Stories priorizadas para la fase inicial del proyecto PeruTech, enfocada en la construcción, optimización semántica y despliegue continuo de la Landing Page estática en GitHub Pages.

Para la administración operativa del ciclo de desarrollo se utilizó Trello como herramienta formal de gestión visual mediante un tablero Kanban. Dicho tablero permitió desglosar cada historia de usuario en tareas técnicas específicas, asignar responsables directos y controlar la transición de los ítems a través de los estados del flujo de trabajo (*To Do*, *Doing* y *Done*), asegurando el cumplimiento riguroso de los criterios de aceptación antes de la liberación final.

<div align="center">
  <img src="../assets/sprint-1/Trello.png" alt="Sprint Backlog 1 en Trello" style="width: 85%;">
  <p><em>Figura 5.1: Estado final de las tareas del Sprint 1 en el tablero Kanban de Trello.</em></p>
</div>

<br>

**Desglose Detallado del Sprint Backlog 1:**

| User Story Id | Title | Task Id | Task Title | Description | Estimation (Hours) | Assigned To | Status (To-do/In-Process/To-Review/Done) |
| :---: | :--- | :---: | :--- | :--- | :---: | :--- | :---: |
| **US01** | Landing: Propuesta de valor | T01 | Maquetación Hero Section | Maquetación semántica del contenedor principal y titulares de valor con HTML5. | 3 | Kevin Patrick Pardo Chumpitazi | Done |
| **US01** | Landing: Propuesta de valor | T02 | Estilización diferencial | Aplicación de hojas de estilo CSS3 para evidenciar la optimización de compras y tiempos. | 2 | Kevin Patrick Pardo Chumpitazi | Done |
| **US01** | Landing: Propuesta de valor | T03 | Diseño Mobile-First | Implementación de media queries para adaptación visual en dispositivos móviles. | 3 | Kevin Patrick Pardo Chumpitazi | Done |
| **US02** | Landing: Segmentos objetivo | T04 | Tarjetas informativas | Estructuración modular de los perfiles Comprador Independiente y Comerciante. | 3 | [Nombre del Integrante 2] | Done |
| **US02** | Landing: Segmentos objetivo | T05 | Llamados a la acción (CTA) | Configuración de enlaces hacia los flujos de registro respectivos de cada segmento. | 2 | [Nombre del Integrante 2] | Done |
| **US02** | Landing: Segmentos objetivo | T06 | Accesibilidad y contraste | Validación de contrastes de color y jerarquía visual conforme a estándares WCAG 2.1. | 2 | [Nombre del Integrante 3] | Done |
| **US03** | Landing: Red de aliados | T07 | Módulo de cobertura | Maquetación del bloque interactivo de sectores urbanos y comercios minoristas. | 2 | [Nombre del Integrante 3] | Done |
| **US03** | Landing: Red de aliados | T08 | Optimización gráfica | Incorporación y compresión de logotipos vectoriales en formato SVG. | 2 | [Nombre del Integrante 4] | Done |
| **US04** | Landing: Registro de interés | T09 | Formulario de suscripción | Creación de campos semánticos para captura de correo electrónico de visitantes. | 2 | [Nombre del Integrante 4] | Done |
| **US04** | Landing: Registro de interés | T10 | Validación de sintaxis | Script en JavaScript con expresiones regulares (RegEx) para comprobación de correo. | 3 | Kevin Patrick Pardo Chumpitazi | Done |
| **US04** | Landing: Registro de interés | T11 | Notificación accesible | Implementación del mensaje interactivo de confirmación tras envío exitoso. | 2 | [Nombre del Integrante 5] | Done |
| **US05** | Landing: FAQ y soporte | T12 | Acordeón informativo | Estructuración semántica de preguntas frecuentes con elementos nativos HTML5. | 2 | [Nombre del Integrante 5] | Done |
| **US05** | Landing: FAQ y soporte | T13 | Lógica de colapso interactivo | Desarrollo de funciones JavaScript para apertura y cierre accesible de tópicos. | 2 | Kevin Patrick Pardo Chumpitazi | Done |
| **US05** | Landing: FAQ y soporte | T14 | Formulario de contacto | Integración del canal de comunicación directa para consultas de soporte. | 2 | [Nombre del Integrante 2] | Done |
| **TS01** | Despliegue en GitHub Pages | T15 | Inicialización GitFlow | Configuración del repositorio `PeruTech-Landing-Page` y esquema de ramas. | 2 | Kevin Patrick Pardo Chumpitazi | Done |
| **TS01** | Despliegue en GitHub Pages | T16 | Pipeline de despliegue | Configuración de la acción automática para compilación y hosting en GitHub Pages. | 1 | Kevin Patrick Pardo Chumpitazi | Done |
| **TS01** | Despliegue en GitHub Pages | T17 | Auditoría Lighthouse | Comprobación de métricas de rendimiento y SEO superando el 90% de puntaje. | 2 | [Nombre del Integrante 3] | Done |

#### 5.2.1.4. Development Evidence for Sprint Review

[Contenido]

#### 5.2.1.5. Execution Evidence for Sprint Review

[Contenido]

#### 5.2.1.6. Services Documentation Evidence for Sprint Review

[Contenido]

#### 5.2.1.7. Software Deployment Evidence for Sprint Review

[Contenido]

#### 5.2.1.8. Team Collaboration Insights during Sprint

[Contenido]

### 5.2.2. Sprint 2

[Contenido]

#### 5.2.2.1. Sprint Planning 2

[Contenido]

#### 5.2.2.2. Aspect Leaders and Collaborators

[Contenido]

#### 5.2.2.3. Sprint Backlog 2

[Contenido]

#### 5.2.2.4. Development Evidence for Sprint Review

[Contenido]

#### 5.2.2.5. Execution Evidence for Sprint Review

[Contenido]

#### 5.2.2.6. Services Documentation Evidence for Sprint Review

[Contenido]

#### 5.2.2.7. Software Deployment Evidence for Sprint Review

[Contenido]

#### 5.2.2.8. Team Collaboration Insights during Sprint

[Contenido]

## 5.3. Validation Interviews

[Contenido]

### 5.3.1. Diseño de Entrevistas

[Contenido]

### 5.3.2. Registro de Entrevistas

[Contenido]

### 5.3.3. Evaluaciones según heurísticas

[Contenido]

## 5.4. Video About-the-Product

[Contenido]

---

# Conclusiones

[Contenido]

# Conclusiones y recomendaciones

[Contenido]

# Video About-the-Team

[Contenido]

# Bibliografía

[Contenido]

# Anexos

[Contenido]
