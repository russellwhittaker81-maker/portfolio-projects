# Copilot Instructions for Portfolio Projects

## Project Vision
This repository documents Russell's structured progression through ethical hacking, offensive security techniques, and defensive countermeasures. It serves as both a **personal learning journal** for security certifications (Sec+, Pentest+, CEH) and a foundation for future **AI-powered cybersecurity learning tools**. 

The goal: Build repeatable workflows from hands-on lab experience, eventually creating ~10 specialized Python bots that make security accessible to the general public (not enterprises).

## Repository Structure

```
├── foundations/              # Core security concepts and theory
├── reconnaissance/           # OSINT & passive reconnaissance (Phase 1 focus)
│   ├── notes.md            # Theory and techniques
│   └── labs.md             # Practical lab exercises
├── scanning/               # Port scanning & service discovery
├── enumeration/            # Active information gathering
├── vulnerability-assessment/ # Identifying weaknesses
├── system-hacking/         # Exploitation techniques
├── web-security/           # Web app vulnerabilities
├── wireless/               # WiFi & wireless security
├── cloud-security/         # Cloud security concepts
└── reflections.md          # Learning insights & patterns
```

Each domain section contains:
- `notes.md` - Conceptual foundation and techniques
- `labs.md` - Hands-on lab exercises and workflows

## Development Conventions

### Language & Environment
- **Primary:** Python 3 for all bot implementations
- **Shell:** Bash/Zsh for CLI scripts and automation
- **Style:** Follow PEP 8 conventions for Python code

### File Organization
- Structure bots as independent Python modules with single responsibility
- Use descriptive names: `osint_bot.py`, `reconnaissance_analyzer.py`, etc.
- Include module-level docstring explaining purpose, inputs, and outputs:
  ```python
  """
  OSINT Reconnaissance Bot
  
  Handles passive information gathering from public sources without alerting targets.
  Aggregates data from WHOIS, DNS, web searches, and public records.
  """
  ```

### Documentation & Comments
- Focus on the "why" behind security decisions, not just the "what"
- Explain data sources and their reliability (API rate limits, data freshness, accuracy)
- Document assumptions about target systems and scope limitations
- Include practical examples of expected input/output for each bot
- Lab notes (`labs.md`) should capture repeatable workflows, not one-off exercises

### Error Handling & User Experience
- Design error messages for non-technical users (minimize jargon, explain when necessary)
- Gracefully handle API rate limits, network timeouts, and unavailable data sources
- Return structured feedback: what data was collected, what failed, and why
- Provide clear confidence levels for gathered intelligence

## Key Patterns & Decisions

### Multi-Source Data Aggregation
- OSINT requires data from multiple sources (APIs, web scraping, databases)
- Design pattern: collector modules that abstract source-specific logic
- Strategy: Fail gracefully if one source is unavailable; aggregate from available sources

### User Accessibility Over Enterprise Features
- Prioritize clear reporting and visualizations over advanced analytics
- Provide simplified interpretations of complex security data
- Avoid assumptions that users understand CIDR notation, protocol details, etc.

### Ethical & Legal Boundaries
- Passive reconnaissance should use only public information sources
- Active reconnaissance requires explicit scope definition to avoid legal issues
- Include clear warnings about legal implications in bot documentation

## Getting Started for AI Agents

1. **Understand the domain:** Each bot solves a specific cybersecurity problem for beginners
2. **Check existing bots:** Review the structure of implemented bots before creating new ones
3. **Follow single responsibility:** Each bot should do ONE thing well
4. **Test with safe examples:** Always validate behavior against non-sensitive targets
5. **Document for users:** Assume the end-user has no security background

## References
- [README.md](../README.md) - Project vision, creator background, security learning journey
