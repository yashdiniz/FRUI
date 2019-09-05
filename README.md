# FRUI framework

Flat & Round User Interface(FRUI)(pronounced froo-ey) is a new lightweight CSS framework. Inspired by [Material UI](https://material.io) but less _materialistic_, this is a venture into building basic UI frameworks with a minimalistic and professional look.

Designed to be a lightweight, minimalistic, and developer-friendly framework, the focus shall be mainly on the following:
+ Using a separate namespace(prefix frui-* for all CSS classes) to stay flexible.
+ Reducing external dependencies.
+ Small file sizes.
+ Cross platform.
+ Easy to hack and customise.

FRUI is simple and minimalistic, and is quick to learn for somebody who already has previous experience in a framework like [Bootstrap](https://getbootstrap.com/) or [MUI](https://www.muicss.com/). This README will introduce you to the basics of the FRUI framework.

>NOTE: This work is currently under NO LICENSE, and so the author Reserves All Rights.(check [LICENSE.md](/yashdiniz/FRUI/blob/master/LICENSE.md))

## Boilerplate code

FRUI already includes [normalize.css](https://necolas.github.io/normalize.css/) which means you may keep this as the base CSS file.

```html
<!doctype html>
<html>
  <head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>Boilerplate code</title>
    <!-- load FRUI -->
    <link href="css/frui.css" rel="stylesheet" type="text/css" />
    <!-- load custom font -->
    <link href="//fonts.googleapis.com/css?family=Roboto:300,400,500,700" rel="stylesheet" type="text/css" />
    <!-- load icon font -->
    <link href="//cdnjs.cloudflare.com/ajax/libs/font-awesome/4.2.0/css/font-awesome.min.css" rel="stylesheet" type="text/css" />
    <!-- add a custom css -->
  </head>
  <body>
    <!-- content goes here -->
  </body>
</html>
```