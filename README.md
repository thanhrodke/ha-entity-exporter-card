# Entity Exporter Card for Home Assistant

A custom Lovelace card for filtering and exporting Home Assistant entities as JSON. Easily search, filter, and export entities for configuration, debugging, or backup purposes.

✨ **Created with Vibe Coding** - This card was developed using AI assistance to transform ideas into practical code!

![Entity Exporter Preview](https://raw.githubusercontent.com/thanhrodke/ha-entity-exporter-card/main/images/entity-exporter-card.png)

## Features

- Filter entities by domain type (light, sensor, switch, etc.)
- Add multiple text filters with OR relationship (show entities matching any filter)
- Live filtering preview while typing
- Export filtered entities as JSON
- Copy to clipboard (in HTTPS contexts)
- Download as JSON file
- Real-time counter of filtered entities

## Installation

### HACS (Recommended)
1. Make sure [HACS](https://hacs.xyz/) is installed
2. Add this repository as a custom repository:
   - Go to HACS → Frontend
   - Click the three dots in the top right
   - Select "Custom repositories"
   - Add `https://github.com/scharc/ha-entity-exporter-card` as URL
   - Category: Lovelace
3. Click "Install" on Entity Exporter Card
4. Add the card to your dashboard

### Manual Installation
1. Download `entity-exporter-card.js` from this repository
2. Upload it to your Home Assistant instance under `/config/www/`
3. Add the resource in your Lovelace configuration:
   ```yaml
   resources:
     - url: /local/entity-exporter-card.js
       type: module
   ```
4. Add the card to your dashboard

## Usage

### Configuration
Add the card to your dashboard:
```yaml
type: entity-exporter-card
```

### How to use
1. Select domains to filter entities by checking/unchecking domain boxes
2. Type in the filter input to find specific entities
3. Click "Add Filter" to save filters (multiple filters work as OR conditions)
4. Use the copy or download buttons to export the filtered entities as JSON

## Examples

### Basic Card
```yaml
type: entity-exporter-card
```

### Filtering Tips
- Domain selection is applied first as a pre-filter
- Text filters are then applied to the domain-filtered set of entities
- Multiple text filters function with OR logic (matches any filter)
- The filter preview updates in real-time as you type
- Clipboard button is automatically hidden when not in HTTPS context

## AI-Assisted Home Automation

This card is specifically designed to work as a bridge between AI systems and Home Assistant:

- **Extract structured data** to share with AI assistants for analyzing your setup
- **Generate automations and scripts** by giving AI precise entity information
- **Troubleshoot issues** by exporting problematic entities with their states
- **Speed up configuration** by providing context to AI tools

### Vibe Coding Development

This card was created using what I call "vibe coding" - a collaborative approach between human creativity and AI assistance. The development process involved:

1. Designing the filtering logic and UI components with AI guidance
2. Debugging complex issues like focus retention and clipboard detection
3. Implementing proper integration with Home Assistant's internal APIs
4. Refining the card's behavior based on testing feedback

Read more about this approach in [VIBE_CODING.md](VIBE_CODING.md).

## Contributing

This project welcomes contributions! Ideas, bug reports, and pull requests are all appreciated.

## License

MIT License - See LICENSE file for details
