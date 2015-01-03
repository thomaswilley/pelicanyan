# Pelicanyan

Pelicanyan brings Jekyll's [Lanyon
Theme](https://github.com/poole/lanyon/) to
[Pelican](http://github.com/getpelican) and adds some Pelican niceties
including a sitemap.xml, robots.txt, humans.txt, etc.

More information about the lanyon theme including screenshots and such
is best found over at the [Lanyon
Repo](https://github.com/poole/lanyon/). Here's a sample:

![Lanyon](https://f.cloud.github.com/assets/98681/1825266/be03f014-71b0-11e3-9539-876e61530e24.png)

## Usage

Assumes you've already got your [blog
created](http://docs.getpelican.com/en/3.5.0/quickstart.html) and have
cloned this repo.

1. Download poole.css, lanyon.css, and syntax.css from the [Lanyon
   repo](https://github.com/poole/lanyon/tree/master/public/css) and save into the static/css directory
2. Set basic theme-specific settings in your blog's pelicanconf.py:
    - THEME='path-to-cloned-repo'
    - GA_ACCOUNT (your GA account id, e.g., 'UA-12344321-1') assuming
    you'd like GA enabled (see base.html)
    - TWITTER_ACCOUNT (e.g., your twitter account name without the @)
    - DIRECT_TEMPLATES = ('index', 'categories', 'authors', 'archives',
      'sitemap', 'robots', 'humans')
    - ROBOTS_SAVE_AS = 'robots.txt'
    - HUMANS_SAVE_AS = 'humans.txt'
    - SITEMAP_SAVE_AS = 'sitemap.xml'
    - DEFAULT_LANG = 'en'
    - DATE_FORMATS = { 'en': '%B %d, %Y', }
    - STATIC_PATHS = ['images', 'favicon.ico'] note: this assumes your
    blog's article images are located in content/images/ and your favicon.ico is located in content/
    - (Additional Required Fields) AUTHOR, SITENAME, SITEURL
    - (Optional) TYPOGRIFY=True (and pip3 install it of course)
    - (Optional) Set SITEDESCRIPTION
    - (Optional) Set your LINKS

## Compatability & Caveats

Pelicanyan's probably best considered alpha at this time and hasn't
undergone much testing - would welcome help finding & fixing bugs and
also with the browser compatability matrix! While it's likely that
Lanyon's options - e.g., reversing the layout, updating color scheme,
etc. - remain functional here, these haven't been tested either.

## Author

**Thomas Willey**
- <https://github.com/thomaswilley>
- <https://twitter.com/thomaswilley>

## License

Open sourced under the [MIT license](LICENSE).
