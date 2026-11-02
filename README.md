# Web de la política de privacidad de Fudemaru

Web estática (HTML y CSS, sin JavaScript, sin cookies, sin recursos de otros dominios) con la política de privacidad de Fudemaru.

**Publicada en:** https://john141423.github.io/fudemaru-privacy/ (inglés: https://john141423.github.io/fudemaru-privacy/en/), desde el repositorio público https://github.com/john141423/fudemaru-privacy (GitHub Pages, rama `main`, carpeta raíz).

## Qué hay aquí

| Archivo | Para qué |
|---|---|
| `index.html` | Política en español (la página principal). |
| `en/index.html` | Política en inglés. |
| `assets/style.css` | Diseño (crema, índigo y violeta; claro y oscuro; móvil, tableta y ordenador). |
| `assets/fonts/` | Fuentes Zen Kaku Gothic New y Klee One recortadas a los caracteres usados, con su licencia (SIL OFL 1.1). |
| `assets/icon-192.png`, `icon-180.png`, `favicon-32.png` | Icono de Fudemaru. |
| `.nojekyll` | Le dice a GitHub Pages que sirva los archivos tal cual. |

Para verla en tu ordenador no hace falta instalar nada: haz doble clic en `index.html`.

## Cómo se actualiza

No edites `index.html` a mano. El texto está en:

- `privacy/POLITICA_PRIVACIDAD.md` (español)
- `privacy/PRIVACY_POLICY_EN.md` (inglés)

Después de cambiarlos, desde la carpeta del proyecto:

```
npm run privacidad
```

Eso vuelve a generar `index.html`, `en/index.html`, las fuentes y los iconos. Cambia también la fecha de «Última actualización» en los dos `.md`.

Los datos que faltan aparecen en la web resaltados en amarillo como **[PENDIENTE DE COMPLETAR…]**. No publiques la web hasta haberlos rellenado.

## Volver a publicarla después de un cambio

Desde la carpeta del proyecto:

1. `npm run privacidad` (regenera la web a partir de los `.md`).
2. Guarda los cambios en git (commit).
3. `npm run privacidad:publicar`: sube `privacy-website/` al repositorio `fudemaru-privacy` con un commit firmado como «Fudemaru <fudemaru.app@gmail.com>» (para no publicar tu correo personal). La primera vez en un ordenador nuevo, Git te pedirá iniciar sesión en GitHub en el navegador.
4. Espera uno o dos minutos y comprueba https://john141423.github.io/fudemaru-privacy/

La dirección no cambia, así que no hay que tocar la app ni Play Console.

## Publicarla desde cero en otra cuenta (solo con el navegador)

1. Entra en <https://github.com> e inicia sesión (o crea una cuenta gratuita).
2. Arriba a la derecha, **+ → New repository**.
   - Repository name: `fudemaru-privacy`
   - Marca **Public** (GitHub Pages gratis necesita un repositorio público).
   - Pulsa **Create repository**.
3. En el repositorio nuevo, pulsa **uploading an existing file**.
4. Arrastra **el contenido** de la carpeta `privacy-website` (no la carpeta en sí): `index.html`, la carpeta `en`, la carpeta `assets` y `.nojekyll`. No hace falta subir este `README.md`.
5. Abajo, pulsa **Commit changes**.
6. Ve a **Settings → Pages**.
   - Source: **Deploy from a branch**.
   - Branch: **main** y carpeta **/ (root)**. Pulsa **Save**.
7. Espera uno o dos minutos y recarga la página de Settings → Pages: aparecerá la dirección

   `https://TU-USUARIO.github.io/fudemaru-privacy/`

   (con tu nombre de usuario de GitHub en minúsculas). La versión en inglés queda en `https://TU-USUARIO.github.io/fudemaru-privacy/en/`.
8. Abre esa dirección en el móvil y en el ordenador y comprueba que se ve bien.

### Cuando la dirección funcione

1. Ponla en `package.json` del proyecto, en `"fudemaru": { "privacyUrl": "https://TU-USUARIO.github.io/fudemaru-privacy/" }`.
2. Ejecuta `npm run android:sync` y `npm run check`: la app mostrará «Política de privacidad» en Opciones y el aviso de `check` desaparecerá.
3. Pega la misma dirección en Play Console → **Contenido de la app → Política de privacidad**.

### Para actualizarla sin la línea de comandos

Ejecuta `npm run privacidad`, vuelve al repositorio `fudemaru-privacy` en GitHub, pulsa **Add file → Upload files**, arrastra otra vez los archivos que hayan cambiado (normalmente `index.html` y `en/index.html`) y pulsa **Commit changes**. En uno o dos minutos la web estará actualizada.

## Privacidad de la propia web

La web no usa cookies, ni analítica, ni fuentes o scripts de otros dominios. GitHub, como alojamiento, puede registrar datos técnicos de las visitas (por ejemplo, la dirección IP) por seguridad; la web lo dice en el pie.
