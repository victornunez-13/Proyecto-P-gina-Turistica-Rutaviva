# RutaViva · Sitio web turístico de Ecuador · Victor Nuñez

Proyecto académico de un sitio web turístico desarrollado con **HTML5 semántico** y **CSS3 externo**, sin JavaScript. Es responsivo con enfoque *Mobile First* y está disponible como imagen en Docker Hub y Github.
 
[![GitHub](https://img.shields.io/badge/GitHub-victornunez--13%2FRutaviva-181717?logo=github&logoColor=white)](https://github.com/victornunez-13/Proyecto-P-gina-Turistica-Rutaviva/tree/main)

[![Docker Hub](https://img.shields.io/badge/Docker%20Hub-victor124312%2Fpagina--turistica--rutaviva-2496ED?logo=docker&logoColor=white)](https://hub.docker.com/r/victor124312/pagina-turistica-rutaviva)

**Repositorio en GitHub:** https://github.com/victornunez-13/Proyecto-P-gina-Turistica-Rutaviva/tree/main
 
**Imagen en Docker Hub:** https://hub.docker.com/r/victor124312/pagina-turistica-rutaviva

---

## Tabla de contenidos

1. [Páginas del sitio](#páginas-del-sitio)
2. [Estructura del proyecto](#estructura-del-proyecto)
3. [Tecnologías y requisitos técnicos](#tecnologías-y-requisitos-técnicos)
4. [Características destacadas](#características-destacadas)
5. [Cómo ejecutar el proyecto](#cómo-ejecutar-el-proyecto)
   - [Opción 1: Abrir directamente en el navegador](#opción-1-abrir-directamente-en-el-navegador)
   - [Opción 2: Docker – descargar desde Docker Hub](#opción-2-docker--descargar-desde-docker-hub)


---

## Páginas del sitio

| Página | Contenido |
|---|---|
| `index.html` | Inicio: presentación, identidad visual y menú de navegación |
| `destinos.html` | 5 destinos turísticos con imágenes y descripciones |
| `galeria.html` | Galería de 15 fotos con filtros por categoría y lightbox |
| `paquetes.html` | 4 paquetes con precios, duración, servicios y tabla comparativa |
| `itinerarios.html` | 2 itinerarios organizados por días y horarios (`<time>`) |
| `contacto.html` | Formulario de consultas con validaciones HTML5 |

---

## Estructura del proyecto

```text
rutaviva/
├── index.html
├── destinos.html
├── galeria.html
├── paquetes.html
├── itinerarios.html
├── contacto.html
├── css/
│   └── styles.css
├── images/
├── Dockerfile
├── .dockerignore
└── README.md
```

---

## Tecnologías y requisitos técnicos

| Requisito | Implementación |
|---|---|
| **HTML5 semántico** | `header`, `nav`, `main`, `section`, `article`, `aside`, `figure`, `figcaption`, `footer`, `form`, `fieldset`, `legend`, `time`, `table` |
| **CSS3 externo** | Una sola hoja de estilos enlazada: `css/styles.css` |
| **Mobile First** | Estilos base para móvil y *media queries* con `min-width` (480, 640, 700, 768, 900, 960, 1024 y 1100 px) |
| **Flexbox** | Navegación, tarjetas, chips y botones |
| **CSS Grid** | Destinos, galería, paquetes, formulario y pie de página |
| **Navegación** | Menú con estado activo (`aria-current="page"`), anclas internas y enlaces entre las 6 páginas |

### Formulario de contacto

Incluye datos personales, destino de interés y mensaje, con validaciones HTML5:

- Atributos: `required`, `pattern`, `minlength` / `maxlength`, `min` / `max`
- Tipos de campo: `email`, `tel`, `date`, `number`
- `select` con opción obligatoria y `checkbox`

---

## Características destacadas

Todo está hecho con **HTML + CSS, sin JavaScript**:

- **Menú hamburguesa** con la técnica del *checkbox hack*
- **Filtro de galería** por categorías con radios + selector `:checked`
- **Lightbox** de fotografías con el pseudo-selector `:target`
- **Pestañas de itinerarios** con radios + selector `:checked`
- **Efecto Ken Burns** (zoom lento) en los héroes de cada página
- **Aparición al hacer scroll** con `animation-timeline: view()`
- **Accesibilidad:** *skip-link*, `alt` descriptivos, `aria-labels`, foco visible, contraste verificado y `prefers-reduced-motion`

---

## Cómo ejecutar el proyecto

### Opción 1: Abrir directamente en el navegador

Abre el archivo `index.html` con tu navegador.

### Opción 2: Docker – descargar desde Docker Hub

No necesitas el código fuente, solo Docker.

**1. Descarga la imagen:**

```bash
docker pull victor124312/pagina-turistica-rutaviva
```

**2. Ejecuta el contenedor:**

```bash
docker run -d --name rutaviva -p 8080:80 victor124312/pagina-turistica-rutaviva
```

**3. Abre el sitio:** http://localhost:8080


---


<p align="center">Proyecto académico · RutaViva · Victor Nuñez</p>
