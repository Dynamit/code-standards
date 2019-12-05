# HTML

Use the HTML 5 doctype

```html
<!doctype html>
```

Declare a [language attribute](http://www.w3.org/html/wg/drafts/html/master/semantics.html#the-html-element) on the opening `<html>` tag.

```html
<html lang="en">
```

Define explicit character encoding to ensure proper rendering of content.

```html
<meta charset="utf-8">
```

Nest tags. Use soft tabs, 2 spaces

```html
<!-- bad -->
<ul>
	<li><a href="...">Lorem ipsum</a></li>
</ul>

<!-- good -->
<ul>
  <li>
    <a href="...">Lorem ipsum</a>
  </li>
</ul>
```

Use lowercase for tags names and attributes.

```html
<!-- bad -->
<IMG SRC="images/tidyman.jpg" ALT="The Tidyman">

<!-- good -->
<img src="images/tidyman.jpg" alt="The Tidyman">
```

Use double quotes for attribute values.

```html
<!-- bad -->
<input type=text>

<!-- good -->
<input type="text">
```

Don’t omit [optional closing tags](http://www.w3.org/TR/html5/syntax.html#optional-tags).

Avoid type attributes on script and stylesheet includes - `text/css` and `text/javascript` are interpreted automatically.

Don't include values for [boolean attributes](https://html.spec.whatwg.org/multipage/infrastructure.html#boolean-attributes).

```html
<!-- bad -->
<input type="checkbox" value="1" checked="checked">

<!-- good -->
<input type="checkbox" value="1" checked>
```

Use [semantic markup](http://www.adobe.com/devnet/html5/articles/semantic-markup.html).

Use tags according to their purpose. For instance, don't use an `<a>` tag when a `<button>` is more appropriate. Aside from making our code more meaningful, using the correct tags has a huge benefit for accessibility.

Button actions stay on the page, while anchors take the user to a different page.

```html
<!-- bad -->
<div>Heading</div>
<div>Paragraph copy</div>
<a href="#" class="button">Submit</a>

<!-- good -->
<h1>Heading</h1>
<p>Paragraph copy</p>
<button>Submit</button>
```

## Separation of Concerns

Avoid obtrusive JavaScript. JavaScript should live in `.js` files. This helps keep a clear separation of concerns and aids in code scalability and maintainability.

```html
<!-- bad -->
<button onclick="submit()">Click Me!</button>
```

Don't rely on markup for visual formatting. (e.g. `<br>`, `<b>`, `<i>`).

```html
<!-- bad -->
<p>
  This code is using <i><b>markup</b></i> for formatting.
  <br>
  <br>
  <br>
  This shouldn't be done!
</p>

<!-- good -->
<p>
  This code is not using <em>markup</em> for formatting.
</p>
<p>
  This is how you do it!
</p>
```

It's OK to use `<strong>` and `<em>` to provide semantic meaning to inline text, but ensure that the appropriate styles are defined in the stylesheet. Do not rely on `<strong>` or `<em>` for visual formatting. No adding of classes to `<strong>` or `<em>`.
