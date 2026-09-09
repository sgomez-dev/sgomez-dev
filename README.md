<div align="center">

<img src="https://readme-typing-svg.herokuapp.com?font=JetBrains+Mono&weight=600&size=28&duration=3000&pause=1000&color=534AB7&center=true&vCenter=true&random=false&width=650&lines=Full-Stack+Engineer;IA+y+LLM+en+producci%C3%B3n;RAG+%C2%B7+Evals+%C2%B7+Agentes+%C2%B7+Bots;Lo+que+no+existe%2C+lo+creo." alt="Santiago Gómez de la Torre: Full-Stack Engineer, IA y LLM en producción, RAG, evals, agentes y bots" />

</div>

# Santiago Gómez de la Torre Romero
### Full-Stack Engineer · IA aplicada · `sgomez.dev` · Santander, Cantabria, España

<img align="right" src="https://media.giphy.com/media/qgQUggAC3Pfv687qPC/giphy.gif" width="270" alt="Animación de terminal" />

Soy Santiago Gómez de la Torre Romero, desarrollador full-stack en **Evenbytes** (Angular, Node.js, GCP) y organizador de **GDG Santander**, con background en SysAdmin, cloud y arquitectura de producto.

Trabajo en llevar sistemas con LLM a producción: búsqueda semántica y RAG, evaluación de calidad con métricas reales, herramientas para agentes de código y bots conversacionales. Lo que construyo lo mido antes de contarlo, y publico también los números que salen mal.

`Ingeniería Informática (UNEATLANTICO)` · `Hack2Progress` · `GDG Santander`

<br clear="right"/>

---

## En qué trabajo

**IA en producción.** Retrieval y RAG con embeddings, evaluación sobre golden sets en vez de impresiones, y observabilidad de lo que devuelve el modelo. Integración de LLM sobre producto que ya existe, no pruebas de concepto que se quedan en la rama.

**Bots y automatización.** Bots conversacionales, pipelines de calificación y agentes que ejecutan acciones reales contra APIs de terceros, con control y trazabilidad desde el primer día.

**Full-stack y plataforma.** TypeScript de punta a punta, Angular y Node.js en el día a día, Python y FastAPI para la parte de datos e IA. Docker, Kubernetes y GCP para que lo anterior aguante en producción.

