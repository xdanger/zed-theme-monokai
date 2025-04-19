# VSCode Theme Color Reference

You can customize your active Visual Studio Code color theme with the `workbench.colorCustomizations` user setting.

```json
{
  "workbench.colorCustomizations": {
    "activityBar.background": "#00AA00"
  }
}
```

Theme colors are available as CSS variables in webviews, and an extension is available which provides IntelliSense for them.

## Color formats

Color values can be defined in the RGB color model with an alpha channel for transparency. As format, the following hexadecimal notations are supported: `#RGB`, `#RGBA`, `#RRGGBB` and `#RRGGBBAA`. R (red), G (green), B (blue), and A (alpha) are hexadecimal characters (0-9, a-f or A-F). The three-digit notation (`#RGB`) is a shorter version of the six-digit form (`#RRGGBB`) and the four-digit RGB notation (`#RGBA`) is a shorter version of the eight-digit form (`#RRGGBBAA`). For example `#e35f` is the same color as `#ee3355ff`.

If no alpha value is defined, it defaults to `ff` (opaque, no transparency). If alpha is set to `00`, the color is fully transparent.

Some colors should not be opaque in order to not cover other annotations. Check the color descriptions to see to which colors this applies.

## Contrast colors

The contrast colors are typically only set for high contrast themes. If set, they add an additional border around items across the UI to increase the contrast.

- `contrastActiveBorder`: An extra border around active elements to separate them from others for greater contrast.
- `contrastBorder`: An extra border around elements to separate them from others for greater contrast.

## Base colors

- `focusBorder`: Overall border color for focused elements. This color is only used if not overridden by a component.
- `foreground`: Overall foreground color. This color is only used if not overridden by a component.
- `disabledForeground`: Overall foreground for disabled elements. This color is only used if not overridden by a component.
- `widget.border`: Border color of widgets such as Find/Replace inside the editor.
- `widget.shadow`: Shadow color of widgets such as Find/Replace inside the editor.
- `selection.background`: Background color of text selections in the workbench (for input fields or text areas, does not apply to selections within the editor and the terminal).
- `descriptionForeground`: Foreground color for description text providing additional information, for example for a label.
- `errorForeground`: Overall foreground color for error messages (this color is only used if not overridden by a component).
- `icon.foreground`: The default color for icons in the workbench.
- `sash.hoverBorder`: The hover border color for draggable sashes.

## Window border

The theme colors for VS Code window border.

- `window.activeBorder`: Border color for the active (focused) window.
- `window.inactiveBorder`: Border color for the inactive (unfocused) windows.

The window border colors are only supported on macOS and Linux (not Windows) and only when the custom title bar is enabled (`"window.titleBarStyle": "custom"`).

## Text colors

Colors inside a text document, such as the welcome page.

- `textBlockQuote.background`: Background color for block quotes in text.
- `textBlockQuote.border`: Border color for block quotes in text.
- `textCodeBlock.background`: Background color for code blocks in text.
- `textLink.activeForeground`: Foreground color for links in text when clicked on and on mouse hover.
- `textLink.foreground`: Foreground color for links in text.
- `textPreformat.foreground`: Foreground color for preformatted text segments.
- `textPreformat.background`: Background color for preformatted text segments.
- `textSeparator.foreground`: Color for text separators.

## Action colors

A set of colors to control the interactions with actions across the workbench.

- `toolbar.hoverBackground`: Toolbar background when hovering over actions using the mouse
- `toolbar.hoverOutline`: Toolbar outline when hovering over actions using the mouse
- `toolbar.activeBackground`: Toolbar background when holding the mouse over actions
- `editorActionList.background`: Action List background color.
- `editorActionList.foreground`: Action List foreground color.
- `editorActionList.focusForeground`: Action List foreground color for the focused item.
- `editorActionList.focusBackground`: Action List background color for the focused item.

## Button control

A set of colors for button widgets such as **Open Folder** button in the Explorer of a new window.

- `button.background`: Button background color.
- `button.foreground`: Button foreground color.
- `button.border`: Button border color.
- `button.separator`: Button separator color.
- `button.hoverBackground`: Button background color when hovering.
- `button.secondaryForeground`: Secondary button foreground color.
- `button.secondaryBackground`: Secondary button background color.
- `button.secondaryHoverBackground`: Secondary button background color when hovering.
- `checkbox.background`: Background color of checkbox widget.
- `checkbox.foreground`: Foreground color of checkbox widget.
- `checkbox.border`: Border color of checkbox widget.
- `checkbox.selectBackground`: Background color of checkbox widget when the element it's in is selected.
- `checkbox.selectBorder`: Border color of checkbox widget when the element it's in is selected.
- `radio.activeForeground`: Foreground color of active radio option.
- `radio.activeBackground`: Background color of active radio option.
- `radio.activeBorder`: Border color of the active radio option.
- `radio.inactiveForeground`: Foreground color of inactive radio option.
- `radio.inactiveBackground`: Background color of inactive radio option.
- `radio.inactiveBorder`: Border color of the inactive radio option.
- `radio.inactiveHoverBackground`: Background color of inactive active radio option when hovering.

