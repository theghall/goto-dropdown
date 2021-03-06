# goto-dropdown

Goto-dropdown makes dropdown menus appear with a click.  It fallsback to CSS when there is no javascript. The menu is also responsive and will switch to mobile at 550px.

## Install

npm install goto-dropdown

## Usage

In the html please note the `goto-css` class.  When that is present the CSS fallback kicks in; it must be present.  When javascript is running that is replaced with `goto-js`
```html
<nav id="main" class="goto-nav">
  <a class="more-menu" href="#"><img src="assets/graphics/more_25x25.png"></a>
  <ul class="goto-menu goto-font4 goto-css">
    <li><a href="#">Menu1</a>
      <ul class="goto-submenu">
        <li><a href="#">Item1</a></li>
        <li><a href="#">Item2</a></li>
        <li><a href="#">Item3</a></li>
      </ul>
    </li>
    <li><a href="#">Menu2</a>
      <ul class="goto-submenu">
        <li><a href="#">Item1</a></li>
        <li><a href="#">Item2</a></li>
        <li><a href="#">Item3</a></li>
      </ul>
    </li>
  </ul>
</nav>
```

Four fonts come with the CSS that you can use to style your menus:<br>
`goto-font1`: Arial, sans-serif<br>
`goto-font2`: Helvetica, sans-serif<br>
`goto-font3`: "Times New Roman", serif<br>
`goto-font4`: Times, serif<br>


```javascript
require('goto-dropdown/lib/goto-style.css');

require('goto-dropdown/lib/more_25x25.png');

const goto = require('goto-dropdown');

// Trigger could be 'click' or 'mouseover'
// The default value is 'click'
goto.navControl(<trigger>);
```

## Release Notes:
1.1.0 Added Responsive menu<br>
1.0.0 Initial release
