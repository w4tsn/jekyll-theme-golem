# Golem

Golem is a compositum Jekyll theme created from other astonishing themes and designs. Checkout the demo [here](https://w4tsn.github.io/golem/).

## Features
- Easy installation
- Compatible with GitHub Pages
- Responsive design (looks just as good on mobile)
- Syntax highlighting, with the help of Pygments
- Markdown and HTML text formatting
- Pagination of posts

## Installation
There are 3 ways to install this theme

1. Install it as a Ruby Gem (for self-hosted sites)
2. Install it with the `jekyll-remote-theme` plugin (for GitHub Pages hosted sites)
3. Fork the project directly

### Ruby Gem method
1. Add this line to your `Gemfile`:

```ruby
gem "golem"
```

2. Install the theme's gems and dependencies:

```bash
$ bundle
```

3. In `_config.yml` add these lines:

```yaml
theme:      golem

permalink:  /:year-:month-:day/:title
paginate:   5
```

Remove any other `theme:` lines.

4. Rename `index.md` to `index.html`. Without this, the `jekyll-paginate` gem will not work.

5. In `about.md`, change the `layout:` field to `post`:

```Markdown
layout: post
```

### GitHub Pages method
1. Add these 2 lines in to your `Gemfile`:

```ruby
gem "jekyll-remote-theme"
gem "jekyll-paginate"
```

2. Install the newly added gems:

```bash
$ bundle
```

3. In `_config.yml` add these lines:

```yaml
remote_theme: w4tsn/jekyll-theme-golem

permalink:    /:year-:month-:day/:title
paginate:     5

plugins:
  - jekyll-paginate
  - jekyll-remote-theme
```

Remove any other `theme:` or `remote_theme:` lines.

4. Rename `index.md` to `index.html`. Without this, the `jekyll-paginate` gem will not work.

5. In `about.md`, change the `layout:` field to `post`:

```Markdown
layout: post
```

### Fork method
1. Fork this repository

2. Delete the unnecessary files/folders: `CODE_OF_CONDUCT.md`, `LICENSE`, `README.md`, `golem.gemspec`

3. Delete the `baseurl` line in `_config.yml`:

```yaml
baseurl:  "/golem"   # delete this line
```

## Usage
Once you've installed the theme, you're ready to work on your Jekyll site. To start off, I would recommend updating `_config.yml` with your site's details.

To build and serve your site, run:

```bash
$ bundle exec jekyll serve
```

And you're all set! Head over to http://127.0.0.1:4000/ to see your site in action.

## Contributing
Found a bug or have a suggestion? Feel free to create an [issue](https://gitlab.com/w4tsn/jekyll-theme-golem/issues) or make a [pull request](https://gitlab.com/w4tsn/jekyll-theme-golem/pulls)!

### Development

#### podman method

For a full development setup with the page served on localhost:4000 on Fedora 31+ use:

```bash
$ sudo podman run --user=root --rm --volume="/home/w4tsn/Code/tale:/srv/jekyll" -it -p 4000:4000 --security-opt label=disable jekyll/jekyll bash
bash# jekyll serve
bash# jekyll serve --incremental
```

## License
See [LICENSE](https://gitlab.com/w4tsn/jekyll-theme-golem/blob/master/LICENSE)

## Attribution

Since this is a composition theme by design, lending lot's of code and features from all over the place, this section is for attribution of all the great creators.

First of all there is the [Golem Theme by Alexander Wellbrock](https://w4tsn.github.io/golem/), which is the foundation of this compositum.

The Project Icon is made by by [Freepik](https://www.flaticon.com/authors/freepik) from www.flaticon.com.
