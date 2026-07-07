MiChiPa es una página de aterrizaje (Landing Page) moderna, estética y responsiva desarrollada
para un negocio local de café de especialidad, platos artesanales y chipas tradicionales. 
El sitio actúa como portal informativo para exhibir los pilares de la marca, los horarios de atención y facilitar el contacto con los clientes.

> 🚧 **Estado del Proyecto:** En desarrollo activo (Under Development).

## ✨ Características Implementadas (Features)

- **Encabezado Semántico:** Menú de navegación estructurado listo para enrutamiento interno (`Inicio`, `Nosotros`, `Menú`, `Contacto`).
- **Sección Hero:** Portada de bienvenida con un eslogan enfocado en la experiencia del usuario y la identidad de marca.
- **Tarjetas de Servicios Integradas:** Bloques modulares dinámicos ("Come", "Bebe", "Disfruta") con recursos optimizados en formato `.avif` y `.png`.
- **Bloque Informativo Central:** Sección con datos esenciales visibles como dirección física y horarios laborales semanales.
- **Footer Corporativo de 3 Columnas:** Espacio dedicado a boletín informativo, datos de contacto directo (+595) y enlaces a redes sociales.

## 🛠️ Tecnologías Utilizadas

- **Frontend:** HTML5 semántico, CSS3 (Layout modular).
- **Control de Versiones:** Git y GitHub.

##  Desafíos Técnicos y Soluciones de Diseño

Durante el desarrollo de la interfaz, apliqué lógica avanzada de CSS para resolver retos de maquetación y adaptabilidad:

### 1. Maquetación Alternada Automatizada (Layout Eficiente)
*   **Problema:** Diseñar las secciones de "Come", "Bebe" y "Disfruta" intercalando la imagen y el texto de izquierda a derecha manualmente requería crear clases repetitivas en el HTML, ensuciando el código.
*   **Solución:** Utilicé las pseudo-clases estructurales `:nth-child(even)` y `:nth-child(odd)` en CSS. De esta forma, el navegador de los usuarios detecta automáticamente si la sección es par o impar,
*   invirtiendo la dirección del flujo mediante `flex-direction: row-reverse`. Esto mantiene el HTML 100% limpio y modular.

### 2. Modularización de Hojas de Estilo
*   **Problema:** Mantener un único archivo CSS con miles de líneas para todo el sitio web vuelve el código inmanejable y propenso a errores de especificidad.
*   **Solución:** Implementé una arquitectura modular utilizando la directiva `@import` en el archivo principal `style.css`.
*   Fragmenté los estilos en archivos independientes encargados de componentes específicos del negocio (`header.css`, `detalles-servicios.css`, `footer.css`), logrando un flujo de trabajo ordenado y escalable.

### 3. Adaptabilidad Responsiva Avanzada (Media Queries)
*   **Problema:** Las secciones con alineación horizontal (Flexbox) se rompen o desbordan cuando se visualizan en pantallas verticales pequeñas como tablets o teléfonos celulares.
*   **Solución:** Diseñé un sistema responsivo basado en puntos de quiebre (*breakpoints*) estratégicos (`1024px`, `992px`, `768px`, `600px`).
*   Utilicé reescritura de propiedades para forzar a los bloques a apilarse verticalmente (`flex-direction: column !important`)
*   y reduje dinámicamente los tamaños de fuente (`font-size`) para garantizar una legibilidad perfecta.

## Lista de Tareas Pendientes (Roadmap)

- [x] Maquetación base del esqueleto HTML.
- [x] Estilización responsiva y adaptabilidad móvil mediante CSS.
- [ ] Creación de las páginas secundarias (`nosotros.html` y `menu.html`).
- [ ] Configuración del enlace dinámico a la API de WhatsApp en el botón "Contáctanos".
- [ ] Optimización SEO general y despliegue final en producción.

