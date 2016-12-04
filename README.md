Adapt
===

> Sweet responsive extends

## Why?
+ Content that is easily extendable across at-rules
+ Programmatically extend content without interpolation

## Getting Started
+ Install with Bower
+ Import dependencies

```
$ bower install --save taffy-adapt
```

```scss
@import 'bower_components/fizz-sass/scss/main';
@import 'bower_components/taffy-adapt/scss/main';
```

## Adapt
+ Helps extending your placeholders

#### Using adapt
Simplify the adapt mixin by wrapping it with your own.

```scss
@mixin foobar($variants) {
  @include adapt('foobar', $variants);
}
```

Now you can use your mixin.

```scss
.foobar {
  @include foobar((1 baz) (2 baz));
}
```

## Loop
+ Helps generate your placeholders
+ Uses `$adapt-loop` global variable to set the scope for each placeholder

#### Using loop
The loop mixin accepts one argument that sets how many times it loops.

```scss
@include adapt-loop(2) {
  %foobar-#{$adapt-loop}-baz {
    // ...
  }

  %foobar-#{$adapt-loop}-qux {
    // ...
  }
}
```
