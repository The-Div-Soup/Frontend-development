# What is Hyperlink?

Hyperlink is one of the most important and innovative feature that web has offer.

Hyperlinks allow us to link the documents to other documents or resources, link the specific part of documents such as images, files, link of other web-page etc.

# How it works?

We can create a link by wrapping it inside `<a>` element which is also knows as anchor tag with `href` attribute, also known as Hypertext Refrence that contains the web address.

```html
<a href="https://www.google.com">Google home page</a>
```

Here we can see, `Google home page` turns into link.

There are various other _attributes_ are available in HTML.

```html
src - It uses in `<img>` tag that apecifies the path of the image.
style - It used to add styles to an element such as color, size, font etc.
target - It used to open the link to the new web-page.
title - It used to defind some additional information about the element.
alt - Alt attribute provides alternative text for an image element.
```

## Block level links

A block-level link in HTML is a link (`<a>` tag) that can include other elements like headings, images, or paragraphs inside it. This makes the entire block clickable.

If you want to make a heading element a link then wrap it in an anchor `<a>` element.

```html
<a href="https://google.com">
    <h2>Go to Google home page</h2>
</a>
```
## Image links

Image link in HTML is when you want to make image into link than wrap the `<img>` element and refrenced file into `<a>` element.

```html
<a href="https://www.google.com">
    <img src="intro-to-HTML.png" alt="Description of image">
</a>
```

# Working of URLs and paths

To understand how _link targets_ work, it's important to know about URLs and file paths. This section explains these concepts.

A URL (Uniform Resource Locator) is a text-based address that specifies the location of a resource on the web. for example Wikipedia's english homepage is located at `https://en.wikipedia.org/wiki/Main_Page`.

## Structure of URL

`https://en.wikipedia.org/wiki/Main_Page`

URL use paths to find files. A path specifies where the resource is located on the web. It can be absolute or relative.

```part_explained
Schema (Protocol): The scheme specifies the method used to access the resource(e.g., http, https, ftp).
Domain (Hostname): The domain is the unique name of the website or server where the resource is hosted (e.g., www.wikipedia.org).
Path: The path indicates the specific location of a resource on the serve (e.g., /wiki/Main_Page).
Query (Optional): The query contains extra information sent to the server, often used for searching or filtering (e.g., ?id=123).
```

## Creating hyperlink locally

_image-link_

The **root** of the directory structure is `Creating-Hyperlink`. When you work locall with the website, there is a root directory that contains the entire site. Inside the root directory, there is an `index.html` file that is our home page or landing page.

There is one more file inside the root directory called `projects`. There is a single file inside the project file is also called `index.html`. Tis index.html will be the landing page for project directory.

- Working in same directory
  
If you want to include hyperlink inside the root directory than you have to specify **top-level** index.html file.

```html
<p>
    You are working within the root directory!
    <a href="index.html">Root Directory</a>
</P>
```

- Working in sub-directory
  
If you want to include hyperline inside the `index.html` pointing to `projects/index.html`, you need to go down into **projects directory** and then you can access index.html file.

```html
<p>
    You are working within the projects directory!
    <a href="projects/index.html">Projects Directory</a>
</P>
```
# Best link practics

There are some best link practics you need to follow when you writing links.

- Meaningful link phrases
  
It's not enough to just slap links on a page. We need to prioritize accessibility for all users. Screen reader users need clear, concise link text to navigate efficiently. Search engines rely on descriptive link text for indexing, while visual readers use it to quickly understand the page's content.

## Good link practics

```html
<p><a href="https://www.mozilla.org/en-US/firefox/">Download Firefox</a></p>
```

## Bad link practics

```html
<p>
  <a href="https://www.mozilla.org/en-US/firefox/">Click here</a> to download
  Firefox
</p>
```

- When linking to a downloadable file, ensure the download attribute is included in the anchor tag
  
When linking to a downloadable resource, you can use the `download` attribute to provide a default save filename.

 ```html 
<p>
  <a href="https://www.example.com/large-report.pdf">
    Download the sales report (PDF, 10MB)
  </a>
</p>
```

# Email links

It is feasible to generate hyperlinks or buttons that, upon activation, initiate a new outbound email message instead of directing the user to a specific resource or webpage. This is done using the `<a>` element and the `mailto:` URL scheme.

```html
<a href="mailto:recipient@example.com">Contact Us</a>
```
This will display "Contact Us" as a clickable link.

- Specifying details

In additional, You can add a subject, message, and other information to the email.

## Here's an example of adding some information

```html
<a href="mailto:recipient@example.com?subject=Your%20Inquiry&body=Please%20provide%20more%20details">Send Inquiry</a>
```
