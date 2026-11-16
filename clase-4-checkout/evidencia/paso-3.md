sin editar, listá fuentes cargadas y qué aplica solo a tests/ vs src/

Voy a revisar las instrucciones del repo y el árbol de archivos, sin modificar nada. Después separo las fuentes cargadas y las que aplican solo a tests/ o src/.
• Ran pwd && rg --files -g 'AGENTS.md' -g '!node_modules' -g '!dist' -g '!build' -g '!*lock*' -g 'pac…
  └ tests/AGENTS.md
    tests/example.spec.ts
    tests/pago.spec.ts
• Explored
  └ Read AGENTS.md
    Read AGENTS.md
    Read package.json
No edité nada. Estas son las fuentes de instrucciones que encontré:

- Instrucciones que me diste: responder en español y marcar A VERIFICAR lo que no se pueda comprobar.
- AGENTS.md del repo: trabajar solo en este repo y con la demo; no usar producción ni datos reales de pago; pedir confirmación antes de agregar dependencias; no borrar ni saltear tests; informar qué se ejecutó y qué quedó sin verificar.
- tests/AGENTS.md: aplica a tests/. Pide usar locators basados en la UI, evitar esperas fijas, incluir el ID del caso y aserciones del resultado esperado; no inventar textos o locators ni ocultar fallos con skip o fixme. Indica como demo permitida https://minimoda-navy.vercel.app/checkout.

Alcance por carpeta:

- tests/: aplica tanto el AGENTS.md raíz como tests/AGENTS.md.
- src/: no encontré esa carpeta en el árbol visible del repo. Si existiera o se creara, aplicaría el AGENTS.md raíz; las reglas específicas de tests/ no se extenderían a src/.
- Configuración de tests: playwright.config.ts apunta Playwright a ./tests; define Chromium, Firefox y WebKit. Eso es configuración, no una fuente de instrucciones para src/.

A VERIFICAR: no comprobé instrucciones fuera de este repo. No ejecuté tests.
