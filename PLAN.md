# Plan Detallado para Usar Elementos Comunes de HTML

## Introducción

Este plan describe el uso de elementos comunes de HTML para estructurar páginas web. Se enfoca exclusivamente en el marcado HTML, sin ningún estilo CSS. El objetivo es proporcionar una guía completa de etiquetas y elementos HTML esenciales, incluyendo tablas, estructuras de navegación, formularios y muchos otros elementos semánticos y estructurales. Este plan ayudará a construir contenido web accesible y bien estructurado.

## Estructura Básica del Documento HTML

Cada documento HTML debe comenzar con la siguiente estructura básica:

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Título del Documento</title>
  </head>
  <body>
    <!-- El contenido va aquí -->
  </body>
</html>
```

- `<!DOCTYPE html>`: Declara el tipo de documento como HTML5.
- `<html>`: Elemento raíz con atributo `lang` para especificar el idioma.
- `<head>`: Contiene metadatos como charset, viewport y título.
- `<meta charset="UTF-8">`: Establece la codificación de caracteres.
- `<meta name="viewport">`: Asegura el diseño responsivo en dispositivos móviles.
- `<title>`: Establece el título de la página mostrado en la pestaña del navegador.
- `<body>`: Contiene el contenido visible de la página.

## Elementos de Texto y Formateo

Usa estos elementos para estructurar y formatear el contenido de texto:

### Encabezados

- `<h1>` a `<h6>`: Definen encabezados con importancia decreciente.
  ```html
  <h1>Encabezado Principal</h1>
  <h2>Subencabezado</h2>
  <h3>Sub-subencabezado</h3>
  ```

### Párrafos y Formateo de Texto

- `<p>`: Define párrafos.
- `<strong>` o `<b>`: Texto en negrita (usa `<strong>` para énfasis semántico).
- `<em>` o `<i>`: Texto en cursiva (usa `<em>` para énfasis semántico).
- `<br>`: Salto de línea.
- `<hr>`: Regla horizontal para rupturas temáticas.

Ejemplo:

```html
<p>
  Este es un párrafo <strong>en negrita</strong> con texto <em>en cursiva</em>.
</p>
<hr />
<p>Siguiente párrafo.</p>
```

### Listas

- `<ul>`: Lista no ordenada (viñetas).
- `<ol>`: Lista ordenada (números).
- `<li>`: Elemento de lista.

Ejemplo:

```html
<ul>
  <li>Primer elemento</li>
  <li>Segundo elemento</li>
</ul>
<ol>
  <li>Primer elemento numerado</li>
  <li>Segundo elemento numerado</li>
</ol>
```

## Enlaces y Navegación

### Hipervínculos

- `<a>`: Crea enlaces a otras páginas o secciones.
  - `href`: URL o ancla.
  - `target`: Abre en nueva pestaña (ej. `_blank`).

Ejemplo:

```html
<a href="https://ejemplo.com">Visitar Ejemplo</a>
<a href="#seccion1">Saltar a Sección 1</a>
```

### Estructura de Navegación

- `<nav>`: Define enlaces de navegación.
  - A menudo contiene `<ul>` y `<li>` para elementos de menú.

Ejemplo:

```html
<nav>
  <ul>
    <li><a href="#inicio">Inicio</a></li>
    <li><a href="#acerca">Acerca de</a></li>
    <li><a href="#contacto">Contacto</a></li>
  </ul>
</nav>
```

## Tablas

Las tablas se usan para mostrar datos tabulares. Elementos clave:

- `<table>`: Contenedor de tabla.
- `<thead>`: Sección de encabezado de tabla.
- `<tbody>`: Sección de cuerpo de tabla.
- `<tr>`: Fila de tabla.
- `<th>`: Celda de encabezado de tabla (negrita por defecto).
- `<td>`: Celda de datos de tabla.
- `<caption>`: Título de tabla para accesibilidad.

Ejemplo:

```html
<table>
  <caption>
    Tabla de Ejemplo
  </caption>
  <thead>
    <tr>
      <th>Nombre</th>
      <th>Edad</th>
      <th>Ciudad</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Juan</td>
      <td>25</td>
      <td>Nueva York</td>
    </tr>
    <tr>
      <td>Ana</td>
      <td>30</td>
      <td>Londres</td>
    </tr>
  </tbody>
