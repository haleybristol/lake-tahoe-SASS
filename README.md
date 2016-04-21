#Lake Tahoe Landing Page

####By Haley Bristol

##Description
This is a web application developed for a CSS course at epicodus code school. 

##Technologies
HTML<br>
CSS<br>
Sass

## Setup Requirements for Sass

Sass can be used from the command line
or as part of a web framework.
The first step is to install the gem:

    gem install sass

After you convert some CSS to Sass, you can run

    sass style.scss

to compile it back to CSS.
For more information on these commands, check out

    sass --help

To install Sass in Rails 2,
just add `config.gem "sass"` to `config/environment.rb`.
In Rails 3, add `gem "sass"` to your Gemfile instead.
`.sass` or `.scss` files should be placed in `public/stylesheets/sass`,
where they'll be automatically compiled
to corresponding CSS files in `public/stylesheets` when needed
(the Sass template directory is customizable...
see [the Sass reference](http://sass-lang.com/docs/yardoc/file.SASS_REFERENCE.html#template_location-option) for details).

Sass can also be used with any Rack-enabled web framework.
To do so, just add

```ruby
require 'sass/plugin/rack'
use Sass::Plugin::Rack
```

to `config.ru`.
Then any Sass files in `public/stylesheets/sass`
will be compiled into CSS files in `public/stylesheets` on every request.

To use Sass programmatically,
check out the [YARD documentation](http://sass-lang.com/documentation/file.SASS_REFERENCE.html#using_sass).

## Formatting

Sass is an extension of CSS
that adds power and elegance to the basic language.
It allows you to use [variables][vars], [nested rules][nested],
[mixins][mixins], [inline imports][imports],
and more, all with a fully CSS-compatible syntax.
Sass helps keep large stylesheets well-organized,
and get small stylesheets up and running quickly,
particularly with the help of
[the Compass style library](http://compass-style.org).

[vars]:    http://sass-lang.com/documentation/file.SASS_REFERENCE.html#variables_
[nested]:  http://sass-lang.com/documentation/file.SASS_REFERENCE.html#nested_rules
[mixins]:  http://sass-lang.com/documentation/file.SASS_REFERENCE.html#mixins
[imports]: http://sass-lang.com/documentation/file.SASS_REFERENCE.html#import

Sass has two syntaxes.
The one presented here, known as "SCSS" (for "Sassy CSS"),
is fully CSS-compatible.
The other (older) syntax, known as the indented syntax or just "Sass",
is whitespace-sensitive and indentation-based.
For more information, see the [reference documentation][syntax].

[syntax]: http://sass-lang.com/documentation/file.SASS_REFERENCE.html#syntax

To run the following examples and see the CSS they produce,
put them in a file called `test.scss` and run `sass test.scss`.

### Nesting

Sass avoids repetition by nesting selectors within one another.
The same thing works for properties.

```scss
table.hl {
  margin: 2em 0;
  td.ln { text-align: right; }
}

li {
  font: {
    family: serif;
    weight: bold;
    size: 1.2em;
  }
}
```

### Variables

Use the same color all over the place?
Need to do some math with height and width and text size?
Sass supports variables, math operations, and many useful functions.

```scss
$blue: #3bbfce;
$margin: 16px;

.content_navigation {
  border-color: $blue;
  color: darken($blue, 10%);
}

.border {
  padding: $margin / 2;
  margin: $margin / 2;
  border-color: $blue;
}
```

### Mixins

Even more powerful than variables,
mixins allow you to re-use whole chunks of CSS,
properties or selectors.
You can even give them arguments. 

```scss
@mixin table-scaffolding {
  th {
    text-align: center;
    font-weight: bold;
  }
  td, th { padding: 2px; }
}

@mixin left($dist) {
  float: left;
  margin-left: $dist;
}

#data {
  @include left(10px);
  @include table-scaffolding;
}
```

### License

The MIT License (MIT)

Copyright (c) [2016] [Haley Bristol]

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

Copyright (c) 2016 Haley Bristol
