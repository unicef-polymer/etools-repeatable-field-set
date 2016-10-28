# \<etools-repetable-field-set\>

A container that helps to display repeatable data sets with counters and options to manage data: add, modify, delete(with confirmation), copy.

### Element properties

* allowCopy - Boolean, default: false
* deleteConfirmationMessage - String, default: Are you sure you want to delete this item?
* deleteConfirmationTitle - String, default: Delete confirmation
* elevation - Number, default: 0
* hidePlus - Boolean, default: false
* hideVerticalDivider - Boolean, default: false
* model - Array, default: [] – notifies
* open - Boolean, default: true
* showCounter - Boolean, default: false
* showHeader - Boolean, default: true
* title - String

## Usage

Examples: 

```html
<etools-repeatable-field-set 
    title="Repeatable field title" 
    model="{{fieldSets}}" 
    elevation="0" 
    hide-plus
    show-counter>
    
    <!-- A repeater that will display your fields as you want -->
    <template is="dom-repeat" items="[[fieldSets]]">
      <div class="layout horizontal flex wrap">
        <paper-input label="First Name" value="{{item.firstName}}"></paper-input>
        <paper-input label="Last Name" value="{{item.lastName}}"></paper-input>
      </div>
    </template>
    
</etools-repeatable-field-set>

<etools-repeatable-field-set 
  title="Repeatable field title" 
  model="{{fieldSets}}" 
  elevation="4" 
  hide-plus 
  hide-vertical-divider>
  
  <!-- A repeater that will display your fields as you want -->
  <template is="dom-repeat" items="[[fieldSets]]"> ... </template>
  
</etools-repeatable-field-set>
  
<etools-repeatable-field-set 
  title="Repeatable field title" 
  model="{{fieldSets}}" 
  elevation="2" 
  allow-copy>
  
  <!-- A repeater that will display your fields as you want -->
  <template is="dom-repeat" items="[[fieldSets]]"> ... </template>
    
</etools-repeatable-field-set>
  
<etools-repeatable-field-set 
  title="Repeatable field title" 
  model="{{fieldSets}}" 
  elevation="2" 
  show-counter
  allow-copy>
  
  <!-- A repeater that will display your fields as you want -->
   <template is="dom-repeat" items="[[fieldSets]]"> ... </template>
    
</etools-repeatable-field-set>
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

```bash
$ bower install --save etools-repeatable-field-set
```

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