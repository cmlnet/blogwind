# blogwind - A hugo blog theme with TailwindCSS

*blogwind* is a theme for the static site generator [Hugo](https://www.gohugo.io). The theme is built with [TailwindCSS](https://www.tailwindcss.com) and based on [hugo-starter-tailwind-basic](https://github.com/bep/hugo-starter-tailwind-basic) and [Blonde](https://github.com/opera7133/Blonde).

**The theme is still in an early version so expect bugs. All feedback is welcomed.**

## Demo

You can see the theme in action at [my personal blog](https://www.c-m-l.net/).

## Features

* Minimal JavaScript
* Design for posts (default), pages and projects
* Set Creative Commons Licence via Frontmatter for posts
* Support for VG Wort tracking pixel

## Installation

### As a module

Add the following line to your config:

```toml
[module]
  [[module.imports]]
    disable = false
    ignoreConfig = false
    path = "github.com/cmlnet/blogwind"
```

Then run `hugo mod get -u`. (This way you can also update the theme.)

Additionally, you have to [npm](https://www.npmjs.com/get-npm) installed and to run the following command:

```bash
hugo mod npm pack
npm install
```

### As a git submodule

Add *blogwind* as a git submodule in your project:

```bash
git submodule add https://github.com/cmlnet/blogwind.git themes/blogwind
```

Then add in your config `theme = "blogwind"`.

Additionally, you have to [npm](https://www.npmjs.com/get-npm) installed and to run the following command:

```bash
hugo mod npm pack
npm install
```

In order to update the theme use the following command:

```bash
git submodule update --remote --merge
```

## Docs

*work in progress*

### Parameters

There are a couple of theme specific parameters that **can** be set in your config:

#### logo

The parameter `logo` allows you to set a graphical logo for your site. The image has to be placed in the folder `/static`. If it is placed in a subfolder therein you need to give the path.

Examples:

```toml
logo = "logo-path.svg" # logo.svg needs to be in /static
```

```toml
logo = "images/logo-path.svg" # logo.svg needs to be in /static/images
```

If this parameter is not set then *blogwind* will default to using the site title.

### Favicons

*blogwind* will look for the following files in the folder `/static/favicons/*:

```
├── android-chrome-192x192.png
├── android-chrome-512x512.png
├── apple-touch-icon.png
├── favicon-16x16.png
├── favicon-32x32.png
└── site.webmanifest
```

If they are found then they will be included in head.

## ToDo

[ ] Documentation
[ ] Switch from a Flexbox to a GridCSS based layout
[ ] Refactor CSS
[ ] Secure Headers
[ ] Build in search
[ ] Schema markup
[ ] 404 page
[ ] Refactor HTML and CSS

## Credits

* [hugo-starter-tailwind-basic](https://github.com/bep/hugo-starter-tailwind-basic)
* [Blonde](https://github.com/opera7133/Blonde)
* [TailwindCSS](https://tailwindcss.com/)
* [heroicons](https://heroicons.com/)
