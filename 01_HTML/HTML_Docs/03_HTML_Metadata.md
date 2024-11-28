# Metadata in HTML

The `head` section contains essential information that helps web browsers understand how to show the webpage properly.This information is known as `Metadata`.

It includes things like the _title_ of the page, links to _style sheets_, _script files_ and even tiny _custom icons_ that appear in browser tabs.

Throughout this document, we will cover the above topics and more. By the end, you'll have a better understanding of how HTML works,how its metadata is added and its importance.

# What is the HTML head?

When you look at the `basic structure` of an HTML document, you'll notice it is divided into 3 _main_ sections:

- `<html>`: This wraps the entire HTML document.
- `<head>`: This specifies all the metadata about the document.
- `<body>`: This contains the main content of the document.

```html
<!DOCTYPE html>
<html lang="en-US">
  <head>
    <meta charset="utf-8" />
    <title>The Div Soup</title>
  </head>
  <body>
    <p>This is the Div Soup page</p>
  </body>
</html>
```

The HTML head refers to all the content written within this `<head>` element. Unlike the content of the `<body>` tag which is displayed on the browser when a web page is rendered, any content that goes in the `head` section stays hidden.

The head's only job is to contain the **metadata** about the document.

# What do you mean by Metadata?

`Metadata` refers to the data that provides information about other data.

In the context of an HTML document, metadata refers to the information about the web page itself such as its title, description, author and other such information.

Metadata is not directly displayed on a web page but is necessary for Search Engine Optimization (SEO), browser rendering and accessibility.

# Adding a title

HTML provides us with a `<title>` element that helps to add a title to the document. It is written in the `<head>` section.

```html
<head>
  <title>The Div Soup</title>
</head>
```

Don't confuse this `<title>` element with the `<h1>` element which is also sometimes referred to as the page title. They are very different!

While `<h1>` is used to define a main heading for a page content, `<title>` represents the title for the entire HTML document. It's contents appear in the browser's tab or as suggested bookmark name when a page is saved as a bookmark. Search engines also use this title when displaying search results related to the web page.

![title is used as bookark name](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/The_head_metadata_in_HTML/bookmark-example.png)

As you can see in the above image, the web page name defined via `<title>` element is used as default name when bookmarking a website.

# Adding metadata with `<meta>` tag

HTML consists of different types of `<meta>` elements that help to metadata to a document. All these tags are included in the `<head>` section.

`<meta>` tag is an empty/void tag. It means it only has an opening tag and not closing tag. So it uses different **attributes** to defines different information about the document.

Let's go over the important ones, one by one. 🚀

## Specifying a document's character encoding

`Character encoding` refers to the method used to represent characters (letters, numbers, symbols, etc.) in a digital format, such as those used in text documents like HTML files.

Simply put, it specifies how a character is represented as binary data, for example ASCII, UTF-8.

For an HTML document, character encoding is specified via the `charset` attribute of the `<meta>` tag.

```html
<meta charset="utf-8" />
```

The above code mentions that the document is only permitted to use the character set defined by utf-8.

UTF-8 is a universal character set that includes all the character from any human language. Hence it is the most common used character set for web pages as it suitable for multilingual websites.

Fox example, a web page can handle both English and Japanese when its character set is defined as utf-8.

![Multilingual websites use character set UTF-8](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/The_head_metadata_in_HTML/correct-encoding.png)

Choosing the correct character set is important for a web page. Suppose we use `ISO-8859-1` instead of `uft-8` in the above example, we get the below result.

![using latin character set](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/The_head_metadata_in_HTML/bad-encoding.png)

`ISO-8859-1` is a character set for Latin alphabet hence the Japanese characters are not properly displayed.

## Adding an author and description

Many `<meta>` elements accept `name` and `content` attributes.

- `name`: specifies the type or purpose of information a \<meta> element contains
- `content`: specifies the actual information or the content asscoiated with the _name_ attribute

These attributes are used to define metadata like author, description, keywords etc.

