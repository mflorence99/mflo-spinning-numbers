# Polymer Component: Calculator-like Display Animated with Spinning Numbers

```mflo-spinning-numbers``` is a Polymer component that displays an integer number,
calculator-fashion and with a spinning animation effect as if the value
represent was being calculated in the background. It was inspired by [Harry's]
(http://stackoverflow.com/users/2606013/harry) excellent response to a recent
[stack*overflow*](http://stackoverflow.com/questions/27956723/css-animation-number-increment-effect)
question.

| Link |  |
|---|---|
| [Demo](http://mflo-spinning-numbers.surge.sh/demo.html) | For an interactive demo |
| [Test](http://mflo-spinning-numbers.surge.sh/test.html) | To run the unit tests |
| [Docs](http://mflo.io/mflo-polymer-components/jsdoc/mflo-spinning-numbers/0.0.1/index.html) | For the generated JSDocs |
| [Info](http://mflo.io/mflo-polymer-components/) | For more information on my Polymer components |
| Install | ```bower install --save mflo-spinning-numbers``` |


## How to Use

The component contains a single, read/write ```value``` property which optionally can be set initially:
 
```html
  <mflo-spinning-numbers value="1234">
  </mflo-spinning-numbers>
```

Additionally, ```value``` can be set programmatically:

```javascript
  var spinner = document.querySelector("mflo-spinning-numbers#the-right-one");
  spinner.value = 1234;
```

The animation effect is triggered whenever ```value``` is set. If no ```value``` is set initially, 
the component displays as blank.


## How to Style

> TODO: I'm using LESS to build the stylesheet and it chokes on the ```@apply()``` custom CSS
mixin. So temporarily I am exposing stylable CSS properties individually.

The options for styling are best shown by example. Here I style the numbers as green on a
black background:

```css
  mflo-spinning-numbers {
    --mflo-spinning-numbers-background-color: black;
    --mflo-spinning-numbers-color: lightgreen;
    --mflo-spinning-numbers-display: inline-block;
    --mflo-spinning-numbers-font-size: 32px;
    --mflo-spinning-numbers-min-width: 280px;
  }
```

These are the default values:

```css
  :host {
    background-color: var(--mflo-spinning-numbers-background-color, white);
    color: var(--mflo-spinning-numbers-color, black);
    display: var(--mflo-spinning-numbers-display, block);
    font-size: var(--mflo-spinning-numbers-font-size, 16px);
    min-width: var(--mflo-spinning-numbers-min-width, 0);
  }
```


## Limitations

Currently, only integers can be shown. A ```value``` is stripped of all characters other
than ```[0-9]``` as it is applied.



## Author

Mark Florence (mflo999@gmail.com).


## MIT License

&copy; 2015 Mark Florence <mflo999@gmail.com>

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


## Resources

- Visit the [author website](http://mflo.io).
- Follow [@mflo999](https://twitter.com/#!/mflo999) on Twitter for updates.