# EXECUTE THIS: Complete MCP Server Setup

**YOUR TASK:** Set up MCP (Model Context Protocol) servers for this project by following these instructions exactly.

---

## STEP 1: Create the Configuration File

**ACTION REQUIRED:** Create a new file called `.mcp.json` in the root of the current project directory with the following content:

```json
{
  "mcpServers": {
    "everything": {
      "command": "mcp-server-everything",
      "args": ["--transport", "stdio"]
    },
    "fetch": {
      "command": "mcp-server-fetch", 
      "args": ["--transport", "stdio"]
    },
    "filesystem": {
      "command": "mcp-server-filesystem",
      "args": ["--transport", "stdio"],
      "env": {
        "ALLOWED_DIRECTORIES": "."
      }
    },
    "git": {
      "command": "mcp-server-git",
      "args": ["--transport", "stdio"]
    },
    "github": {
      "command": "mcp-server-github",
      "args": ["--transport", "stdio"]
    },
    "memory": {
      "command": "mcp-server-memory", 
      "args": ["--transport", "stdio"]
    },
    "sequential-thinking": {
      "command": "mcp-server-sequential-thinking",
      "args": ["--transport", "stdio"]
    },
    "time": {
      "command": "mcp-server-time",
      "args": ["--transport", "stdio"]
    },
    "puppeteer": {
      "command": "mcp-server-puppeteer",
      "args": ["--transport", "stdio"]
    },
    "sqlite": {
      "command": "mcp-server-sqlite",
      "args": ["--transport", "stdio", "--db-path", "./data.db"]
    }
  }
}
```

---

## STEP 2: Install the MCP Servers

**ACTION REQUIRED:** Run these installation commands to install all MCP servers globally:

```bash
# Install all official MCP reference servers
npm install -g @modelcontextprotocol/server-everything
npm install -g @modelcontextprotocol/server-fetch  
npm install -g @modelcontextprotocol/server-filesystem
npm install -g @modelcontextprotocol/server-git
npm install -g @modelcontextprotocol/server-memory
npm install -g @modelcontextprotocol/server-sequential-thinking
npm install -g @modelcontextprotocol/server-time

# Install additional useful servers
npm install -g @modelcontextprotocol/server-github
npm install -g @modelcontextprotocol/server-puppeteer
npm install -g @modelcontextprotocol/server-sqlite
```

**ALTERNATIVE:** If npm packages don't exist with those exact names, try the uvx approach:

Update the `.mcp.json` file to use uvx commands instead:
- Replace `"command": "mcp-server-NAME"` with `"command": "uvx"`
- Replace `"args": ["--transport", "stdio"]` with `"args": ["mcp-server-NAME"]`

Example for git server:
```json
"git": {
  "command": "uvx",
  "args": ["mcp-server-git"]
}
```

---

## STEP 3: Verify and Complete Setup

After creating the `.mcp.json` file and installing servers:

1. **Save the .mcp.json file** in the project root directory
2. **Inform the user** that they need to restart Claude Code for the changes to take effect
3. **After restart**, these MCP tools should be available:

### Expected Tools After Setup:

#### 🔧 Everything Server (Test/Reference)
- `mcp__everything__test_tool`
- `mcp__everything__demo_prompt`
- `mcp__everything__example_resource`
- `mcp__everything__debug_info`

#### 🌐 Fetch Server (Web Content)
- `mcp__fetch__get` - Fetch URL content
- `mcp__fetch__get_html` - Fetch and parse HTML
- `mcp__fetch__get_text` - Extract plain text
- `mcp__fetch__get_json` - Fetch JSON APIs

#### 📁 Filesystem Server (File Operations)
- `mcp__filesystem__read_file` - Read file contents
- `mcp__filesystem__write_file` - Write to files
- `mcp__filesystem__list_directory` - List directory contents
- `mcp__filesystem__search_files` - Search for files
- `mcp__filesystem__get_file_info` - File metadata
- `mcp__filesystem__create_directory` - Create directories
- `mcp__filesystem__move_file` - Move/rename files
- `mcp__filesystem__delete_file` - Delete files

