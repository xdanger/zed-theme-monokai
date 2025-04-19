# User themes now in Preview

Today we're excited to share that you can now bring your own theme to [Zed Preview](https://zed.dev/releases/preview)!

## Adding a theme

Themes are stored in the `themes/` subdirectory under the Zed config:

```text
~/.config/zed/themes
```

Each theme file can contain multiple themes—such as light and dark variants—under the same theme family.

The basic structure of a theme file looks like this:

```json
// ~/.config/zed/themes/my-cool-theme.json
{
  "$schema": "https://zed.dev/schema/themes/v0.2.0.json",
  "name": "My Cool Theme",
  "author": "You!",
  "themes": [
    {
      "name": "My Cool Dark Theme",
      "appearance": "dark",
      "style": {
        "editor.background": "#000"
        // ...
      }
    },
    {
      "name": "My Cool Light Theme",
      "appearance": "light",
      "style": {
        "editor.background": "#fff"
        // ...
      }
    }
  ]
}
```

Add a theme file to the `themes` directory and it will be available in the theme selector the next time Zed loads.

In the near future we'll make it so Zed can automatically detect changes in the `themes` directory.

## Modifying an existing theme

In addition to bringing your entire theme, you can also override values in the active theme via the Zed settings:

```json
// ~/.config/zed/settings.json
{
  "theme": "One Dark",
  "experimental.theme_overrides": {
    "editor.background": "#333"
  }
}
```

Changes set in `experimental.theme_overrides` apply to every theme.

Additionally, Zed will live-reload when this setting is changed, making it a great way to iterate quickly while building a theme.

## Using a VS Code theme

If are looking to use an existing VS Code theme in Zed, we have a work-in-progress theme importer available in the Zed repo.

Note that you'll need to have the Zed [development toolchain](https://zed.dev/docs/developing-zed) setup locally in order to use the theme importer.

You can run it against a VS Code theme file and it will output a Zed theme based on it:

```bash
cargo run -p theme_importer -- ~/Downloads/vitesse-dark-soft.json
```

While the resulting theme will likely not be perfect, this can be a good starting point if you're looking to bring over a theme from VS Code.

## Go forth and theme

Themes are still in the early stages, but we hope you enjoy this first taste. As always, feedback and suggestions are welcome on our [GitHub](https://github.com/zed-industries/zed).

Tweet [@zeddotdev](https://twitter.com/zeddotdev) to show us your fresh new looks for Zed.

We can't wait to see all your new themes!

Source: [User themes now in Preview](https://zed.dev/blog/user-themes-now-in-preview)
