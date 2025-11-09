# Scrapy MCP Server

**The Self-Healing Revolution for Web Scraping**

MCP (Model Context Protocol) server that enables AI-powered automatic repair of Scrapy spiders. When websites change, your scrapers fix themselves.

## The Problem

Web scrapers break constantly. Websites change structure, deploy A/B tests with different HTML layouts, implement new anti-bot protections, or update their design without notice. Selectors stop working, parsing logic fails, and data pipelines break. Until now, fixing broken scrapers meant manual debugging sessions and emergency fixes.

**Not anymore.**

## Self-Healing: The Game Changer

`scrapy-mcp-server` brings autonomous repair to web scraping infrastructure. AI assistants can inspect live requests, analyze what changed, and automatically fix broken spiders - without human intervention.

### How It Works

`scrapy-mcp-server` provides the debugging capabilities. Combined with monitoring systems and CI/CD automation (integration not included), the workflow becomes:

1. **Monitor detects spider failure** (empty results, errors, data quality issues)
2. **Automatically triggers GitHub Action** (or any CI/CD system)
3. **AI debugs the spider via MCP** - analyzes requests, responses, and HTML structure
4. **Generates the fix** - updated selectors, parsing logic, anti-bot handling, API fallbacks
5. **Creates pull request** with the repaired spider ready for review
6. **Review and merge** (or auto-merge with confidence)

This transforms scraping infrastructure from brittle and high-maintenance to resilient and self-sustaining.

## Tested Against Real-World Scenarios

`scrapy-mcp-server` has been validated against common scraping challenges:

- ✅ **Website Structure Changes** - Layout updates, CSS class modifications
- ✅ **A/B Testing** - Multiple HTML variants served randomly
- ✅ **Anti-Bot Detection** - Identifying and adapting to protection mechanisms
- ✅ **API Integration** - Automatic fallback to services like Zyte API when needed

## Capabilities

AI assistants using `scrapy-mcp-server` can:

- 🔍 **Inspect** live Scrapy requests and responses
- 🐛 **Debug** broken spiders by analyzing HTML structure changes
- 🔧 **Fix** selectors and parsing logic automatically
- 🔄 **Self-Heal** entire scraping infrastructure

## Quick Start

### Installation

Run the MCP server using `uvx`:

```bash
uvx scrapy-mcp-server
```

### Configuration

Add to your MCP client configuration (e.g., Claude Desktop):

```json
{
  "mcpServers": {
    "scrapy-inspector": {
      "command": "uvx",
      "args": ["scrapy-mcp-server"]
    }
  }
}
```

## Usage Example

Once configured, AI assistants can help fix broken spiders:

```markdown
# Fix Scrapy Spider: Example Data Collection

Fix an existing Scrapy spider that collects data from a target website.

## Task

1. Inspect the existing code: spider in `myproject/spiders/example.py` and items in `myproject/items.py`
2. Run the spider to confirm it's no longer collecting data: `scrapy crawl example`
3. Debug and fix the spider using the **MCP scrapy-inspector** tool

Note: Start with the `create_spider` tool to understand the spider development and debugging logic.

## Environment

- **Python:** 3.13.1 (with virtual environment `.venv`)
- **Scrapy:** 2.13.3 (with Scrapy project `myproject`)
```

The AI assistant will analyze the spider, identify what changed on the website, and provide the necessary fixes.

## Use Cases

- **Production Monitoring**: Automatically repair spiders when websites change structure
- **Zero-Downtime Scraping**: Detect and fix issues before they impact data pipelines
- **Scale Operations**: Maintain hundreds of spiders without proportional maintenance overhead
- **Development Speed**: Fix broken spiders in minutes instead of hours
- **Team Efficiency**: Consistent debugging approach across all developers

## Why This Changes Everything

Traditional web scraping requires constant manual maintenance. Every website change, A/B test deployment, or anti-bot update means developer time, emergency fixes, and data pipeline interruptions.

With self-healing capabilities:
- **Reduce maintenance time by 90%+**
- **Fix issues before they impact production**
- **Scale scraping operations without scaling teams**
- **Handle A/B testing and anti-bot measures automatically**

## Requirements

- Python >= 3.8
- Compatible with Windows, Linux, and macOS (Intel & Apple Silicon)
- MCP-compatible AI assistant (Claude, etc.)

## Why MCP?

The Model Context Protocol provides a standardized way for AI assistants to interact with development tools. This means:

- Works with any MCP-compatible AI assistant
- Secure local execution
- No data leaves your machine
- Extensible and future-proof

## License

Copyright © 2015–2025 CoreDump Engineering. All rights reserved.