## Dropdown control

A set of colors for all Dropdown widgets such as in the Integrated Terminal or the Output panel. Note that the
Dropdown control is not used on macOS currently.

- `dropdown.background`: Dropdown background.
- `dropdown.listBackground`: Dropdown list background.
- `dropdown.border`: Dropdown border.
- `dropdown.foreground`: Dropdown foreground.

## Input control

Colors for input controls such as in the Search view or the Find/Replace dialog.

- `input.background`: Input box background.
- `input.border`: Input box border.
- `input.foreground`: Input box foreground.
- `input.placeholderForeground`: Input box foreground color for placeholder text.
- `inputOption.activeBackground`: Background color of activated options in input fields.
- `inputOption.activeBorder`: Border color of activated options in input fields.
- `inputOption.activeForeground`: Foreground color of activated options in input fields.
- `inputOption.hoverBackground`: Background color of activated options in input fields.
- `inputValidation.errorBackground`: Input validation background color for error severity.
- `inputValidation.errorForeground`: Input validation foreground color for error severity.
- `inputValidation.errorBorder`: Input validation border color for error severity.
- `inputValidation.infoBackground`: Input validation background color for information severity.
- `inputValidation.infoForeground`: Input validation foreground color for information severity.
- `inputValidation.infoBorder`: Input validation border color for information severity.
- `inputValidation.warningBackground`: Input validation background color for information warning.
- `inputValidation.warningForeground`: Input validation foreground color for warning severity.
- `inputValidation.warningBorder`: Input validation border color for warning severity.

## Scrollbar control

- `scrollbar.shadow`: Scrollbar slider shadow to indicate that the view is scrolled.
- `scrollbarSlider.activeBackground`: Scrollbar slider background color when clicked on.
- `scrollbarSlider.background`: Scrollbar slider background color.
- `scrollbarSlider.hoverBackground`: Scrollbar slider background color when hovering.

## Badge

Badges are small information labels, for example, search results count.

- `badge.foreground`: Badge foreground color.
- `badge.background`: Badge background color.

## Progress bar

- `progressBar.background`: Background color of the progress bar shown for long running operations.

## Lists and trees

Colors for list and trees like the File Explorer. An active list/tree has keyboard focus, an inactive does not.

- `list.activeSelectionBackground`: List/Tree background color for the selected item when the list/tree is active.
- `list.activeSelectionForeground`: List/Tree foreground color for the selected item when the list/tree is active.
- `list.activeSelectionIconForeground`: List/Tree icon foreground color for the selected item when the list/tree is active.
- `list.dropBackground`: List/Tree drag and drop background when moving items around using the mouse.
- `list.focusBackground`: List/Tree background color for the focused item when the list/tree is active.
- `list.focusForeground`: List/Tree foreground color for the focused item when the list/tree is active.
- `list.highlightForeground`: List/Tree foreground color of the match highlights when searching inside the list/tree.
- `list.hoverBackground`: List/Tree background when hovering over items using the mouse.
- `list.hoverForeground`: List/Tree foreground when hovering over items using the mouse.
- `list.inactiveSelectionBackground`: List/Tree background color for the selected item when the list/tree is inactive.
- `list.inactiveSelectionForeground`: List/Tree foreground color for the selected item when the list/tree is inactive.
- `list.invalidItemForeground`: List/Tree foreground color for invalid items, for example an unresolved root in explorer.
- `list.errorForeground`: Foreground color of list items containing errors.
- `list.warningForeground`: Foreground color of list items containing warnings.

## Activity Bar

The Activity Bar is displayed on the far left or right of the workbench and allows to switch between views of the Side Bar.

- `activityBar.background`: Activity Bar background color.
- `activityBar.foreground`: Activity Bar foreground color (for example used for the icons).
- `activityBar.inactiveForeground`: Activity Bar item foreground color when it is inactive.
- `activityBar.border`: Activity Bar border color with the Side Bar.
- `activityBarBadge.background`: Activity notification badge background color.
- `activityBarBadge.foreground`: Activity notification badge foreground color.
- `activityBar.activeBorder`: Activity Bar active indicator border color.
- `activityBar.activeBackground`: Activity Bar optional background color for the active element.
- `activityBar.activeFocusBorder`: Activity bar focus border color for the active item.

## Side Bar

The Side Bar contains views like the Explorer and Search.

