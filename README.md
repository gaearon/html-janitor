html-janitor
============

Sanitises HTML.

Uses UMD for support in AMD and Common JS environments.

## Installation

```
bower install html-janitor
# or
npm install html-janitor
```

## Usage

```javascript
require(['html-janitor'], function (HTMLJanitor) {
  var div = document.querySelector('.myDiv');
  var janitor = new HTMLJanitor({
    // Only listed tags will be allowed
    tags: {
      // Allow any href and target="_blank" on <a>:
      a: { href: true, target: '_blank' },
      // Rewrite h2 to h1:
      h2: 'h1'
    }
  });
  console.log(janitor.clean(div.outerHTML));
});
```