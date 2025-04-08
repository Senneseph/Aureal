# Aureal/A3D Archaeology Project - Test Framework

This directory contains test suites and verification tools for the Aureal/A3D Archaeology Project.

## Test Structure

```
/tests
├── scrapers/              # Tests for web scraping tools
│   └── vogons_scraper/    # Tests for VOGONS forum scraper
├── analysis/              # Tests for analysis tools
├── emulation/             # Tests for emulation configurations
└── integration/           # End-to-end integration tests
```

## Running Tests

Most tests can be run using Rust's built-in test framework:

```powershell
# Run all tests
cargo test

# Run specific test suite
cargo test --package vogons_scraper
```

## Test Data

Test data files are stored in the `/tests/data` directory. These include:

- Sample HTML files for scraper testing
- Mock audio data for analysis testing
- Reference outputs for validation

## Adding New Tests

When adding new tests:

1. Create a new test file in the appropriate subdirectory
2. Add any necessary test data to the `/tests/data` directory
3. Document the purpose and expected outcomes of the tests
4. Ensure tests are isolated and do not depend on external resources when possible

## Continuous Integration

In the future, we plan to set up automated testing through GitHub Actions or similar CI services.
