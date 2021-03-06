Human CSS Numbers
======

Human CSS Numbers is a set of CSS micro-attributes for specifying numbers of lengths in human-friendly form.
It is a sister package to `human-css-colors` and `human-css-classes` and is used by the latter.

Summary
-------

`human-css-numbers` is a set of attributes for specifying numbers of lengths,
designed for use in micro-class frameworks such as `human-css-classes`.

It exposes two CSS variables: `--number` and `--length` which you can use in your own CSS micro-attribute or micro-class rules.

It allows numbers to be specified using English words such as "two",
or Arabic numerals such as "2",
and percents as in "ten percent" or "half width",
and fractions such as "1/2".
and lengths as in "five rem".

### Caveat

`human-css-numbers` uses CSS custom properties, also known as CSS variables, in its implementation.
This excludes IE11 from consideration.

### Units and measures

Many micro-class frameworks suffer from a proliferation of classes such as `width-75`.
This limits the user to only the classes the designer provides.
In contrast, we provide individual micro-attributes for numbers, lengths, and units,
so we can write

```
<div 50% width>
<div two rem border>
<div three columns>
```

THe special keyword `size` indicates a ratio to a current size of 100%.
For instance, the following might specify a `flex-basis` of one-third the screen width:

```
<div flex>
  <div basis one third size>
```

All standard CSS units are provided as micro-attributes.
including lengths such as `px`, `em`, and `rem`.
Common numbers and percentages may also be used as micro-attributes,
in addition to built-in classes such as `1/2`.

Installation
------------

    npm install --save-dev @rtm/human-css-numbers
    yarn add @rtm/human-css-numbers

Then, in some file that a CSS pre-processor will process:

    @import "@rtm/human-css-numbers";
