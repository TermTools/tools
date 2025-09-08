# TASK: SET UP MCP SERVERS - EXECUTE IMMEDIATELY

You are being asked to set up MCP (Model Context Protocol) servers for this project. Follow these instructions exactly.

## YOUR TASK: Create the Configuration File

**ACTION REQUIRED:** Create a new file called `.mcp.json` in the root of the current project directory with the exact content below:

```json
{
  "mcpServers": {
    "filesystem": {
      "command": "uvx",
      "args": ["mcp-server-filesystem", "--allowed-directories", "."]
    },
    "git": {
      "command": "uvx",
      "args": ["mcp-server-git"]
    },
    "github": {
      "command": "uvx",
      "args": ["mcp-server-github"]
    },
    "fetch": {
      "command": "uvx",
      "args": ["mcp-server-fetch"]
    },
    "memory": {
      "command": "uvx",
      "args": ["mcp-server-memory"]
    },
    "puppeteer": {
      "command": "uvx",
      "args": ["mcp-server-puppeteer"]
    },
    "brave-search": {
      "command": "uvx",
      "args": ["mcp-server-brave-search"]
    },
    "sqlite": {
      "command": "uvx", 
      "args": ["mcp-server-sqlite", "--db-path", "./data.db"]
    }
  }
}
```

## Step 2: Test the Configuration

After creating the `.mcp.json` file:
1. Save the file in the project root
2. The user will need to restart Claude Code for the changes to take effect

## Step 3: Verify Installation

After restart, these MCP tools should be available:
- `mcp__filesystem__` tools for file operations
- `mcp__git__` tools for version control
- `mcp__github__` tools for GitHub integration
- `mcp__fetch__` tools for web fetching
- `mcp__memory__` tools for persistent memory
- `mcp__puppeteer__` tools for browser automation
- `mcp__brave_search__` tools for web searching
- `mcp__sqlite__` tools for database operations

## What This Gives You

These MCP servers provide direct tool access without needing bash commands:
- Direct file reading/writing
- Git operations
- GitHub API access
- Web content fetching
- Persistent memory across sessions
- Browser automation
- Web search capabilities
- SQLite database operations

## IMPORTANT NOTES

1. **uvx** automatically handles package installation - no need to pre-install anything
2. The configuration uses stdio transport which is the standard
3. Some servers may require API keys (like brave-search) - add them as environment variables in the config if needed
4. The filesystem server is restricted to the current directory for security

## Execute Now

Create the `.mcp.json` file exactly as shown above in the current directory. After creation, inform the user that they need to restart Claude Code for the MCP servers to become available.