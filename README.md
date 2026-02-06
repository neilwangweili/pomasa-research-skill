# pomasa-research-skill

A Claude Code skill plugin for researching any topic and producing structured outputs (articles, reports, analyses, etc.) using the [POMASA](https://github.com/neilwangweili/pomasa) multi-agent generator framework.

It should be noted that the core development of [POMASA](https://github.com/eXtremeProgramming-cn/pomasa) which in [Extreme Programming China](https://github.com/eXtremeProgramming-cn) was completed by [@Jeff Xiong](https://github.com/gigix), whose exceptional technical expertise was instrumental in the realization of this project. I was merely responsible for the subsequent, minor encapsulation work required to transform it into the skill format.

## Features

- Works from **any directory** — automatically manages POMASA workspace in `~/.pomasa/pomasa/`
- Flexible topic selection: provide your own topic or get AI-assisted suggestions
- Multiple output formats: WeChat articles, research reports, technical analyses, etc.
- Auto-clones and keeps POMASA framework up to date
- Opens the output directory in Finder/Explorer when complete

## Installation

```bash
claude plugin add neilwangweili/pomasa-research-skill
```

## Usage

After installation, simply tell Claude Code:

```
Help me research the impact of AI agents on software development workflows.
```

Or trigger directly:

```
/pomasa-research
```

The skill will:

1. **Set up environment** — Clone or update POMASA to `~/.pomasa/pomasa/`
2. **Determine topic** — Use your topic directly, or help you explore and pick one
3. **Research pipeline** — Design research approach → generate multi-agent system → run agents → produce output
4. **Show results** — Open the project output directory in your file manager

## How It Works

This skill orchestrates the full POMASA research workflow:

1. Confirms your topic or helps you discover one through AI-assisted exploration
2. Uses brainstorming to design the research approach and determine output format
3. Generates a complete multi-agent system using POMASA patterns
4. Runs the agent pipeline to collect and analyze data
5. Produces the final output (article, report, analysis, etc.)
6. Opens the output folder for you to review

All project files are stored in `~/.pomasa/pomasa/{project-id}/`.

## Requirements

- [Claude Code](https://claude.ai/claude-code) with skill support
- Git (for cloning POMASA)
- Internet access (for web research)
