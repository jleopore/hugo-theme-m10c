# m10c theme

![Intro](https://github.com/vaga/hugo-theme-m10c/blob/master/images/cover.png)

A Hugo minimalistic theme for bloggers.

## Fork details

This fork generally tracks the [upstream repo](https://github.com/vaga/hugo-theme-m10c), but with the following changes:
- Uses vanilla css instead of Sass. This allows you to modify and override the stylesheets with a regular hugo installation rather than hugo_extended, which includes a Sass parser.
- Adds clickable tags to the header, as a navigation aid.

## Getting started

### Installation

Create a new Hugo site:
```bash
$ hugo new site [path]
```

Clone this repository into `themes/` directory:
```bash
$ cd [path]
$ git clone https://github.com/vaga/hugo-theme-m10c.git themes/m10c
```

Add this line  in the `config.toml` file:
```toml
theme = "m10c"
```

### Configuration

In your `config.toml` file, define the following variables in `params`:

- `author`: Name of the author
- `description`: Short description of the author
- `avatar`: Path of file containing the author avatar image
- `menu_item_separator`: Separator between each menu item. HTML allowed (default: " - ")
- `favicon`: Absolute path of your favicon.ico file (default: "/favicon.ico")

To add a menu item, add the following lines in `menu`:

```
[[menu.main]]
  identifier = "tags"
  name = "Tags"
  url = "/tags/"
```

For more details about menus, see [the hugo docs](https://gohugo.io/content-management/menus/#readout).

To add a social link, add the following lines in `params`:

```
[[params.social]]
  name = "github"
  url = "https://github.com/vaga"
```

To change theme colors, add the following lines in `params`:

```
[params.style]
  darkestColor = "#d35050"
  darkColor = "#212121"
  lightColor = "#f5e3e0"
  lightestColor = "#f5f5f5"
  primaryColor = "#fff"
```

If you want the above theme colors, you can see the [exampleSite/config.toml](/exampleSite/config.toml) file.

To override css styles, add a file called `extra.css` to `{your site directory}/assets/`

## License

This theme is released under the [**MIT**](/LICENSE.md) License.

## Acknowledgements

- [feather](https://feathericons.com/) - [MIT](https://github.com/feathericons/feather/blob/master/LICENSE) [<sup>(download as json)</sup>](https://unpkg.com/feather-icons/dist/icons.json)
