# Hugo Hero Theme

Hero is a multi-page business theme with fullscreen hero images and fullwidth sections.

[Live Demo](https://hugo-hero.netlify.app/) |
[Zerostatic Themes](https://www.zerostatic.io/theme/hugo-hero/)

<!-- ![Hugo Hero Theme screenshot](https://www.zerostatic.io/theme/hugo-hero/hugo-hero-screenshot.png) -->

## Installation

**1. Install Hugo**

To use this theme you will first need to have Hugo installed. Please follow the
official [installation
guide](https://gohugo.io/getting-started/installing/).

⚠️ **Note:** Check your Hugo version - **Hugo Extended** is required!

⚠️ **Note:** Do not use apt-get for Debian systems since it hasn't been updated.

Instead, download the latest extended version from
[here](https://github.com/gohugoio/hugo/releases/tag/v0.149.0). Download file
`hugo_extended_0.149.0_linux-amd64.deb` and execute:

    sudo dpkg -i hugo_extended_0.149.0_linux-amd64.deb

This theme uses [Hugo Pipes](https://gohugo.io/hugo-pipes/scss-sass/) to
compile SCSS and minify assets which means if you not using the Hugo extended
version this theme will not work. To check your version of Hugo, run `hugo
version`. Make sure you see __/extended__ after the version number, for example
_Hugo Static Site Generator v0.82.0/extended darwin/amd64 BuildDate: unknown_
You do not need to use version v0.82.0 specifically, it just needs to have the
_/extended_ part.

**2. Create a new Hugo site**

This will create a fresh Hugo site in the folder `rifrobotics`.

```
hugo new site rifrobotics
```

**3. Install the theme**

Use `vcs` to clone this theme into the sites themes folder
`rifrobotics/themes`. You should end up with the following folder structure
`rifrobotics/themes/hugo-hero-theme`

```
cd /path/to/rif-website-2025
vcs import rifrobotics/themes/ < themes.repos
```
<!-- git clone git@github.com:zerostaticthemes/hugo-hero-theme.git themes/hugo-hero-theme -->

**4. Copy the example content**

Copy the entire contents of the
`rifrobotics/themes/hugo-hero-theme/exampleSite/` folder to root folder of your
Hugo site, ie `rifrobotics/`. To copy the files using terminal, make sure you
are still in the projects root, ie the `rifrobotics` folder.

```
cd /path/to/rif-website-2025/rifrobotics
cp -a themes/hugo-hero-theme/exampleSite/. .
cp -a themes/hugo-hero-theme/layouts .
```

**5. Run Hugo**

After installing the theme for the first time, generate the Hugo site.

You run this command from the root folder of your Hugo site ie `rifrobotics/`

```
hugo
```

For local development run Hugo's built-in local server.

```
hugo server
```

Now enter [`localhost:1313`](http://localhost:1313) in the address bar of your
browser.

## Deployment

Coming soon ...

<!-- ### Netlify -->

<!-- [![Deploy to -->
<!-- Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/zerostaticthemes/hugo-hero-theme) -->

<!-- This theme includes a `netlify.toml` which is [configured to deploy to -->
<!-- Netlify](https://discourse.gohugo.io/t/deploy-your-theme-to-netlify/15508) from -->
<!-- the `exampleSite` folder. If you have installed this theme into a new Hugo site -->
<!-- and the exampleSite folder was copied or removed, you should delete the -->
<!-- `netlify.toml` file. -->

## Configuring Theme

### Homepage meta tags

Often a homepage requires special meta tags such as a meta description or og
meta data for twitter, facebook etc. You can configure these values in the
`config.toml`

```toml
# config.toml
...

  [params.homepage_meta_tags]
    meta_description = "a description of your website."
    meta_og_title = "My Theme"
    meta_og_type = "website"
    meta_og_url = "https://www.mywebsite.com"
    meta_og_image = "https://www.mywebsite.com/images/tn.png"
    meta_og_description = "a description of your website."
    meta_twitter_card = "summary"
    meta_twitter_site = "@mytwitterhandle"
    meta_twitter_creator = "@mytwitterhandle"

```

### Set meta tags on a per layout basis

You can set meta tags on a per template basis using a block. For example, you might want to write a custom meta description for the `/services` page. You can insert any valid HTML meta data inside the `{{ define "meta_tags }}` block at the top of a template.

```
// layouts/services/list.html
...

{{ define "meta_tags" }}
    <meta name="description" content="We offer a variety of services in the finance industry" />
{{ end }}

{{ define main }}
...
```

<!-- ### Google Analytics -->

<!-- Add your google analytics ID to the `config.toml` -->

<!-- ```toml -->
<!-- # config.toml -->
<!-- [params] -->
<!--   google_analytics_id="UA-132398315-1" -->
<!-- ``` -->

### Menu

You can edit and add main menu links in the `config.toml` under `[[menu.main]]`

## License (from author)

- Don't create ports or new versions of this theme without asking me
- You can't re-distribute or re-sell this theme as your own template

## Credits

- Beautiful royalty free Illustrations by Icons8 - https://icons8.com/illustrations/style--pixeltrue
- Stock images by Unsplash - https://unsplash.com/
- Feature icons by Noun Project - https://thenounproject.com/

**More Hugo Themes by Zerostatic**

- [Hugo Hero](https://github.com/zerostaticthemes/hugo-hero-theme) - Open-source business theme
- [Hugo Whisper](https://github.com/zerostaticthemes/hugo-whisper-theme) - Open-source documentation theme
- [Hugo Serif](https://github.com/zerostaticthemes/hugo-serif-theme) - Open-source business theme
- [Hugo Winston](https://github.com/zerostaticthemes/hugo-winston-theme) - Open-source blog theme
- [Hugo Advance](https://www.zerostatic.io/theme/hugo-advance/) - Premium advanced multi page business & marketing theme
- [Hugo Paradigm](https://www.zerostatic.io/theme/hugo-paradigm/) - Premium landing page + site builder theme
- [Hugo Lever](https://www.zerostatic.io/theme/hugo-lever/) - Premium personal / bio theme
- [Hugo Shard](https://www.zerostatic.io/theme/hugo-lever/) - Premium SAAS / landing page theme

**Find hundreds more Hugo themes on [Built At
Lightspeed](https://builtatlightspeed.com/category/hugo)**
