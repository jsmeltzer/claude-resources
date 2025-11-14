# Claude Skills & Resources

A collection of custom Claude skills, useful prompts, and AI workflow tools.

## 📁 Repository Structure

```
claude-resources/
├── skills/                    # Custom Claude skills
│   └── learn-tech/            # Tech learning program creator
├── prompts/                   # Useful prompts (future)
├── workflows/                 # Common AI workflows (future)
└── README.md                  # This file
```

## 🎯 What's Inside

### Skills

#### learn-tech

A comprehensive skill for creating and teaching structured software engineering learning programs.

**Features:**

- Token-efficient documentation (~85% reduction in overhead)
- Break-friendly 1-2 hour modules
- Code-first teaching with challenges
- Design principles integrated naturally
- Production-quality outcomes

[View skill documentation →](skills/learn-tech/README.md)

**Installation:**

```bash
cd skills/learn-tech
zip -r learn-tech.zip learn-tech/
# Upload to Claude.ai → Settings → Capabilities → Skills
```

## 🚀 Usage

### Using a Skill

Once installed in Claude, reference it in any chat:

```
Use learn-tech to create a learning program for [topic]
```

### Adding New Skills

1. Create new folder in `skills/`
2. Add SKILL.md and supporting files
3. Update this README
4. Commit and push

## 📝 Future Additions

**Planned Skills:**

- [ ] code-review (structured code review workflow)
- [ ] doc-generator (technical documentation creator)
- [ ] test-strategy (test planning and generation)

**Planned Prompts:**

- [ ] Architecture review prompts
- [ ] PR description templates
- [ ] Debugging workflow prompts

## 🔧 Maintenance

### Updating a Skill

1. Edit files in `skills/[skill-name]/`
2. Re-zip if needed
3. Re-upload to Claude
4. Commit changes

### Version Control

- Each skill should maintain its own version info
- Use semantic versioning (v1.0.0, v1.1.0, etc.)
- Document changes in skill's README

## 📚 Resources

- [Claude Skills Documentation](https://docs.claude.com)
- [MCP Server Documentation](https://modelcontextprotocol.io)

## 👤 Author

**J Smeltzer**

- Frontend Engineer
- Expanding my tech stack

## 📄 License

Personal use. Individual skills may have their own licenses.

---

_Last Updated: November 2025_
