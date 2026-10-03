# vibin-themes

Repository containing theme assets for VIBIN Launcher.

## Structure

```
vibin-themes/
├── themes.json          # Manifest listing all available themes
├── teams.json           # Manifest listing selectable teams
├── ayanokoji/           # Theme folder (id = "ayanokoji")
│   ├── logo.png         # Theme logo
│   ├── wallpaper.gif    # Animated wallpaper (optional)
│   ├── wallpaper.png    # Static wallpaper fallback
│   └── preview.png      # Preview image shown in theme picker
```

## themes.json format

```json
{
  "version": "1.0",
  "themes": [
    {
      "id": "ayanokoji",
      "name": "Ayanokoji",
      "folder": "ayanokoji",
      "seedColor": "0xFFFF9800",
      "accentColor": "0xFFFF6D00",
      "scaffoldColor": "0xFF0A0605",
      "surfaceColor": "0xFF1A0E0C",
      "onSurfaceColor": "0xFFFFEDE8",
      "glassTintBase": "0xFFFF7043",
      "glassSurfaceAlpha": 0.14,
      "glassShadowAlpha": 0.32,
      "logo": "logo.png",
      "wallpaperGif": "wallpaper.gif",
      "wallpaperPng": "wallpaper.png",
      "preview": "preview.png"
    }
  ]
}
```

## Adding a new theme

1. Create a new folder with the theme id (e.g., `mytheme/`)
2. Add `logo.png`, `wallpaper.png` (or `wallpaper.gif`), and `preview.png`
3. Add an entry to `themes.json` with the theme's colors and asset filenames
4. Push to the `main` branch

The launcher will automatically fetch `themes.json` on startup and show
downloadable themes in the theme picker.
