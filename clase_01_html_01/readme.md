# 🌐 Guía de Estudio: Fundamentos de HTML (Clase 1)

> **Resumen de clase:** Introducción a la anatomía web, semántica de títulos y párrafos, factores de posicionamiento en buscadores (SEO/UX), contenedores, imágenes y enlaces.

---

## 🔍 1. Semántica y Factores de Posicionamiento (SEO & UX)

Los motores de búsqueda priorizan las páginas según su estructura de código y la experiencia de usuario:

| Factor | ¿Qué evalúa el buscador? | Impacto en Desarrollo Web |
| :--- | :--- | :--- |
| **Jerarquía Semántica** | `<h1>` vs `<p>` | El buscador da máxima relevancia al título principal (`<h1>`) para entender el tema central. El texto en párrafos (`<p>`) aporta contexto secundario. |
| **Geolocalización (SEO Local)** | Ubicación del usuario | Filtra y prioriza resultados geográficamente cercanos (ej: búsquedas en México no muestran páginas de Argentina si la necesidad es física). |
| **Velocidad de Carga** | Tiempo de renderizado inicial | Un sitio que tarda más de 3 segundos es penalizado. Se debe optimizar el peso de imágenes y la limpieza del código. |
| **Tiempo de Permanencia** | *Dwell Time* vs *Bounce Rate* | Si el usuario entra y vuelve de inmediato a Google, indica contenido confuso. Si permanece leyendo, Google premia el sitio en el ranking. |

---

## 🏗️ 2. Anatomía de un Documento HTML

Un archivo web se divide en un contenedor global y dos áreas diferenciadas:

1. **`<html>...</html>`**: Elemento raíz que envuelve todo el documento. Se suele configurar con el idioma: `<html lang="es">`.
2. **`<head>...</head>`**: Sección técnica invisible para el usuario. Contiene los metadatos de la página (codificación UTF-8, título de la pestaña, descripción para Google y favicon).
3. **`<body>...</body>`**: Lienzo visible. Contiene toda la estructura visual: secciones, textos, imágenes, botones y formularios.

---

## 🏷️ 3. Elementos y Etiquetas Explicadas

* **`<h1>` a `<h3>`**: Jerarquía de encabezados ordenados de mayor a menor relevancia.
* **`<p>`**: Párrafos de texto regular explicativo.
* **`<section>`**: Etiqueta semántica que agrupa bloques temáticos dentro de la página.
* **`<div>`**: Contenedor genérico en bloque sin valor semántico, utilizado para maquetación y diseño.
  * **`class`**: Identificador reutilizable para varios elementos (ej: `.card`).
  * **`id`**: Identificador único e irrepetible por página (funciona como un DNI).
* **Unicode / Emojis**: Símbolos y caracteres textuales ligeros que no requieren cargar archivos de imagen externos.
* **`<img>`**: Etiqueta de autocierre para insertar imágenes.
  * `src`: Ruta o URL directa del archivo de imagen.
  * `alt`: Texto alternativo descriptivo obligatorio para accesibilidad y SEO.
  * `width`: Atributo numérico en píxeles para ajustar el ancho manteniendo la proporción original.
* **`<a>`**: Elemento de hipervínculo con su atributo `href`. Al envolver a un elemento `<button>`, transforma al botón completo en un enlace navegable.

---

## ⌨️ 4. Buenas Prácticas en el Editor (VS Code)

* **Numeración de líneas:** Facilita la comunicación en revisiones de código en equipo, delimitación precisa de bloques con errores y lectura de reportes en la consola de depuración.
* **Indentación / Tabulado:** Organiza visualmente las jerarquías de elementos padres e hijos, facilitando la detección de etiquetas abiertas.
* **Atajos de teclado:**
  * `Alt + Flecha Arriba / Abajo`: Mueve la línea seleccionada hacia arriba o abajo.
  * `Alt + Shift + Flecha Abajo / Arriba`: Duplica la línea actual tantas veces como sea necesario.

---

## 💻 5. Código Completo de Referencia Comentado

<pre><code>&lt;!DOCTYPE html&gt;
&lt;html lang="es"&gt;

