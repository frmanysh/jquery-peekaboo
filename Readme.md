# jquery-peekaboo

  Triggers appear/disappear event on scrolling.

## Installation

```html
<script src="jquery-1.8.0.js"></script>
<script src="jquery-peekaboo.js"></script>
```

## Usage

```javascript
jQuery(function() {

  /**
   * Take appear or disappear callbacks.
   */

  $('.boxes').peekaboo(function() {
    // on appear callback
    console.log('boo!');
  }, function() {
    // on disappear callback
    console.log('peek-a...');
  });
 
  /**
   * Or trigger them with offset option.
   */
    
  $('.boxes').peekaboo({
    onAppear: function() { ... },
    onDisappear: function() { ... }.
    offset: 200 // offset from the top/bottom of the window
  });
 
  /**
   * peekaboo triggers appear or disappear events.
   */
  
  $('.boxes').on('appear disappear', function(e) {
    console.log(this, $(this).data('pkb-state'));
  });
});
```

See [example](http://uniba.jp/jquery-peekaboo/examples/).

## Authors

  - Seiya Konno &lt;seiya@uniba.jp&gt; ([nulltask](https://github.com/nulltask))

## License

(The MIT License)

Copyright (c) 2012 Uniba Inc. &lt;info@uniba.jp&gt;

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
'Software'), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
