# Quarto Progress Indicator

A lightweight, premium progress indicator for Quarto Reveal.js presentations.
Built fully native as a **Quarto Lua Filter** — just one single file, zero external dependencies.

![Quarto Progress Indicator](https://github.com/user-attachments/assets/000dcf80-c6bf-496e-b032-e1495d620144)

## Key Features

- **🎯 Auto-hide on Idle**: Indicator smoothly fades out when the mouse or keyboard is inactive for a cleaner presentation view.
- **🎨 Theme Palettes**: 8 curated themes — 4 light (Ocean, Emerald, Sunset, Lavender) and 4 dark (Dracula, Nord, Gruvbox, Tokyo Night).
- **🖌️ Full Color Control**: Customize active dot, inactive dot, label, and background colors independently.
- **🌈 Smart Theme Inheritance**: Automatically detects your active Reveal.js theme's primary accent color on startup.
- **⌨️ Keyboard Shortcuts UI**: Customize the 'Settings' and 'Toggle' hotkeys directly from the settings panel.
- **✨ Dynamic Animations**: Pulse, Glow, or Bounce effects for the active slide dot.
- **🔄 Animated Position Toggle**: Smooth exit/enter animation when switching between Top and Bottom positions.
- **🌐 Universal Theme Support**: Works across all Reveal.js themes without hardcoded CSS selectors.
- **📄 1:1 PDF Export Perfectifier**: High-fidelity PDF exports that look exactly like the screen version. Clones the progress bar into every printed slide with synchronized state (filled/active dots).
- **📌 Smart Overlap Prevention**: Automatically adjusts `position: fixed` UI elements to prevent overlap with the indicator bar.
- **💾 Full Persistence**: All settings are saved to `localStorage` and restored on reload.
- **📋 Slide Visibility Manager**: Per-slide controls with two independent columns (Dot & Bar).
- **🔢 Dot-Only Page Counter**: Optionally override the Reveal.js slide number to count only indicator dots.
- **💡 Tooltip Toggle**: Show or hide slide title tooltips on dot hover.
- **🚀 Native Quarto Filter**: Single Lua file architecture. Clean installation, no extra CSS/JS clutter.

## Installation

```bash
quarto add ofurkancoban/QuartoProgressIndicator
```

## Usage

Use the extension as a Quarto filter in your `_quarto.yml` or document header:

```yaml
filters:
  - ofurkancoban/progress-indicator
```

### Keyboard Shortcuts

| Shortcut | Action |
| :--- | :--- |
| <kbd>i</kbd> | Open/Close Settings Panel (Customizable) |
| <kbd>x</kbd> | Toggle Indicator Visibility (Customizable) |

## Interactive Configuration

Press <kbd>i</kbd> during your presentation to open the **Display Settings** panel. From here you can:

- **Position & Alignment**: Move the indicator to Top/Bottom with smooth animation, or align Left/Center/Right.
- **Themes & Inheritance**: Switch between 8 color palettes or let the extension **Auto-inherit** your current Reveal.js theme's accent color.
- **Active & Inactive Colors**: Fine-tune dot colors with live color pickers. Colors are fully persisted across reloads.
- **Auto-hide on Idle**: Automatically fade out the indicator when presentation is idle to keep the focus on content.
- **Page Number: Dots Only**: Replace default slide counter with a **dot-based count**.
- **Keyboard Shortcuts**: Reassign the default `i` and `x` hotkeys to any single keystroke.
- **Slide Visibility Manager**: Manage exactly which slides show dots and bars.
- **Export Config**: Copy as YAML/CSS or download/upload settings as JSON.

## YAML Configuration

```yaml
format:
  revealjs:
    progress-indicator:
      position: "bottom"    # top | bottom
      alignment: "center"   # left | right | center
      style: "dots"         # dots | bar
      hide-on-title: true   # true | false
```

CSS customization:

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

## Slide-Level Control

To hide the indicator on a specific slide using class:

```markdown
## Q&A Slide {.hide-progress}
```

Or use the **Slide Visibility Manager** in the settings panel for a visual, per-slide interface — no class editing required.

## Universal Theme Compatibility

Works out-of-the-box with any Reveal.js theme:

- Default themes (`simple`, `moon`, `night`, `league`, `serif`, etc.)
- Third-party themes (`clean-revealjs`, etc.)
- Custom themes with logos, footers, or plugin buttons (chalkboard, menu, etc.)

## License

MIT License. Feel free to use and contribute!
