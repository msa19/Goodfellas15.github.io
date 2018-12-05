# How to edit this website
1. All information is in the index.md file
2. md is markdown file. Jerkyll is going to convert markdown into html for us
3. Markdown is good to learn because many people write documentation using markdown and LaTex (for formulas)
4. In the index file you can use both *HTML* and *md*
5. Each person is in-charge of their own part, because I want everyone has chance to learn.
6. This is [a quick reference of MD from WordPress](https://en.support.wordpress.com/markdown-quick-reference/), and [mother of HTML](https://www.w3schools.com/)

# The author of this template provide extra configuration below.


### Configuration variables

Cayman Blog will respect the following variables, if set in your site's `_config.yml`:

```yml
title: [The title of your site]
description: [A short description of your site's purpose]
```

Additionally, you may choose to set the following optional variables:

```yml
show_downloads: ["true" or "false" to indicate whether to provide a download URL]
google_analytics: [Your Google Analytics tracking ID]
```


### SEO tags

Cayman Blog includes simple SEO tags from [jekyll-social-metatags](https://github.com/lorepirri/jekyll-social-metatags). Have a look at the page for its usage.

The usage is compatible with the plugin [Jekyll SEO Tag](https://github.com/jekyll/jekyll-seo-tag), which provides a battle-tested template of crowdsourced best-practices.

To switch to a better SEO tags however, one should install [Jekyll Feed plugin](https://github.com/jekyll/jekyll-feed):

1. Add this line to your site's Gemfile:

    ```ruby
    gem 'jekyll-seo-tag'
    ```

2. And then add this line to your site's `_config.yml`:

    ```yml
    gems:
      - jekyll-seo-tag
    ```

3. Replace with the following, the `<!-- jekyll-seo-tag -->` comment in your site's `default.html`:

      ```liquid
      {% seo %}
      ```

For more information about configuring this plugin, see the official [Jekyll SEO Tag](https://github.com/jekyll/jekyll-seo-tag) page.


### Stylesheet

If you'd like to add your own custom styles:

1. Create a file called `/assets/css/style.scss` in your site
2. Add the following content to the top of the file, exactly as shown:
    ```scss
    ---
    ---

    @import "{{ site.theme }}";
    ```
3. Add any custom CSS (or Sass, including imports) you'd like immediately after the `@import` line

### Layouts

If you'd like to change the theme's HTML layout:

1. [Copy the original template](https://github.com/lorepirri/cayman-blog/blob/master/_layouts/default.html) from the theme's repository<br />(*Pro-tip: click "raw" to make copying easier*)
2. Create a file called `/_layouts/default.html` in your site
3. Paste the default layout content copied in the first step
4. Customize the layout as you'd like

### Sass variables

If you'd like to change the theme's [Sass variables](https://github.com/lorepirri/cayman-blog/blob/master/_sass/variables.scss), set new values before the `@import` line in your stylesheet:

```scss
$section-headings-color: #0086b3;

@import "{{ site.theme }}";
```

## Roadmap

See the [open issues](https://github.com/lorepirri/cayman-blog/issues) for a list of proposed features (and known issues).

### Previewing the theme locally

If you'd like to preview the theme locally (for example, in the process of proposing a change):

1. Clone down the theme's repository (`git clone https://github.com/lorepirri/cayman-blog`)
2. `cd` into the theme's directory
3. Run `script/bootstrap` to install the necessary dependencies
4. Run `script/server` to start the preview server
5. Visit [`localhost:4000`](http://localhost:4000) in your browser to preview the theme

### Running tests

The theme contains a minimal test suite, to ensure a site with the theme would build successfully. To run the tests, simply run `script/cibuild`. You'll need to run `script/bootstrap` one before the test script will work.
