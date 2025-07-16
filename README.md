# Frontend Mentor - Solución para Order summary card ✨

Esta es una solución al desafío [Order summary card en Frontend Mentor](https://www.frontendmentor.io/challenges/order-summary-component-QlPmajDUj). Los desafíos de Frontend Mentor te ayudan a mejorar tus habilidades de codificación construyendo proyectos realistas.

## Tabla de Contenidos 📋

- [Resumen](#resumen-📝)
  - [El desafío](#el-desafío)
  - [Captura de pantalla](#captura-de-pantalla-📸)
  - [Enlace](#enlace-🔗)
- [Mi Proceso](#mi-proceso-🚀)
  - [Construido con](#construido-con-🏗️)
  - [Lo que aprendí](#lo-que-aprendí-🧠)
  - [Desarrollo Continuo](#desarrollo-continuo-📈)
  - [Recursos Útiles](#recursos-útiles-📚)
- [Autor](#autor-🧑‍💻)
- [Agradecimientos](#agradecimientos-🙌)

## Resumen 📝

### El desafío

Los usuarios deberían ser capaces de:

- Ver estados de hover para elementos interactivos.

### Captura de pantalla 📸

![Captura de pantalla de la solución de la tarjeta de resumen de pedido](./design/desktop-design.jpg)

### Enlace 🔗

- URL de la Solución (Repositorio): [https://github.com/josecervera20/order-summary-card](https://github.com/josecervera20/order-summary-card)

## Mi Proceso 🚀

### Construido con 🏗️

- Marcado semántico HTML5
- Propiedades personalizadas de CSS (Variables CSS)
- Flexbox (para el diseño del plan y centrado)
- Diseño Mobile-first
- [Google Fonts](https://fonts.google.com/specimen/Red+Hat+Display) (Fuente Red Hat Display)

### Lo que aprendí 🧠

Durante este proyecto, reforcé mis habilidades en varias áreas clave de CSS y HTML:

- **Uso de Variables CSS**: Practiqué la definición y el uso de variables CSS para gestionar la paleta de colores de manera eficiente, lo que facilita el mantenimiento y la escalabilidad del código.
  ```css
  :root {
    --pale-blue: hsl(225, 100%, 94%);
    --bright-blue: hsl(245, 75%, 52%);
    /* ... otras variables ... */
  }
  .card__cta {
    background-color: var(--bright-blue);
  }
  ```
- **Diseño Mobile-First**: Abordé el diseño comenzando por los estilos para dispositivos móviles y luego utilicé media queries para adaptar la tarjeta a pantallas más grandes (desktop).

  ```css
  body {
    /* Estilos base para móvil */
    min-height: 100vh;
    padding: 40px 0;
    display: flex;
  }

  @media (min-width: 768px) {
    body {
      /* Adaptaciones para desktop */
      background-image: url("../images/pattern-background-desktop.svg");
      background-repeat: no-repeat;
    }
  }
  ```

- **Pseudo-elementos (`::before`)**: Implementé la imagen de cabecera de la tarjeta utilizando un pseudo-elemento `::before` y `background-image`, lo que me permitió un control preciso sobre su posicionamiento y el `overflow` con el `border-radius` de la tarjeta.
  ```css
  .card::before {
    content: "";
    display: block;
    width: 100%;
    height: 180px;
    background-image: url("../images/illustration-hero.svg");
    background-size: cover;
    background-position: center;
  }
  ```
- **Estados de Hover y Transiciones**: Apliqué efectos de hover a los elementos interactivos (`<a>`) para mejorar la experiencia del usuario, incluyendo cambios de color, opacidad y subrayado, utilizando transiciones suaves para un efecto más pulido.

  ```css
  .card__cta:hover {
    opacity: 0.8;
    cursor: pointer;
  }

  .card__change:hover {
    color: var(--bright-blue);
    text-decoration: none;
    cursor: pointer;
  }
  ```

### Desarrollo Continuo 📈

Me gustaría seguir profundizando en:

- **Animaciones CSS**: Explorar animaciones más complejas para mejorar la interactividad sin depender excesivamente de JavaScript.
- **Accesibilidad (a11y)**: Prestar más atención a los atributos ARIA y la semántica HTML para asegurar que mis proyectos sean accesibles para todos los usuarios.
- **Optimización de imágenes**: Aprender más sobre las mejores prácticas para servir imágenes de manera eficiente, incluyendo formatos y técnicas de carga diferida.

### Recursos Útiles 📚

- [The Markdown Guide](https://www.markdownguide.org/) - Una excelente referencia para la sintaxis de Markdown que utilicé para formatear este README.

## Autor 🧑‍💻

- GitHub - [@josecervera20](https://github.com/josecervera20)

## Agradecimientos 🙌

Agradezco a la comunidad de Frontend Mentor por proporcionar desafíos tan valiosos que me permiten mejorar mis habilidades y construir proyectos realistas.
