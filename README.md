# Apple IIe Wikipedia Application

A Wikipedia-like knowledge base application for the Apple IIe computer running DOS 3.3.

## Overview

This project brings a searchable encyclopedia to the Apple IIe, featuring:
- **Full-text search** across articles
- **Indexed browsing** by category
- **Hyperlink navigation** between related topics
- **Storage-efficient data format** for floppy disk compatibility
- **DOS 3.3 native** compatibility (no additional loaders needed)

## System Requirements

- Apple IIe computer
- DOS 3.3 Master Disk (original or clone)
- Minimum 48KB RAM (64KB recommended)
- Single 5.25" floppy drive (more drives for larger databases)

## Installation

1. Boot with DOS 3.3 master disk
2. Insert WIKI disk when prompted
3. Type: `RUN WIKI` and press ENTER
4. Follow on-screen menu

## Features

### Main Menu
- Search articles by keyword
- Browse by category
- View article index
- Configure settings

### Article Display
- Full text with word wrapping
- Embedded cross-references (marked with *)
- Page-by-page navigation
- Return to menu option

### Search System
- Case-insensitive matching
- Partial word search
- Category filtering
- Relevance ranking

## File Structure

```
WIKI.SYSTEM    - Main application (Applesoft BASIC + Machine Language)
WIKI.ARTICLES  - Compressed article database
WIKI.INDEX     - Fast lookup index
WIKI.CATS      - Category definitions
WIKI.CONFIG    - User settings and preferences
```

## Memory Layout

```
$0000 - $9FFF  - Applesoft BASIC & data (40KB)
$A000 - $BFFF  - Reserved for BASIC program
$C000 - $CFFF  - I/O & ROM
$D000 - $FFFF  - DOS 3.3 reserved
```

## Article Format

Articles are stored in a compressed text format:
- Keywords stored as 2-byte tokens
- Cross-references as special markers
- Metadata (author, date, category) in header

## Usage Commands

| Command | Description |
|---------|-------------|
| `SEARCH TEXT` | Find articles containing TEXT |
| `BROWSE CATEGORY` | List articles in category |
| `READ ARTICLE#` | Display specific article |
| `INDEX` | Show complete article list |
| `HELP` | Display help information |

## Development Status

- [x] Core article system
- [x] Search engine
- [x] DOS 3.3 integration
- [x] Basic UI framework
- [ ] Article compression
- [ ] Network sync (future)

## License

Public Domain - Share freely on vintage computing networks

## Author

Created for the Apple IIe community - 2026

---

*The Apple IIe belongs to Apple Computer, Inc. DOS 3.3 is a trademark of Apple Computer, Inc.*
