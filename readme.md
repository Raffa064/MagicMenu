# About
I made this to learn more of css after see a [video](https://youtu.be/ArTVfdHOB-M), i tried to no copy the max of code that i can, so my code is my own version.

# How to use
For use thie magic menu on your project, you can copy this [css file](https://github.com/Raffa064/MagicMenu/menu.css), change the variables in the :root selector and add this html code on your body:

```html
<div class="magic-menu" --type="footer">
    <!--I maked the --type to alow to create left/right menus, bud i will not implement it.-->
    <ul class="options">
        <!--OPTIONS-->
    </ul>
</div>
```

The option need to have this format:

```html
<li class="opt">
<span class="opt-icon" style="--accent: <OPTION BACKGROUND>; --accent-dark: <OPTION ICON COLOR (if supported my your icon provider...)>;"><!--The option icon--></span>
    <span class="opt-title"><!--Your option title--></span>
</li>
```

Finally you will need to add this script:
```javascript
var options = document.querySelectorAll('.opt')
function setOption() {
    options.forEach((item) => item.classList.remove('active'))
    this.classList.add('active')
}
options.forEach((item) => item.addEventListener('click', setOption))
```