# EXECUTE THIS: Complete MCP Server Setup

**YOUR TASK:** Set up MCP (Model Context Protocol) servers for this project by following these instructions exactly.

---

## STEP 1: Create the Configuration File

**ACTION REQUIRED:** Create a new file called `.mcp.json` in the root of the current project directory with the following content:

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
    "sqlite": {
      "command": "uvx", 
      "args": ["mcp-server-sqlite", "--db-path", "./data.db"]
    },
    "time": {
      "command": "uvx",
      "args": ["mcp-server-time"]
    },
    "sequential-thinking": {
      "command": "uvx",
      "args": ["mcp-server-sequential-thinking"]
    },
    "everything": {
      "command": "uvx",
      "args": ["mcp-server-everything"]
    }
  }
}
```

---

## STEP 2: Verify Setup

**NO INSTALLATION NEEDED!** The `uvx` command automatically handles downloading and running the MCP servers on-demand. This is why we use `uvx` - it's a Python tool runner that installs packages automatically when first used.

**Note:** The first time each server is used, `uvx` will download it automatically. This may take a few seconds per server on first use.

---

## STEP 3: Complete Setup

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

1. **Verify uvx is installed:** Run `which uvx` to confirm uvx is available
   - If not installed, install with: `pip install uv`

2. **Verify .mcp.json location:** Must be in the project root directory

3. **Check for errors:** Look for any error messages when Claude Code starts

4. **Test a server manually:** Try running `uvx mcp-server-git --help` to verify it works

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