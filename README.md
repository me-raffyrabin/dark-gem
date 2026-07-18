# RPG World Builder — Photo Edition

A standalone, browser-based tool for building interactive landscapes and characters for React Native (or any) RPG games. Now with **photo import**!

## What's New

### Landscape from Photo
- Drag & drop or click to upload any photo
- The app resamples the image to your map dimensions
- Each pixel is matched to the closest tile color
- One-click "Convert to map" generates the full tile grid
- Great for turning real-world terrain photos, sketches, or concept art into playable maps

### Character from Photo
- Upload a character portrait or reference image
- Click "Extract colors" to auto-detect:
  - **Hair color** from the top region
  - **Skin tone** from the center/face region
  - **Outfit color** from the lower/body region
- Colors are instantly applied to the SVG preview
- Fine-tune manually after extraction

## Features

- **Landscape Editor**: Paint tile-based maps with 10 terrain types
- **Character Creator**: Build unlimited heroes with stats, equipment, and skills
- **Photo-to-Game Pipeline**: Import photos for both landscapes and characters
- **Export**: Structured JSON ready for your game engine

## Quick Start

1. Open `index.html` in any modern browser
2. No build step, no server, no dependencies
3. Your work auto-saves to browser localStorage

## React Native Integration

The exported JSON follows this schema:

```json
{
  "version": "1.0",
  "generated": "2026-07-18T00:00:00.000Z",
  "maps": [
    {
      "id": "map_forest_realm",
      "name": "Forest Realm",
      "width": 12,
      "height": 10,
      "tileset": { "grass": { "name": "Grass", "color": "#7cb342" }, ... },
      "layers": [
        { "name": "ground", "tiles": ["grass", "grass", "water", ...] }
      ]
    }
  ],
  "characters": [
    {
      "id": "c123abc",
      "name": "Hero 1",
      "class": "Warrior",
      "level": 1,
      "stats": { "str": 10, "dex": 10, "int": 10, "con": 10, "wis": 10, "cha": 10 },
      "colors": { "skin": "#ffccaa", "hair": "#5d4037", "outfit": "#1976d2" },
      "equipment": { "weapon": "Iron Sword", "armor": "Leather Vest", "accessory": "None" },
      "skills": ["Attack", "Defend"]
    }
  ]
}
```

## File Structure

```
rpg-world-builder/
├── index.html      # The complete app (HTML + CSS + JS)
└── README.md       # This file
```

## License

MIT — use it freely in your games.
