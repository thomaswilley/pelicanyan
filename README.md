# Pelicanyan

Pelicanyan brings Jekyll's [Lanyon Theme](https://github.com/poole/lanyon/) to
[Pelican](http://github.com/getpelican) and adds some Pelican niceties
including a sitemap.xml, robots.txt, humans.txt, etc.

More information about the lanyon theme including screenshots and such
is best found over at the [Lanyon Repo](https://github.com/poole/lanyon/). Here's a sample:

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
3. Add your profile photo - Replace the 400x400 PNG located at
   static/img/profile.png with your own

Then to try it out locally, back in your blog's directory:
```bash
$ make clean && make devserver && open http://localhost:8000
```

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

### Example Quickstart

```bash
$ mkdir sample_blog && cd sample_blog/
$ python3 -m virtualenv --no-site-packages --distribute venv
$ source venv/bin/activate
$ pip3 install pelican markdown typogrify
$ pelican-quickstart
```

```
  Where do you want to create your new web site? [.]
  What will be the title of this web site? sample blog
  Who will be the author of this web site? me
  What will be the default language of this web site? [en]
  Do you want to specify a URL prefix? e.g., http://example.com
  (Y/n) n
  Do you want to enable article pagination? (Y/n) n
  Do you want to generate a Fabfile/Makefile to automate
  generation and publishing? (Y/n) Y
  Do you want an auto-reload & simpleHTTP script to assist with theme
  and site development? (Y/n) Y
  Do you want to upload your website using FTP? (y/N) n
  Do you want to upload your website using SSH? (y/N) n
  Do you want to upload your website using Dropbox? (y/N) n
  Do you want to upload your website using S3? (y/N) n
  Do you want to upload your website using Rackspace Cloud Files?
  (y/N) n
  Do you want to upload your website using GitHub Pages? (y/N) n
  Done. Your new project is available at /xyz/sample_blog
```

```bash
$ git clone https://github.com/thomaswilley/pelicanyan.git
$ vim pelicanconf.py
```
Append the following to pelicanconf.py:

```
THEME = 'pelicanyan'
GA_ACCOUNT = 'UA-12344321-1'
TWITTER_ACCOUNT = 'getpelican'
DIRECT_TEMPLATES = ('index', 'categories', 'authors', 'archives', 'sitemap', 'robots', 'humans')
ROBOTS_SAVE_AS = 'robots.txt'
HUMANS_SAVE_AS = 'humans.txt'
SITEMAP_SAVE_AS = 'sitemap.xml'
DEFAULT_LANG = 'en'
DATE_FORMATS = { 'en': '%B %d, %Y', }
STATIC_PATHS = ['images', 'favicon.ico']
SITEDESCRIPTION = 'sample blog'
TYPOGRIFY=True
```

```bash
$ cd pelicanyan/static/css/
$ wget https://raw.githubusercontent.com/poole/lanyon/master/public/css/lanyon.css
$ wget https://raw.githubusercontent.com/poole/lanyon/master/public/css/poole.css
$ wget https://raw.githubusercontent.com/poole/lanyon/master/public/css/syntax.css
$ cd ../../../
```
(back in /xyz/sample_blog)

```bash
$ make clean && make html && make serve
$ open http://localhost:8000
```
