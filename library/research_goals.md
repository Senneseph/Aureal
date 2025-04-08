# Aureal/A3D Research Library

## Overview
Central knowledge base for the Aureal/A3D Archaeology Project, implemented as a wiki-style documentation system.

## Project Structure
```
/
├── library/              # Central knowledge base
│   ├── wiki/            # Wiki content
│   │   ├── technical/   # Technical documentation
│   │   ├── historical/  # Historical research
│   │   ├── legal/      # Legal documentation
│   │   └── research/   # Research findings
│   ├── citations/       # Source citations and references
│   ├── snapshots/      # Point-in-time documentation captures
│   └── assets/         # Shared media and resources
├── labs/                # Research and development labs
├── src/                 # Source code
├── docs/                # Project documentation
└── tests/              # Test suites
```

## Integration Points
- Labs reference library content using `@lib:path/to/article`
- Citations managed through `@cite:key` references
- Assets linked via `@asset:filename`

## Setup and Usage
[Setup instructions moved to SETUP.md]

## Contributing
1. Check existing documentation before creating new pages
2. Follow the citation guidelines in CITATIONS.md
3. Create snapshots before major changes
4. Cross-reference between lab documents and wiki pages

