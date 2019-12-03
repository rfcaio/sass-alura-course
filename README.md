# About

> Code examples based on Alura's Sass course.

## Examples

**Variables**

An example on how to create a variable and how you should use it:

```scss
$default-color: #096;

.app-header {
  background-color: $default-color;
}
```

**Mixins**

An example on how to create a mixin and how you should use it:

```scss
@mixin rounded-border {
  -webkit-border-radius: .3em;
          border-radius: .3em;
}

.btn-rounded {
  @include rounded-border;
}
```

An example on how you can set parameters in mixins:

```scss
@mixin rounded-border($radius: .3em) {
  -webkit-border-radius: $radius;
          border-radius: $radius;
}

.btn-rounded {
  @include rounded-border;
}

.panel-rounded {
  @include rounded-border(4px);
}
```

**Comments**

An example on how to create a comment and how you should use it:

```scss
// a simple comment in sass
$default-color: #096;
```

**Nesting**

An example on how to nesting CSS selectors:

```scss
.panel {
  color: #bbb;

  h4 {
    font-size: 1.6rem;
  }

  a {
    text-decoration: none;

    &:hover {
      text-decoration: underline;
    }
  }
}
```

**Import**

An example on how to import Sass files (the extension `.scss` is optional). `CSS` files can be imported as well:

```scss
@import 'normalize.css';

@import 'mixin.scss';

// or

@import 'mixin';
```

**Color functions**

An example on how to use Sass color functions:

```scss
body {
  background-color: darken(cyan, 10);
  color: lighten(gold, 25);
}
```

**Placeholders**

An example on how to create a placeholder and how you should use it:

```scss
%default-border {
  border: .25rem solid #bbb;
}

.btn {
  .btn-default {
    @extend %default-border;
    background-color: #fff;
  }
}
```

**Media queries**

An example on how to create a media query inside a CSS selector:

```scss
.panel {
  width: 100%;

  h1 {
    font-size: 5rem;
  }

  @media(max-width: 768px) {
    width: 96%;

    h1 {
      font-size: 2.5rem;
    }
  }
}
```

An example on how you can use a media query as a variable:

```scss
$medium: '(max-width: 768px)';

.menu {
  width: 50%;

  @media #{$medium} {
    width: 100%;
  }
}
```
