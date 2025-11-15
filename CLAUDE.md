# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This repository contains custom Claude skills and AI workflow resources. The primary focus is the **learn-tech** skill, which creates token-efficient, structured learning programs for software engineering topics.

## Repository Structure

```
claude-resources/
├── skills/                    # Custom Claude skills
│   └── learn-tech/            # Main skill: tech learning program creator
│       ├── SKILL.md           # Primary skill instructions (8,000+ tokens)
│       ├── README.md          # User-facing documentation
│       ├── INSTALL.md         # Installation guide
│       └── templates/         # File templates for learning programs
└── README.md                  # Repository overview
```

## Working with Skills

### Skill Structure

Each skill in `skills/` follows this pattern:
- **SKILL.md**: Main instruction file that Claude reads when the skill is active
- **README.md**: Human-friendly documentation
- **templates/**: Supporting files and templates used by the skill

### Creating Skills

Skills are distributed as ZIP files and uploaded to Claude.ai. To prepare a skill for distribution:

```bash
cd skills/[skill-name]
zip -r [skill-name].zip .
# Upload to Claude.ai → Settings → Capabilities → Skills
```

### Testing Skills Locally

When testing skill changes, read the SKILL.md file directly to verify instructions:
- SKILL.md contains all teaching patterns, documentation strategies, and workflow instructions
- Changes to SKILL.md require re-zipping and re-uploading to Claude.ai to take effect
- Template files in `templates/` are referenced by SKILL.md but not directly read by Claude

## learn-tech Skill Details

### Purpose
Creates token-efficient learning programs for software engineering topics with:
- 12-module structure across 4 phases (~40-50 hours total)
- Minimal documentation overhead (85% reduction vs traditional approaches)
- Code-first teaching with active learning challenges
- Break-friendly 1-2 hour modules

### Key Design Principles

**Token Efficiency Strategy:**
- PROGRESS.txt: <100 tokens (current module, commit, next step)
- MODULE_X_PLAN.md: 500-1000 tokens (brief outlines, not full content)
- MODULE_X_COMPLETE.md: 300-500 tokens (minimal summaries)
- Comprehensive README.md: Claude doesn't read during sessions

**Teaching Pattern:**
1. Show code first → Ask learner to analyze → Explain line-by-line
2. Small challenges after each concept
3. Design principles integrated naturally with callout boxes
4. Check for questions after each objective (not just module end)
5. Distinguish first vs subsequent encounters with concepts

**Session Management:**
- Commit after each module with detailed message
- Provide git commands + continuation prompt in separate blocks
- Continuation uses <1,200 tokens vs 8,000+ in previous approaches

### File Modifications

When editing learn-tech skill files:
- **SKILL.md changes**: Require re-packaging and re-uploading to take effect
- **Template changes**: Used as reference patterns, not directly executed
- **README.md changes**: For human documentation only

## GitHub Integration

### GitHub Actions Setup

This repository uses Claude's GitHub Actions integration to respond to @claude mentions in issues and PRs.

**Workflow file:** [.github/workflows/claude.yml](.github/workflows/claude.yml)

**Setup requirements:**
1. ✅ GitHub App installed and authorized (https://github.com/apps/claude)
2. ✅ Workflow file created at `.github/workflows/claude.yml`
3. ⚠️  Add `ANTHROPIC_API_KEY` as a repository secret:
   - Go to Settings → Secrets and variables → Actions
   - Click "New repository secret"
   - Name: `ANTHROPIC_API_KEY`
   - Value: Your Anthropic API key
4. ✅ GitHub App has "read & write" access to: Contents, Issues, Pull requests

**How to use:**
- Mention `@claude` in any issue or PR comment
- The GitHub Action will trigger and Claude will respond
- Check the Actions tab for logs if Claude doesn't respond

## Development Workflow

### Making Changes

Since this is primarily a documentation and skill repository:
1. Edit SKILL.md or template files as needed
2. Test by reading files directly in Claude Code
3. Update README.md to reflect changes
4. Commit with descriptive messages
5. For skill distribution: re-zip and upload to Claude.ai

### Version Control

- Skills should maintain version info in SKILL.md metadata
- Use semantic versioning (v1.0.0, v1.1.0, etc.)
- Document significant changes in skill's README

### Git Operations

Standard git workflow applies:
```bash
git add .
git commit -m "Brief summary

- Key change 1
- Key change 2"
git push origin main
```

## Learner Profile (Built into learn-tech)

- Frontend engineer (JavaScript, React) expanding to broader software engineering
- Code-first learning approach preferred
- Claude Free tier user (5-hour token limit per session)
- Values production-quality, portfolio-worthy outcomes
- Prefers 1-2 hour learning sessions with break-friendly structure

## Common Tasks

### Update learn-tech Skill
1. Edit `skills/learn-tech/SKILL.md`
2. Test changes by reading file directly
3. Re-zip: `cd skills/learn-tech && zip -r learn-tech.zip .`
4. Upload to Claude.ai
5. Commit changes to repository

### Add New Skill
1. Create `skills/[new-skill-name]/` directory
2. Add SKILL.md with skill instructions
3. Add README.md for user documentation
4. Add any necessary templates or supporting files
5. Update main README.md
6. Commit and push

### Test Skill Instructions
Read the SKILL.md file directly to verify instructions are clear and complete. The file should be self-contained with all necessary patterns and examples.
