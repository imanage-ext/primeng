
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Join the chat at https://gitter.im/primefaces/primeng](https://badges.gitter.im/primefaces/primeng.svg)](https://gitter.im/primefaces/primeng?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
[![npm version](https://badge.fury.io/js/primeng.svg)](https://badge.fury.io/js/primeng)
[![Build Status](https://travis-ci.org/primefaces/primeng.svg?branch=master)](https://travis-ci.org/primefaces/primeng)

# IM PrimeNG

Forked from PrimeNG UI Components for Angular

See [PrimeNG homepage](http://www.primefaces.org/primeng) for live showcase and documentation.

### Additional Features in this fork

- The autocomplete component allows the user to mouse hover over a suggestion in the dropdown and select it by hitting the Tab key. But this can cause accidental updates when keyboard navigating and the mouse pointer is present where the suggestion dropdown shows. A new input property **highlightOnMouseHover** has now been added to the autocomplete component to disable this behavior. This property is set to true by default and will continue to behave as explained above. But if the developer passes the value false to this property, the mouse hover will continue to highlight the suggestion, but will not select it on hitting Tab.

- When keyboard navigating across multiple autocomplete fields with the dropdown buttons, the tab moves from the input to the dropdown button before navigating to the next autocomplete field. Where there are a large number of these fields, this can result in a tedious amount of tabbing before getting to another field. In order to avoid this, the dropdown button now has tabindex="-1" set on it.

- The autocomplete component has the option to highlight the first item in the suggestions list. This is set by using the input property autoHighlight. But this will always highlight the first suggestion and hence cause the problem of selecting the first item when Tabbing from one field to the other. But at the same time, the user would like this to be enabled in cases where they start typing and only one suggestion is left and want to select it. To allow this, we have added another input property called **autoHighlightOnlySuggestion**. This will only highlight the first suggestion if it is the only one.

- Two new events, **onKeyDown** and **onDropdownKeyDown** have been added to get the keydown events from the input and the dropdown items. This can be used to manipulate those events, prevent propagation of those events etc.

- There are two new Input properties, **headerValue** and **footerValue**. These inputs take string values and if set will show a header and footer item in the dropdown list, respectively.

- Title attributes have been added to the input text and the dropdown list item allowing a tooltip to show on mouse hover. This will be helpful when the value needs to be truncated in the UI.

- Additional Aria attributes have been added to the autocomplete component to enable screen readability of the dropdown list. For proper functioning of this feature, it expects the list items to have a property called 'id'.

### Publishing to NPM

- Make the necesary changes
- Update the version number in package.json
- Run `npm run build-redistribute`
- Run `npm publish`

### About PrimeNG

![alt text](https://www.primefaces.org/wp-content/uploads/2018/05/primeng-sidebar.svg "PrimeNG")

PrimeNG is a collection of rich UI components for Angular. All widgets are open source and free to use under MIT License. PrimeNG is developed by [PrimeTek Informatics](http://www.primetek.com.tr), a vendor with years of expertise in developing open source UI solutions. For project news and updates, please follow us on [twitter](https://twitter.com/prime_ng) and visit our [blog](https://www.primefaces.org/blog).

 - **80+ Components:** The most complete set of native widgets featuring 80+
   easy to use components for all your UI requirements.

- **Open Source:** Hosted at GitHub, all widgets are open source and free to use under MIT license. Feel the power of open source.

- **Productivity:** Allocate your valuable time on business logic rather than dealing with the complex user interface requirements.

- **Themes:** Don't get tied up in just one look&feel. Choose from a variety of options including material and flat design.

- **Templates:** Professionally designed highly customizable native Angular CLI application templates to get started in no time.

- **Mobile:** Enhanced mobile user experience with touch optimized responsive design elements.

---

#### Download

PrimeNG is available at NPM, if you have an existing application run the following command to download it to your project.

```
npm install primeng --save
npm install primeicons --save
```

#### Angular CLI Integration

Add PrimeNG and PrimeIcons as a dependencies.

```
"dependencies": {
  //...
  "primeng": "^7.0.0",
  "primeicons": "^1.0.0"
},
```

Configure required styles at the styles section, example below uses the Nova Light theme.

```
"styles": [
  "node_modules/primeng/resources/themes/nova-light/theme.css",
  "node_modules/primeng/resources/primeng.min.css",
  "node_modules/primeicons/primeicons.css",
  //...
],
```

That is all, you may now import PrimeNG components, for a working example visit the [PrimeNG CLI QuickStart sample](https://github.com/primefaces/primeng-quickstart-cli) at GitHub.
