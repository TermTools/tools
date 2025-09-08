# 📚 Complete MCP Reference Guide
**Official ModelContextProtocol Servers - Universal Setup for Every Project**

**Repository:** https://github.com/modelcontextprotocol/servers  
**Generated:** 2025-09-07  
**Purpose:** Universal MCP setup for any development project

---

## 🎯 **Overview**

The official ModelContextProtocol reference servers provide a comprehensive toolkit that works with **any programming language, framework, or project type**. These 7 servers give Claude enhanced capabilities for development, research, and automation.

**`★ Insight ─────────────────────────────────────`**
**Reference Implementation Quality:** These are the canonical, official implementations maintained by the MCP team - ensuring reliability and consistent updates.
**Universal Compatibility:** Works across all project types - React, Python, Go, Rust, PHP, etc. - no project-specific dependencies.
**Complete Development Coverage:** The 7 servers cover every major development need from version control to advanced reasoning.
**`─────────────────────────────────────────────────`**

---

## 🔧 **Quick Setup (Copy-Paste)**

### **1. Installation**
```bash
# Install all official MCP reference servers
npm install -g @modelcontextprotocol/server-everything
npm install -g @modelcontextprotocol/server-fetch  
npm install -g @modelcontextprotocol/server-filesystem
npm install -g @modelcontextprotocol/server-git
npm install -g @modelcontextprotocol/server-memory
npm install -g @modelcontextprotocol/server-sequential-thinking
npm install -g @modelcontextprotocol/server-time
```