```html
<meta name="author" content="Author of the document" />
<meta
  name="description"
  content="The Div Soup aims to simplify and provide
in depth web development content to help beginners get started with building websites and application. "
/>
```

## Setting a page's viewport configuration

HTML provides a viewport meta tag which is crucial for creating responsive web designs that adapt to various screen sizes and devices. When we view a web page on different devices such as laptops, desktops, tablets or smartphones, the viewport tag controls how a web page is displayed and scaled on the screen.

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

- `name="viewport"`: defines that this meta tag is for setting the viewport details
- `initial-scale`: this sets the initial scale of the web page when it is first loaded. Here `initial-scale=1.0` means that the webpage is initially displayed at its original size without any zooming.
- `width`: tells the browser the viewport should be in relation to the device's screen width. Here `width=device-width` sets the width of the viewport to match the width of the device's screen.

# Adding custom icons for a website

Adding custom icons to a website enhances its visual appeal and helps users identify and interact with the site more effectively, especially when bookmarking or saving it to their home screen. These custom icons are called `favicons` which is a 16-pixel square icon.

HTML provides a `<link>` element which accepts `href` attribute to specify the URL of the image used for the icon. The most common formats used for the icon are `.ico`, `.gif` and `.png`.

```html
<link rel="icon" href="favicon.ico" type="image/x-icon" />
```

`<link>` has accepts `rel` attribute to specify multiple favicon files for different devices and resolutions.

```html
<!-- For Apple devices -->
<link rel="apple-touch-icon" sizes="144x144" href="apple-touch-icon.png" />
<link rel="apple-touch-icon" sizes="114x114" href="apple-touch-icon.png" />
<link rel="apple-touch-icon" href="apple-touch-icon.png" />
<!-- For other devices -->
<link rel="icon" type="image/png" sizes="32x32" href="favicon-32x32.png" />
<link rel="icon" type="image/png" sizes="16x16" href="favicon-16x16.png" />
```

These apple touch icons are used specifically for iOS devices and are displayed when users save a web page to their home screen.

# Applying CSS to HTML

CSS is used to control the presentation and layout of HTML documents. It helps to add colors, fonts and control spacing, borders and more.

It is always recommended to create an external CSS stylesheet with extension `.css` and link it to the HTML document using the `<link>` element in the `<head>` section.

```html
<link rel="stylesheet" href="my-css-file.css" />
```

This `<link>` element accepts a `rel` attribute with value _stylesheet_ to show that it refers to an external CSS file. `href` attribute specifies the relative path to the CSS file.

# Applying JavaScript to HTML

JavaScript helps to add interactivity to a web page. It helps to create interactve elements that respond to a user's actions like clicks, mouse movements etc. and handle the dynamic content.

JavaScript is added to an HTML document using a `<script>` element. A separate JavaScript file with extension `.js` is created and linked via the `src` attribute of this element.

```html
<script src="my-js-file.js" defer></script>
```

This element also goes in the `<head>` section. It should always contain the `defer` attribute which tells the browser to load the JavaScript file only after the page has finished parsing the HTML code. This ensures that all the HTML elements are available before a JavaScript file can make a reference to them, thus avoiding the "element doesn't exist" errors.

# Setting the primary language of the document

The primary language of a web page refers to the main language in which the content of the page is written. It is specified using the `lang` attribute in the `<html>` tag of the HTML document.

```html
<html lang="en">
  …
</html>
```

In the above code, `lang="en"` indicates that the primary language for the document is English. Some other examples are:

- "en" for English
- "fr" for French
- "es" for Spanish
- "de" for German
- "ja" for Japanese
- "zh" for Chinese

If the content of the document includes multiple languages, it is recommended to use the `lang` attribute on `<html>` tag to represent the primary language of the entire document and also specify the language for specific parts of the content using the same attribute on individual elements.

```html
<p>Japanese example: <span lang="ja">ご飯が熱い。</span>.</p>
```

This helps assistive technologies correctly pronounce or translate the content and improves the accuracy of language-specific features in browsers.
