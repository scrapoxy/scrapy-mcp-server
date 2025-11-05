# Scrapy MCP Server

MCP (Model Context Protocol) server for Scrapy request inspection and debugging.

## Installation & Usage

Use `uvx` to run the MCP server:

```bash
uvx scrapy-mcp-server
```

## Configuration

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

## Requirements

- Python >= 3.8
- Compatible with Windows, Linux, and macOS (Intel & Apple Silicon)

## License

Copyright © 2015–2025 CoreDump Engineering. All rights reserved.
