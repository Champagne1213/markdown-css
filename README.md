makrdown-css
=========

Markdown css is a command tool to convert css style into markdown inline style.

## Install

*maxOS*

```bash
xcode-select --install
pip install markdown-css
```

**linux**

```bash
apt-get install libxml2-dev libxslt1-dev python-dev
apt-get install python-lxml
pip install markdown-css
```

## Getting started

```bash
pip install markdown-css
mkdir public
touch style.css
markdown -h
markdown-css pub.html --style=style.css --out=public
```

### Themes

https://github.com/wecatch/markdown-css/tree/master/themes

### Demo

```
git clone https://github.com/wecatch/markdown-css.git
cd themes
markdown-css demo.html --style=simple.css --out=public
```

## Selector

markdown-css support css selector like these:

*element selector*

```css
p {
    margin: 10px 0;
}
```


*multi element selector*

```css
h1,p,h2,pre {
    color: #333;
}
```

*all element*

```css
* {
    font-size: 14px
}
```

*pseudo-selector*

```css
h1:before {
    content: '#'
}
```

*child element seletor*

```css
blockquote p {
    color:#888;
}

```
> Pseudo-selector can't be used in inline-style, these selectos are write into <style> tag
