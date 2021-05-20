---
layout: post
category: "Documentation"
tag: "How To's"
title: Design System Cheatsheet
subtitle: "Information on how to fill in content for the design system on GitHub pages"
permalink: /documentation/cheatsheet/
---

## Basic Syntax

<table class="doc-table">
  <thead>
    <tr>
      <th>Markdown</th>
      <th>Result</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td># Heading 1</td>
      <td>
        <h1>Heading 1</h1>
        <small>
          <i class="icn icn-Important-Filled"></i>
          Do not use, it is automatically added to a page heading.
        </small>
      </td>
    </tr>
    <tr>
      <td>## Heading 2</td>
      <td><h2>Heading 2</h2></td>
    </tr>
    <tr>
      <td>### Heading 3</td>
      <td><h3>Heading 3</h3></td>
    </tr>
    <tr>
      <td>#### Heading 4</td>
      <td><h4>Heading 4</h4></td>
    </tr>
    <tr>
      <td>Standard paragraph. Lorem ipsum sit dolor amet</td>
      <td>
        <p>Standard paragraph. Lorem ipsum sit dolor amet</p>
      </td>
    </tr>
    <tr>
      <td>**bold text**</td>
      <td><b>bold text</b></td>
    </tr>
    <tr>
      <td>*italicized text*</td>
      <td><i>italicized text</i></td>
    </tr>
    <tr>
      <td>~~Strikethrough text~~</td>
      <td><s>Strikethrough text</s></td>
    </tr>
    <tr>
      <td>> blockquote</td>
      <td>
        <blockquote>
          <p>blockquote</p>
        </blockquote>
      </td>
    </tr>
    <tr>
      <td>
        1. First item<br>
        2. Second item<br>
        3. Third item
      </td>
      <td>
        <ol>
          <li>First item</li>
          <li>Second item</li>
          <li>Third item</li>
        </ol>
      </td>
    </tr>
    <tr>
      <td>
        - First item<br>
        - Second item<br>
        - Third item
      </td>
      <td>
        <ul>
          <li>First item</li>
          <li>Second item</li>
          <li>Third item</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>[link](https://example.com)</td>
      <td><a class="link" href="https://example.com">link</a></td>
    </tr>
    <tr>
      <td>[external link](https://example.com){:target="_blank"}</td>
      <td><a class="link" target="_blank" href="https://example.com">external link</a> (opens in a new tab)</td>
    </tr>
    <tr>
      <td>![Some alt text](https://via.placeholder.com/150)</td>
      <td><img src="https://via.placeholder.com/150" alt="Some alt text"></td>
    </tr>
    <tr>
      <td>&#60;span class="snip">Something highlighted&#60;/span></td>
      <td><span class="snip">Something highlighted</span></td>
    </tr>
    <tr>
      <td>&#60;i class="icn icn-Worker-Filled">&#60;/i></td>
      <td><i class="icn icn-Worker-Filled"></i></td>
    </tr>
  </tbody>
</table>

## Extended Syntax

<table class="doc-table">
  <thead>
    <tr>
      <th>Markdown</th>
      <th>Result</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <pre>
| Heading column 1   | Heading column 2 |
| ------------------ | ---------------- |
| Row 1 - Column 1   | Row 1 - Column 2 |
| Row 2 - Column 1   | Row 2 - Column 2 |
{: .doc-table}
        </pre>
      </td>
      <td>
        <table class="doc-table">
          <thead>
            <tr>
              <th>Heading column 1</th>
              <th>Heading column 2</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td>Row 1 - Column 1</td>
              <td>Row 1 - Column 2</td>
            </tr>
            <tr>
              <td>Row 2 - Column 1</td>
              <td>Row 2 - Column 2</td>
            </tr>
          </tbody>
        </table>
      </td>
    </tr>
    <tr>
      <td>
        <pre>
{&#37; include snippet.html code='
  &#60;button class="button" type="button">Default&#60; /button>
' &#37;}
        </pre>
      </td>
      <td>
{% include snippet.html code='

<button class="button" type="button">Default</button>

' %}
      </td>
    </tr>
    <tr>
      <td>
        <pre>
<!-- Content switch -->
<!-- Content switch tab 1 -->
{&#37; capture switch-content-1 %}
  Switch content 1. This can be anything.
{&#37; endcapture %}

<!-- Content switch tab 2 -->
{&#37; capture switch-content-2 %}
  Switch content 2. This can be anything.
{&#37; endcapture %}

<!-- Render Content -->
{&#37; include content-switch.html for="demo"
           content-1-label="One" content-1=switch-content-1
           content-2-label="Two" content-2=switch-content-2
%}
        </pre>
      </td>
      <td>
<!-- Content switch -->
<!-- Content switch tab 1 -->
{% capture switch-content-1 %}
  Switch content 1. This can be anything.
{% endcapture %}

<!-- Content switch tab 2 -->
{% capture switch-content-2 %}
  Switch content 2. This can be anything.
{% endcapture %}

<!-- Render Content -->
{% include content-switch.html for="demo"
           content-1-label="One" content-1=switch-content-1
           content-2-label="Two" content-2=switch-content-2
%}
      </td>
    </tr>
    <tr>
      <td>
        <pre>
{&#37; include do-dont.html 
  do-img="buttons-do.jpg"
  do-text="Use capital case for labeling buttons."
  dont-img="buttons-dont.jpg"
  dont-text="Do not use uppercase."
%}
        </pre>
      </td>
      <td>
{% include do-dont.html 
  do-img="buttons-do.jpg"
  do-text="Use capital case for labeling buttons."
  dont-img="buttons-dont.jpg"
  dont-text="Do not use uppercase."
%}
      </td>
    </tr>
  </tbody>
</table>