# A Peek Behind the "Link", the Web's Superpower

## The Link Is Born

If the web is essentially a way to exchange text, how is it better than books?
In addition to being freely accessible and distributable for virtually no cost,
texts created on the web can refer to one another, a process that's so common
we might miss how special it is. On the Web, HTML documents can organically
relate (link) to one another, allowing pieces of information to reference one
another without the constraint of a hierarchical structure.

This idea was discovered by [Tim Berners-Lee][TBL] while he was working at
European Organization for Nuclear Research (CERN).

## A Blueprint for Implementing Links

How can text reference other text? Let's daydream and pretend we are designing
the web and Wikipedia at the same time. We have two independent pieces of
content.

```
Socrates bio

Socrates was a classical Greek philosopher credited as one of the founders of
Western philosophy and is known as the first moral philosopher...

Plato bio
...
Along with his teacher, Socrates (we would like to reference the `Socrates bio` here)...
```

How can `Plato's bio` reference `Socrates bio`? What does it mean to reference
another piece of information?

We essentially want to state that a certain piece of information is related to
another piece of information. We are annotating data with metadata. Metadata is
data which describes other data. If my driver license is a piece of data the
fact that it's released by the state of New York is metadata about my license,
it provides information about my license.

Our annotation should state that the annotated data references external data
(it’s a  `link`) and that this specific occurrence of a `link` points to a
specific occurrence of information.

## How Tim Bernes Lee solved the problem

Tim Bernes Lee developed an annotation language named Hypertext Markup Language
(HTML). This language allows us to annotate (markup in HTML parlance)
information.

HTML is a language to define and describe data. HTML provides a number of
built-in content classifications (different types of data) which are expressed
using tags. Each tag broadly defines the marked-up content. Tags then have
attributes which further describe the specific occurrence of a tag (a type of
data).

Anatomy of an HTML tag:

```html
<opening tag content-attribute=attribute value>
    Content
</closing tag> <!-- its a closing tag because the tag name begins with a '/'. By the way, this is an HTML comment -->
```

In our case, we want to describe a link between two pieces of information. If
were to Google [how to define a link with html]()

![](https://curriculum-content.s3.amazonaws.com/web-development/how-to-define-a-link-with-html.jpeg)

Google did a great job with this query. From the top result snippet, we learn
that:

1. Use the `<a>` tag (a type of element) to define a link.
2. Use the `href` attribute to state where the external data is located.

With these instructions, we can translate our generic tag into an `<a>` tag. 

```html
<!-- These are comments  -->
<!-- Generic tag -->
<opening tag content-attribute=attribute value>
    Content
</closing tag>

<!-- Actual link tag -->
<a href='https://en.wikipedia.org/wiki/Socrates'>
    Socrates
</a>
```

We just used HTML to build a link and express one of the most fundamental
features of the web. The ability to relate information to one another. 

This simple pattern applies to all HTML elements.

1. Tags classify the type of data
2. Attributes describe the specific occurrence of an HTML element

[TBL]: https://en.wikipedia.org/wiki/Tim_Berners-Lee
