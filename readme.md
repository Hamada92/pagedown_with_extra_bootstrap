#Overview
I needed pagedown converter and pagedown extra to work together, unfortunately pagedown extra is not an NPM package, this is where this package comes in. It bundles the pagedown converter, editor, sanitizer and extra in one NPM package.

## Usage
```
yarn add pagedown-with-extra-bootstrap
```

or 

```
npm i pagedown-with-extra-bootstrap
```

If you're using es6, you can do :

```javascript
import Markdown from 'pagedown-with-extra-bootstrap/pagedown.js';

export default function initiate_editor(){
  $('textarea.wmd-input').each(function(i, input) {
    var attr, converter, editor;
    attr = $(input).attr('id').split('wmd-input')[1];
    converter = new Markdown.Converter();
    Markdown.Extra.init(converter, {highlighter: "highlight"});
    editor = new Markdown.Editor(converter, attr);
    return editor.run();
  });
```

