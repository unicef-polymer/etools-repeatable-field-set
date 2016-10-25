# \<etools-repetable-field-set\>

A container that helps to display repeatable data sets with counters and options to manage data: add, modify, delete(with confirmation), copy.

The development for this element it's on hold for now because of compatibility issues on IE11 and Edge browsers.

You can still use it and customize it or reuse it's functionality as you need in your app. 

## Usage

First you need to add this element to your app, edit `etools-repeatable-field-set.html` and add your data model fields
in the div with `class="item-content"` by replacing
```html
 `<slot name="data-row-[[index]]"></slot>
```
with your content fields.


Then use it like this:

```html
<etools-repeatable-field-set 
    title="Repeatable field title" 
    model="{{fieldSets}}" 
    elevation="0" 
    hide-plus
    show-counter></etools-repeatable-field-set>

<etools-repeatable-field-set 
  title="Repeatable field title" 
  model="{{fieldSets}}" 
  elevation="4" 
  hide-plus 
  hide-vertical-divider></etools-repeatable-field-set>
  
<etools-repeatable-field-set 
  title="Repeatable field title" 
  model="{{fieldSets}}" 
  elevation="2" 
  allow-copy></etools-repeatable-field-set>
  
<etools-repeatable-field-set 
  title="Repeatable field title" 
  model="{{fieldSets}}" 
  elevation="2" 
  show-counter
  allow-copy></etools-repeatable-field-set>
``` 

## Styling

Use this css variables and mixins to style this element.

Custom property | Description | Default
----------------|-------------|----------
`--repeatable-items-header-bg` | Header background | `#1e86bf`
`--repeatable-items-add-btn-bg` | Add new set/row of data button bg color | `#8dc63f`
`--repeatable-items-title` | Mixin applied to header(title bar) | `{}`
`--repeatable-items-element-container` | Mixin applied to element container | `{}`
`--repeatable-items-collapse-container` | Mixin applied to collapsible container | `{}`
`--repeatable-items-item-container` | Mixin applied to each item/row | `{}`
`--repeatable-items-item-content` | Mixin applied to each item data fields(right side of delete and copy buttons) | {}
`--repeatable-items-item-content-with-counter` | Same as `--repeatable-items-item-content` but in case counters are active | `{}`
`--repeatable-items-vertical-divider` | Mixin applied to vertical divider between actions and data content | `{}`
`--repeatable-items-vertical-divider-bgcolor` | Vertical divider color | `#9e9e9e`
`--repeatable-items-counter-badge` | Mixin applied to counter badge | `{}`
`--repeatable-items-action-btn` | Mixin applied to action buttons (delete and copy) | `{}`
`--repeatable-items-delete-btn-color` | Delete button color | `ea4022`
`--repeatable-items-copy-btn-color` | Copy button color | `#757575`
`--repeatable-items-lone-vertical-divider` | Mixin applied if to divider bar in case action buttons are not displayed | `{}`


## Install

Bower package not available.
Download the source code or clone the repository and add it to your app.

## Preview element locally

Install needed dependencies by running: `$ bower install`.
Make sure you have the [Polymer CLI](https://www.npmjs.com/package/polymer-cli) installed. Then run `$ polymer serve` to serve your element application locally.

## Running Tests

You need to have `web-component-tester` installed (if not run `npm install -g web-component-tester`)
```bash
$ wtc
```
or 
```bash
$ wtc -p
```