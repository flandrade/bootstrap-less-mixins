# Bootstrap as a Less Mixin Library

This is a project setup to use Bootstrap as a Less mixin library. 

## Why?

Bootstrap doesn't encourage semantic markup. Instead, the framework encourges to 
include Bootstrap-specific attributes to the markup and, therefore, we use HTML
for design, not structure.  

We can use Bootstrap whilst maintaining semantic HTML markup by using the Less 
mixins. This way, we'll decouple the markup from the CSS framework.

## Example 

We can go from this: 

```html
<div class='row section'>
  <div class='col-xs-12 col-sm-5 col-md-3 article'>
    Content
  </div>
</div>
````

To this: 

```html
<section>
  <article>
    Content
  </article>
</section>
```

With the following style: 

```less
section {
  .make-row();
  article {
    .make-xs-column(12);
    .make-sm-column(5);
    .make-md-column(3);
  }
}
```

## Some available mixins

```
container-fixed()
make-row()
make-xs-column()
make-xs-column-offset()
make-xs-column-push()
make-xs-column-pull()
make-sm-column-offset()
make-sm-column-push()
make-sm-column-pull()
make-md-column-offset()
make-md-column-push()
make-md-column-pull()
make-lg-column-offset()
make-lg-column-push()
make-lg-column-pull()
clearfix()
```

## Recommended reading

[Meaningful CSS](http://alistapart.com/article/meaningful-css-style-like-you-mean-it). 