# Sixa Chips 🍌🍈

Sitio web oficial de **Sixa Chips** — chips de plátano y chips de fruta de pan,
fritas al momento con ingredientes naturales.

🔗 **En producción:** <https://sixachips.github.io/>

## Tecnologías

Sitio 100% estático, sin frameworks ni dependencias:

- HTML5 semántico con metadatos SEO (Open Graph, canonical, JSON-LD)
- CSS moderno: mobile-first, custom properties, tipografía fluida con `clamp()`
- JavaScript vanilla progresivo (el sitio funciona sin JS)
- Accesible: navegación por teclado, `aria-*`, `prefers-reduced-motion`

## Estructura

```
.
├── index.html          # Página principal (one-page)
├── domino.html         # Reglas del dominó + CTA a domino.sixachips.com
├── css/styles.css      # Estilos
├── js/main.js          # Menú móvil y año dinámico
├── assets/             # Favicon e imágenes
├── site.webmanifest    # Manifiesto PWA básico
├── robots.txt          # Rastreo + referencia al sitemap
├── sitemap.xml         # Sitemap
├── AGENTS.md           # Instrucciones para agentes de IA
└── .nojekyll           # Sirve los archivos tal cual, sin Jekyll
```

## Desarrollo local

No hay build step. Solo sirve los archivos desde la raíz:

```bash
python3 -m http.server 8000
```

Luego abre <http://localhost:8000>.

## Despliegue

El sitio se despliega automáticamente a **GitHub Pages** desde `main`
(GitHub Actions: *Deploy from a branch*). Todo lo que se hace *push* a
`main` queda en producción.

## Contacto

- 📧 info@sixachips.com
- 📞 +506 8841 5024
- 📍 Paraíso de Sixaola, Limón, Costa Rica

