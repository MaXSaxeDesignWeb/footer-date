# footer-date.js

Month and Year in Footer with disappearing JS

## footer.html

```html
<footer class="container" id="footer">
    <script src="http://cdn.mf/date.js/footer-date.js"></script>
</footer>
```

## footer-date.js

```javascript
var d = new Date();
var y = 0;
var year = d.getFullYear().toString();
var m = ["January", "February", "March", "April", "May", "June", "July", "August", "September", "October", "November", "December"]
var month = m[d.getMonth()];
var footer = "";
var footer0 = "MaX Falstein gTLD &copy; MaX Falstein and Falstein Inc. &#8212; ";
var footer1 = " ";
var footer2 = " &#8212; Patents and Trademarks Pending";
footer = footer0.concat(month.concat(footer1.concat(year.concat(footer2))));
document.getElementById("footer").innerHTML = footer;
```

## Operations

The appending of `footer` to the inner HTML of the fooer using `document.getElementById("footer").innerHTML` repleaces `<script src="http://cdn.mf/date.js/footer-date.js"></script>` with
`MaX Falstein gTLD &copy; MaX Falstein and Falstein Inc. &#8212; January 2018 &#8212; Patents and Trademarks Pending` giving the impression when inspecting the source the footer is not procedurally generated unless viewing the sources and network tabs in developer tools in most browsers.