&lt;!-- CABEZA: Metadatos para el navegador y buscadores --&gt;
&lt;head&gt;
  &lt;!-- Codificación estándar para reconocer acentos, eñes y caracteres especiales --&gt;
  &lt;meta charset="UTF-8"&gt;
  
  &lt;!-- Título de la pestaña y título principal para resultados de Google --&gt;
  &lt;title&gt;Adopción de Perritos | Refugio Patitas&lt;/title&gt;
  
  &lt;!-- Descripción resumida que muestra el buscador en sus resultados --&gt;
  &lt;meta name="description" content="Encontrá a tu compañero ideal. Adopción responsable de perritos."&gt;
  
  &lt;!-- Favicon: Ícono que acompaña al título en la pestaña del navegador --&gt;
  &lt;link rel="icon" href="https://cdn-icons-png.flaticon.com/512/616/616408.png"&gt;
&lt;/head&gt;

&lt;!-- CUERPO: Todo lo visible dentro de la ventana web --&gt;
&lt;body&gt;

  &lt;!-- SECCIÓN 1: Presentación inicial del sitio --&gt;
  &lt;section&gt;
    &lt;!-- h1: Título de máxima jerarquía semántica (tema central) --&gt;
    &lt;h1&gt;🐶 Adopción de Perritos&lt;/h1&gt;
    
    &lt;!-- h2: Subtítulo de menor jerarquía subordinado a h1 --&gt;
    &lt;h2&gt;Encontrá a tu compañero ideal&lt;/h2&gt;
    
    &lt;!-- p: Bloque de texto regular --&gt;
    &lt;p&gt;Conocé a los perritos rescatados que están buscando un hogar lleno de amor. Cada adopción salva una vida. ❤️&lt;/p&gt;
    
    &lt;!-- button: Botón interactivo clickeable --&gt;
    &lt;button&gt;Quiero Adoptar 🐾&lt;/button&gt;
  &lt;/section&gt;

  &lt;!-- SECCIÓN 2: Catálogo de perritos estructurado con tarjetas --&gt;
  &lt;section&gt;
    &lt;h2&gt;Nuestros Perritos en Adopción&lt;/h2&gt;
    &lt;h3&gt;Conocé a los rescatados que esperan una familia&lt;/h3&gt;
    &lt;p&gt;Elegí una tarjeta para ver la información de cada perrito y coordinar una visita.&lt;/p&gt;

    &lt;!-- div: Contenedor genérico agrupado por clase reusable ("card") --&gt;
    &lt;div class="card"&gt;
      &lt;div class="card-icon"&gt;🐕&lt;/div&gt;
      &lt;h3&gt;Milo (Cachorro)&lt;/h3&gt;
      &lt;p&gt;Macho de 3 meses, tamaño mediano, juguetón y con vacunas al día.&lt;/p&gt;
      &lt;button&gt;Conocer a Milo&lt;/button&gt;
    &lt;/div&gt;

    &lt;div class="card"&gt;
      &lt;div class="card-icon"&gt;🦮&lt;/div&gt;
      &lt;h3&gt;Luna (Adulto)&lt;/h3&gt;
      &lt;p&gt;Hembra de 2 años, muy tranquila, sociable con niños y otros animales.&lt;/p&gt;
      &lt;button&gt;Conocer a Luna&lt;/button&gt;
    &lt;/div&gt;

    &lt;div class="card"&gt;
      &lt;div class="card-icon"&gt;🐩&lt;/div&gt;
      &lt;h3&gt;Tobi (Senior)&lt;/h3&gt;
      &lt;p&gt;Macho de 7 años, educado, busca un hogar calmo donde descansar.&lt;/p&gt;
      &lt;button&gt;Conocer a Tobi&lt;/button&gt;
    &lt;/div&gt;

    &lt;!-- Tarjeta con imagen real y botón anidado en enlace --&gt;
    &lt;div class="card"&gt;
      &lt;!-- img: src define la ruta directa, alt describe la foto, width define ancho en px --&gt;
      &lt;img src="https://images.unsplash.com/photo-1543466835-00a7907e9de1?w=400" 
           alt="Cachorro mestizo jugando con una pelota" 
           width="250"&gt;
      &lt;h3&gt;Rocky (Cachorro rescatado)&lt;/h3&gt;
      &lt;p&gt;Cachorro de 4 meses, muy juguetón y lleno de energía. Busca una familia con patio.&lt;/p&gt;
      
      &lt;!-- Enlace &lt;a&gt; que envuelve al &lt;button&gt; para convertirlo en enlace de navegación --&gt;
      &lt;a href="https://ejemplo.com/formulario-adopcion"&gt;
        &lt;button&gt;Conocer a Rocky&lt;/button&gt;
      &lt;/a&gt;
    &lt;/div&gt;
  &lt;/section&gt;

&lt;/body&gt;
&lt;/html&gt;</code></pre>