## Module 1 - Getting Started  

### <ins>Crea tu primera página HTML</ins>

- Crea una carpeta `app` en tu ordenador  
- Crea una página llamada `index.html` dentro de la carpeta `app` en tu ordenador Abre esa página en tu editor de texto favorito
	- Yo personalmente uso VSCode

### <ins>Escriba el siguiente código `boilerplate` en el archivo `index.html`</ins>

- Este es su código HTML boilerplate  
- Le está diciendo al navegador que index.html es un archivo HTML y que lo renderice como un sitio web HTML. 
- La etiqueta `head` es donde se declaran los metadatos, el título y se enlazan los archivos de estilo.  
- La etiqueta `body` es donde se empieza a escribir el código de la página web.
	- La parte visible del documento HTML se encuentra entre `<body>` y `</body>`. 
- La etiqueta `title` se utiliza para dar título a la página.
- La etiqueta `h1` se utiliza para mostrar un título en la página.

```html
<!DOCTYPE html>
<html>

  <head>
    <title>My First HTML Page</title>

  </head>
  <body>

    <h1>My First Web Page</h1>
  </body>

</html>
```


### <ins>Ejecute su primer archivo HTML</ins>

- Para ejecutar su aplicación localmente   
    - Guarde los cambios en la página `index.html`.  
    - A continuación, abra implícitamente su archivo `index.html` en el navegador

### <ins>Ejecutar la aplicación en Internet GRATIS</ins>

