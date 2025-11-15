# learn-tech Skill

A comprehensive skill for creating and teaching structured software engineering learning programs with Claude.

## What This Skill Does

### 1. Creates Learning Programs
When you say "Create a learning program for [topic]", Claude will:
- Design a 12-module curriculum tailored to your background
- Set up project structure with documentation
- Generate all module plans
- Create token-efficient progress tracking

### 2. Teaches Throughout
During all teaching sessions, Claude:
- Follows your preferred learning style (code-first, challenges, validation)
- Integrates design principles and best practices
- Uses token-efficient documentation patterns
- Enables easy session breaks and continuation

## Key Features

✅ **Token Efficient** - Minimal documentation overhead (~85% reduction)  
✅ **Break Friendly** - 1-2 hour modules, clean continuation between sessions  
✅ **Deep Learning** - Code-first thinking, challenges, frequent validation  
✅ **Production Quality** - Portfolio-worthy outcomes, best practices throughout  
✅ **Natural Teaching** - Design principles, tips, tricks integrated in flow  

## Your Learning Preferences (Built Into Skill)

- **Show code first** → Ask what you think → Explain line-by-line
- **Small challenges** after each concept to reinforce learning
- **Check for questions** after each objective (not just at module end)
- **Design principles** taught naturally + explicit callout boxes
- **Tips & tricks** mentioned naturally (keyboard shortcuts, terminal commands, etc.)
- **Distinguish first vs subsequent** encounters with concepts
- **Quality focus** - Production-ready, not throwaway code

## How to Use

### Starting a New Learning Program

```
Use learn-tech to create a learning program for [TOPIC].

[Optional context:]
- I'm a [your background]
- I want to [your goal]
- I have [experience level]
```

**Example:**
```
Use learn-tech to create a learning program for Docker.
I'm a frontend developer with no Docker experience.
I want to containerize my Node.js apps.
```

### Continuing After a Break

At the end of each session, Claude will give you a continuation prompt. Copy and paste it in a new chat:

```
Use the learn-tech skill to continue my [Topic] learning program.
Use filesystem MCP to:
1. Read /path/to/project/docs/PROGRESS.txt
2. Find relevant MODULE_X_PLAN.md if needed
3. Continue from checkpoint

Project location: /path/to/project
```

**Important:** The prompt must include "Use the learn-tech skill" to ensure Claude activates the skill in the new session and follows all the teaching patterns.

## What Gets Created

```
your-learning-project/
├── README.md                    # Comprehensive overview (human-friendly)
├── .gitignore
├── docs/
│   ├── PROGRESS.txt             # Minimal tracker (AI reads this)
│   ├── GLOSSARY.md              # Optional reference
│   ├── ROADMAP.md               # Visual overview
│   ├── MODULE_1_PLAN.md         # Brief outline for each module
│   ├── MODULE_2_PLAN.md
│   ├── ...
│   └── sessions/
│       ├── MODULE_1_COMPLETE.md # Minimal summaries
│       ├── MODULE_2_COMPLETE.md
│       └── ...
└── src/                         # Your actual project code
```

## Token Efficiency

### Old Approach (Your Previous Programs)
- Large LEARNING_PROGRESS.md: 5,000+ tokens
- Reading multiple files: 8,000+ tokens per session start
- **20-30% of tokens spent on documentation**

### New Approach (This Skill)
- Minimal PROGRESS.txt: ~100 tokens
- Brief module plans: ~500-1000 tokens
- Continuation prompt: ~100 tokens
- **~1,200 tokens total (~85% reduction)**

More tokens for actual teaching!

## Program Structure

**12 modules in 4 phases** (~40-50 hours total)

**Phase 1: Foundations** (Modules 1-3)
- Setup and core concepts

**Phase 2: Application** (Modules 4-6)
- Building real functionality

**Phase 3: Advanced** (Modules 7-9)
- Complex patterns and features

**Phase 4: Production** (Modules 10-12)
- Testing, deployment, polish

Each module: 60-90 minutes (split to Part A/B if >2 hours)

## Teaching Pattern

For each learning objective:

1. **Introduce concept** (why it matters)
2. **Show code** (before explaining)
3. **Ask what you think** (encourage reflection)
4. **Explain line-by-line** (detailed first time, brief after)
5. **Integrate design principles** (natural + callout boxes)
6. **Share tips/tricks** (when relevant)
7. **Assign small challenge** (you write code)
8. **Check for questions** (after each objective)

## Session Management

**Commit after each module** with detailed message:
```
Module X complete: [summary]
- Key achievement 1
- Key achievement 2
- Next: Module Y
```

**At break point**, Claude provides (in separate blocks):
1. Git commands to commit
2. Continuation prompt for next session

**Starting new session**: Paste continuation prompt, Claude picks up where you left off

## Best Practices

Every module ends with a checklist:
```
✅ Module Complete - Best Practices Check:
- [ ] [Relevant practice 1]
- [ ] [Relevant practice 2]
- [ ] [Relevant practice 3]
```

Walk through together to ensure quality.

## Customization

The skill automatically adapts based on:
- Your experience level (beginner vs transitioning from X)
- Your goals (work project vs learning vs portfolio)
- Topic type (language vs framework vs tool vs concept)

Claude will ask clarifying questions when you start a new program.

## What Makes This Different

✅ **Token optimized** for Claude Free tier  
✅ **Break-friendly** for busy schedules  
✅ **Deep learning** over quick tutorials  
✅ **Production quality** outcomes  
✅ **Your preferences** built in  

## Files in This Skill

```
learn-tech/
├── SKILL.md                           # Main skill (Claude reads this)
├── README.md                          # This file (for you)
└── templates/
    ├── PROGRESS.txt                   # Template for progress tracker
    ├── continuation-prompt.txt        # Template for session continuation
    ├── module-plan-outline.md         # Template for module plans
    └── module-complete-summary.md     # Template for completion summaries
```

## Installation

1. Zip the `learn-tech` folder
2. Go to Claude.ai → Settings → Capabilities → Skills
3. Click "Upload skill"
4. Upload the ZIP file
5. Enable the skill

## Using the Skill

Once installed, just mention it:
```
Use learn-tech to create a learning program for [topic]
```

or

```
Continue my [topic] learning program (with continuation prompt)
```

Claude will automatically reference the skill and follow all your preferences!

## Tips

- The skill is designed for software engineering topics
- Works best for topics where you have some programming background
- Creates portfolio-worthy projects, not throwaway demos
- Optimized for 1-2 hour learning sessions
- Token efficient for Claude Free tier

## Support

The skill includes:
- Detailed teaching patterns
- Token efficiency strategies
- Adaptation guidelines
- Troubleshooting section
- Example interactions

If something isn't working as expected, let Claude know and it can adjust!

---

**Enjoy your efficient, effective learning programs!** 🚀
