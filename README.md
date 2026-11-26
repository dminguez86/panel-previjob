# Panel PREVIJOB

Plataforma visual de acceso a las herramientas de PREVIJOB. Pensada para que el equipo abra cada aplicación sin tener que buscar el enlace.

Web publicada: https://panel-previjob.onrender.com

## Cómo añadir una herramienta

1. Abre `index.html` y localiza el array `TOOLS` (al final del archivo, dentro de `<script>`).
2. Añade un objeto nuevo, por ejemplo:

```js
{
  id: "registro-epi",
  name: "Registro de EPI",
  href: "https://ejemplo.onrender.com",
  icon: "documento",
  color: "#0277ab"
}
```

3. El campo `icon` debe ser una clave de `ICONS`. Las que ya existen son `formacion` (birrete), `documento` y `bombilla`. Para un icono nuevo, añade su SVG en `ICONS` con la misma clave.
4. Guarda, haz commit y `git push` a `main`. Render actualiza la web solo.

No pongas contraseñas en este repositorio ni en la página.
