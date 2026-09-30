# Fincas Productivas · La Huerta LAB

Presentaciones del curso **Fincas Productivas**, en HTML. Dos modalidades que
comparten el mismo sistema visual y el mismo motor.

- **`/`** — Online, Semana 1: El bosque como modelo. 43 diapositivas.
- **`/presencial/`** — Presencial, Día 1: El bosque como modelo. 43 diapositivas.

Lienzo de 1920 × 1080 que se escala solo. No necesita PowerPoint ni conexión:
tipografías, ilustraciones y fotos van dentro del repositorio.

## Verlas

- **En local:** abre `index.html` con doble clic.
- **En línea:** Settings → Pages → Deploy from a branch → `main` / `root`.
  El presencial queda en `.../presencial/`.

Cada diapositiva tiene su propia dirección: `.../#29` abre la 29, pero solo al
cargar la página; si ya está abierta hay que recargar.

## Atajos

| Tecla | Qué hace |
|---|---|
| `→` `←` `PgDn` `PgUp` `Espacio` | Avanzar y retroceder |
| `Inicio` `Fin` | Primera y última |
| `1`–`9` | Saltar a una diapositiva |
| `R` | Volver a la portada |
| Botón de la esquina | Pantalla completa |

`Ctrl/Cmd + P` produce un PDF de una diapositiva por página.

## Estructura

```
index.html              Online · Semana 1
presencial/index.html   Presencial · Día 1
assets/deck.css         Sistema visual, compartido por las dos
assets/deck.js          Motor <deck-stage>, compartido
assets/fonts/           Archivo y Fraunces
assets/img/             Ilustraciones, fotos e imágenes generadas
```

Las dos modalidades apuntan al mismo `assets`. Un cambio de color o de
tipografía se aplica a ambas sin duplicar nada.

## Qué cambia entre una y otra

Solo ocho diapositivas: portada, agenda del día, cómo funciona el curso, la
ronda de presentación, el cierre del principio 1, el calendario, las prácticas
y lo que sigue. El resto del contenido es idéntico.

## Sobre las imágenes

- **`foto-*`** — Fotos reales de La Huerta.
- **`ia-*`** — Generadas con IA. Ilustran el diagnóstico de la parte 1 y 2, de
  la 6 a la 17. No documentan lugares reales y no deben presentarse como si lo
  hicieran: acompañan al dato, no lo prueban. Las fuentes de cada cifra están
  citadas abajo en su diapositiva.
- Los esquemas de los principios van sobre `.lamina`, una hoja de papel crema
  puesta encima del fondo verde.

## Editar una diapositiva

Cada diapositiva es un `<section data-label="...">` dentro de `<deck-stage>`.
Se edita el texto y se recarga. No hay compilación ni dependencias.

| Clase | Para qué |
|---|---|
| `.eyebrow` | Antetítulo en versalitas. `.coral` lo pasa a naranja |
| `h1` `h2` `h3` | Titulares. Lo que va en `<em>` sale en Fraunces cursiva lima |
| `.lead` · `.dato` | Bajada y párrafo de apoyo |
| `.cifra` | Un dato grande y solo en la diapositiva |
| `.ng` dentro de `.cifras tres` / `.dos` | Dos o tres datos en fila |
| `.tarjetas tres` / `.dos` / `.cuatro` | Rejilla de tarjetas |
| `.lista` · `.lista.num` | Lista con viñeta o numerada |
| `.lamina` | Hoja de papel crema para los esquemas |
| `.tabla` | Dos columnas con líneas |
| `.chips` · `.chip` | Etiquetas sueltas |
| `.fuente` | Cita de la fuente, abajo del todo |
| `.paso` | Marcador arriba a la derecha |

### Fotos de fondo

Van como fondo del `.d`, antes del `.pad`, y son 16:9 exactos:

```html
<div class="foto" style="background-image:url(assets/img/foto-22-el-metodo.webp)"></div>
<div class="velo izq"></div>
```

- **`velo izq`** oscurece el lado del texto y deja ver la imagen por la derecha.
  Se usa donde el contenido se queda en la mitad izquierda. Exige el sujeto a la
  derecha; si cae a la izquierda, se le añade `espejo` al `.foto`.
- **`velo full`** deja la imagen de textura al 18 %. Se usa donde el contenido
  ocupa todo el ancho: tarjetas, cifras en tres columnas, láminas.

### Animaciones

```html
<h2 data-anim="sube" style="--d:120ms">Titular</h2>
```

Valores: `sube`, `baja`, `izq`, `der`, `zoom`, `revela`, `dibuja-x`,
`dibuja-y`, `traza`. `--d` es el retardo.

### Notas del orador

En el bloque `<script type="application/json" id="speaker-notes">` al final de
cada `index.html`, una por diapositiva y en orden.

## Reglas de composición

- Cuerpo nunca por debajo de 34 px; titulares de 90 px para arriba.
- Poco texto por diapositiva: lo demás lo dice quien presenta.
- Contraste alto siempre.
- El lima se usa poco, y por eso se nota. El coral queda para el dato incómodo.

## Pendientes

- [ ] Presencial: reescribir las ocho notas del orador marcadas
      «[Por reescribir para el presencial]»
- [ ] La diapositiva 5, la que abre la parte 1, sigue sin imagen
- [ ] Fecha del video del recorrido por La Huerta (diapositiva 42 del online)

---

La Huerta LAB · Yotoco, Valle del Cauca
