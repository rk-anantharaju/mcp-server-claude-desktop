# mcp-server-claude-desktop
Integrate MCP server with Claude Desktop with stdio transport


**Run the server:**

python mcp-server.py


**Connecting with Cluade Desktop**

Open Config
Profile -> Settings -> Developer -> Edit Config

Add following element in the in the json config file.

```json
  "mcpServers": {
    "text-analysis": {
      "command": "/path/to/python",
      "args": [
        "/path/to/mcp-server/mcp-server.py"
      ]
    }
  }

Restart Claude Desktop app after updating the config.


**How to Check the intergration?**