Disponible para proyectos remotos. Escríbeme por [LinkedIn](https://linkedin.com/in/sgomez-dev).

---

## En lo que estoy ahora

**[Claude Canvas](https://github.com/sgomez-dev/claude-canvas)**
Un toolkit TUI que le da a Claude Code su propio display: abre un panel interactivo junto a la conversación, la persona actúa ahí y la respuesta vuelve al agente como un valor exacto en vez de prosa que interpretar. Elegir uno de ocho ficheros o aprobar tres hunks de un diff y rechazar el cuarto es mucho más barato en un panel que escribiéndolo.

Es un fork del proof of concept de [David Siegel](https://github.com/dvdsgl/claude-canvas), publicado por él como no soportado. Lo que añado va desde lo aburrido hasta lo estructural: unificar dos capas de IPC incompatibles en un solo transporte con token por canvas, cerrar una inyección de comandos en el spawn, soporte de Windows, y una suite de tests y CI en tres sistemas operativos que antes no existían. Encima de esa base salieron los primitivos genéricos (`picker`, `form`, `table`, `diff`) y la composición de varios en un mismo panel.
`TypeScript` `Bun` `Ink` `tmux` `293 tests` `CI Linux/macOS/Windows`

**[Búsqueda semántica para NudaUI](https://rag.nudaui.dev)**
Servicio de retrieval sobre el catálogo de NudaUI: embeddings con Voyage AI, API en FastAPI y un golden set de 45 consultas reales para evaluarlo. El hit@1 pasó de 0,67 a 0,80 iterando el índice, y las categorías que empeoraron están documentadas igual que las que mejoraron.
`Python` `FastAPI` `Voyage AI` `Evals`

**Medir primero**
Newsletter quincenal en español sobre lo que aprendo construyendo estos sistemas. Números reales, incluidos los que no salen.
🔗 [Suscríbete en LinkedIn](https://linkedin.com/in/sgomez-dev)

---

## Proyectos

**[NudaUI](https://nudaui.dev)**
Librería de componentes que empezó con 28 piezas y hoy son 1.503 repartidas en 81 categorías. Cero dependencias, cero `npm install`, cero build step: copias y pegas, y funciona en cualquier stack. Accessibility-first por defecto y licencia MIT. Los agentes de IA pueden consumir el catálogo estructurado directamente desde el servidor.
`CSS` `JavaScript` `Framework-agnostic` `MIT`

**[sgomez-cli](https://cli.sgomez.dev)**
Developer toolkit que scaffoldea, configura y lanza proyectos en 14 frameworks de JS, Python y Go. Añade Docker, CI/CD, auth, base de datos y testing a proyectos que ya existen, e incluye `sgomez doctor` para diagnosticar el estado de un repo. 73 tests, publicado en npm.
`Node.js` `TypeScript` `Commander.js` `npm`

**[Portfolio OS](https://sgomez.dev)**
Un portafolio interactivo que simula un sistema operativo en el navegador. Mis proyectos, como ventanas.
`Next.js` `Vite` `Tailwind` `Motion`

**[Blog técnico](https://blog.sgomez.dev)**
Next.js y Supabase con arquitectura hexagonal, panel de administración propio con subida de imágenes y newsletter con doble opt-in conforme a RGPD. Escribo sobre desarrollo, producto e IA.
`Next.js` `Supabase` `MDX` `Resend`

**EliteEstate Manager**
SaaS inmobiliario multi-tenant para agencias en Centroamérica. Migración de Firebase a Supabase con 12 migraciones SQL y una suite de 48 tests que verifica el aislamiento por RLS entre tenants. La capa de datos está terminada y la de aplicación viene después.
`Supabase` `PostgreSQL` `RLS` `TypeScript`

**Bot de trading algorítmico**
Proyecto personal en TypeScript, unas 4.800 líneas y 88 tests. Validación walk-forward, ejecución de órdenes en Binance y control completo desde Telegram.
`TypeScript` `Node.js` `Telegram Bot API`

---

## Stack

**Lenguajes:** TypeScript, JavaScript, Python, Bash, Rust
**Frontend:** Angular, React, Vue, Next.js, Nuxt, Svelte, Tailwind, Vite
**Backend e IA:** Node.js, Express, FastAPI, Supabase, Firebase, APIs de LLM, RAG y embeddings
**DevOps:** GCP, AWS, Azure, Docker, Kubernetes, Cloudflare, Linux, Nginx, Jenkins
**Datos:** PostgreSQL, MySQL, MongoDB

<p>
  <img src="https://skillicons.dev/icons?i=ts,js,python,bash,rust,angular,react,vue,nextjs,nuxtjs,svelte,tailwind" alt="TypeScript, JavaScript, Python, Bash, Rust, Angular, React, Vue, Next.js, Nuxt, Svelte, Tailwind" />
  <img src="https://skillicons.dev/icons?i=nodejs,express,fastapi,supabase,firebase,gcp,aws,azure,docker,kubernetes,cloudflare,postgres" alt="Node.js, Express, FastAPI, Supabase, Firebase, GCP, AWS, Azure, Docker, Kubernetes, Cloudflare, PostgreSQL" />
</p>

---

## Estadísticas

<p>
  <img src="https://streak-stats.demolab.com?user=sgomez-dev&theme=transparent&hide_border=true&ring=534AB7&fire=534AB7&currStreakLabel=888780&sideLabels=888780&currStreakNum=888780&sideNums=888780&dates=888780" width="48%" alt="Racha de contribuciones de sgomez-dev en GitHub" />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=sgomez-dev&layout=compact&theme=transparent&hide_border=true&title_color=888780&text_color=888780" width="48%" alt="Lenguajes más usados por sgomez-dev" />
</p>

---

## Conectemos

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/sgomez-dev)
[![Portfolio](https://img.shields.io/badge/sgomez.dev-000000?style=flat&logo=safari&logoColor=white)](https://sgomez.dev)
[![Blog](https://img.shields.io/badge/blog.sgomez.dev-534AB7?style=flat&logo=hashnode&logoColor=white)](https://blog.sgomez.dev)
[![Instagram](https://img.shields.io/badge/Instagram-E4405F?style=flat&logo=instagram&logoColor=white)](https://instagram.com/santigt1503)

---

<div align="center">
  <img src="https://komarev.com/ghpvc/?username=sgomez-dev&color=534AB7&style=flat-square&label=Visitas+al+perfil" alt="Contador de visitas al perfil" />
</div>
