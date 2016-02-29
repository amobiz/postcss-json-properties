# postcss-json-properties
PostCSS plugin that read json file to css custom properties.

## Motivation

Sometimes you need share settings between JavaScript and CSS.

## Proposal

Read in a json file:

```js
{
	"maxWidth": "1024px",
	"primaryColor": "#1f587a",
	"bgColor": "#efefef",
	"darkBgColor": "#263238",
	"logo": {
		"img": "/assets/logo.png"
	}
}
```

Into:

```css
:root {
	--maxWidth: 1024px;
	--primaryColor: #1f587a;
	--bgColor: #efefef;
	--darkBgColor: #263238;
	--logo-img: "/assets/logo.png";
}
```

Use:

```css
@import "constants.json";

.logo {
  background-image: url(var(--logo-img));
}
```

## Contribute
If you found this might be useful or got some ideas, please leave a comment in this [issue](https://github.com/amobiz/postcss-json-properties/issues/1).

## License
MIT

## Author

[Amobiz](https://github.com/amobiz)
