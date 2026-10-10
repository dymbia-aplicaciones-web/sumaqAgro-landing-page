# SumaqAgro — Landing Page

[![Release](https://img.shields.io/badge/release-v2.0.1-brightgreen.svg)](#versionado-y-flujo-de-trabajo)
[![Stack](https://img.shields.io/badge/stack-HTML5%20%7C%20CSS3%20%7C%20JavaScript-blue.svg)](#stack-tecnológico)
[![i18n](https://img.shields.io/badge/i18n-ES%20%7C%20EN-orange.svg)](#internacionalización)
[![Course](https://img.shields.io/badge/UPC-Aplicaciones%20Web-red.svg)](https://www.upc.edu.pe/)
[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg)](LICENSE.md)

Repositorio oficial de la **landing page de SumaqAgro**, la plataforma SaaS de agricultura de precisión de la startup peruana **Dymbia**.

Sitio web estático, responsive y bilingüe (español e inglés), desarrollado con **HTML5, CSS3 y JavaScript vanilla**.

Proyecto desarrollado para el curso **Aplicaciones Web** de la Universidad Peruana de Ciencias Aplicadas (UPC), ciclo **2026-20**.

---

## Información Académica

- **Institución:** Universidad Peruana de Ciencias Aplicadas (UPC)
- **Facultad:** Facultad de Ingeniería
- **Carrera:** Ingeniería de Software
- **Curso:** Aplicaciones Web - 1ASI0730
- **Ciclo Académico:** 2026-20
- **Docente:** Villafuerte Bazan, Oscar Ivan

---

## Descripción del Proyecto

**Startup:** Dymbia  
**Producto:** SumaqAgro

**Dymbia** busca cerrar la brecha de digitalización del sector agroalimentario peruano. Su propuesta se orienta a pequeños y medianos productores, cooperativas agrarias y asesores técnicos de las cadenas de **papa andina** y **café de especialidad**.

La landing page presenta la propuesta de valor de SumaqAgro bajo el lema:

> Cultiva con información. Decide con precisión.

El sitio muestra las soluciones del producto, los segmentos de usuarios, el equipo de desarrollo y los planes de suscripción.

### Soluciones Presentadas

1. **Monitoreo Satelital de Vigor y Humedad:** información basada en índices NDVI y NDWI mediante Sentinel-2.
2. **Contabilidad de Costos por Lote:** registro financiero y cálculo del precio mínimo de venta.
3. **Certificación Digital de Calidad de Cosecha:** constancias PDF con código QR auditable.
4. **Prescripciones y Alertas Agronómicas:** avisos relacionados con heladas, plagas y estrés hídrico.

Estas soluciones describen la propuesta del producto; la landing page cumple una función informativa y comercial.

---

## Secciones del Sitio

| Sección | Descripción |
|---|---|
| Inicio | Propuesta de valor y llamadas a la acción |
| Nosotros | Presentación de Dymbia y SumaqAgro |
| Nuestro equipo | Perfiles de los cinco integrantes |
| ¿A quién ayudamos? | Agricultores, líderes de cooperativas y asesores técnicos |
| Soluciones | Capacidades principales del producto |
| Demostración | Presentación audiovisual de SumaqAgro |
| Planes | Planes de suscripción y selector de facturación |
| Impacto | Información sobre el contexto agrícola |
| Testimonios | Sección de opiniones presentada en el sitio |
| Llamada a la acción | Invitación a conocer y utilizar la plataforma |
| Footer | Enlaces de navegación y páginas legales |

### Páginas Legales

- **Política de Privacidad:** información sobre el tratamiento y protección de datos.
- **Términos de Servicio:** condiciones de uso de la plataforma.
- **Política de Cookies:** información sobre almacenamiento de preferencias y gestión de cookies.

---

## Características Técnicas

- **Diseño responsive:** adaptación a dispositivos móviles, tablets y computadoras.
- **Navegación móvil:** menú desplegable con actualización del estado `aria-expanded`.
- **Facturación interactiva:** selección entre precios mensuales y anuales.
- **Internacionalización:** contenido disponible en español e inglés.
- **Persistencia de idioma:** almacenamiento de la preferencia mediante `localStorage`.
- **SEO:** título, descripción, palabras clave y metadatos Open Graph.
- **Accesibilidad:** estructura semántica, textos alternativos, etiquetas accesibles y enlace para saltar al contenido.
- **Recursos visuales:** imágenes, iconos SVG y tipografía Inter.

### Internacionalización

Las traducciones se aplican mediante atributos `data-i18n` y diccionarios de idioma.

El selector permite cambiar entre español e inglés y actualizar el idioma del documento. La preferencia se conserva entre visitas mediante `localStorage`.

---

## Stack Tecnológico

| Área | Tecnología |
|---|---|
| Estructura | HTML5 |
| Estilos y diseño responsive | CSS3 |
| Interactividad | JavaScript vanilla |
| Tipografía | Inter |
| Iconografía | SVG |
| Control de versiones | Git y GitHub |
| Gestión y diseño | Jira y Miro |

> SumaqAgro propone una solución de software en la nube. Su alcance no contempla la fabricación ni instalación de sensores físicos o dispositivos IoT.

---

## Ejecución Local

La landing page no requiere compilación.

### 1. Clonar el repositorio

```bash
git clone https://github.com/dymbia-aplicaciones-web/sumaqAgro-landing-page.git
cd sumaqAgro-landing-page
```

### 2. Iniciar un servidor local

Con Python instalado:

```bash
python -m http.server 8080
```

### 3. Abrir el sitio

Acceder a:

```text
http://localhost:8080
```

También puedes utilizar la extensión **Live Server** de Visual Studio Code.

---

## Organización del Proyecto

- **Página principal:** contenido y estructura de la landing page.
- **Estilos:** presentación visual y reglas responsive.
- **JavaScript:** navegación, selección de idioma y facturación.
- **Recursos:** imágenes, fuentes e iconos.
- **Páginas legales:** privacidad, términos de servicio y cookies.
- **Documentación:** README, historial de cambios y licencia.

---

## Equipo de Desarrollo

| Integrante |
|---|
| Solorzano Sullca, Benjamin |
| Tejada Pumacayo, Yamil Jared |
| Vargas Enriquez, Jose Carlos |
| Sanca Condori, Miguel |
| Duarte Ruffner, Drago Derick |

---

## Versionado y Flujo de Trabajo

El proyecto utiliza **GitFlow** para organizar el desarrollo:

- `main`: versión de producción.
- `develop`: integración de cambios.
- `feature/*`: desarrollo de funcionalidades y documentación.
- `release/*`: preparación de versiones.
- `fix/*`: corrección de errores.

Los mensajes de commit siguen **Conventional Commits**:

```text
feat(landing): add team presentation section
fix(i18n): correct billing period translations
docs(readme): update project information for Aplicaciones Web
style(footer): improve responsive layout
```

### Versiones

El repositorio cuenta con los tags:

- `v2.0.1`
- `v2.0.0`
- `v1.1.0`
- `v1.0.0`

Consultar [CHANGELOG.md](CHANGELOG.md) para conocer el historial de cambios.

---

## Repositorios

- **Landing page:** https://github.com/dymbia-aplicaciones-web/sumaqAgro-landing-page
- **Reporte académico:** https://github.com/dymbia-aplicaciones-web/sumaqAgro-report

---

## Licencia

Distribuido bajo la licencia **CC BY-NC-SA 4.0**.

Consultar [LICENSE.md](LICENSE.md) para conocer sus condiciones.

© 2026 Dymbia — SumaqAgro.