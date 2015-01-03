# Pelicanyan

Pelicanyan brings Jekyll's [Lanyon
Theme](https://github.com/poole/lanyon/) to
[Pelican](http://github.com/getpelican).

More information about the lanyon theme including screenshots and such
is best found over at the [Lanyon
Repo](https://github.com/poole/lanyon/). Here's a sample:

![Lanyon](https://f.cloud.github.com/assets/98681/1825266/be03f014-71b0-11e3-9539-876e61530e24.png)

## Usage

0. Assumes you've already got your [blog
   created](http://docs.getpelican.com/en/3.5.0/quickstart.html)
1. Clone this repo
2. Download poole.css, lanyon.css, and syntax.css from the [Lanyon
   repo](https://github.com/poole/lanyon/tree/master/public/css) and save into the static/css directory
3. Set basic theme-specific settings in your blog's pelicanconf.py:
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
undergone much testing. If you find bugs by all means help fix them and
build out a browser compatability matrix. While most likely things like
reversing the layout, updating color scheme, and other options
associated with Lanyon remain possible here, these haven't been tested
either.

## Author

**Thomas Willey**
- <https://github.com/thomaswilley>
- <https://twitter.com/thomaswilley>

## License

Open sourced under the [MIT license](LICENSE).
