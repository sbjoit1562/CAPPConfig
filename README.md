# CAPP Config

Configuration file for CAPP application with version management and "What's New" features.

## Overview

This repository contains the configuration file for CAPP (Chrome Application) that includes:
- Version management with semantic versioning
- "What's New" information for different releases
- Promotional content and branding

## Configuration Structure

The main configuration file is `chrome-config.json` which includes:

### Version Management
- `latestVersion`: Current version of the application
- Version-based "What's New" entries with detailed release information

### What's New Features
Each version entry includes:
- Version number and release date
- Title and description
- Features list
- Improvements list
- Call-to-action button with URL

### Promotional Content
- "Made by Core Team" branding text

## Usage

### Accessing the Configuration
```javascript
// Fetch the configuration
fetch('https://raw.githubusercontent.com/sbjoit1562/CAPPConfig/main/chrome-config.json')
  .then(response => response.json())
  .then(config => {
    console.log('Latest version:', config.latestVersion);
    console.log('What\'s new:', config.whats_new[config.latestVersion]);
  });
```

### Getting What's New for a Specific Version
```javascript
const version = '1.0.0';
const whatsNew = config.whats_new[version];
if (whatsNew) {
  console.log('Features:', whatsNew.features);
  console.log('Improvements:', whatsNew.improvements);
}
```

## Adding New Versions

When releasing a new version:

1. Update the `latestVersion` field
2. Add a new entry to the `whats_new` object:

```json
"1.1.0": {
  "version": "1.1.0",
  "releaseDate": "2024-02-01",
  "title": "Feature Update",
  "description": "New features and improvements in this release.",
  "features": [
    "New feature 1",
    "New feature 2"
  ],
  "improvements": [
    "Performance improvements",
    "Bug fixes"
  ],
  "cta_text": "View Release Notes",
  "cta_url": "https://github.com/sbjoit1562/CAPPConfig/releases/tag/v1.1.0"
}
```

## Repository Information

- **Repository**: https://github.com/sbjoit1562/CAPPConfig
- **Maintained by**: Core Team
- **Latest Version**: 1.0.0

## Contributing

This configuration is maintained by the Core Team. For updates or changes, please contact the maintainers.

## License

This project is maintained by the Core Team for internal use.
