# DOCALSA ONE — laboratorio de pruebas (base V1.9)

Prototipo **independiente**, de tres páginas HTML, preparado para publicar en un **sitio Netlify nuevo**, separado de la V11 de producción. No requiere instalación ni compilación.

## Contenido

- `inicio.html`: entrada simulada, panel y departamentos.
- `index.html`: Ingeniería y Supervisores.
- `transportacion.html`: Transportación e inventario.
- `netlify.toml`: publica la raíz del repositorio y dirige `/` a `inicio.html`.

## Primera publicación (solo en un sitio nuevo)

1. Crea un repositorio **privado** nuevo en GitHub, por ejemplo `docalsa-one-laboratorio`.
2. Sube los archivos de esta carpeta a la **raíz** del repositorio. No subas credenciales ni datos reales.
3. En Netlify, elige **Add new project → Import an existing project → GitHub**.
4. Autoriza el repositorio **nuevo** (no selecciones el repositorio de V11).
5. Configura: rama `main`; **build command vacío**; **publish directory `.`**.
6. Publica como **sitio nuevo** y comprueba que la URL principal muestre la entrada DOCALSA ONE.
7. En adelante, los cambios confirmados en `main` se desplegarán automáticamente en ese sitio.

## Reglas importantes

- **No conectar este repositorio al sitio de producción V11.**
- No modificar la configuración ni variables del sitio de producción.
- El prototipo usa `localStorage` y no tiene autenticación ni autorización reales. **No introducir datos personales o empresariales sensibles.**
- Las simulaciones entre Ingeniería y Transportación funcionan en el **mismo navegador y origen web**; no sincronizan datos entre dispositivos.
- `X-Robots-Tag` desalienta la indexación, pero **no protege** el sitio. Para limitar el acceso, configura protección de sitio en Netlify según tu plan antes de distribuir la URL.
- Para actualizaciones automáticas desde ChatGPT, la conexión GitHub debe autorizarse; de lo contrario, hay que confirmar cambios en GitHub manualmente.

## Verificación sugerida

1. Abre la URL del sitio de pruebas y entra al panel.
2. Abre Ingeniería y verifica Supervisores, proyectos y colaboración.
3. Crea una solicitud de Transportación; abre Transportación y comprueba su estado.
4. Actualiza la página y verifica la persistencia local.
5. Realiza una modificación en el repositorio de pruebas y verifica un despliegue nuevo en Netlify.
