# Quarto Progress Indicator

A lightweight, premium progress indicator for Quarto Reveal.js presentations.
This extension is built with **pure JavaScript and CSS**, requiring **no Lua dependency**, making it easy to install and highly performant.

![Quarto Progress Indicator](https://cdn.jumpshare.com/preview/Tm5HtCCTB01HqtcDvKp56grF8lfW7iKN1MBLhaJrXaww7uXYQ-X4Xz09tUrOsZJj_oTdJyRmiWmOy1MneZDOc1HKJxY4IR2_5KPbYOQel_Q)

## Key Features

- **Interactive Settings Menu**: Configure your indicator live during the presentation.
- **Visual Theme Palettes**: Choose from 6+ professional themes (Nord, Indigo, Emerald, Slate, Rose, Cyber).
- **Dynamic Animations**: Pulse, Glow, or Bounce effects for the active slide dot.
- **Smart Persistence**: All settings (color, size, theme, etc.) are saved in your browser and persist across reloads.
- **Keyboard Shortcuts**: Instant access to configuration and visibility controls.
- **Zero Lua Dependency**: Works purely in the browser environment.
- **Responsive Design**: Automatically adapts to different screen sizes and light/dark modes.

## Installation

Add the extension to your project:

```bash
quarto add ofurkancoban/QuartoProgressIndicatorExtension
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
| <kbd>c</kbd> | Open/Close Settings Menu |
| <kbd>x</kbd> | Toggle Indicator Visibility |

## Interactive Configuration

Press <kbd>c</kbd> during your presentation to open the **Display Settings** panel. From here you can:

- **Themes**: Switch between professional color palettes instantly.
- **Position & Alignment**: Move the indicator to the Top/Bottom or Left/Center/Right.
- **Styling**: Toggle between **Dots** and **Progress Bar** styles.
- **Color Picker**: Fine-tune active and inactive colors with a live picker.
- **Visibility Manager**: Hide the indicator on specific slides or the title slide.
- **Export Config**: Copy your current settings as YAML/CSS to permanently save them in your project.

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
  --dot-size: 8px;
  --section-spacing: 15px;
}
```

## License

MIT License. Feel free to use and contribute!
