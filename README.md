# Danny's Claude Agents

Other Claude stuff is in https://github.com/dannysmith/dotfiles but these global agents are kept in a seperate repo to avoid theneed to symlink them.

Clone this repo into `~/.claude/agents` to use them.

## Best Practices for Creating Agents

Based on Claude's generated security-auditor example and research into best practices:

### YAML Frontmatter Structure
```yaml
---
name: agent-name              # Concise kebab-case identifier
description: |                # Detailed description with examples
  Use this agent when... 
  Examples with context/user/assistant/commentary format
color: red                    # Visual identifier (optional)
tools: Read, Grep, Bash      # Specific tools (optional - inherits all if omitted)
---
```

### Description Best Practices
- Include multiple examples showing when to use the agent
- Use format: Context → User query → Assistant response → Commentary
- Be specific about triggers and use cases
- Help Claude Code understand when to delegate

### System Prompt Structure
1. **Role Definition**: Clear identity with experience level
2. **Core Focus Areas**: Systematic breakdown of responsibilities  
3. **Methodology**: Step-by-step approach
4. **Process**: Detailed workflow
5. **Output Requirements**: Specific formatting and deliverables
6. **Quality Assurance**: Guidelines for accuracy and reliability

### Design Principles
- **Single Responsibility**: Each agent should have one clear purpose
- **Tool Limitation**: Only grant necessary tools for security and focus
- **Comprehensive Coverage**: Address all aspects within the agent's domain
- **Actionable Output**: Provide specific, implementable recommendations
- **Context Awareness**: Consider the full environment and constraints

### Creation Workflow
1. Start with Claude-generated foundation (using `/agent` command)
2. Analyze the generated structure and content
3. Iterate and customize based on specific needs
4. Test with real scenarios
5. Refine based on performance

## TEMP - Setup Tasks

See here for more inspiration: https://github.com/wshobson/agents
