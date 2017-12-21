# A peek behind the "link". The web's superpower
## The link is born
If the web is essentially a way of exchange text why is it better than books? In the previous section we hinted that respect to the book, the web has a few additional superpowers.

What working at European Organization for Nuclear Research (CERN), [Tim Bernes Lee](https://en.wikipedia.org/wiki/Tim_Berners-Lee) submitted a proposal to improve how CERN organized its vast amount of information. Tim Bernes Lee also noted that his proposal could be used by others since they will soon face similar challenges.

A foundational aspect of Tim Bernes Lee's proposal was to organically relate (link) information, allowing each piece of information to reference one another without the constraint of a hierarchical structure. This is the insight Tim Bernes Lee had while working at CERN and it's one of the key tenets of the web.

## A blueprint for implementing links
How can text reference other text? Let's daydream and pretend we are designing the web and Wikipedia at the same time. We have two independent pieces of content.

```
Socrates bio
Socrates was a classical Greek philosopher credited as one of the founders of Western philosophy and is known as the first moral philosopher...

Plato bio
...
Along with his teacher, Socrates (we would like to reference the `Socrates bio` here)...
```

How can `Plato's bio` reference `Socrates bio`? What does it mean to reference another piece of information?

We essentially want to state that a certain piece of information is related to another piece of information. We are annotating data with metadata. Metadata is data which describes other data. If my driver license is a piece of data that fact that it's released by the state of New York is metadata about my license, it provides information about my license.

Our annotation should state that the annotated data references external data (it’s a  `link`) and that this specific occurrence of a `link` points to a specific occurrence information.

## How Tim Bernes Lee solved the problem
Tim Bernes Lee developed an annotation language named Hypertext Markup Language (HTML). This language allows us to annotate (markup in HTML parlance) information.

HTML is a language to define and describe data. HTML provides a number of build in content classifications (different types of data) which are expressed using tags. Each tag broadly defines the marked-up content. Tags then have attributes which further describe the specific occurrence of a tag (a type of data).

Anatomy of an HTML tag
```html
<opening tag content-attribute=attribute value>
    Content
</closing tag>
```

In our case, we wanted to describe a link between two pieces of information. If were to Google [how to define a link with html]()
![](https://curriculum-content.s3.amazonaws.com/web-development/how-to-define-a-link-with-html.jpeg)

Google did a great job with this query. From the top result snippet, we learn that:

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

We just used HTML to build a link and express one of the most fundamental features of the web. The ability to relate information to one another. 

This simply pattern applies to all HTML elements.

1. Tag to classify the type of data
2. Attributes to describe the specific occurrence of an HTML element
