# Panel PREVIJOB

Plataforma visual de acceso a las herramientas de PREVIJOB. Pensada para que el equipo abra cada aplicación sin tener que buscar el enlace.

Web publicada: https://panel-previjob.onrender.com

## Cómo añadir una herramienta o una carpeta

1. Abre `index.html` y localiza el array `TOOLS` (al final del archivo, dentro de `<script>`).
2. Añade un objeto:

- Enlace: `{ id, name, href, icon, color }`
- Carpeta (para agrupar cursos u otras herramientas): `{ id, name, icon, color, items: [ ... ] }`. Las carpetas se abren en `#id`. Puedes anidar más carpetas dentro de `items`.
- Sin enlace todavía: el mismo objeto, sin `href` ni `items`. Se mostrará como «Próximamente».

Ejemplo de curso dentro de una carpeta:

```js
{
  id: "ruido",
  name: "Curso de ruido",
  href: "https://curso-ruido-prl.onrender.com",
  icon: "ruido",
  color: "linear-gradient(160deg,#0f7b6c,#14b8a6)"
}
```

3. El campo `icon` debe ser una clave de `ICONS`. Las que ya existen son `formacion` (birrete), `documento`, `bombilla`, `tecnicos` (caja de herramientas) y `ruido` (altavoz). Para un icono nuevo, añade su SVG en `ICONS` con la misma clave.
4. Guarda, haz commit y `git push` a `main`. Render actualiza la web solo.

No pongas contraseñas en este repositorio ni en la página.
