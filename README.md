# Fincas Productivas · Semana 1 · El bosque como modelo

Presentación de la clase en vivo del curso **Fincas Productivas** de La Huerta LAB.
42 diapositivas en HTML, pensadas para proyectarse en un directo.

Lienzo de 1920 × 1080 que se escala solo al tamaño de la pantalla. No necesita
PowerPoint ni conexión: las tipografías y las ilustraciones van dentro del repo.

## Verla

- **En local:** abre `index.html` con doble clic.
- **En línea:** activa GitHub Pages (Settings → Pages → Deploy from a branch →
  `main` / `root`). Queda en `https://<usuario>.github.io/<repositorio>/`.

## Atajos

| Tecla | Qué hace |
|---|---|
| `→` `←` `PgDn` `PgUp` `Espacio` | Avanzar y retroceder |
| `Inicio` `Fin` | Primera y última |
| `1`–`9` | Saltar a una diapositiva |
| `R` | Volver a la portada |
| Botón de la esquina | Pantalla completa |

Para un PDF de una diapositiva por página: `Ctrl/Cmd + P` → Guardar como PDF.

## Estructura

```
index.html              Las 42 diapositivas y las notas del orador
assets/deck.css         Sistema visual de La Huerta LAB
assets/deck.js          Motor <deck-stage>: navegación, escalado, impresión
assets/fonts/           Archivo y Fraunces
assets/img/             Las ilustraciones de los principios
```

## Editar una diapositiva

Cada diapositiva es un `<section data-label="...">` dentro de `<deck-stage>`.
Para cambiar un texto, se edita ahí y se recarga el navegador. No hay
compilación ni dependencias.

Piezas disponibles, todas definidas en `assets/deck.css`:

| Clase | Para qué |
|---|---|
| `.eyebrow` | Antetítulo en versalitas. `.coral` lo pasa a naranja |
| `h1` `h2` `h3` | Titulares. Lo que va en `<em>` sale en Fraunces cursiva lima |
| `.lead` · `.dato` | Bajada y párrafo de apoyo |
| `.cifra` | Un dato grande y solo en la diapositiva |
| `.ng` dentro de `.cifras tres` / `.dos` | Dos o tres datos en fila |
| `.tarjetas tres` / `.dos` / `.cuatro` | Rejilla de tarjetas |
| `.lista` · `.lista.num` | Lista con viñeta o numerada |
| `.lamina` | Hoja de papel crema para los esquemas dibujados |
| `.tabla` | Dos columnas con líneas |
| `.chips` · `.chip` | Etiquetas sueltas |
| `.fuente` | Cita de la fuente, abajo del todo |
| `.paso` | Marcador arriba a la derecha |

### Animaciones

Se declaran con un atributo y se repiten cada vez que se vuelve a la
diapositiva:

```html
<h2 data-anim="sube" style="--d:120ms">Titular</h2>
```

Valores: `sube`, `baja`, `izq`, `der`, `zoom`, `revela`, `dibuja-x`,
`dibuja-y`, `traza`. `--d` es el retardo.

### Notas del orador

Van en el bloque `<script type="application/json" id="speaker-notes">` al final
de `index.html`, una por diapositiva y en orden. El motor las carga y avisa del
cambio de diapositiva a la ventana que lo contenga, para un visor de notas
aparte.

## Reglas de composición

El sistema viene de proyectar en un directo de YouTube, donde manda la
legibilidad a tamaño pequeño:

- Cuerpo nunca por debajo de 34 px; titulares de 90 px para arriba.
- Poco texto por diapositiva: lo demás lo dice quien presenta.
- Contraste alto siempre: crema sobre verde bosque, o al revés.
- El lima se usa poco, y por eso se nota. El coral queda para el dato incómodo.

## Pendientes de contenido

- [ ] Fecha del video del recorrido por La Huerta (diapositiva 41)
- [ ] Confirmar la fecha del en vivo

---

La Huerta LAB · Yotoco, Valle del Cauca
