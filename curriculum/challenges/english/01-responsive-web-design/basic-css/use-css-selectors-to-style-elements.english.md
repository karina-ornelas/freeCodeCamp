---
id: bad87fee1348bd9aedf08805
title: Use CSS Selectors to Style Elements
challengeType: 0
videoUrl: 'https://scrimba.com/c/cJKMBT2'
---

## Description
<section id='description'>
With CSS, there are hundreds of CSS <code>properties</code> that you can use to change the way an element looks on your page.
When you entered <code>&#60;h2 style="color: red;"&#62;CatPhotoApp&#60;/h2&#62;</code>, you were styling that individual <code>h2</code> element with <code>inline CSS</code>, which stands for <code>Cascading Style Sheets</code>.
That's one way to specify the style of an element, but there's a better way to apply <code>CSS</code>.
At the top of your code, create a <code>style</code> block like this:

```html
<style>
</style>
```

Inside that style block, you can create a <code>CSS selector</code> for all <code>h2</code> elements. For example, if you wanted all <code>h2</code> elements to be red, you would add a style rule that looks like this:

```html
<style>
  h2 {
    color: red;
  }
</style>
```

Note that it's important to have both opening and closing curly braces (<code>{</code> and <code>}</code>) around each element's style rule(s). You also need to make sure that your element's style definition is between the opening and closing style tags. Finally, be sure to add a semicolon to the end of each of your element's style rules.
</section>

## Instructions
<section id='instructions'>
Delete your <code>h2</code> element's style attribute, and instead create a CSS <code>style</code> block. Add the necessary CSS to turn all <code>h2</code> elements blue.
</section>

## Tests
<section id='tests'>

```yml
tests:
  - text: Remove the style attribute from your <code>h2</code> element.
    testString: assert(!$("h2").attr("style"), 'Remove the style attribute from your <code>h2</code> element.');
  - text: Create a <code>style</code> element.
    testString: assert($("style") && $("style").length >= 1, 'Create a <code>style</code> element.');
  - text: Your <code>h2</code> element should be blue.
    testString: assert($("h2").css("color") === "rgb(0, 0, 255)", 'Your <code>h2</code> element should be blue.');
  - text: Ensure that your stylesheet <code>h2</code> declaration is valid with a semicolon and closing brace.
    testString: assert(code.match(/h2\s*\{\s*color\s*:.*;\s*\}/g), 'Ensure that your stylesheet <code>h2</code> declaration is valid with a semicolon and closing brace.');
  - text: Make sure all your <code>style</code> elements are valid and have a closing tag.
    testString: assert(code.match(/<\/style>/g) && code.match(/<\/style>/g).length === (code.match(/<style((\s)*((type|media|scoped|title|disabled)="[^"]*")?(\s)*)*>/g) || []).length, 'Make sure all your <code>style</code> elements are valid and have a closing tag.');

```

</section>

## Challenge Seed
<section id='challengeSeed'>

<div id='html-seed'>

```html
<h2 style="color: red;">CatPhotoApp</h2>
<main>
  <p>Click here to view more <a href="#">cat photos</a>.</p>

  <a href="#"><img src="https://bit.ly/fcc-relaxing-cat" alt="A cute orange cat lying on its back."></a>

  <div>
    <p>Things cats love:</p>
    <ul>
      <li>cat nip</li>
      <li>laser pointers</li>
      <li>lasagna</li>
    </ul>
    <p>Top 3 things cats hate:</p>
    <ol>
      <li>flea treatment</li>
      <li>thunder</li>
      <li>other cats</li>
    </ol>
  </div>

  <form action="/submit-cat-photo">
    <label><input type="radio" name="indoor-outdoor" checked> Indoor</label>
    <label><input type="radio" name="indoor-outdoor"> Outdoor</label><br>
    <label><input type="checkbox" name="personality" checked> Loving</label>
    <label><input type="checkbox" name="personality"> Lazy</label>
    <label><input type="checkbox" name="personality"> Energetic</label><br>
    <input type="text" placeholder="cat photo URL" required>
    <button type="submit">Submit</button>
  </form>
</main>
```

</div>



</section>

## Solution
<section id='solution'>

```html
<style>
  h2 {
    color: blue;
  }
</style>
<h2>CatPhotoApp</h2>
<main>
  <p>Click here to view more <a href="#">cat photos</a>.</p>

  <a href="#"><img src="https://bit.ly/fcc-relaxing-cat" alt="A cute orange cat lying on its back."></a>

  <div>
    <p>Things cats love:</p>
    <ul>
      <li>cat nip</li>
      <li>laser pointers</li>
      <li>lasagna</li>
    </ul>
    <p>Top 3 things cats hate:</p>
    <ol>
      <li>flea treatment</li>
      <li>thunder</li>
      <li>other cats</li>
    </ol>
  </div>

  <form action="/submit-cat-photo">
    <label><input type="radio" name="indoor-outdoor" checked> Indoor</label>
    <label><input type="radio" name="indoor-outdoor"> Outdoor</label><br>
    <label><input type="checkbox" name="personality" checked> Loving</label>
    <label><input type="checkbox" name="personality"> Lazy</label>
    <label><input type="checkbox" name="personality"> Energetic</label><br>
    <input type="text" placeholder="cat photo URL" required>
    <button type="submit">Submit</button>
  </form>
</main>
```
</section>
