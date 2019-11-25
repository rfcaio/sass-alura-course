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
