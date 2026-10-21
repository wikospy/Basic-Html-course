# HTML — BASIC

## 1. HTML fundamentals

HTML describes the meaning and structure of a web document. An element is usually made from an opening tag, content, and a closing tag; attributes add information to an element.

**Syntax**

```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <title>Page title</title>
  </head>
  <body>
    <!-- Visible document content -->
  </body>
</html>
```

**Example:** A page begins with `<!doctype html>` so the browser uses standards mode, and `lang="en"` helps assistive technology and search engines.

**Use / do not use:** Use this structure for every standalone page. Do not put visible page content in `head`, and do not omit the doctype.

**Write yourself:** Create `Basics/fundamentals.html` with a title, a language, one comment, and one visible paragraph.

## 2. Text

Headings communicate hierarchy; paragraphs group prose; `strong` and `em` communicate importance and emphasis. `b` and `i` are presentational alternatives and should not replace meaning.

**Syntax**

```html
<h1>Recipe collection</h1>
<h2>Vegetarian recipes</h2>
<p>Use <strong>fresh</strong> ingredients and <em>read the instructions</em>.</p>
<p>Water is H<sub>2</sub>O and 2<sup>3</sup> is 8.</p>
<hr>
```

**Example:** Use `del` and `ins` to show a price change, and `mark` to highlight a search result.

**Use / do not use:** Use headings for structure, not just larger text. Use CSS for appearance. Use `br` for a meaningful line break (such as an address), not to create vertical spacing.

**Write yourself:** Write a product description with one heading, two paragraphs, one emphasized phrase, one highlighted phrase, and one line break in an address.

## 3. Links

An anchor navigates to a URL or document fragment.

**Syntax**

```html
<a href="about.html">About us</a>
<a href="https://example.com" target="_blank" rel="noopener">Reference</a>
<a href="#contact">Jump to contact</a>
<a href="mailto:hello@example.com">Email us</a>
<a href="guide.pdf" download>Download the guide</a>
```

**Example:** A site navigation uses relative links such as `products.html`; a reference link uses an absolute URL.

**Use / do not use:** Use links for navigation or resources. Do not use a link as a button for an action, and do not use `target="_blank"` without an appropriate `rel`.

**Write yourself:** Make a three-link navigation, a section link, and a download link. Give the destination section a matching `id`.

## 4. Images

`img` embeds an image; `alt` supplies its text alternative.

**Syntax**

```html
<img src="images/coffee.jpg" alt="A cup of coffee on a wooden table"
     width="640" height="480">
```

**Example:** A decorative divider can use `alt=""`; an informative product photo needs a useful description.

**Use / do not use:** Always provide `alt`. Use real dimensions to reduce layout shifts. Do not put important text only inside an image, and do not use a vague alt value like `"image"`.

**Write yourself:** Add two local images: one informative image with descriptive alt text and one decorative image with empty alt text.

## 5. Lists

Use unordered lists for unordered items, ordered lists for sequence, and description lists for term/value pairs.

**Syntax**

```html
<ul><li>Tea</li><li>Coffee</li></ul>
<ol><li>Open the app</li><li>Sign in</li></ol>
<dl><dt>HTML</dt><dd>A markup language for document structure.</dd></dl>
```

**Example:** A recipe uses an unordered ingredient list and an ordered method list.

**Use / do not use:** Use lists when items belong together. Do not use repeated paragraphs or manual numbers when the content is a list.

**Write yourself:** Mark up a packing checklist, a five-step setup guide, and three web terms with definitions.

## 6. Basic containers

`div` is a generic block container; `span` is a generic inline container.

**Syntax**

```html
<div class="card"><h2>News</h2><p>Latest update.</p></div>
<p>Save <span class="keyboard-key">Ctrl + S</span>.</p>
```

**Example:** A `div` groups a card for styling; a `span` marks one phrase inside a sentence.

**Use / do not use:** Use these only when no semantic element fits. Do not replace `nav`, `article`, or `button` with a `div`.

**Write yourself:** Build a notification using one `div` and one `span`, then identify which parts could become semantic elements.

## 7. Basic semantic structure

Semantic elements describe a page region to browsers and assistive technology.

**Syntax**

```html
<header>Brand and page heading</header>
<nav aria-label="Primary"><a href="/">Home</a></nav>
<main><section><h2>News</h2><article><h3>Update</h3></article></section></main>
<footer>Copyright information</footer>
```

**Example:** A blog page uses `main` for its unique content, `article` for each post, and `footer` for site-wide information.

**Use / do not use:** Use the element whose meaning matches the content. Do not add landmarks just to make markup look sophisticated.

**Write yourself:** Create a page skeleton with a header, labeled navigation, one main section, two articles, and a footer.

## 8. Tables

Tables represent relationships between row and column data, not layout.

**Syntax**

```html
<table>
  <caption>Monthly expenses</caption>
  <thead><tr><th scope="col">Month</th><th scope="col">Total</th></tr></thead>
  <tbody><tr><th scope="row">January</th><td>$120</td></tr></tbody>
  <tfoot><tr><th scope="row">Total</th><td>$120</td></tr></tfoot>
</table>
```

`colspan="2"` combines columns; `rowspan="2"` combines rows.

**Example:** An invoice uses header cells for column names and row names, plus a total in `tfoot`.

**Use / do not use:** Use tables for tabular data and include a caption and scopes. Do not use tables for page layout.

**Write yourself:** Create a three-column grade table with a caption, header row, body rows, and a footer average. Use one `colspan`.

## 9. Forms

Forms collect named controls. Only successful controls with a `name` are submitted.

**Syntax**

```html
<form action="/signup" method="post">
  <label for="email">Email</label>
  <input id="email" name="email" type="email" placeholder="you@example.com" required>
  <button type="submit">Sign up</button>
</form>
```

Input types include `text`, `number`, `email`, `password`, `tel`, `url`, `date`, `time`, `checkbox`, `radio`, `file`, `submit`, and `reset`.

**Example:** A login form uses `email` and `password`; a profile form may use `tel` and `date`.

**Use / do not use:** Use a real `button` for submission and a `label` for every control. Use `disabled` only when an interaction is unavailable, `readonly` when a value may be submitted but not edited. Do not rely on placeholders as labels.

**Write yourself:** Build a contact form with name, email, phone, message, one checkbox, one radio group, submit, and reset controls. Give every submitted control a `name`.

## BASIC checkpoint

Before starting ADVANCED, explain:

- Why the doctype, `lang`, title, and `alt` matter.
- The difference between a link and a button.
- Why heading order, labels, table scopes, and `name` attributes matter.
- When a `div` is appropriate.

## BASIC project

Build a small accessible **personal profile page** using only the topics above. It must contain navigation, a heading hierarchy, an image, an about section, a skills list, a project table, and a contact form. Write it in `projects/basic-profile/` and test every link and form control yourself.