#### 🔀 Git Server (Version Control)
- `mcp__git__status` - Get repository status
- `mcp__git__log` - Show commit history
- `mcp__git__diff` - Show file differences
- `mcp__git__show` - Show commit details
- `mcp__git__branch` - Branch operations
- `mcp__git__add` - Stage files
- `mcp__git__commit` - Create commits
- `mcp__git__search` - Search repository content

#### 🐙 GitHub Server (GitHub Integration)
- `mcp__github__create_issue` - Create GitHub issues
- `mcp__github__create_pull_request` - Create PRs
- `mcp__github__list_issues` - List repository issues
- `mcp__github__list_pull_requests` - List PRs
- `mcp__github__get_issue` - Get issue details
- `mcp__github__get_pull_request` - Get PR details

#### 🧠 Memory Server (Persistent Storage)
- `mcp__memory__store` - Store information
- `mcp__memory__retrieve` - Retrieve stored data
- `mcp__memory__search` - Search memory content
- `mcp__memory__create_entity` - Create knowledge entities
- `mcp__memory__create_relationship` - Link entities
- `mcp__memory__get_graph` - Retrieve knowledge graph
- `mcp__memory__update_entity` - Update stored information

#### 🤔 Sequential Thinking Server (Problem Solving)
- `mcp__sequential_thinking__analyze` - Analyze complex problems
- `mcp__sequential_thinking__plan` - Create step-by-step plans
- `mcp__sequential_thinking__reflect` - Reflect on approaches
- `mcp__sequential_thinking__iterate` - Iterative problem solving
- `mcp__sequential_thinking__synthesize` - Combine insights

#### ⏰ Time Server (Time Operations)
- `mcp__time__current` - Get current time
- `mcp__time__convert` - Convert between timezones
- `mcp__time__format` - Format time strings
- `mcp__time__parse` - Parse time from strings
- `mcp__time__add` - Add time periods
- `mcp__time__subtract` - Subtract time periods
- `mcp__time__compare` - Compare times

#### 🌐 Puppeteer Server (Browser Automation)
- `mcp__puppeteer__screenshot` - Take screenshots
- `mcp__puppeteer__scrape` - Scrape web pages
- `mcp__puppeteer__click` - Click elements
- `mcp__puppeteer__type` - Type text
- `mcp__puppeteer__navigate` - Navigate to URLs

#### 💾 SQLite Server (Database)
- `mcp__sqlite__query` - Execute SQL queries
- `mcp__sqlite__execute` - Execute SQL commands
- `mcp__sqlite__list_tables` - List database tables
- `mcp__sqlite__describe_table` - Get table schema

---

## TROUBLESHOOTING

If tools aren't available after restart:

1. **Check if npm packages exist:** The npm package names might be different. Try:
   - Search for packages: `npm search @modelcontextprotocol`
   - Or use the uvx approach described above

2. **Verify .mcp.json location:** Must be in the project root directory

3. **Check for errors:** Look for any error messages when Claude Code starts

4. **Alternative package names to try:**
   - Instead of `@modelcontextprotocol/server-NAME`
   - Try: `mcp-server-NAME` 
   - Or: `@mcp/server-NAME`

---

## WHAT THIS GIVES YOU

Once set up, you'll have direct access to:
- **File operations** without bash commands
- **Git operations** with structured tools
- **Web fetching** for research and APIs
- **Persistent memory** across sessions
- **Time utilities** for scheduling
- **Problem-solving** assistance
- **Browser automation** capabilities
- **Database** operations

---

## EXECUTION SUMMARY

1. ✅ Create `.mcp.json` file with the configuration above
2. ✅ Try npm installation commands first
3. ✅ If npm fails, modify .mcp.json to use uvx approach
4. ✅ Save file in project root
5. ✅ Tell user to restart Claude Code
6. ✅ Verify tools are available after restart

**START NOW:** Begin with Step 1 - Create the .mcp.json file!