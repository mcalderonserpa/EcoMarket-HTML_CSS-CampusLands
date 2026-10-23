# 🌿 EcoMarket - Tienda en Línea Sostenible

> **Plataforma web de comercio electrónico dedicada a productos ecológicos, reutilizables y sustentables.**  
> Diseñada bajo la filosofía de consumo consciente, arquitectura **Mobile First** y desarrollada exclusivamente con **HTML5 Semántico y CSS3 Puro (0% JavaScript, sin frameworks)**.

---

## 📋 Tabla de Contenidos
1. [Descripción del Proyecto](#-descripción-del-proyecto)
2. [Vistas Principales y Funcionalidades](#-vistas-principales-y-funcionalidades)
3. [Especificaciones Técnicas](#-especificaciones-técnicas)
4. [Estructura de Archivos](#-estructura-de-archivos)
5. [Instrucciones de Visualización Local](#-instrucciones-de-visualización-local)
6. [Galería de Capturas de Pantalla](#-galería-de-capturas-de-pantalla)
7. [Guía de Despliegue](#-guía-de-despliegue)
8. [Gestión de Versiones (GitFlow)](#-gestión-de-versiones-gitflow)

---

## 📖 Descripción del Proyecto

**EcoMarket** surge como una respuesta a la creciente necesidad de un consumo responsable y transparente frente a la proliferación de plásticos de un solo uso. La plataforma ofrece una experiencia de compra limpia, accesible e intuitiva que conecta a consumidores conscientes con productores y artesanos sustentables.

### ¿Por qué este proyecto?
- **Consumo Consciente:** Interfaz diseñada con paletas de color naturales y orgánicas que transmiten calma, frescura y autenticidad.
- **UX/UI "Clean":** Aprovechamiento armónico del espacio en blanco, tipografía altamente legible y componentes interactivos sin saturación visual.
- **Complejidad Técnica sin Scripts:** Todo el comportamiento de la plataforma (menús responsivos, validaciones de formularios, estados de favoritos y carruseles) está implementado mediante las capacidades avanzadas de **CSS3 moderno**.

---

## 🖥️ Vistas Principales y Funcionalidades

### 1. Página de Inicio (`index.html`)
- **Header:** Logotipo con icono ecológico, menú de navegación semántico y accesos rápidos a búsqueda y carrito de compras.
- **Banner Hero:** Mensaje inspirador (*"Compra responsable, vive sostenible"*), subtítulo y botón CTA (*"Explorar productos"*) con micro-interacción de brillo suave.
- **Productos Destacados:** Grid responsivo de 6 tarjetas con efecto **hover lift** que eleva la tarjeta suavemente mediante `transform: translateY(-8px)` y sombra multicapa difusa.
- **Footer Institucional:** Enlaces a políticas, canales de atención al cliente y redes sociales.

### 2. Catálogo de Productos (`views/productos.html`)
- **Barra Superior:** Buscador visual con icono y selector de ordenamiento por relevancia y precio.
- **Sidebar de Filtros Sticky:** Barra lateral izquierda que acompaña el desplazamiento del usuario (`position: sticky`), con filtros por:
  - Categorías (*Hogar Sustentable*, *Moda Ética*, *Cuidado Personal*, *Alimentos Bio*).
  - Control deslizante de rango de precios (`<input type="range">`) con etiquetas legibles.
  - Disponibilidad (*En Stock*, *Agotados*).
- **Grid de 20 Productos:** Matriz responsiva adaptativa:
  - **Desktop (≥ 1024px):** 4 columnas.
  - **Tablet (640px - 1023px):** 2 columnas.
  - **Móvil (< 640px):** 1 columna.
- **Card de Producto:** Imagen con zoom suave al cursor, categoría, título, precio, badge de stock y botón de favoritos con activación visual mediante pseudo-clases CSS (`:active` y `:target`).
- **Paginación Visual:** Navegación semántica con control activo y deshabilitado.

### 3. Sobre Nosotros (`views/sobre-nosotros.html`)
- **Historia de Origen:** Layout flexible en **Flexbox** que combina narrativa fundacional e imagen ilustrativa.
- **Principios Ecológicos:** Grid de 4 pilares sostenibles con iconos representativos (*100% Sin Plástico*, *Comercio Justo y Local*, *Huella de Carbono Neutra* y *Cruelty Free y Botánico*).
- **Carrusel CSS de Testimonios:** Tarjetas de testimonios con **CSS Scroll-Snap** horizontal, calificación en estrellas y efecto dinámico de elevación, rotación del avatar y expansión al pasar el mouse.

### 4. Página de Contacto (`views/contacto.html`)
- **Formulario Inteligente:** Campos para Nombre, Email, Asunto y Mensaje con validación nativa HTML5 y retroalimentación visual inmediata en CSS puro:
  - Bordes rojos y fondos de alerta para campos vacíos/inválidos (`:invalid`).
  - Bordes verdes y mensajes de confirmación para datos válidos (`:valid`).
- **Canales Directos:** Horarios, líneas de atención y ubicación presencial.
- **Mapa Estático:** Imagen cartográfica estilizada con diseño minimalista.
- **Redes Sociales:** Botones interactivos con animación de escala elástica (`transform: scale(1.08)`).

---

## 🛠️ Especificaciones Técnicas

| Requerimiento | Implementación |
|---|---|
| **Estructura** | HTML5 Semántico (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<figure>`, `<footer>`) |
| **Estilos** | CSS3 Modular con Variables Nativas (Design Tokens) |
| **Interactividad** | Pseudo-clases puras (`:hover`, `:active`, `:focus-within`, `:target`, `:valid`, `:invalid`) |
| **Layouts** | CSS Grid y Flexbox bidimensional |
| **JavaScript** | **0% (Estrictamente sin scripts)** |
| **Librerías / Frameworks** | **Ninguna (CSS puro)** |
| **Enfoque** | Mobile First con Media Queries progresivas |
| **Accesibilidad** | Soporte de contraste WCAG y regla `@media (prefers-reduced-motion: reduce)` |

---

## 📂 Estructura de Archivos

```
EcoMarket/
├── css/
│   ├── main.css            # Design tokens, reset, tipografía y utilidades
│   ├── layout.css          # Header sticky, Footer, contenedores y sistemas Grid
│   ├── components.css      # Tarjetas, botones, inputs, badges y sidebar sticky
│   └── animations.css      # Keyframes, transiciones y efectos hover
├── img/
│   ├── products/           # 22 fotografías de productos ecológicos (500x500)
│   ├── icons/              # 16 iconos PNG transparentes institucionales
│   └── hero/               # Banners, mapa, historia y retratos de clientes
├── views/
│   ├── productos.html      # Catálogo con 20 productos y filtros
│   ├── sobre-nosotros.html # Misión, principios y carrusel de testimonios
│   └── contacto.html       # Formulario inteligente con validación pura CSS
├── download_images.ps1     # Script de descarga automatizada de assets
├── generate_icons.ps1      # Script generador de los iconos PNG vectoriales
├── index.html              # Página de Inicio (Home)
└── README.md               # Documentación técnica del proyecto
```

---

## 🚀 Instrucciones de Visualización Local

### Requisitos previos
Solo necesitas un navegador web moderno (Google Chrome, Mozilla Firefox, Microsoft Edge o Safari).

### Pasos para ejecutar localmente
1. **Clonar el repositorio:**
   ```bash
   git clone https://github.com/TU_USUARIO/EcoMarket_NombreApellido.git
   cd EcoMarket_NombreApellido
   ```

2. **Abrir en el navegador:**
   - **Opción A (Directa):** Haz doble clic en el archivo `index.html`.
   - **Opción B (Recomendada con VS Code):** Abre la carpeta en Visual Studio Code, haz clic derecho sobre `index.html` y selecciona **"Open with Live Server"**.

3. *(Opcional)* Si deseas regenerar los iconos o descargar de nuevo las imágenes:
   ```powershell
   # En PowerShell dentro del directorio raíz:
   .\download_images.ps1
   .\generate_icons.ps1
   ```

---

## 📸 Galería de Capturas de Pantalla

### 1. Página de Inicio (Home)
| Versión Escritorio | Versión Móvil |
|:---:|:---:|
| *(Captura Desktop - Home)* | *(Captura Móvil - Home)* |

### 2. Catálogo de Productos
| Versión Escritorio (Grid 4 Col + Sidebar) | Versión Móvil (Grid 1 Col) |
|:---:|:---:|
| *(Captura Desktop - Catálogo)* | *(Captura Móvil - Catálogo)* |

### 3. Sobre Nosotros
| Historia y Principios (Escritorio) | Carrusel de Testimonios (Móvil) |
|:---:|:---:|
| *(Captura Desktop - Nosotros)* | *(Captura Móvil - Nosotros)* |

### 4. Contacto
| Formulario con Validación CSS (Escritorio) | Canales y Redes (Móvil) |
|:---:|:---:|
| *(Captura Desktop - Contacto)* | *(Captura Móvil - Contacto)* |

> [!NOTE]
> Puedes añadir tus capturas de pantalla en una carpeta `docs/screenshots/` y referenciarlas en la tabla anterior antes de la entrega final.

---

## 🌐 Guía de Despliegue

La plataforma está optimizada para ser desplegada inmediatamente en cualquier proveedor de alojamiento estático:

### Opción 1: Despliegue en Netlify (Recomendado)
1. Inicia sesión en [Netlify](https://www.netlify.com/).
2. Haz clic en **"Add new site"** $\rightarrow$ **"Import an existing project"**.
3. Conecta tu cuenta de GitHub y selecciona el repositorio `EcoMarket_NombreApellido`.
4. En **Publish directory**, déjalo en blanco o escribe `/` (la raíz contiene `index.html`).
5. Haz clic en **"Deploy EcoMarket"**. En segundos tendrás tu URL pública HTTPS activa.

### Opción 2: Despliegue en Vercel
1. Inicia sesión en [Vercel](https://vercel.com/).
2. Selecciona **"Add New Project"** e importa tu repositorio de GitHub.
3. Deja los valores predeterminados (Framework Preset: *Other*) y haz clic en **"Deploy"**.

### Opción 3: GitHub Pages
1. En tu repositorio de GitHub, ve a **Settings** $\rightarrow$ **Pages**.
2. En la sección **Branch**, selecciona la rama `main` y la carpeta `/ (root)`.
3. Haz clic en **Save**. En un par de minutos tu sitio estará en `https://TU_USUARIO.github.io/EcoMarket_NombreApellido/`.

---

## 🌿 Gestión de Versiones (GitFlow)

El desarrollo del proyecto siguió un flujo estricto basado en **Conventional Commits** y ramas por sección:

```
main --------------------------------------------------------------------------->
       \                                                                /
        \-- [feature/project-setup] -> Commit 1: Inicialización        /
        \-- [feature/html-home]     -> Commit 2: Home semántico        /
        \-- [feature/html-catalog]  -> Commit 3: Catálogo semántico    /
        \-- [feature/html-about]    -> Commit 4: Nosotros semántico    /
        \-- [feature/html-contact]  -> Commit 5: Contacto semántico    /
        \-- [feature/css-base]      -> Commit 6: Design Tokens & Layout/
        \-- [feature/css-components]-> Commit 7: Componentes & UI      /
        \-- [feature/css-animations]-> Commit 8: Animaciones & Hover   /
        \-- [feature/assets-img]    -> Commit 9: Assets e Imágenes     /
        \-- [feature/documentation] -> Commit 10: Documentación README /
```

---

*Proyecto desarrollado con pasión por la sustentabilidad y el diseño web limpio.*