- Si quieres ejecutar tu aplicación en Internet y compartir la URL con tu socio sigue estos pasos  
- Ve a [Netlify Drop](https://app.netlify.com/drop)
- Suelta la carpeta que contiene tu HTML y CSS le (si tienes una) en esa página donde dice `Arrastra y suelta la carpeta de tu sitio aquí`.
- Y ¡voilá! Se creará una URL única que podrás compartir con tu socio.

> Puedes ver el ejemplo [aquí](https://happy-ramanujan-9ca090.netlify.app)

**¡Si no escribo `<! DOCTYPE html>` ¿funcionará HTML5?**

- No, el navegador no podrá identificar que se trata de un documento HTML y las etiquetas HTML 5 no funcionarán correctamente.  
- Los navegadores modernos son lo suficientemente inteligentes como para renderizar el contenido HTML, pero puede que no esté optimizado correctamente.

**DOM**
![dom](src/dom.png)
- El documento HTML se representa como un árbol 
- Cada nodo del árbol es un objeto  
- El objeto `document` representa el árbol DOM
- El nodo `<html>` está en la raíz
- `<head>` y `<body>` son sus hijos
- Los nodos hoja contienen el texto del documento  
- "My Application", "This is title", y "This is link" son los nodos hoja.  
- La api DOM está disponible para capturar eventos de usuario y dar acceso a sus hijos

> NOTA: Si ponemos algo después de la etiqueta final `</body>`, entonces eso se mueve automáticamente dentro del cuerpo, al final, ya que la especificación HTML requiere que todo el contenido debe estar dentro de `<body>`.

> NOTA: Los navegadores modernos son inteligentes. Si el navegador encuentra HTML malformado, lo corrige automáticamente al hacer el DOM. Por ejemplo: el navegador insertará automáticamente la etiqueta `<html>` en la parte superior si no se proporciona.

### <ins>When should you use section, div or article?</ins>

**section**
+ Agrupar contenidos con un único tema relacionado 
+ Como una subsección de un artículo largo 
+ Normalmente tiene encabezamiento y pie de página
```html
<section>
	<h2>Subtitle</h2>
	<p>My long paragraph</p>
</section>
```
**article**
- Representa el contenido completo y autónomo de una página. 
- Puede ser una entrada de foro, un artículo de periódico, una entrada de blog 
- Su contenido independiente  
- Tiene sentido por sí mismo
```html
<article>
	<h2>Subtitle</h2>
	<p>My long paragraph</p>
</article>
```

**div**
- No transmite ningún significado  
- Suele denominarse elemento de último recurso 
- Se utiliza cuando ningún otro elemento es adecuado
```html 
<div>
  <h2>Subtitle</h2>
  <p>My long paragraph</p>
</div>
```
**Headings**
- Las etiquetas Heading forman parte del HTML semántico  
- Se utilizan para dene encabezados  
- Van de `h1` a `h6`  
- El tamaño por defecto es el mayor para `h1` y el menor para `h6`
```html
<h1>My Heading 1</h1>
<h2>My Heading 2</h2>
<h3>My Heading 3</h3>
<h4>My Heading 4</h4>
<h5>My Heading 5</h5>
<h6>My Heading 6</h6>
```

- Los encabezados se utilizan con fines de SEO  
    - Optimización para motores de búsqueda  
    - Útiles para indexar páginas y la estructura de la página  
- Puede dar formato a los estilos de fuente según sus necesidades para estas etiquetas

```html 
<h1 style="font-size:72px;">My Heading</h1>
```

**Paragraph**
- El elemento `p` se utiliza para escribir un párrafo de texto en HTML.  
- Puede incluir p dentro de otros elementos como div, section, article

> CONSEJO: no añada espacios en blanco adicionales - el navegador eliminará los espacios y líneas sobrantes cuando se muestre la página. Utiliza otras propiedades HTML y CSS para añadir espacios en blanco según tus necesidades.

```html
<div>
  <p style="font-size:12px;">This is a paragraph.</p>
</div>
```

**Links / Anchor elements**
- Los enlaces permiten a los usuarios navegar  
    - De una página a otra 
    - O incluso de una sección de la página a otra sección de la misma página 
- Los enlaces en HTML se denominan Hiperenlaces  
- El siguiente enlace le llevará a `https://www.google.com`.
- El atributo `href` especifica la dirección de destino

```html
<a href="https://www.google.com">Google</a>
```

**Images**
- HTML le permite añadir imágenes en su sitio web  
- El atributo `src` es donde se especifica la ubicación de la imagen. 
    - Puede ser una imagen de Internet  
    - O de su máquina local

```html
<img src="https://via.placeholder.com/150">
```

- La etiqueta `img` también contiene otro atributo llamado `alt`.  
- Los atributos `alt` permiten mostrar un texto alternativo en caso de que la imagen no esté disponible para su visualización.  
    - Por ejemplo, si no hay conexión a Internet o el usuario utiliza un lector de pantalla.

**Image Sizes**
- Puedes ajustar el tamaño de tu imagen utilizando las propiedades `width` y `height` o la propiedad style

```html 
<img src="https://via.placeholder.com/150" alt="placeholder" width="150"
height="150">
<img src="https://via.placeholder.com/150" alt="placeholder"
style="width:150px; height:150px;">
```

**Image as Links**
- Puede hacer que las imágenes sean clicables utilizando etiquetas `anchor` a su alrededor.  
- Esto se puede utilizar para navegar a otro lugar haciendo clic en la imagen

```html
<a href="https://www.google.com">
	<img src="https://via.placeholder.com/150" alt="placeholder" width="150" height="150">
</a>
```

## Module 2 - Styling your Module 2 - Styling your

### <ins>Crear un archivo CSS</ins>

- Cree un archivo `style.css` dentro de la carpeta `app` que creó anteriormente al crear su primera página HTML.  
- Sus estilos irán en este archivo `style.css`.

### <ins>A continuación, añada su estilo en el archivo `index.html`.</ins>

- Debe utilizar la etiqueta de enlace para incluir su archivo de estilo dentro de su archivo HTML

```html
<head>
  <meta charset="utf-8" />
  <title>Valentine Gift</title>

  <link rel="stylesheet" type="text/css" href="style.css" />
</head>
```

### <ins>Ahora vamos a crear el cuerpo de tu tarjeta de San Valentín</ins>
- Reemplace la etiqueta `body` en su `index.html` le para que coincida con el siguiente código  
- Usted está agregando `card` DIV que será el contenedor de su tarjeta de felicitación. Añadiremos los estilos más tarde.  
- Dentro del DIV `card` añade dos etiquetas H1
		- Estos son tus encabezados  
		- H1 son los encabezados más grandes disponibles  
		- También puedes cambiar el tamaño de letra según tus necesidades.
- También asignamos las `clases` apropiadas a nuestro HTML para que podamos darles estilo más tarde.  
      - Aprenderás sobre las clases más adelante

```html
<body>
  <div class="card">

    <h1 class="quote">You're the CSS to my HTML</h1>

    <h1 class="message">Happy Valentine's Day</h1>
  </div>

</body>
```

### <ins>Ahora vamos a añadir tu primer estilo</ins>
- Vamos a añadir estilos para su tarjeta de San Valentín  
- Estamos utilizando .card - class selector para agarrar la tarjeta DIV y darle estilo  
- Aquí sólo estamos estableciendo un bonito rojo `border: 10px sólido #E53038;`   
- `height: 100vh;` se hace para que coincida con la altura de la etiqueta del cuerpo - que es la altura de la vista completa del puerto. 
- `display: flex;` hace que esta `card` DIV sea un flex-box.  
    - Sólo estamos haciendo que todos nuestros `flex-children` se alineen en posición vertical y horizontalmente centrados en una columna.  
    - NOTA: Aprenderemos sobre ex-box en la sección posterior.

```css
.card {
  border: 10px solid #E53038;
  height: 300px;
  width: 300px;
  padding: 20px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
```

**Selectors**
- En términos simples, los selectores se utilizan para tomar un elemento del DOM y aplicarle estilos. 
- Hay diferentes tipos de selectores que aprenderás a continuación
- Las imágenes muestran el selector de etiquetas  
- Estamos agarrando todas las etiquetas `<p>` en nuestro documento HTML y aplicándoles el color `rojo` y un margen de `3px`.  
- `color` es la propiedad. `red` es el valor de la propiedad  
- `margin` es la propiedad. `3px` es el valor de la propiedad  
- Hay muchos otros valores que puede utilizar para aplicar estilos correctos a su página web.

**.class**
- Selecciona todos los elementos con el nombre de clase dado  
- Seleccionará todos los p con class="myClass"  
- Escribe un punto (.) seguido del nombre de la clase

```html
<p class="myClass">This is a paragraph</p>
```

```css
.myClass {
  background-color: yellow;
```


**child .class**
- Puede apuntar a un elemento hijo utilizando una jerarquía de clases
```css
// syntax

.parent .child {
    background-color: yellow;
}
```

- Debe escribir el nombre de la clase padre seguido de un espacio, y a continuación el nombre de la clase hija.  
- El siguiente ejemplo añadirá `background-color: yellow` al párrafo

```html
<div class="parent">
    <p class="child">This is a paragraph</p>
</div>
```

```css
.parent .child {
  background-color: yellow;
}
```


**#id**
- Estilizar el elemento con el atributo `id` dado  
- En el siguiente ejemplo `myParagraph` es el id del párrafo  
- Seleccionamos los elementos añadiendo `#` seguido del atributo `id` del elemento

```html
<p id="myParagraph">This is a paragraph</p>
```

```css
#myParagraph {
  background-color: yellow;
}
```

**element tag**
- Puedes seleccionar directamente un elemento por su nombre de etiqueta y aplicar los estilos  
- En este caso no tienes que mencionar el `id` o la `class` - simplemente escribe el nombre del elemento en tus estilos y añádele propiedades.  
- El siguiente ejemplo tomará todos los elementos `p` y les aplicará el estilo
```html
<p>This is a paragraph</p>
```

```css
p{  
background-color: yellow;
}
```

**Mix n match**
- Los selectores mencionados son las formas básicas y más comunes de seleccionar elementos y aplicarles estilos.  
- También puede combinar cualquiera de los selectores anteriores para aplicar los estilos  

**Id and Class**
- `id="miParrafo"` forma el selector Id 
- `class="miClase"` forma el selector de clase
```html
<p id="myParagraph" class="myClass">This is a paragraph</p>
```

```css
#myParagraph.myClass {
  background-color: yellow;
}
```

**Element and Class**
- `p` se utiliza como selector de elemento 
- `class="myClass"` forma el selector de clase
```html
<p class="myClass">This is a paragraph</p>
```

```css
p.myClass {
  background-color: yellow;
}
```

### <ins>Advanced Selectors</ins>

**adjacent selector**
- Selecciona sólo el elemento precedido por el elemento anterior. 
- En este caso, sólo el primer párrafo después de cada ul tendrá texto rojo.

```html
<ul></ul>
<p></p>
```

```css
ul + p {
    color: red;
}
```

**attributes selector**
- Sólo seleccionará las etiquetas de anclaje que tengan un atributo title
```css
a[title] {
    color: green;
}
```

- Aplicará estilo a todas las etiquetas de anclaje que enlacen a `https://www.gammatech.school/`.
```css
a[href="https://www.gammatech.school/"] {
    color: #1f6053; /* green */
}
```

- La estrella designa que el valor que procede debe aparecer en alguna parte del valor del atributo 
```css
a[href*="mma"] {
    color: #1f6053;

}
```
- El atributo "contiene" un valor 
- Debe ser una palabra entera
```css
[title~="cat"] {
    border: 5px solid yellow;
}
```

```css
<img src="cat1.jpg" title="small cat" width="150" height="113"> //
selected
<img src="cat2.gif" title="catssss" width="224" height="162"> // NOT
selected

<img src="dog.gif" title="dog" width="200" height="358"> // NOT selected
```

- El atributo "contiene" un valor 
- NO tiene que ser una palabra entera

```css
[title*="cat"] {
    border: 5px solid yellow;
}
```

```css
<img src="cat1.jpg" title="small cat" width="150" height="113"> //
selected
<img src="cat2.gif" title="catssss" width="224" height="162"> // selected
<img src="dog.gif" title="dog" width="200" height="358"> // NOT selected
```

- Valor del atributo "empieza por"  
- El valor TIENE que ser una palabra entera  
  - O una palabra entera    
  - O palabra seguida de -
```css
[title|="cat"] {
    border: 5px solid yellow;
}
```

```html
<img src="cat1.jpg" title="cat-like small" width="150" height="113"> //
selected
<img src="cat2.gif" title="cat" width="224" height="162"> // selected
<img src="dog.gif" title="dog" width="200" height="358"> // NOT selected
```

- Valor del atributo "empieza por"  
- El valor NO tiene que ser una palabra entera

```css
[title^="ca"] {
    border: 5px solid yellow;
}
```

```html
<img src="cat1.jpg" title="cat-like small" width="150" height="113"> //
selected
<img src="cat2.gif" title="cat" width="224" height="162"> // selected
<img src="dog.gif" title="dog" width="200" height="358"> // NOT selected
```

- Valor del atributo "termina con"  
- El valor NO tiene que ser una palabra entera

```css
[title$="at"] {
    border: 5px solid yellow;
}
```

```html
<img src="cat1.jpg" title="cat-like small" width="150" height="113"> //
NOT selected
<img src="cat2.gif" title="cat" width="224" height="162"> // selected
<img src="dog.gif" title="dog" width="200" height="358"> // NOT selected
```

### <ins>Backgrounds</ins>
- Puedes establecer diferentes fondos para tus elementos  
- El fondo de un elemento es el tamaño total del elemento, incluyendo el relleno y el borde (pero no el margen).  
- A continuación se muestra la lista de todas las propiedades de fondo
```css
background-color
background-image
background-position
background-size
background-repeat
background-origin
background-clip
background-attachment
```

- Puede definir todas las propiedades con una sola declaración  
- Estas son algunas de las propiedades de fondo más utilizadas  
- Añade el color de fondo `lightblue`  
- Añade la imagen de fondo `myImage.png`  
- Establece `no-repeat` background, lo que significa que no repetirá la imagen de fondo.  
    - Por defecto se repite tanto vertical como horizontalmente. 
- Establece la posición de fondo `center`.
```css
body {
  background: lightblue url("myImage.png") no-repeat center;
}
```

### <ins>Colors</ins>
- La propiedad color especifica el color del texto  
- Puede especificar la propiedad color en diferentes elementos utilizando diferentes tipos de selectores 
- Puede especificar colores por su nombre, su valor hexadecimal o su valor RGB
```css
h1 {
  color: red;

}

h1.myClass {
  color: #02af00;

}

h1#myId {
  color: rgb(111,111,111);

}
```

### <ins>Borders</ins>
- Puedes añadir bordes a tus elementos HTML 
- A continuación se muestra la lista de todas las propiedades de borde
```css
border-width
border-style (required)
border-color
```
- En el siguiente ejemplo
- `5px` es el ancho del borde 
- `solid` es el estilo del borde  
    - Otros ejemplos son `dotted`, `double`, `dashed`. 
- `red` es el color del borde  
    - Puedes especificar los colores por su nombre, su valor hexadecimal o su valor RGB.
```css
h1 {
  border: 5px solid red;
}
```

### <ins>Fun with Border Radius</ins>

**Shapes**
- Los bordes también tienen otra propiedad llamada `border-radius` con la que puedes dar diferentes formas a tus elementos
- Si el radio del borde es del 50%, el cuadrado se convertirá en un círculo.
```css
.square {
  border-radius: none;

}

.circle {
  border-radius: 50%;

}
```

**Shorthand**
- Si se establece un valor, este radio se aplica a las 4 esquinas.  
- Si se establecen dos valores, el primero se aplica a las esquinas superior izquierda e inferior derecha, el segundo a las esquinas superior derecha e inferior izquierda.  
- Si se establecen tres valores, el segundo se aplica a las esquinas superior derecha e inferior izquierda.  
- Si se establecen cuatro valores, se aplicarán a las esquinas superior izquierda, superior derecha, inferior derecha e inferior izquierda (en ese orden).
```html
<div class="card one">
	<h1 class="">One</h1>
</div>
<div class="card two">
	<h1 class="">Two</h1>
</div>
<div class="card three">
	<h1 class="">Three</h1>
</div>
<div class="card four">
	<h1 class="">Four</h1>
</div>
```

```css
// all 4 corners
.one {

  border-radius: 50%;
}

// 10% top-left and bottom-right,  20% top-right and bottom-left
.two {

  border-radius: 10% 20%
}

// 10% top-left, 20% top-right and also bottom-left, 30% bottom-right
.three {

  border-radius: 10% 20% 30%;
}

// top-left, top-right, bottom-right, bottom-left corner (in that order)
.four {

  border-radius: 10% 20% 30% 40%;
}

.card {
  border: 10px solid #E53038;
  height: 100px;
  width: 100px;
  padding: 20px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin-bottom: 20px;

}
```

**Circle and leaf**

**Circle**
```css
.circle {
    border-radius: 50%;
}
```

**Leaf**
```css
.leaf {
    border-radius: 5px 20px 5px;
}
```


