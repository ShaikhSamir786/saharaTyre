# SaharaTyre Agent Configuration

## Overview

This project uses specialized agent skills located in `agents/skills/`. Each skill is a focused expert for specific domains. Any AI assistant working on this project should load the relevant skill when the task matches its domain.

## Available Skills

| Skill | Purpose | When to Use |
|-------|---------|-------------|
| `performance-engineer.md` | System-wide performance analysis and optimization | "Why is this slow" questions, load testing, capacity planning |
| `seo-engineer.md` | Technical SEO, structured data, AEO/GEO optimization | SEO audits, schema markup, sitemap configuration, AI answer engine optimization |
| `ui-ux-engineer.md` | Visual and interaction design direction | "How should this look/flow" questions, design system decisions |

## How to Use Skills

When your task matches a skill's domain, read and follow the instructions in that skill file:

```
Read agents/skills/performance-engineer.md
Read agents/skills/seo-engineer.md
Read agents/skills/ui-ux-engineer.md
```

## Skill Activation Rules

**performance-engineer** activates for:
- Cross-component performance diagnosis
- Load testing and capacity planning
- Performance target-setting
- Bottleneck identification across multiple layers

**seo-engineer** activates for:
- Technical SEO audits
- Structured data/schema markup implementation
- Sitemap/robots.txt configuration
- Core Web Vitals ranking factor optimization
- AEO/GEO content structure optimization

**ui-ux-engineer** activates for:
- Design direction requests ("how should this look")
- New UI design from scratch
- Design review of implemented UI
- Design system decisions
- Interaction flow design

## Skill Boundaries

Each skill has clear ownership boundaries:

| Skill Owns | Does NOT Own |
|------------|--------------|
| **performance-engineer**: Cross-stack performance diagnosis, load testing, capacity planning | Single-component optimization (delegated to owning skill) |
| **seo-engineer**: Technical SEO, structured data, crawlability, AEO/GEO | Render performance UX (→ frontend-engineer), content writing |
| **ui-ux-engineer**: Visual/interaction design, information architecture, design systems | Component implementation code (→ frontend-engineer), accessibility auditing |

## Inter-Skill Coordination

Skills hand off work to each other with specific evidence:

- **performance-engineer** → **backend-engineer**: API/business-logic bottlenecks with profiling evidence
- **performance-engineer** → **database-engineer**: Query/index bottlenecks with EXPLAIN ANALYZE evidence
- **seo-engineer** → **frontend-engineer**: Core Web Vitals ranking-relevant underperformance
- **ui-ux-engineer** → **frontend-engineer**: Design implementation with specific states/spacing/behavior

## Project Conventions

### Code Style
- Follow existing patterns in the codebase
- Use established libraries and utilities already in use
- Maintain consistency with neighboring files

### Security
- Never commit secrets or keys
- Follow security best practices
- Scope credentials appropriately

### Testing
- Verify changes with tests when available
- Run lint/typecheck commands if provided
- Check README for testing approach

### Git
- Only commit when explicitly requested
- Inspect status and diff before committing
- Stage only intended files

## Skill File Structure

Each skill file follows this structure:
1. **Purpose**: Why this skill exists
2. **Scope**: What it owns and doesn't own
3. **When This Skill Activates**: Trigger conditions
4. **Core Responsibilities**: Primary duties
5. **Engineering Principles**: Guiding philosophy
6. **Technical Knowledge**: Domain expertise
7. **Decision-Making Framework**: How to make choices
8. **Workflow**: Step-by-step process
9. **Implementation Guidelines**: Practical rules
10. **Interaction With Other Skills**: Coordination patterns
11. **Expected Output**: What this skill delivers
12. **Examples**: Concrete use cases

## Project Configuration Files

| File | Purpose |
|------|---------|
| `opencode.jsonc` | OpenCode configuration (provider, agents, skills, context) |
| `gemini.md` | Google Gemini context file |
| `context.md` | Full project context for AI assistants |
| `llms.txt` | Business profile for LLM consumption |
| `ai.txt` | Crawl policy for AI crawlers |
| `AGENTS.md` | This file - agent skill configuration |

## Adding New Skills

To add a new skill:
1. Create a new `.md` file in `agents/skills/`
2. Follow the existing structure (see any skill file for template)
3. Add YAML frontmatter with `name` and `description`
4. Update this AGENTS.md file with the new skill entry

## Troubleshooting

If a skill doesn't activate when expected:
1. Check if the task matches the skill's activation conditions
2. Verify the skill file exists and is properly formatted
3. Ensure the skill's scope covers the requested work
4. Check for conflicts with other skills' ownership boundaries