- `sideBar.background`: Side Bar background color.
- `sideBar.foreground`: Side Bar foreground color. The Side Bar is the container for views like Explorer and Search.
- `sideBar.border`: Side Bar border color on the side separating the editor.
- `sideBarTitle.foreground`: Side Bar title foreground color.
- `sideBarSectionHeader.background`: Side Bar section header background color.
- `sideBarSectionHeader.foreground`: Side Bar section header foreground color.
- `sideBarSectionHeader.border`: Side bar section header border color.

## Editor colors

The most prominent editor colors are the token colors used for syntax highlighting and are based on the language grammar installed. These colors are defined by the Color Theme but can also be customized.

- `editor.background`: Editor background color.
- `editor.foreground`: Editor default foreground color.
- `editorLineNumber.foreground`: Color of editor line numbers.
- `editorLineNumber.activeForeground`: Color of the active editor line number.
- `editorCursor.background`: The background color of the editor cursor. Allows customizing the color of a character overlapped by a block cursor.
- `editorCursor.foreground`: Color of the editor cursor.

Selection colors are visible when selecting one or more characters:

- `editor.selectionBackground`: Color of the editor selection.
- `editor.selectionForeground`: Color of the selected text for high contrast.
- `editor.inactiveSelectionBackground`: Color of the selection in an inactive editor.

Find feature colors:

- `editor.findMatchBackground`: Color of the current search match.
- `editor.findMatchHighlightBackground`: Color of the other search matches.
- `editor.findRangeHighlightBackground`: Color the range limiting the search (Enable 'Find in Selection' in the find widget).

## Terminal colors

- `terminal.background`: The background of the Integrated Terminal's viewport.
- `terminal.foreground`: The default foreground color of the Integrated Terminal.
- `terminal.ansiBlack`: 'Black' ANSI color in the terminal.
- `terminal.ansiBlue`: 'Blue' ANSI color in the terminal.
- `terminal.ansiBrightBlack`: 'BrightBlack' ANSI color in the terminal.
- `terminal.ansiBrightBlue`: 'BrightBlue' ANSI color in the terminal.
- `terminal.ansiBrightCyan`: 'BrightCyan' ANSI color in the terminal.
- `terminal.ansiBrightGreen`: 'BrightGreen' ANSI color in the terminal.
- `terminal.ansiBrightMagenta`: 'BrightMagenta' ANSI color in the terminal.
- `terminal.ansiBrightRed`: 'BrightRed' ANSI color in the terminal.
- `terminal.ansiBrightWhite`: 'BrightWhite' ANSI color in the terminal.
- `terminal.ansiBrightYellow`: 'BrightYellow' ANSI color in the terminal.
- `terminal.ansiCyan`: 'Cyan' ANSI color in the terminal.
- `terminal.ansiGreen`: 'Green' ANSI color in the terminal.
- `terminal.ansiMagenta`: 'Magenta' ANSI color in the terminal.
- `terminal.ansiRed`: 'Red' ANSI color in the terminal.
- `terminal.ansiWhite`: 'White' ANSI color in the terminal.
- `terminal.ansiYellow`: 'Yellow' ANSI color in the terminal.

## Debug colors

- `debugToolBar.background`: Debug toolbar background color.
- `debugToolBar.border`: Debug toolbar border color.
- `editor.stackFrameHighlightBackground`: Background color of the top stack frame highlight in the editor.
- `editor.focusedStackFrameHighlightBackground`: Background color of the focused stack frame highlight in the editor.
- `debugIcon.breakpointForeground`: Icon color for breakpoints.
- `debugIcon.breakpointDisabledForeground`: Icon color for disabled breakpoints.

## Git colors

- `gitDecoration.addedResourceForeground`: Color for added Git resources. Used for file labels and the SCM viewlet.
- `gitDecoration.modifiedResourceForeground`: Color for modified Git resources. Used for file labels and the SCM viewlet.
- `gitDecoration.deletedResourceForeground`: Color for deleted Git resources. Used for file labels and the SCM viewlet.
- `gitDecoration.untrackedResourceForeground`: Color for untracked Git resources. Used for file labels and the SCM viewlet.
- `gitDecoration.ignoredResourceForeground`: Color for ignored Git resources. Used for file labels and the SCM viewlet.
- `gitDecoration.conflictingResourceForeground`: Color for conflicting Git resources. Used for file labels and the SCM viewlet.

## Extension colors

Color IDs can also be contributed by extensions through the color contribution point. These colors also appear when using code complete in the `workbench.colorCustomizations` settings and the color theme definition file. Users can see what colors an extension defines in the extension contributions tab.

Source: [VS Code Theme Color Reference](https://code.visualstudio.com/api/references/theme-color)
