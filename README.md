# Quarto Progress Indicator

A lightweight, premium progress indicator for Quarto Reveal.js presentations.
This extension is built with **pure JavaScript and CSS**, requiring **no Lua dependency**, making it easy to install and highly performant.

![Quarto Progress Indicator](https://github.com/user-attachments/assets/000dcf80-c6bf-496e-b032-e1495d620144)

## Key Features

- **🎨 Theme Palettes**: 8 curated themes — 4 light (Ocean, Emerald, Sunset, Lavender) and 4 dark (Dracula, Nord, Gruvbox, Tokyo Night).
- **🖌️ Full Color Control**: Customize active dot, inactive dot, label text, and background colors independently.
- **✨ Dynamic Animations**: Pulse, Glow, or Bounce effects for the active slide dot.
- **🔄 Animated Position Toggle**: Smooth exit/enter animation when switching between Top and Bottom positions.
- **🌐 Universal Theme Support**: Works across all Reveal.js themes (simple, moon, league, clean-revealjs, etc.) without hardcoded CSS selectors.
- **📌 Smart Overlap Prevention**: Automatically detects and adjusts all `position: fixed` UI elements to prevent collisions with the indicator bar.
- **💾 Smart Persistence**: All settings are saved in `localStorage` and persist across reloads.
- **💡 Tooltip Toggle**: Show or hide slide titles on hover.
- **📤 Export & Import**: Save/load settings as JSON files, or copy as YAML/CSS for permanent project configuration.
- **⌨️ Keyboard Shortcuts**: Instant access to configuration and visibility controls.
- **📱 Responsive Design**: Automatically adapts to different screen sizes and light/dark modes.
- **🚀 Zero Lua Dependency**: Works purely in the browser environment.

## Installation

Add the extension to your project:

```bash
quarto add ofurkancoban/QuartoProgressIndicator
```

## Usage

To use the extension, include the HTML file in your `_quarto.yml` or document header:

```yaml
format:
  revealjs:
    include-after-body: _extensions/ofurkancoban/progress-indicator/progress-indicator.html
```

### Keyboard Shortcuts

| Shortcut | Action |
| :--- | :--- |
| <kbd>i</kbd> | Open/Close Settings Menu |
| <kbd>x</kbd> | Toggle Indicator Visibility |

## Interactive Configuration

Press <kbd>i</kbd> during your presentation to open the **Display Settings** panel. From here you can:

- **Position & Alignment**: Move the indicator to Top/Bottom with smooth slide animation, or align Left/Center/Right.
- **Themes**: Switch between 8 professional color palettes — each theme sets active, inactive, background, and label colors simultaneously.
- **Active & Inactive Colors**: Fine-tune dot and label colors with live color pickers.
- **Background Color**: Customize the indicator bar's background color.
- **Styling**: Toggle between **Dots** and **Progress Bar** styles.
- **Visibility Manager**: Hide the indicator on specific slides or the title slide.
- **Tooltip Toggle**: Show or hide slide title tooltips on hover.
- **Export Config**: Copy as YAML/CSS or download/upload settings as JSON.

## YAML Configuration

While the interactive menu is the easiest way to customize, you can also set defaults in your `_quarto.yml`:

```yaml
format:
  revealjs:
    progress-indicator:
      position: "bottom"    # top | bottom
      alignment: "center"   # left | right | center
      style: "dots"         # dots | bar
      hide-on-title: true   # true | false
```

And customize aesthetics in your CSS:

```css
:root {
  --primary-color: #3b60e4;
  --inactive-color: #bbbbbb;
  --indicator-bg: rgba(255, 255, 255, 0.9);
  --label-color: #888;
  --dot-size: 8px;
  --section-spacing: 15px;
}
```

## Universal Theme Compatibility

The indicator automatically adapts to any Reveal.js theme by dynamically scanning the DOM for `position: fixed` elements and adjusting them to prevent overlap. This means it works out-of-the-box with:

- Default Reveal.js themes (`simple`, `moon`, `night`, `league`, `serif`, etc.)
- Third-party themes (`clean-revealjs`, etc.)
- Any custom theme with logos, footers, or plugin buttons (chalkboard, menu, etc.)

## License

MIT License. Feel free to use and contribute!