### **2. Configuration**
Create `.mcp.json` in project root:
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
    }
  }
}
```

### **3. Activation**
1. Save configuration
2. Restart Claude Code
3. Test tools (see Testing section below)

---

## 📋 **Detailed Server Breakdown**

### **🔧 Everything Server**
**Purpose:** Reference/test server with comprehensive examples

**Capabilities:**
- Demonstration of MCP patterns and capabilities
- Test prompts and resources
- Tool showcases and examples
- Development and debugging utilities

**Expected Tools:**
- `mcp__everything__test_tool`
- `mcp__everything__demo_prompt`
- `mcp__everything__example_resource`
- `mcp__everything__debug_info`

**Use Cases:**
- Learning MCP capabilities
- Testing MCP functionality
- Development and debugging
- Reference implementation examples

---

### **🌐 Fetch Server**
**Purpose:** Web content fetching and conversion optimized for LLM usage

**Capabilities:**
- Fetch web pages and convert to LLM-friendly formats
- Extract text content from HTML
- Handle various web content types
- Respect robots.txt and rate limiting

**Expected Tools:**
- `mcp__fetch__get` - Fetch URL content
- `mcp__fetch__get_html` - Fetch and parse HTML
- `mcp__fetch__get_text` - Extract plain text
- `mcp__fetch__get_json` - Fetch JSON APIs

**Use Cases:**
- Research and information gathering
- API integration
- Content analysis
- Web scraping for development

---

### **📁 Filesystem Server** 
**Purpose:** Secure file operations with configurable access controls

**Capabilities:**
- Safe file reading and writing
- Directory traversal with security controls
- File search and pattern matching
- Access control and permissions

**Expected Tools:**
- `mcp__filesystem__read_file` - Read file contents
- `mcp__filesystem__write_file` - Write to files
- `mcp__filesystem__list_directory` - List directory contents
- `mcp__filesystem__search_files` - Search for files
- `mcp__filesystem__get_file_info` - File metadata
- `mcp__filesystem__create_directory` - Create directories
- `mcp__filesystem__move_file` - Move/rename files
- `mcp__filesystem__delete_file` - Delete files

**Use Cases:**
- Project file management
- Code organization
- Configuration file handling
- Build artifact management

---

### **🔀 Git Server**
**Purpose:** Tools to read, search, and manipulate Git repositories

**Capabilities:**
- Repository status and information
- Commit history and diffs
- Branch management
- File change tracking

**Expected Tools:**
- `mcp__git__status` - Get repository status
- `mcp__git__log` - Show commit history
- `mcp__git__diff` - Show file differences
- `mcp__git__show` - Show commit details
- `mcp__git__branch` - Branch operations
- `mcp__git__add` - Stage files
- `mcp__git__commit` - Create commits
- `mcp__git__search` - Search repository content

**Use Cases:**
- Version control operations
- Code review assistance
- Release management
- Repository analysis

---

### **🧠 Memory Server**
**Purpose:** Knowledge graph-based persistent memory system

**Capabilities:**
- Store and retrieve information across sessions
- Build knowledge graphs of project information
- Maintain context and relationships
- Persistent learning and memory

**Expected Tools:**
- `mcp__memory__store` - Store information
- `mcp__memory__retrieve` - Retrieve stored data
- `mcp__memory__search` - Search memory content
- `mcp__memory__create_entity` - Create knowledge entities
- `mcp__memory__create_relationship` - Link entities
- `mcp__memory__get_graph` - Retrieve knowledge graph
- `mcp__memory__update_entity` - Update stored information

**Use Cases:**
- Project knowledge management
- Cross-session context retention
- Learning from past interactions
- Building project-specific knowledge bases

---

### **🤔 Sequential Thinking Server**
**Purpose:** Dynamic and reflective problem-solving through thought sequences

**Capabilities:**
- Break down complex problems into steps
- Iterative reasoning and reflection
- Multi-step analysis and planning
- Dynamic problem-solving strategies

**Expected Tools:**
- `mcp__sequential_thinking__analyze` - Analyze complex problems
- `mcp__sequential_thinking__plan` - Create step-by-step plans
- `mcp__sequential_thinking__reflect` - Reflect on approaches
- `mcp__sequential_thinking__iterate` - Iterative problem solving
- `mcp__sequential_thinking__synthesize` - Combine insights

**Use Cases:**
- Complex problem decomposition
- Architecture planning
- Debugging complex issues
- System design and analysis

---

### **⏰ Time Server**
**Purpose:** Time and timezone conversion capabilities

**Capabilities:**
- Current time in various formats
- Timezone conversions
- Date calculations
- Time formatting and parsing

**Expected Tools:**
- `mcp__time__current` - Get current time
- `mcp__time__convert` - Convert between timezones
- `mcp__time__format` - Format time strings
- `mcp__time__parse` - Parse time from strings
- `mcp__time__add` - Add time periods
- `mcp__time__subtract` - Subtract time periods
- `mcp__time__compare` - Compare times

**Use Cases:**
- Logging and timestamps
- Scheduling and planning
- International collaboration
- Time-based calculations

---

## 🧪 **Testing Your Setup**

### **Verification Commands**
```bash
# Test each server (example tool names)
mcp__git__status              # Should show git repository status
mcp__time__current            # Should return current time
mcp__fetch__get               # Should be available for URL fetching
mcp__filesystem__list_directory # Should list current directory
mcp__memory__search           # Should be available for memory operations
mcp__sequential_thinking__analyze # Should be available for problem analysis
mcp__everything__test_tool    # Should provide test functionality
```

### **Troubleshooting**
If tools aren't available:
1. **Check Installation:** Verify all servers installed globally
2. **Restart Claude Code:** Exit and restart to reload MCP config
3. **Check .mcp.json:** Ensure file is in project root with correct syntax
4. **Tool Names:** Try variations like `mcp__server_name__tool_name`

---

## 🚀 **Benefits for Development**

### **Universal Compatibility**
- Works with any programming language
- No framework-specific dependencies
- Cross-platform support
- Consistent interface across projects

### **Enhanced Claude Capabilities**
- **File Operations:** Safe, controlled file system access
- **Version Control:** Git operations without shell commands
- **Web Integration:** Fetch external resources and APIs
- **Time Utilities:** Timezone-aware time operations
- **Persistent Memory:** Remember context across sessions
- **Advanced Reasoning:** Multi-step problem solving
- **Testing/Debugging:** Comprehensive development tools

### **Project Benefits**
- **Faster Development:** Direct tool access without shell commands
- **Better Context:** Persistent memory of project details
- **Enhanced Research:** Web content fetching and analysis
- **Improved Planning:** Sequential thinking for complex tasks
- **Time Awareness:** Proper timestamp and scheduling handling
- **Version Control:** Structured git operations

---

## 📝 **Best Practices**

### **Security**
- Review filesystem server permissions
- Use allowed directories configuration
- Be cautious with write operations
- Validate external fetch URLs

### **Performance** 
- Use memory server for frequently accessed information
- Cache fetch results when appropriate
- Limit filesystem operations to necessary directories
- Use sequential thinking for complex analysis only

### **Maintenance**
- Keep servers updated with npm updates
- Monitor for new official server releases
- Review and update .mcp.json as needed
- Test tools after Claude Code updates

---

## 🔄 **Update Process**

### **Keeping Servers Current**
```bash
# Update all official MCP servers
npm update -g @modelcontextprotocol/server-everything
npm update -g @modelcontextprotocol/server-fetch  
npm update -g @modelcontextprotocol/server-filesystem
npm update -g @modelcontextprotocol/server-git
npm update -g @modelcontextprotocol/server-memory
npm update -g @modelcontextprotocol/server-sequential-thinking
npm update -g @modelcontextprotocol/server-time
```

### **Configuration Updates**
- Check official repository for new server options
- Update .mcp.json with new capabilities
- Test new tools and features
- Update project documentation

---

## 📊 **Summary Table**

| Server | Primary Function | Key Tools | Universal Value |
|--------|------------------|-----------|-----------------|
| **Everything** | Testing/Reference | test_tool, demo_prompt | Development & Learning |
| **Fetch** | Web Content | get, get_html, get_json | Research & Integration |
| **Filesystem** | File Operations | read_file, write_file, list_directory | Project Management |
| **Git** | Version Control | status, log, diff, commit | Code Development |
| **Memory** | Knowledge Graph | store, retrieve, search | Context Retention |
| **Sequential** | Problem Solving | analyze, plan, reflect | Complex Analysis |
| **Time** | Time Operations | current, convert, format | Scheduling & Logging |

---

**🎯 Result:** Complete MCP toolset providing enhanced Claude capabilities for any development project, with official support and continuous updates from the ModelContextProtocol team.

**📧 Maintainer:** Chris Nowlan  
**🔄 Last Updated:** 2025-09-07  
**📖 Source:** https://github.com/modelcontextprotocol/servers