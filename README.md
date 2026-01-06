# Ghostty Settings Visual Config

A beautiful, interactive settings generator for the [Ghostty](https://ghostty.org) terminal emulator. Generate your `~/.config/ghostty/config` file with a visual interface.

**Live Demo:** [GitHub Pages](https://ventz.github.io/ghostty-settings-visual-config/)

## Features

- **Visual Settings Editor**: Configure all commonly-used Ghostty settings through an intuitive UI
- **Real-time Config Generation**: See your configuration update as you make changes
- **Live Preview**: Visual preview of your terminal appearance (colors, fonts, cursor)
- **Config Import**: Paste existing config to populate the form
- **Color Palette Picker**: Visual editor for all 16 ANSI colors
- **Keybind Builder**: Visual builder for custom keybindings with modifier keys and actions
- **Copy to Clipboard**: One-click copy of generated config
- **Helpful Comments**: Generated config includes descriptions and valid options for each setting

## Usage

1. Open `index.html` in your browser (or visit the GitHub Pages demo)
2. Configure your settings using the visual interface
3. Copy the generated config
4. Save to `~/.config/ghostty/config`

## Settings Categories

- **Fonts**: Font family, size, thickening, synthetic styles, font variants
- **Colors & Theme**: Theme selection, background/foreground colors, contrast
- **Color Palette**: 16 ANSI colors (normal and bright variants)
- **Cursor**: Style, color, opacity, blinking
- **Background Effects**: Opacity, blur, background images
- **Window**: Padding, decorations, dimensions, resize overlay
- **Mouse & Input**: Scroll speed, focus follows mouse, click behavior
- **Clipboard**: Read/write permissions, copy-on-select, paste protection
- **Shell & Command**: Shell command, integration, scrollback, notifications
- **Keybindings**: Custom keyboard shortcuts with visual builder
- **macOS Settings**: Titlebar style, Option key, dock icon customization
- **Linux/GTK Settings**: Tab bar, single instance, Adwaita styling
- **Quick Terminal**: Position, size, screen, animation

## Intentionally Skipped Settings

The following obscure/advanced settings are intentionally not included in the visual generator. These are rarely needed and can be added manually to your config file if required:

### Terminal Protocol Settings
- `vt-kam-allowed` - VT keyboard action mode
- `enquiry-response` - Response to ENQ character
- `osc-color-report-format` - OSC color report format (8-bit, 16-bit, none)
- `title` - Hardcoded window title
- `title-report` - Title reporting (for tmux, etc.)
- `term` - TERM environment variable (included in Shell section but rarely changed)

### Advanced Graphics/Rendering
- `grapheme-width-method` - Unicode grapheme width calculation method
- `freetype-load-flags` - FreeType font loading flags
- `image-storage-limit` - Inline image storage limit
- `alpha-blending` - Alpha blending mode
- `font-codepoint-map` - Custom Unicode codepoint to font mapping

### Fine-tuning Adjustments
- `adjust-cell-width` - Cell width adjustment
- `adjust-cell-height` - Cell height adjustment
- `adjust-font-baseline` - Font baseline adjustment
- `adjust-underline-position` - Underline position adjustment
- `adjust-underline-thickness` - Underline thickness adjustment
- `adjust-strikethrough-position` - Strikethrough position adjustment
- `adjust-strikethrough-thickness` - Strikethrough thickness adjustment
- `adjust-cursor-thickness` - Cursor thickness adjustment
- `adjust-cursor-height` - Cursor height adjustment
- `adjust-box-thickness` - Box drawing thickness adjustment
- `adjust-overline-position` - Overline position adjustment
- `adjust-overline-thickness` - Overline thickness adjustment

### Linux-specific Advanced Settings
- `linux-cgroup` - Linux cgroup usage
- `linux-cgroup-memory-limit` - cgroup memory limit
- `linux-cgroup-processes-limit` - cgroup process limit
- `linux-cgroup-hard-fail` - Fail if cgroup unavailable
- `x11-instance-name` - X11 instance name (WM_CLASS)
- `class` - Window class name
- `gtk-custom-css` - Custom GTK CSS path
- `async-backend` - Async I/O backend

### Link/URL Settings
- `link` - Custom link patterns
- `link-url` - URL pattern matching

### Config Management
- `config-file` - Additional config file path
- `config-default-files` - Load default config files
- `custom-shader` - Custom OpenGL shader path
- `custom-shader-animation` - Shader animation mode

### Other Advanced Settings
- `font-variation` - Font variation settings (OpenType)
- `font-variation-bold` / `font-variation-italic` / `font-variation-bold-italic` - Per-style variations
- `window-new-tab-position` - New tab position
- `window-inherit-working-directory` - Inherit working directory
- `window-inherit-font-size` - Inherit font size
- `auto-update` - Auto-update behavior (macOS)
- `app-notifications` - Application notifications
- `quit-after-last-window-closed` - Quit behavior (macOS)

## Development

This is a single-file static HTML application with no build process or dependencies. Simply edit `index.html` and open in a browser.

### Useful Ghostty Commands

```bash
# List available fonts
ghostty +list-fonts

# List available themes
ghostty +list-themes

# Show current config
ghostty +show-config

# Validate config
ghostty +validate-config
```

## License

MIT

## Credits

Made with love by [ventz](https://github.com/ventz) for the Ghostty terminal emulator community.
