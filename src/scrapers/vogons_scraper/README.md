# VOGONS Forum Scraper

A web scraper designed to collect information about Aureal/A3D technology from the VOGONS (Very Old Games On New Systems) forums.

## Purpose

This tool is part of the Aureal/A3D Archaeology Project. It automates the collection of forum posts, discussions, and technical information related to Aureal Semiconductor's A3D technology from the VOGONS community, which is a valuable resource for information about vintage hardware and software.

## Features

- Scrapes the VOGONS forum for posts related to Aureal/A3D technology
- Filters content based on configurable search terms
- Saves results in structured JSON format
- Configurable depth and scope of scraping
- Respects the forum's robots.txt and implements rate limiting

## Usage

```bash
# Basic usage with default settings
cargo run

# Specify custom parameters
cargo run -- --url "https://vogons.org/viewforum.php?f=46" --max-pages 20 --output "aureal_data.json" --search-terms "Aureal,A3D,Vortex,SQ2500"
```

### Command Line Options

- `-u, --url <URL>`: Starting URL for scraping (default: VOGONS sound card forum)
- `-m, --max-pages <NUMBER>`: Maximum number of pages to scrape (default: 10)
- `-o, --output <FILE>`: Output file path (default: vogons_data.json)
- `-s, --search-terms <TERMS>`: Comma-separated list of search terms (default: "Aureal,A3D,Vortex")

## Output Format

The scraper produces a JSON file with the following structure:

```json
{
  "forum_name": "VOGONS",
  "posts": [
    {
      "title": "Post title",
      "url": "https://vogons.org/viewtopic.php?t=12345",
      "author": "Username",
      "date": "2023-01-01",
      "content": "Post content...",
      "relevance_score": 0.85
    },
    ...
  ],
  "search_terms": ["Aureal", "A3D", "Vortex"],
  "total_pages_scraped": 10
}
```

## Ethical Considerations

This scraper is designed to:
- Respect the VOGONS forum's robots.txt
- Implement appropriate rate limiting to avoid server load
- Only collect publicly available information
- Be used for research purposes only

## Development Status

This is an initial implementation with placeholder functionality. The actual scraping logic needs to be refined based on the VOGONS forum structure and further testing.

## Next Steps

1. Refine the HTML selectors based on actual VOGONS forum structure
2. Implement proper pagination handling
3. Add content relevance scoring
4. Improve error handling and recovery
5. Add tests and validation
