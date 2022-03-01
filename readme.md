# Begriffe

- JAMStack: Vorgenerierte Apps und Webseiten mit Datenzugriff über Microservices

# NodeJS

- HTTP Server: [Fastify](https://www.fastify.io)
  - TS Ready
  - Async/Await
  - 91% im StateOfJS für 2021
- Runtime: [DENO](https://deno.land)
  - Basis: Rust + V8
  - NodeJS Server sollten auf DENO setzen, damit Zugriffe auf vieles per Default verboten sind
  - TypeScript funktioniert Out-of-the-Box.
  - Eigene [Standard-Library](https://deno.land/std/)
- Threading: [Tinypool](https://github.com/Aslemammad/tinypool)
  - Threading Lösung auf Basis von Piscina, viel schlanker
- Threading: [Piscina](https://github.com/piscinajs/piscina)
  - Die Threading-Lösung für Worker-Pools in NodeJS
- Backend-Framework: [Adonis](https://adonisjs.com/adonisjs-at-a-glance)
  - Ähnlich zu Rails, Laraval und Django
- Headless-CMS: [Strapi](https://strapi.io)
  - Self-Hosted (AWS, Heroku, Azure, ...), OpenSource, REST- oder GraphQL-Zugriff
  - Besseres Contentful?, Teilweise als Buggy eingeordnet, Fast 10x Sterne zu KeyStoneJS auf GitHub
- Headless-CMS: [Keystone](https://keystonejs.com)
  - Hosting auf Vercel, AWS, Azure, etc.
  - Präferiert von Wes Bos und Max Stoiber. Wohooo.
  - Backend Datenbank als MongoDB bzw. via Prisma

# Datenbank

- Datenbank mit API: [Supabase](https://supabase.com)
  - Alternative zu Firebase. Postgres-basiert. Supported durch Mozilla.
- API-Layer für Datenbank: [Hasura](https://hasura.io)
  - Effektiv eine Art API-Layer auf Datenbanken, GraphQL- bzw. REST-Zugriff möglich
  - Incl. API Gateway, Authorization, Caching, etc.
  - Support für Postgres, Amazon Aurora und Google BigQuery
- ORM für Datenbank: [Prisma]()
  - Support für Postgres, MySQL, SQLite, ...

# Frameworks

- JAMStack Framework: [Redwood](https://github.com/redwoodjs/redwood/blob/main/README.md)
  - React (UI Rendering), GraphQL (Datenzugriff Frontend), Prisma (Datenbank-API), Fastify (HTTP-Server), Pino (Logger)
  - Gutes Setup. Teils überlappend mit dem Wes Bos Advanced React Kurs.
  - Teils ein wenig altmodisch: Webpack, Babel etc. und nichts von Vite, SWC, etc. Nichts von der Innovation von Remix, NextJS, etc.
- Serverless Backend: [NHost](https://nhost.io)
  - Integriert eine Vielzahl von Services (Auth, Datenbank via Hasura, File-Store, Emails) als Managed Plattform
  - Gute Plattform für Startups, Noch Beta, Relativ geringe Verbreitung

# Auth

- Authentication: **[Clerk](https://clerk.dev)**
  - Moderner Ersatz für Auth0? Integriert UserManagement selber
  - Will die diversen Probleme anderer Plattformen gelöst haben.
  - Integration mit Supabase + Hasura vorbereitet
  - Die React-Integration sieht super smooth aus
- Authentication: **[MagicLink](https://magic.link)**
  - Dreht sich alles um Passwort-freie Logins
  - Pay per Login Bezahlmodell. Interessante Idee.
- Authentication: [Auth0](https://auth0.com/)
  - Mittlerweile sehr enterprise-ig... Integration teils etwas aufwendig
- Authentication: [Keycloak](https://www.keycloak.org)
  - Self-Hosted, OpenSource, By RedHat
- Authentication: [Ory](https://www.ory.sh)
  - OpenSource, Hosted-Angebot (in dem Fall kommerziell)
  - Erscheint moderner als Keycloak
- Datenbank + Authentification: [Supabase](https://github.com/supabase/supabase)
  - Bietet wie Firebase auch Authentification mit an

# Hosting

- Edge Hosting: [Netlify Edge Handlers](https://www.netlify.com/products/edge/edge-handlers/)
  - Early Access (Stand 2022, Februar)
- Edge Hosting: [Cloudflare Workers](https://workers.cloudflare.com)
  - Sehr günstig
  - Support für dynamische Assets (Bilder) an der Edge
- Edge Hosting: [Vercel Edge Functions](https://vercel.com/docs/concepts/functions/edge-functions)
  - Middleware Supprt
  - Beta (Stand 2022, Februar)
- Worldwide Deploy: [Fly.io](https://fly.io)
- Static Hosting: [Cloudflare Pages](https://pages.cloudflare.com)
  - Github und Gitlab Integration

# Tooling

- Formatierer: [DPrint](https://dprint.dev/overview/)
  - Rust-basiert (30x schneller als Prettier)
  - Via WASM im Browser lauffähig
- Bundler: [Parcel](https://parceljs.org)
  - Compiler setzt auf SWC auf (Rust-basiert)
  - Usage-Modell mit Start beim HTML sehr schön
- Bundler: [Vite](https://vitejs.dev)
  - ESBuild für Production-Build
  - Bundlefrei während der Entwicklung
  - Teilweise etwas eingeschränkt bzgl. Flexibilität
  - Vom VueJS Autoren-Team
  - Rollup-Plugins sind teilweise verwendbar
- Compiler: [SWC](https://swc.rs)
  - Rust-basiert
  - Integration mit Jest und Webpack möglich
  - Als Standard-Compiler in NextJS, Parcel und DENO
  - Unterstützt Browserslist für Cross-Browser-Output
- Compiler: [ESBuild](https://esbuild.github.io)
  - Go-basiert, Hobbyprojekt, Rust wäre evtl. der bessere Kandidat
  - SWC ist wohl schneller, Rust-basiert und flexibler
  - ESBuild wird von Remix verwendet
- Compiler für CSS: [Parcel CSS](https://github.com/parcel-bundler/parcel-css)
  - Parser und Minifier im Stile von PostCSS
  - Browserslist Integration
  - 100x schneller als CSSNano

# Static Site

- Static Site Builder: [Astro](https://astro.build)
  - Partial Hydration erlaubt eine teilweise Dynamisierung
  - Ziel ist aber sicherlich 90% statisch zu haben
  - Gut für klassische Content-reiche Homepages
- Static Site Builder: [Gatsby](https://www.gatsbyjs.com)
  - Jede Menge Plugins und intuitive GraphQL-Abfrage für Daten
  - Ist dramatisch gefallen im "Interest" im State of JS 2021.

# Frontend Frameworks

- Framework: [Remix](https://github.com/remix-run/remix)
  - Cooles Konzept bzgl. Server/Client Split
  - "We think Remix has a better set of tradeoffs than Next.js"
    - Evtl. zündet es deshalb für mich :)
    - Blog Post: [NextJS vs. Remix](https://remix.run/blog/remix-vs-next)
  - Von den React-Router Leuten + Kent C Dodds
- Framework: [NextJS](https://nextjs.org)
  - Fast schon der Klassiker für hybride Apps
  - Endlos viele Features aber etliches auch baked-in (CSS-in-JS)

# Testing

- E2E Testing: **[Playwright](https://playwright.dev)**
  - "Usage" steigt dramatisch. Scheinbar bald beliebter als Cypress.
  - Vergleich zu Cypress:
    - https://medium.com/geekculture/is-playwright-better-than-cypress-playwright-vs-cypress-151bd65a224f
    - https://cathalmacdonnacha.com/cypress-vs-playwright-which-is-best-for-e2e-testing
    - https://alisterbscott.com/2021/10/27/five-reasons-why-playwright-is-better-than-cypress/
- E2E Testing: [Cypress](https://www.cypress.io)
  - "Satisfaction" sinkt aktuell. "Interest" auch. StateOfJS 2021
- Testing Utilities: **[TestingLibrary](https://testing-library.com)**
  - Einfach eine gute Idee. Verdient weit oben im StateOfJS 2021.
  - Support für React, DOM, Cypress und Puppeteer
  - "Accessible by Default" - gute Idee über den Weg Komponenten zu adressieren
- Test-Runner: [Vitest](https://vitest.dev)
  - Basiert auf Vite und damit schneller als andere
  - TS und JSX Support eingebaut
  - Schön im Vergleich zu Jest: API wird importiert, statt global definiert
- Test-Runner: **[Jest](https://jestjs.io)**
  - Etabliert und flexibel
  - Addon: [HappyDOM](https://github.com/capricorn86/happy-dom) für Performance-optimierte DOM-Simulation

# Desktop

- Desktop-App-Framework: [Tauri](https://github.com/tauri-apps/tauri)
  - Moderner Ersatz für Electron. Nicht auf V8/Chrome-Basis sondern Rust und [WRY](https://github.com/tauri-apps/wry).
  - 600KB Apps möglich. Runtime daher wohl sehr kompakt.

# TypeScript

- Utilities für TypeScript: [TS Toolbelt](https://github.com/millsp/ts-toolbelt)
- Utilities für TypeScript: [Utility Types](https://github.com/piotrwitek/utility-types)
  - Letztes Release 2019, aber ein paar nette Dinge enthalten.
- Rätsel für TypeScript: [Type Challenges](https://github.com/type-challenges/type-challenges)
  - Oje. Nicht so einfach.

# React Components

- Virtualization/Windowing: [React Virtual](https://react-virtual.tanstack.com)
  - Hook-basiert. Demo sehr imposant. Erinnert an frühere qooxdoo-Challenges.
- Charting: [React Charts](https://react-charts.tanstack.com)
  - Moderne Lösung auf Basis von D3 und gut in React integriert
- Charting: [ReaViz](https://github.com/reaviz/reaviz)
  - Moderne Lösung auf Basis von D3 und gut in React integriert
- Data Table: [React Table](https://github.com/TanStack/react-table)
  - Headless, ohne Styles, Relativ klein + aber aktuell 02-2022 noch Alpha
- Data Loading: [SWR](https://swr.vercel.app)
  - Gute Datenlade-Lösung mit Caching, etc.
- Data Loading: [React Query](https://github.com/tannerlinsley/react-query)
  - Effektiv eine Alternative zu SWR
- ARIA: **[React ARIA](https://react-spectrum.adobe.com/react-aria/)**
  - Projekt von Adobe mit etlichen Hilfsmethoden (als Hooks) für ARIA-Support
- Abstand: [Spacer by Josh](https://www.joshwcomeau.com/react/modern-spacer-gif/)
  - Ersatz der alten 1px GIFs. Besser als Komponenten selber Abstände zu geben.
- Hooks: [React Use](https://github.com/streamich/react-use)
  - Ein Vielzahl an Hooks für diverse Einsatzzwecke
- Gesture Hooks: [Use Gesture](https://github.com/pmndrs/use-gesture)
  - Kombinierbar mit React Spring + tolle Demos
- Markdown: [MDX](https://mdxjs.com)
  - Wohl die eleganteste Lösung für die Integration von Markdown-Inhalten in Mitten von ReactJS
- Tracking: [React Tracking](https://github.com/nytimes/react-tracking)
  - Deklarative [Tracking Lösung der NYT](https://open.nytimes.com/introducing-react-tracking-declarative-tracking-for-react-apps-2c76706bb79a)

# React State Management

> Jotai is close to Recoil. Zustand is close to Redux.

- State Management: [Zustand](https://github.com/pmndrs/zustand)
  - In der Tat sehr schön. Einfaches globales State-Management mit sehr wenig Boilerplate und Hooks.
  - Gleiche Autoren wie das atomare *Jotai*
- State Management: [Recoil](https://recoiljs.org/)
  - Verglichen mit *Zustand* hat es den Vorteil der hohen Modularität (Atoms)
  - Macht viel viel Sinn. Einzig sonderbar ist, dass man den `key` braucht, obwohl man ja immer mit State-Instanzen arbeitet.
  - Bietet Snapshots und damit Recoil Dev Tools aber noch keine Browser-Tools (Stand 02-2022)
- State Management: **[Jotai](https://jotai.org)** [Kurs](https://egghead.io/lessons/react-share-state-between-react-components-with-jotai-useatom)
  - "Inspired by Recoil." - Interessant, also beide sehr neu!
  - Kommt [ohne den fragwürdigen `key` von Recoil aus](https://jotai.org/docs/basics/comparison).
  - Schöne [Immer-Integration](https://jotai.org/docs/integrations/immer)
  - [Vergleich mit Recoil](https://blog.logrocket.com/jotai-vs-recoil-what-are-the-differences/)
  - Interessanter Blog-Post vom Autor: [Valtio vs. Jotai](https://blog.axlight.com/posts/when-i-use-valtio-and-when-i-use-jotai/)
- State Management: [MobX State Tree](https://mobx-state-tree.js.org/intro/welcome)
  - Reduzierter Boilerplate aber die Typisierung wirkt irgendwie doppelt zu TypeScript
- State Management: [NanoStores](https://github.com/nanostores/nanostores)
  - Liest sich ein wenig wie *Jotai* von den Leuten hinter vielen PostCSS-Sachen (Andrey Sitnik, ...)

# React Animation

- [Framer Motion](https://github.com/framer/motion)
  - Brilliante Lösung für Komponenten-Animationen
- [React Spring](https://github.com/pmndrs/react-spring)
  - Gleiche Autoren wie *Jotai*

# Kurse

- [CSS for JS Devs](https://css-for-js.dev)
- [JavaScript Testing]()
- [Advanced React]()

# CSS / Styling

- React Styling: [Vanilla Extract](https://vanilla-extract.style)
  - Type-safe, static compilation, CSS Variables
  - CSS Modules Nachfolger quasi
- CSS Reset: [Modern CSS Reset](https://piccalil.li/blog/a-modern-css-reset/)
- CSS Reset: [CSS Reset by Josh](https://www.joshwcomeau.com/css/custom-css-reset/ )
- CSS Schatten: [Shadows](https://shadows.brumm.af/)
  - [Mehrere gestapelte Schatten statt einer ist natürlicher](https://www.joshwcomeau.com/css/designing-shadows/)
- CSS Gradient: [Non Boring Gradient](https://non-boring-gradients.netlify.app)
  - Sehr schön. Interpolation im LAB-Raum verbessert Übergänge massiv.
  - Basiert auf ColorJS
- CSS Gradient: [Gradient Generator](https://www.joshwcomeau.com/gradient-generator/)
  - Alternative zu dem oben Josh Comeau und [Blog-Post](https://www.joshwcomeau.com/css/make-beautiful-gradients/)

# JS Libraries

- Datum: [DayJS](https://github.com/iamkun/dayjs/)
  - Kompatibel mit MomentJS: parsen, validieren und formatieren.
- Datum: [Luxon](https://github.com/moment/luxon/)
  - Von den Autoren von MomentJS. Auf Basis von Intl. Immutable, Zeitzonen, I18N, etc.
- Datenverarbeitung: [Immer](https://immerjs.github.io/immer/)
  - Pragmatische Manipulation komplexer immutable Datenstrukturen
- Farben: [ChromaJS](https://vis4.net/chromajs/)
  - LAB Farben, Delta-E-Vergleich, ... umfangreich
- Farben: [ColorJS](https://colorjs.io)
  - Modernere Variante von *ChromeJS*
  - Von Lea Verou
- GUID: [NanoID](https://github.com/ai/nanoid)
  - Moderner, kleiner, schnelle GUID Generator
- Events: [NanoEvents](https://github.com/ai/nanoevents)
  - Super kleine Library für Custom Events

# Fonts

- Subsetting: [Glyphhanger](https://github.com/zachleat/glyphhanger)
  - Scannt HTML-Seiten und extrahiert benutzte Zeichen, kann dann Fonts entsprechend Subsetten

# Tools

- Shell Scripts: [ZX](https://github.com/google/zx)
  - Scripting mit Node v16 und netter Integration in Bash Child Prozesse
- NPM Dependencies: [DepCheck](https://github.com/depcheck/depcheck)
  - Erkennt Dependencies, die nicht (mehr) verwendet werden.

# Lösungen

- [Senden bei Verlassen](https://css-tricks.com/send-an-http-request-on-page-exit/)
  - Keep Alive vs. SendBeacon
