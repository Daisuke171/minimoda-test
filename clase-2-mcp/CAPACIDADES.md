# Capacidades y Límites de los MCP

**Playwright MCP**
- **Qué pudo hacer:** Interactuar de forma autónoma con la tienda MiniModa, simular clics, comprobar stock y (tras configurarlo) sacar capturas de pantalla de la web y el carrito.
- **Límites encontrados:** Chocó fuertemente contra el aislamiento (sandbox) del entorno. Requirió instalar dependencias del sistema operativo (`bubblewrap`) y el binario de Chromium manualmente por fuera del agente, ya que el entorno bloqueaba la ejecución nativa.

**MCP Propio (Generador de Casos)**
- **Qué pudo hacer:** Estructurar y guardar automáticamente casos de prueba en formato Markdown, validando los campos (título, prioridad, pasos) mediante Zod y escribiendo los archivos en disco.
- **Límites encontrados:** Al principio no pudo instalarse ni registrarse solo por restricciones de red y permisos de solo lectura en la carpeta `.codex`. Hubo que instalarlo desde la terminal anfitriona.

**Tiempo ahorrado**
La configuración inicial consumió bastante tiempo por las barreras del entorno aislado. Sin embargo, una vez configurados y con permisos, el ahorro es enorme: Playwright evita hacer el flujo de compras a mano para validar la UI, y el MCP propio elimina el trabajo repetitivo de maquetar documentos de prueba, estandarizando la redacción al instante.
