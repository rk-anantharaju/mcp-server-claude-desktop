# mcp-server-claude-desktop
Integrate Local MCP server with Claude Desktop, this uses stdio transport mode.


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
```


This tells Claude Desktop:

- Start a local process
- Use /path/to/python as the executable and run mcp-server.py
- Communicate with it over stdio, which is the default MCP transport when no transport is specified.
<br>


<br/>

**How to Check the intergration?**
Restart Claude Desktop app after updating the config. Try with a sample query as shown,

<img width="600" height="500" alt="claude-sample-output" src="https://github.com/user-attachments/assets/13371e86-caef-42b6-b0c9-7f311ff7a175" />

