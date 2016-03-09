# l10n-behavior

Polymer.l10nBehavior provides a normalized interface to localize strings.

Based on the [ECMAScript Internationalization API Specification](http://ecma-international.org/ecma-402/1.0/)


## Work in progress


## Usage

1) Add Polymer.l10nBehavior to the behaviors list in the JS file or script of your component:

```js
behaviors: [Polymer.l10nBehavior]
```

2) Import the behavior in your HTML:

```html
<link rel="import" href="../l10n-behavior/l10n-behavior.html">
```

To locate a value, just do the following:
```html
{{locale('value', lang)}}
```

You can override in your component the options to set to the localize function. These options are based on the ECMAScript Internationalization API Specfication. 

### Example

```html
  <template>
    <p>{{localize(12, 'en')}}</p>
  </template>
  ...
  Polymer({
    is: 'my-element',
    properties:{
      optionsL10n:{
        value: function(){
          return { style: 'currency', currency: 'USD' };
        }
      }
    },
    behaviors: [
      Polymer.l10nBehavior
    ]

  });
  ...
```



