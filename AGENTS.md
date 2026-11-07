# AGENTS.md

Instrucciones para agentes de IA (y humanos) que trabajen en este repositorio.

## Descripción del proyecto

Sitio estático de **Sixa Chips**, una empresa de frituras (chips de plátano y
chips de fruta de pan). Se sirve mediante **GitHub Pages** en
<https://sixachips.github.io/>.

## Estructura del proyecto

```
.
├── index.html          # Página única (one-page), todo el contenido aquí
├── css/styles.css      # Única hoja de estilos, sin frameworks
├── js/main.js          # JS progresivo y mínimo (el sitio funciona sin JS)
├── assets/             # Favicon e imágenes
├── site.webmanifest    # Manifiesto PWA básico
├── robots.txt          # SEO: rastreo + referencia al sitemap
├── sitemap.xml         # SEO: sitemap del sitio
└── .nojekyll           # GitHub Pages sirve los archivos tal cual, sin Jekyll
```

## Stack y restricciones

- **HTML + CSS + JS vanilla.** No agregar frameworks (React, Vue, Tailwind,
  Bootstrap, etc.) ni librerías externas. La gracia del sitio es que es simple
  y sin dependencias.
- **Sin loaders ni bundlers.** Los archivos se sirven tal cual; las rutas en
  HTML deben ser **relativas** (compatibles con GitHub Pages en subcarpetas).
- **Sin elementos `style=` ni `onclick=` inline.** Estilos en `css/styles.css`
  y comportamiento en `js/main.js`.

## Comandos

```bash
# Servidor local de desarrollo (desde la raíz del repo)
python3 -m http.server 8000
# → http://localhost:8000
```

No hay build step: lo que se commitea es lo que se despliega.

## Convenciones

### HTML
- Idioma del contenido: **español** (`lang="es"`). El inglés solo para nombres
  de archivos, clases y commits.
- HTML semántico: `header`, `nav`, `main`, `section`, `article`, `footer`.
- Mantener la accesibilidad: textos alternativos, etiquetas `aria-*` en
  controles interactivos, enlace "saltar al contenido", jerarquía de encabezados.
- Los metadatos SEO (description, canonical, Open Graph) deben mantenerse
  consistentes al agregar páginas.

### CSS
- Mobile-first, con `@media (min-width: ...)` para breakpoints.
- Usar las custom properties de `:root` como tokens (colores, radios, sombras).
  No hardcodear colores nuevos; agregar tokens si hace falta.
- Nomenclatura en kebab-case, sin preprocesadores.

### JavaScript
- Mínimo y progresivo: mejoras, no requisitos. Cualquier funcionalidad debe
  degradar sin JS.
- Cargar con `defer`. Sin librerías.

## Checks antes de hacer commit

1. El sitio carga sin errores en consola del navegador.
2. No se introdujeron dependencias ni rutas absolutas (`/assets/...`).
3. Verificar la página en viewport móvil (~375px) y escritorio.
4. Si se agrega una página nueva: actualizar `sitemap.xml` y la navegación.

## No hacer

- No subir binarios grandes (imágenes de producto pesadas) sin comprimir.
- No tocar `venv/` ni otros artefactos listados en `.gitignore`.
- No cambiar la URL canónica (`https://sixachips.github.io/`) salvo que el
  dominio cambie.
- No eliminar `.nojekyll`.

# Información para el sitio.

## **Nuestra Historia: Raíces, Esfuerzo y Sabor Auténtico**

**De la tierra al corazón de Sixaola**  
**Sixachips** es una microempresa familiar nacida en **Paraíso de Sixaola, Limón**, respaldada por una trayectoria de 29 años en el cultivo del plátano. Durante los primeros diez años, la cosecha familiar se exportaba a Miami y Nueva York a través de firmas como Dole y Del Monte. Sin embargo, en 2008, intensas inundaciones dejaron al país casi sin plantaciones y forzaron la pérdida de esos mercados internacionales, redirigiendo el esfuerzo hacia la distribución en el mercado nacional.

**Un giro artesanal y sostenible**  
Frente a los constantes retos del mercado y las temporadas de precios bajos, en 2017 la familia decidió transformar su propia cosecha e iniciar la producción de **chips de plátano**. Al ser elaborado de forma artesanal y directamente por el agricultor, cada lote se procesa mediante controles cuidadosos y manuales que garantizan la máxima calidad con un menor impacto ambiental.

**Trabajo comunitario y comercio justo**  
Con el propósito de generar oportunidades en una zona rural donde el empleo es limitado, la familia adaptó su propia casa para instalar la producción e integrar a vecinos y familiares al equipo de trabajo. Hoy, Sixachips se destaca por impulsar el desarrollo local, practicar el **comercio justo**, apoyar a otros productores de la zona y promover la inclusión y la diversidad.

**Tradición e innovación en cada empaque**  
Actualmente, la marca ofrece una variedad de chips de **plátano verde, plátano maduro, limón y sal, y fruta de pan**. Cada producto se elabora como un alimento **100% costarricense con materia prima nacional**, certificado como **libre de gluten** y **sin grasas trans**, reflejando la pureza y el orgullo del campo limonense.


## Contacto

Teléfono: +506 88415024
Contacto: info@sixachips.com
