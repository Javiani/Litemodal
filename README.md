
#★ Lite Modal ★

###✌ A very light-weight, simple to use, state driven dialog Css library ✌


##↳ Motivation

Sometimes you realize that all available modals in the web does not fit in your project, maybe because it doesn't work as you expected or just because it loads a lot of things you don't want.

Lite model was designed to give the simplest form of a modal or, if you prefer, the minimum required code to display a Html/Css dialog.

You can use it just like it is, or adding new features that suits best for you.

##↳ Strategy

Lite Modal rely on `display:inline-block` technic to do the centered positioning of dialog content. It's fluid and works without any calculations, so browser can update positioning on it's own, so it's FAST.

The properties and states of modal should be done by adding to `div.litemodal` new classes such as `loading`, `minimized`, `maximized` and so on. This means that Javascript should be used only to add/remove classes to change modal's presentation.

##↳ Getting Started

1. Download *litemodal.css* or *litemoda.min.css* and set it on your page.
2. Add new Css rules and states to change modal style and state.

##↳  API

### .litemodal{}
It's the dialog container, is used to keep modal states such as `loading`, and it starts with `display:none` by default.

### .litemodal:before{}
It's the overlay of modal, rendered with `:before` pseudo-class in order to save some html code. It is `black` with `0.8` of opacity set by default.

### .litemodal .m-body{}
It's the content of modal, is the centered area of dialog window, it has width set to `40%` and height to `50%` by default, and can be change as you like.

---

###↳ Live Example

Here's just an example of a simple dialog using some Javascript to do the open, loading and closing events. [live demo]().

#### Example HTML
```html
<div class="litemodal">
	<div class="m-body">
		<a href="#/modal-close" class="close">X</a>
		<h2>Yeeey! =)</h2>
	</div>
</div>
```

#### Example Css
```css
.litemodal.open{
	display:block;
}

.litemodal.loading .m-body{
	background-image:url(//www.xiconeditor.com/image/icons/loading.gif);
	background-repeat:no-repeat;
	background-position:right bottom;
}

/*Overlay*/
.litemodal:before{
	background-color:gray;
}

/*Modal document*/
.litemodal .m-body{
	padding:0 10px 10px;
	background:#fff;
}
```
