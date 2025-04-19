# Zed Themes

## Theme Structure

The `themes` directory in an extension should contain one or more theme files.

Each theme file should adhere to the JSON schema specified at [`https://zed.dev/schema/themes/v0.2.0.json`](https://zed.dev/schema/themes/v0.2.0.json).

The structure of a Zed theme is defined in the [Zed Theme JSON Schema](https://zed.dev/schema/themes/v0.2.0.json).

A Zed theme consists of a Theme Family object including:

- `name`: The name for the theme family
- `author`: The name of the author of the theme family
- `themes`: An array of Themes belonging to the theme family

The core components a Theme object include:

1. Theme Metadata:
   - `name`: The name of the theme
   - `appearance`: Either "light" or "dark"
2. Style Properties under the `style`, such as:
   - `background`: The main background color
   - `foreground`: The main text color
   - `accent`: The accent color used for highlighting and emphasis
3. Syntax Highlighting:
   - `syntax`: An object containing color definitions for various syntax elements (e.g., keywords, strings, comments)
4. UI Elements:
   - Colors for various UI components such as:
     - `element.background`: Background color for UI elements
     - `border`: Border colors for different states (normal, focused, selected)
     - `text`: Text colors for different states (normal, muted, accent)
5. Editor-specific Colors:
   - Colors for editor-related elements such as:
     - `editor.background`: Editor background color
     - `editor.gutter`: Gutter colors
     - `editor.line_number`: Line number colors
6. Terminal Colors:
   - ANSI color definitions for the integrated terminal

It's recommended to look at [existing themes](https://github.com/zed-industries/zed/tree/main/assets/themes) to get a more comprehensive idea of what can be styled.

## Adding a User Theme

Themes are stored in the `themes/` subdirectory under the Zed config:

```
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

## Modifying an Existing Theme

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

## Using a VS Code Theme

If you are looking to use an existing VS Code theme in Zed, there is a work-in-progress theme importer available in the Zed repo.

Note that you'll need to have the Zed [development toolchain](https://zed.dev/docs/developing-zed) set up locally in order to use the theme importer.

You can run it against a VS Code theme file and it will output a Zed theme based on it:

```
cargo run -p theme_importer -- ~/Downloads/vitesse-dark-soft.json
```

While the resulting theme will likely not be perfect, this can be a good starting point if you're looking to bring over a theme from VS Code.

Sources:

- [Zed Extensions: Themes](https://zed.dev/docs/extensions/themes)
- [User themes now in Preview](https://zed.dev/blog/user-themes-now-in-preview)
