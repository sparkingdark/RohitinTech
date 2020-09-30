title: How to combine multiple Google Font imports.
tags: ["Web Development"]
---

A lot of times, I use other people's code or tutorials.

Often, they make multiple requests to **Google Fonts** when they want to use more than one font.

It looks something like this-

```html
<link href="//fonts.googleapis.com/css?family=Lora:400,700,400italic,700italic" rel="stylesheet" type="text/css"/>
<link href="//fonts.googleapis.com/css?family=Open+Sans:300italic,400italic,600italic,700italic,800italic,400,300,600,700,800" rel="stylesheet" type="text/css"/>
```

This increases page load time.

Call me slow internet guy, but I adore fast loading sites.

So what I do is - 

I combine multiple Font imports into a single request.

## How to combine multiple google fonts import.

This is how I do it —

```html
<link href="//fonts.googleapis.com/css?family=font1|font2|fontN" rel="stylesheet" type="text/css"/>
```

Take a close look at this part `family=font1|font2|fontN`

`font1` will be the name and weight of the first font, 

`font2` will be the name and weight of the second font and

`fontN` will be the name and weight of the nth font.

All of them separated by `|`.

For the example above, it will go from this —

```html
<link href="//fonts.googleapis.com/css?family=Lora:400,700,400italic,700italic" rel="stylesheet" type="text/css"/>
<link href="//fonts.googleapis.com/css?family=Open+Sans:300italic,400italic,600italic,700italic,800italic,400,300,600,700,800" rel="stylesheet" type="text/css"/>
```

To this

```html
<link href="//fonts.googleapis.com/css?family=Lora:400,700,400italic,700italic|Open+Sans:300italic,400italic,600italic,700italic,800italic,400,300,600,700,800" rel="stylesheet" type="text/css"/>
```

Do this and you will decrease load time by a few millisecond. 

When you are trying to make a page load faster, every millisecond counts.

## Follow these steps to import google font yourself:

1. Choose the first font you want.
2. Then click on "+ Select this style" for the styles that you want.

    ![Select first font](/img/select-first-google-font.png)

    A side panel will open up. Like the one in the picture

3. Then select another font. 
4. Again click on "+ Select this style" for the styles that you want.

    ![Select second font](/img/select-second-font.png)

5. Now click on the embed tab in the side menu.

    ![Import](/img/import-google-font.png)

6. Copy the `<link>` to import.

    This link is exactly like the one we created earlier.

7. Now paste this link in the `<head>` of your document and enjoy faster speed.

If you know someone who needs to see this, Share!