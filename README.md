# Clase 3 → Miércoles 21 de marzo

### CSS

**Algunos apuntes iniciales:**  

- CSS es sigla de Cascading Stylesheets. 

- CSS no es un lenguaje de programación. No tiene variables, ciclos ni funciones. Aunque sí ofrecen algo parecido a las condicionales (módulos que permiten adaptar la presentación del contenido a características del dispositivo, llamados media queries). 

- CSS es un lenguaje descriptivo que ofrece lo necesario para definir y crear la presentación de la página web ya estructurada (mediante HTML)

- CSS3 es su versión más reciente, en ella se incorporan propiedades que nos permiten agregar transiciones, animaciones, transformaciones, esquinas redondeadas, sombras, gradientes, etc.

#### Regla CSS

**Las reglas son el bloque constructivo más básico del CSS**. Una regla CSS generalmente tiene un `selector` y `{declaraciones}`, dentro de las declaraciones podemos encontrar los pares `propiedad:valor;`. 

Primero **pongamos atención a los distintos selectores posibles**, en tanto son los responsables de señalar a los elementos HTML que serán afectos por lo definido en las declaraciones de la regla:

- Podemos tener selectores cuyo nombre es igual a un elemento HTML, así, por ejemplo, el selector `body{}` apunta a todo lo que sea incluido dentro del elemento HTML `<body>…</body>`. Una variación sobre lo mismo es el caso del selector `body div p{}`, que apunta al elemento HTML `<p>…</p>`, que está dentro del elemento HTML `<div>…</div>`, que, a su vez, está dentro del elemento HTML `<body>…</body>`. Pero la variación recién presentado es distinta de la que presenta un selector `body, div, p{}` donde las comas obligan a apuntar, por igual, a cada elemento HTML mencionado.

- Podemos tener selectores cuyo nombre tiene un "::agregado" útil para apuntar a una parte de un elemento HTML, así por ejemplo el selector `p::first-line{}` apuntará solo la primera línea del elemento HTML `<p></p>`. A estos "selectores con ::agregado" se les llama [pseudoelementos](https://developer.mozilla.org/es/docs/Web/CSS/Pseudoelementos). 

- Podemos tener selectores cuyo nombre tiene un ":agregado" para apuntar a un estado especial de un elemento HTML, así por ejemplo el selector `p:hover{}` afectará todo el elemento HTML `<p></p>` cada vez que el mouse pase por encima suyo. A estos "selectores con :agregado" se les llama [pseudoclases](https://developer.mozilla.org/es/docs/Web/CSS/Pseudo-classes).

- Podemos tener selectores apuntando a elementos según los atributos que tengan dentro de la `<primera etiqueta>` del elemento HTML. Así, por ejemplo: 

   - `p.inicio{}` apuntará a todo elemento HTML `<p class="inicio"></p>`. Dicho de otra forma: apuntará a todo elemento elemento HTML `<p></p>` mientras tenga un atributo de clase, con variable inicio.
   - `p#bajada{}` apuntará al elemento HTML `<p id="bajada"></p>`. Dicho de otra forma: apuntará al único elemento HTML `<p></p>` que tenga un atributo de identidad, con variable bajada.
   - `p:lang(it){}` apuntará a todo elemento HTML `<p lang="it"></p>`. Dicho de otrao forma: apuntará a todo elemento HTML `<p></p>` que tenga un [atributo de idioma (language)](https://www.w3.org/International/questions/qa-html-language-declarations.es), con variable it (italiano).
   - `a[href$=".pdf"] {}` apuntará a todo elemento HTML `<a></a>` que en su atributo de referencias de hipertexto `href=""` contenga una documento extensión ".pdf".
  
Con este listado ya cubrimos una parte importante de los posibles selectores. Para revisar más: [CSS Selector Reference](https://www.w3schools.com/cssref/css_selectors.asp). 

**Ahora pongamos atención las "media queries"**. Este es un módulo CSS3 que permite adaptar la representación del contenido a características del dispositivo, y puede ser agregada en el vínculo al estilo CSS o directamente en la hoja de estilo, de las siguientes maneras:

```
<!-- CSS media query dentro de un atributo de un elemento HTML <link>…</link> -->
<link rel="stylesheet" media="screen and (max-width: 600px)" href="example.css" />

<!-- CSS media query dentro del estilo -->
<style>
@media screen and (max-width: 600px) {
  sidebar {
    display: none;
  }
}
</style>
```

Noten que cuando las "media queries" se usan dentro del estilo, afectan solo a las reglas que estén contenidas dentro de los paréntesis de llave. Con eso siempre presente, no tendrán problemas al aprovechar las posibilidades de las [media queries](https://developer.mozilla.org/es/docs/CSS/Media_queries).

**Para seguir explorando CSS, necesitamos echar mano a un documento HTML que ya esté preparado**. Para partir, lo más adecuado sería copiar un único archivo de este repositorio, y ponerlo dentro de la carpeta que trabajaste la [clase recién pasada](https://github.com/profesorfaco/dno037-2018-02). Ese documento es [estilo.css](https://raw.githubusercontent.com/profesorfaco/dno037-2018-03/gh-pages/estilo.css).

**En el desarrollo de la clase vamos a revisar:**

- [modelos de color](https://es.wikipedia.org/wiki/Modelo_de_colores) ([RGB](https://es.wikipedia.org/wiki/RGB) y [HSL](https://es.wikipedia.org/wiki/Modelo_de_color_HSL)) y [consejos sobre el uso de color](https://material.io/color).
- [proporciones](https://elmaquetadorerrante.wordpress.com/2010/07/11/cuerpo-de-fibonacci/), ["pairing"](https://fonts.google.com/) y [otras consideraciones](http://webtypography.net/toc/) [tipográficas](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Text)
- [curvas de velocidad](http://www.bufa.es/css3-transitions/) de las transiciones. 

- - - - - 

[Clase anterior](https://github.com/profesorfaco/dno037-2018-02) | [Siguiente clase](https://github.com/profesorfaco/dno037-2018-04)
