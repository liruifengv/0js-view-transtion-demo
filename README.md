# Zero JS view transitions in MPA

Chrome 126 supports “cross-document view transitions”.

[Demo is here 🚀](https://0js-view-transition.zeabur.app/blog)

To enable it, you only need to add a `@view-transition` to your website style:

```css
<style>
  @view-transition {
    navigation: auto; /* enabled! */
  }
</style>
```

Then, add same `view-transition-name` style to elements you want to animate:

```astro
// list.astro
<a href="/detail" style={{ "view-transition-name": slug }}>list item title</a>
```

```astro
// detail.astro
<div style={{ "view-transition-name": slug }}>detail Title</a>
```

It works!
