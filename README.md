<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=26&duration=3200&pause=900&color=534AB7&center=true&vCenter=true&random=false&width=720&lines=Full-Stack+Engineer+%C2%B7+IA+en+producci%C3%B3n;RAG%2C+evals%2C+agentes+y+bots;hit%401+de+0%2C67+a+0%2C80.+Publiqu%C3%A9+las+dos+cifras.;Lo+que+no+existe%2C+lo+creo." alt="Santiago Gómez de la Torre: Full-Stack Engineer, IA en producción, RAG, evals, agentes y bots" />

<br/>

**Santiago Gómez de la Torre Romero**
Full-Stack Engineer · Cofundador de [SkyQuetz Consulting](https://skyquetz.com) · Santander, España

[![Portfolio](https://img.shields.io/badge/sgomez.dev-000000?style=for-the-badge&logo=safari&logoColor=white)](https://sgomez.dev)
[![Blog](https://img.shields.io/badge/blog-534AB7?style=for-the-badge&logo=hashnode&logoColor=white)](https://blog.sgomez.dev)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/sgomez-dev)
[![CV](https://img.shields.io/badge/CV-534AB7?style=for-the-badge&logo=readdotcv&logoColor=white)](https://sgomez.dev/CV_Santiago_G%C3%B3mez_de_la_Torre_Romero.pdf)
[![Email](https://img.shields.io/badge/contacto@sgomez.dev-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:contacto@sgomez.dev)

<br/>

<a href="https://claude-canvas.sgomez.dev">
  <img src="./assets/claude-canvas-demo.gif" width="85%" alt="Claude Canvas: un panel interactivo se abre junto a Claude Code, se elige un fichero y la respuesta vuelve al agente como un valor exacto" />
</a>

<sub><b>Claude Canvas</b> · Claude Code no tiene pantalla. Le di una.</sub>

</div>

---

Llevo sistemas con LLM a producción: retrieval y RAG, evaluación con golden sets propios, herramientas para agentes de código y bots conversacionales. Trabajo con Angular, Node.js y GCP en **Evenbytes**, organizo **GDG Santander** y en 2026 cofundé **SkyQuetz Consulting**, donde llevo la ingeniería.

Lo que construyo lo mido antes de contarlo. Cuando un número baja, ese también lo publico.

---

## Los números

| Qué                                                  | Cuánto                     | Dónde                                                               |
| ---------------------------------------------------- | -------------------------- | ------------------------------------------------------------------- |
| Precisión del primer resultado en búsqueda semántica | **0,67 → 0,80** hit@1      | [NudaUI RAG](https://blog.sgomez.dev/rag-busqueda-semantica-nudaui) |
| Componentes UI copy-paste, cero dependencias         | **1.503** en 81 categorías | [NudaUI](https://nudaui.dev)                                        |
| Tests y sistemas operativos en CI                    | **600+** tests, **3** SO   | [Claude Canvas](https://github.com/sgomez-dev/claude-canvas)        |
| Frameworks que scaffoldea en un comando              | **14**                     | [sgomez-cli](https://cli.sgomez.dev)                                |
| Aislamiento entre tenants verificado por test        | **48** tests sobre RLS     | EliteEstate Manager                                                 |
| Repositorios públicos                                | **40+**                    | [github.com/sgomez-dev](https://github.com/sgomez-dev)              |

---

## En lo que estoy ahora

### [Claude Canvas](https://claude-canvas.sgomez.dev) · `plugin de Claude Code`

Claude Code no tiene pantalla. Le di una.

Abre un panel interactivo de terminal junto a la conversación: eliges un fichero entre ocho, apruebas tres hunks de un diff y rechazas el cuarto, rellenas cinco campos. Tu respuesta le vuelve al agente como un valor exacto y no como prosa que tenga que interpretar.

Partí del proof of concept de [David Siegel](https://github.com/dvdsgl/claude-canvas), que él publicó como no soportado, y lo llevé a algo que aguanta uso diario. Unifiqué dos capas de IPC incompatibles (una de ellas no le entregaba la respuesta a nadie) en un solo transporte con token por canvas, cerré una inyección de comandos en el spawn, añadí soporte de Windows y monté una suite de tests con CI en tres sistemas operativos donde no había ni uno. Encima de esa base salieron las primitivas reutilizables y la composición de varias en un mismo panel.

```bash
/plugin marketplace add sgomez-dev/claude-canvas
```

`TypeScript` `Bun` `Ink` `tmux` `IPC` · 9 tipos de panel · MIT

### [NudaUI](https://nudaui.dev) · `librería de componentes`

Empezó con 28 piezas que necesitaba para un proyecto mío. Hoy son 1.503 repartidas en 81 categorías, y sigo siendo el único que las mantiene.

Lo que la separa del resto es lo que no tiene. Cero dependencias, cero `npm install`, cero build step. Copiás el HTML y el CSS, los pegás, y funciona en React, Vue, Svelte, Astro, Laravel, Django o un `.html` suelto abierto desde el escritorio. JavaScript solo donde de verdad hace falta. Accesibilidad de entrada y no como issue pendiente, MIT sin letra pequeña, y nada que se rompa cuando actualices otra cosa.

Encima del catálogo monté una [búsqueda semántica](https://blog.sgomez.dev/rag-busqueda-semantica-nudaui): preguntás en lenguaje natural y te devuelve el componente que sirve. Pipeline de RAG completo sin frameworks de RAG, con embeddings de Voyage, retrieval por coseno y servicio en FastAPI. Lo evalúo contra un golden set de 45 consultas reales. El hit@1 subió de 0,67 a 0,80 iterando el índice, y la categoría que empeoró está documentada igual de visible que las que mejoraron.

Después [reescribí la documentación](https://blog.sgomez.dev/nudaui-agent-friendly-documentacion-agentes) asumiendo que quien la lee es un agente y no una persona, porque cada vez más lo es. El catálogo se consume estructurado directo del servidor, sin scrapear HTML.

`Next.js` `TypeScript` `CSS` `Python` `FastAPI` `Voyage AI` · 1.503 componentes · 81 categorías · MIT

### [Synentria](https://synentria.skyquetz.com) · `producto de SkyQuetz`

Motor de auditoría SEO y GEO. Le pasas una URL y devuelve hallazgos priorizados con parches aplicables. Ningún hallazgo lo decide un modelo de lenguaje: todos salen de comprobaciones deterministas, y el modelo solo redacta prosa alrededor de algo que ya existe. Escribí el motor.

`TypeScript` `Nuxt` `Node` `Evals`

### Medir primero · `newsletter`

Quincenal, en español, sobre lo que aprendo construyendo esto. Números reales, incluidos los que no salen.
[Suscribirse en LinkedIn](https://linkedin.com/in/sgomez-dev)

---

## Open source que mantengo

<p align="center">
  <a href="https://github.com/sgomez-dev/claude-canvas">
    <img width="49%" src="https://github-readme-stats.vercel.app/api/pin/?username=sgomez-dev&repo=claude-canvas&bg_color=00000000&title_color=534AB7&icon_color=534AB7&text_color=888780&hide_border=true" alt="Claude Canvas" />
  </a>
  <a href="https://github.com/sgomez-dev/sgomez-cli">
    <img width="49%" src="https://github-readme-stats.vercel.app/api/pin/?username=sgomez-dev&repo=sgomez-cli&bg_color=00000000&title_color=534AB7&icon_color=534AB7&text_color=888780&hide_border=true" alt="sgomez-cli" />
  </a>
</p>

**[sgomez-cli](https://cli.sgomez.dev)** · Scaffoldea, configura y despliega proyectos en 14 frameworks de JS, Python y Go. Añade Docker, CI/CD, auth, base de datos y testing a repos que ya existen, y trae `sgomez doctor` para diagnosticar el estado de uno. 73 tests, publicada en npm.

---

## Cómo trabajo

**IA que llega a producto, no a demos.** Integro LLM sobre lo que ya está en producción. Evalúo con golden sets en vez de impresiones y dejo observabilidad sobre lo que devuelve el modelo, porque una respuesta que suena bien y una correcta no son lo mismo.

**Bots y agentes con trazabilidad.** Pipelines de calificación, bots conversacionales y agentes que ejecutan acciones reales contra APIs de terceros. Control desde el primer día, no parcheado después.

**No solo el código, también el resultado.** Cofundar una consultora cambia el trabajo: hay que decidir el alcance, hablar con el cliente y responder de lo entregado.

> Disponible para proyectos remotos. Escríbeme a [contacto@sgomez.dev](mailto:contacto@sgomez.dev) o por [LinkedIn](https://linkedin.com/in/sgomez-dev).

---

## Stack

**Lenguajes** TypeScript · JavaScript · Python · Bash · Rust
**Frontend** Angular · React · Vue · Next.js · Nuxt · Svelte · Tailwind · Vite
**Backend e IA** Node.js · Express · FastAPI · Supabase · Firebase · APIs de LLM · RAG y embeddings
**DevOps** GCP · AWS · Azure · Docker · Kubernetes · Cloudflare · Linux · Nginx · Jenkins
**Datos** PostgreSQL · MySQL · MongoDB

<p align="center">
  <img src="https://skillicons.dev/icons?i=ts,js,python,bash,rust,angular,react,vue,nextjs,nuxtjs,svelte,tailwind" alt="TypeScript, JavaScript, Python, Bash, Rust, Angular, React, Vue, Next.js, Nuxt, Svelte, Tailwind" />
  <br/>
  <img src="https://skillicons.dev/icons?i=nodejs,express,fastapi,supabase,firebase,gcp,aws,azure,docker,kubernetes,cloudflare,postgres" alt="Node.js, Express, FastAPI, Supabase, Firebase, GCP, AWS, Azure, Docker, Kubernetes, Cloudflare, PostgreSQL" />
</p>

---

<details>
<summary><b>Más proyectos</b></summary>

<br/>

**EliteEstate Manager** · SaaS inmobiliario multi-tenant para agencias en Centroamérica. Migración de Firebase a Supabase con 12 migraciones SQL y 48 tests que verifican el aislamiento por RLS entre tenants.
`Supabase` `PostgreSQL` `RLS` `TypeScript`

**Bot de trading algorítmico** · Proyecto personal en TypeScript, unas 4.800 líneas y 88 tests. Validación walk-forward, ejecución de órdenes en Binance y control completo desde Telegram.
`TypeScript` `Node.js` `Telegram Bot API`

**[Portfolio OS](https://sgomez.dev)** · Portafolio interactivo que simula un sistema operativo en el navegador. Mis proyectos, como ventanas.
`Next.js` `Vite` `Tailwind` `Motion`

**[Blog técnico](https://blog.sgomez.dev)** · Next.js y Supabase con arquitectura hexagonal, panel de administración propio con subida de imágenes y newsletter con doble opt-in conforme al RGPD.
`Next.js` `Supabase` `MDX` `Resend`

**[GeekLab](https://github.com/sgomez-dev/GeekLab)** · E-commerce full-stack con catálogo avanzado, carrito persistente, foro en tiempo real por WebSockets y API GraphQL.
`Svelte 5` `Node.js` `Express`

**[SyncCart](https://github.com/sgomez-dev/SyncCart)** · Extensión de Chrome que unifica carritos de Amazon, PcComponentes y MediaMarkt en una sola interfaz con calculadora de presupuesto.
`Plasmo` `React 18` `TypeScript`

**[Sortlab](https://sortlab.sgomez.dev)** · Visualizador interactivo de 15 algoritmos de ordenamiento con animaciones y explicaciones estructuradas.
`React` `TypeScript` `Framer Motion`

</details>

<details>
<summary><b>Para agentes y LLM</b></summary>

<br/>

Mi sitio expone contexto estructurado para que un agente pueda leerlo sin scrapear HTML:

- [`sgomez.dev/llms.txt`](https://sgomez.dev/llms.txt)
- [`sgomez.dev/openapi.json`](https://sgomez.dev/openapi.json)
- [`sgomez.dev/developers`](https://sgomez.dev/developers)

El catálogo de NudaUI también se consume estructurado desde el servidor, sin pasar por la web.

</details>

---

## Actividad

<div align="center">

<img width="48%" src="https://streak-stats.demolab.com?user=sgomez-dev&theme=transparent&hide_border=true&ring=534AB7&fire=534AB7&currStreakLabel=888780&sideLabels=888780&currStreakNum=888780&sideNums=888780&dates=888780" alt="Racha de contribuciones de sgomez-dev" />
<img width="41%" src="https://github-readme-stats.vercel.app/api/top-langs/?username=sgomez-dev&layout=compact&langs_count=8&hide_border=true&bg_color=00000000&title_color=534AB7&text_color=888780" alt="Lenguajes más usados" />

<img src="https://github-readme-activity-graph.vercel.app/graph?username=sgomez-dev&bg_color=00000000&color=534AB7&line=534AB7&point=888780&area=true&hide_border=true" alt="Gráfico de actividad de sgomez-dev" />

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/sgomez-dev/sgomez-dev/output/snake-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/sgomez-dev/sgomez-dev/output/snake.svg" />
  <img src="https://raw.githubusercontent.com/sgomez-dev/sgomez-dev/output/snake.svg" alt="Grafo de contribuciones de sgomez-dev" />
</picture>

</div>

---

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/sgomez-dev)
[![Portfolio](https://img.shields.io/badge/sgomez.dev-000000?style=flat&logo=safari&logoColor=white)](https://sgomez.dev)
[![Blog](https://img.shields.io/badge/blog.sgomez.dev-534AB7?style=flat&logo=hashnode&logoColor=white)](https://blog.sgomez.dev)
[![Instagram](https://img.shields.io/badge/Instagram-E4405F?style=flat&logo=instagram&logoColor=white)](https://instagram.com/santigt1503)

<img src="https://komarev.com/ghpvc/?username=sgomez-dev&color=534AB7&style=flat-square&label=Visitas+al+perfil" alt="Contador de visitas al perfil" />

</div>