</table>
```

Elementos adicionales de tabla:

- `<tfoot>`: Sección de pie de tabla.
- `<col>` y `<colgroup>`: Para estilo de columnas (útil para estructura).

## Formularios

Los formularios recopilan entrada del usuario. Incluyen varios tipos de entrada:

- `<form>`: Contenedor de formulario con atributos `action` y `method`.
- `<input>`: Varios tipos de entrada (texto, email, contraseña, radio, checkbox, fecha, número, etc.).
- `<textarea>`: Entrada de texto multilínea.
- `<select>` y `<option>`: Menús desplegables.
- `<button>`: Botones de envío o acción.
- `<fieldset>` y `<legend>`: Agrupan elementos de formulario.
- `<label>`: Etiquetas para entradas.

Ejemplo:

```html
<form action="/enviar" method="post">
  <fieldset>
    <legend>Información Personal</legend>
    <label for="nombre">Nombre:</label>
    <input type="text" id="nombre" name="nombre" required />
    <br />
    <label for="email">Email:</label>
    <input type="email" id="email" name="email" required />
    <br />
    <label for="fecha">Fecha de nacimiento:</label>
    <input type="date" id="fecha" name="fecha" />
    <br />
    <label for="edad">Edad:</label>
    <input type="number" id="edad" name="edad" min="1" max="120" />
    <br />
    <label
      ><input type="radio" name="genero" value="masculino" /> Masculino</label
    >
    <label
      ><input type="radio" name="genero" value="femenino" /> Femenino</label
    >
    <br />
    <label
      ><input type="checkbox" name="boletin" /> Suscribirse al boletín</label
    >
    <br />
    <textarea id="mensaje" name="mensaje" rows="4" cols="50"></textarea>
    <br />
    <select id="pais" name="pais">
      <option value="us">Estados Unidos</option>
      <option value="uk">Reino Unido</option>
    </select>
    <br />
    <button type="submit">Enviar</button>
  </fieldset>
</form>
```

## Imágenes y Multimedia

- `<img>`: Incrusta imágenes.

  - `src`: Fuente de imagen.
  - `alt`: Texto alternativo para accesibilidad.
  - `width` y `height`: Dimensiones.

- `<audio>`: Incrusta audio.
- `<video>`: Incrusta video.
- `<iframe>`: Incrusta contenido externo.

Ejemplos:

```html
<img src="imagen.jpg" alt="Descripción de imagen" width="300" height="200" />

<audio controls src="audio.mp3"></audio>

<video controls width="320" height="240">
  <source src="video.mp4" type="video/mp4" />
</video>

<iframe src="https://ejemplo.com" width="300" height="200"></iframe>
```

## Elementos Estructurales y Semánticos

Estos proporcionan significado al contenido:

- `<header>`: Contenido introductorio o navegación.
- `<footer>`: Información de pie de página.
- `<section>`: Agrupación temática de contenido.
- `<article>`: Contenido autocontenido.
- `<aside>`: Barra lateral o contenido relacionado.
- `<main>`: Contenido principal.
- `<div>`: Contenedor genérico (usa elementos semánticos cuando sea posible).
- `<span>`: Contenedor en línea.
- `<figure>` y `<figcaption>`: Figuras con leyendas.
- `<time>`: Fechas y horas.
- `<mark>`: Texto resaltado.
- `<details>` y `<summary>`: Contenido colapsable.

Ejemplo:

```html
<header>
  <h1>Título del Sitio Web</h1>
  <nav>
    <!-- Navegación aquí -->
  </nav>
</header>
<main>
  <section>
    <h2>Contenido Principal</h2>
    <article>
      <p>Contenido del artículo.</p>
      <figure>
        <img src="imagen.jpg" alt="Imagen" />
        <figcaption>Leyenda de la imagen</figcaption>
      </figure>
      <p>
        Publicado el <time datetime="2023-10-01">1 de octubre de 2023</time>
      </p>
      <p>Este es texto <mark>resaltado</mark>.</p>
      <details>
        <summary>Más detalles</summary>
        <p>Información adicional aquí.</p>
      </details>
    </article>
  </section>
  <aside>
    <p>Información relacionada.</p>
  </aside>
</main>
<footer>
  <p>Información de derechos de autor.</p>
</footer>
```

## Otras Etiquetas Comunes

- `<blockquote>`: Texto citado.
- `<cite>`: Cita.
- `<code>`: Código en línea.
- `<pre>`: Texto preformateado.
- `<abbr>`: Abreviaturas con atributo title.
- `<address>`: Información de contacto.

Ejemplo:

```html
<blockquote>
    <p>Esta es una cita.</p>
    <cite>Nombre del Autor</cite>
</blockquote>
<p>Usa <code><code></code> para código en línea.</p>
<pre>
Texto preformateado
    con espacios preservados.
</pre>
<abbr title="HyperText Markup Language">HTML</abbr>
<address>
    123 Calle Principal<br>
    Ciudad, Estado 12345
</address>
```

## Mejores Prácticas

1. **HTML Semántico**: Usa elementos semánticos apropiados para mejor accesibilidad y SEO.
2. **Anidación Correcta**: Asegura que los elementos estén correctamente anidados.
3. **Accesibilidad**: Incluye atributos `alt` para imágenes, `label` para entradas de formulario y usa encabezados jerárquicamente.
4. **Validación**: Usa validadores HTML para verificar errores.
5. **Mejora Progresiva**: Construye con HTML primero, luego mejora con otras tecnologías si es necesario.
6. **Evita Etiquetas Obsoletas**: No uses etiquetas como `<font>`, `<center>`, etc.

## Pasos de Implementación

1. Planifica la estructura de la página usando elementos semánticos.
2. Agrega contenido con encabezados y párrafos apropiados.
3. Implementa navegación con `<nav>` y enlaces.
4. Crea tablas para datos tabulares.
5. Agrega formularios para interacción del usuario.
6. Incluye imágenes, audio y video con texto alternativo apropiado.
7. Valida el HTML usando herramientas en línea.
8. Prueba en múltiples navegadores para consistencia.

Este plan proporciona una base para crear documentos HTML estructurados y accesibles usando muchos elementos comunes.
