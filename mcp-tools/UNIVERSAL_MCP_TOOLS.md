# 🛠️ Universal MCP Tools List
**Generic tools that work in every project**

---

## 🔀 **Git Tools**
- `mcp__git__git_status` - Get repository status
- `mcp__git__git_diff` - Show file differences  
- `mcp__git__git_log` - Show commit history
- `mcp__git__git_commit` - Create commits
- `mcp__git__git_add` - Stage files
- `mcp__git__git_branch` - Manage branches

## ⏰ **Time Tools**
- `mcp__time__get_current_time` - Get current date and time
- `mcp__time__convert_time` - Convert between timezones

## 🌐 **Web Fetch Tools**
- `mcp__fetch__fetch` - Fetch web content
- `mcp__fetch__fetch_json` - Fetch JSON APIs
- `mcp__fetch__fetch_html` - Fetch and parse HTML

## 📁 **File System Tools**
- `mcp__filesystem__list_directory` - List directory contents
- `mcp__filesystem__read_file` - Read file contents
- `mcp__filesystem__write_file` - Write to files
- `mcp__filesystem__search_files` - Search for files

---

## ⚙️ **Simple Setup**

Add to `.mcp.json`:

```json
{
  "mcpServers": {
    "git": {
      "command": "uvx",
      "args": ["mcp-server-git"]
    },
    "time": {
      "command": "uvx", 
      "args": ["mcp-server-time"]
    },
    "fetch": {
      "command": "uvx",
      "args": ["mcp-server-fetch"]
    }
  }
}
```

---

**These 4 categories cover the essentials for any development project.**