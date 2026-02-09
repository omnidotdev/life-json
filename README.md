<div align="center">

# life.json Schema

JSON Schema specification for portable digital identity

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE.md)

</div>

## Overview

life.json is your **portable digital identity**, not a data warehouse.

- **Actual data** - Identity, preferences, assistant context (small, truly portable)
- **References** - Accounts, memories, knowledge, finances (pointers to where data lives)

The anti-lock-in value comes from knowing **where** all your data lives and having **export paths** from each product.

## Slices

| Slice | Type | Description |
|-------|------|-------------|
| `identity` | Actual data | Name, timezone, locale, bio |
| `preferences` | Actual data | Language, theme, communication style |
| `assistants` | Actual data | Per-assistant learned context |
| `accounts` | References | Connected platform accounts |
| `social` | References | Social profiles and links |
| `relationships` | References | Key people and connections |
| `calendar` | References + prefs | Calendar refs and scheduling preferences |
| `memories` | References | Pointers to photos, videos, moments |
| `knowledge` | References | Pointers to notes and knowledge bases |
| `finances` | References + prefs | Account refs and financial preferences |

## Usage

```json
{
  "$schema": "https://life.omni.dev/life.schema.json",
  "identity": {
    "name": "Brian",
    "timezone": "America/Los_Angeles"
  },
  "preferences": {
    "language": "en",
    "theme": "dark"
  }
}
```

## Validation

```bash
npx ajv validate -s life.schema.json -d examples/minimal.json
```

## License

The code in this repository is licensed under MIT, &copy; [Omni LLC](https://omni.dev). See [LICENSE.md](LICENSE.md) for more information.
