# Claude Code Slash Commands

Production-ready slash commands for [Claude Code](https://docs.anthropic.com/en/docs/claude-code) that accelerate development through intelligent automation and multi-agent orchestration.

## Overview

This repository contains **52 production-ready slash commands** designed to enhance your development workflow with Claude Code. Commands are organized into two primary categories:

- **Workflows**: Multi-agent orchestration for complex, multi-step tasks
- **Tools**: Single-purpose utilities for specific operations

## Prerequisites

These commands require [Claude Code](https://docs.anthropic.com/en/docs/claude-code) and the [Claude Code Subagents](https://github.com/wshobson/agents) collection for full orchestration capabilities.

## Installation

```bash
cd ~/.claude
git clone https://github.com/wshobson/commands.git
git clone https://github.com/wshobson/agents.git  # Required for subagent orchestration
```

## Quick Start

Commands are organized in `tools/` and `workflows/` directories. Use them with directory prefixes:

```bash
/tools:api-scaffold user management with authentication
/tools:security-scan check for vulnerabilities
/workflows:feature-development implement chat functionality
```

To use commands without prefixes, flatten the directories:
```bash
cp tools/*.md .
cp workflows/*.md .
```

## Command Categories

### Workflows (14 commands)

Workflows orchestrate multiple specialized agents to handle complex, multi-domain tasks. They analyze requirements, delegate to appropriate specialists, and coordinate results.

#### Feature Development & Review
- **feature-development** - Complete feature implementation with backend, frontend, testing, and deployment agents
- **full-review** - Comprehensive code analysis from multiple specialist perspectives
- **smart-fix** - Intelligent issue analysis and resolution with automatic delegation

#### Development Process Automation
- **git-workflow** - Git workflow implementation with branching strategies and PR templates
- **improve-agent** - Agent performance optimization through prompt engineering
- **legacy-modernize** - Legacy codebase modernization with specialized refactoring agents
- **ml-pipeline** - ML pipeline creation with data and ML engineering specialists
- **multi-platform** - Cross-platform application development with coordinated agents
- **workflow-automate** - CI/CD, monitoring, and deployment automation

#### Advanced Orchestration
- **full-stack-feature** - Multi-platform features with backend, frontend, and mobile agents
- **security-hardening** - Security-first implementation with specialized security agents
- **data-driven-feature** - ML-powered features with data science specialists
- **performance-optimization** - End-to-end optimization with performance specialists
- **incident-response** - Production incident resolution with operations specialists

### Tools (38 commands)

Tools provide focused, single-purpose functionality for specific development tasks.

#### AI & Machine Learning
- **ai-assistant** - Production-ready AI assistants and chatbots
- **ai-review** - Specialized review for AI/ML codebases
- **langchain-agent** - LangChain/LangGraph agents with modern patterns
- **ml-pipeline** - End-to-end ML pipelines with MLOps
- **prompt-optimize** - AI prompt optimization for performance and quality

#### Architecture & Code Quality
- **code-explain** - Detailed explanations of complex code
- **code-migrate** - Code migration between languages, frameworks, or versions
- **refactor-clean** - Code refactoring for maintainability and performance
- **tech-debt** - Technical debt analysis and prioritization

#### Data & Database
- **data-pipeline** - Scalable data pipeline architectures
- **data-validation** - Comprehensive data validation systems
- **db-migrate** - Advanced database migration strategies

#### DevOps & Infrastructure
- **deploy-checklist** - Deployment configurations and checklists
- **docker-optimize** - Container optimization strategies
- **k8s-manifest** - Production-grade Kubernetes deployments
- **monitor-setup** - Comprehensive monitoring and observability
- **slo-implement** - Service Level Objectives (SLOs) implementation
- **workflow-automate** - Development and operational workflow automation

#### Development & Testing
- **api-mock** - Realistic API mocks for development and testing
- **api-scaffold** - Production-ready API endpoints with complete implementation
- **test-harness** - Comprehensive test suites with framework detection

#### Security & Compliance
- **accessibility-audit** - Accessibility testing and remediation
- **compliance-check** - Regulatory compliance verification (GDPR, HIPAA, SOC2)
- **security-scan** - Security scanning with automated remediation

#### Debugging & Analysis
- **debug-trace** - Advanced debugging and tracing strategies
- **error-analysis** - Error pattern analysis and resolution
- **error-trace** - Production error diagnosis
- **issue** - Well-structured issue creation for GitHub/GitLab

#### Dependencies & Configuration
- **config-validate** - Application configuration validation and management
- **deps-audit** - Dependency security and licensing audit
- **deps-upgrade** - Safe dependency upgrades

#### Documentation & Collaboration
- **doc-generate** - Comprehensive documentation generation
- **pr-enhance** - Pull request enhancement with quality checks
- **standup-notes** - Daily standup note generation

#### Cost Optimization
- **cost-optimize** - Cloud and infrastructure cost optimization

#### Onboarding & Setup
- **onboard** - Development environment setup for new team members

#### Context Management
- **context-save** - Save project context and architectural decisions
- **context-restore** - Restore saved context for continuity
- **multi-agent-review** - Multi-perspective code review
- **smart-debug** - Deep debugging with specialized agents
- **multi-agent-optimize** - Full-stack optimization

## Usage Patterns

### Daily Development Workflow

#### Morning: Feature Development
```bash
# Start new feature with comprehensive implementation
/workflows:feature-development Add OAuth2 authentication with Google and GitHub

# Scaffold specific API endpoints
/tools:api-scaffold user profile CRUD with avatar upload
```

#### Debugging & Problem Resolution
```bash
# Intelligent problem analysis and fix
/workflows:smart-fix Dashboard loading slowly, users seeing 5+ second wait times

# Trace specific errors
/tools:error-trace Analyze high memory usage in production pods
```

#### Code Review & Quality
```bash
# Comprehensive multi-agent review
/tools:multi-agent-review Review PR #123 payment processing implementation

# Security scanning
/tools:security-scan Comprehensive scan for OWASP Top 10 vulnerabilities
```

#### Deployment Preparation
```bash
# Generate deployment checklist
/tools:deploy-checklist OAuth2 authentication feature deployment

# Optimize containers
/tools:docker-optimize Optimize authentication service container

# Create Kubernetes manifests
/tools:k8s-manifest Production deployment with auto-scaling
```

### Command Chaining

Commands are designed to work together in sequences:

#### Building Complete Features
```bash
# 1. Implement with workflow
/workflows:feature-development Add real-time chat with WebSockets

# 2. Add security measures
/tools:security-scan Focus on WebSocket vulnerabilities

# 3. Optimize performance
/tools:multi-agent-optimize Optimize message delivery

# 4. Prepare deployment
/tools:deploy-checklist Real-time chat deployment
/tools:k8s-manifest WebSocket service with sticky sessions
```

#### Modernizing Legacy Code
```bash
# 1. Start modernization
/workflows:legacy-modernize Migrate Express.js v4 to modern architecture

# 2. Update dependencies
/tools:deps-upgrade Update all dependencies to latest versions

# 3. Clean up code
/tools:refactor-clean Remove deprecated patterns

# 4. Add tests
/tools:test-harness Ensure 100% test coverage

# 5. Deploy
/tools:docker-optimize Create production build
/tools:k8s-manifest Deploy with zero-downtime strategy
```

## When to Use Workflows vs Tools

### Use Workflows When:
- Tackling complex, multi-domain problems
- Solution approach is unclear
- Need coordination between multiple specialists
- Implementing complete features end-to-end
- Require adaptive problem-solving

**Examples:**
- "Implement user authentication system" → `/workflows:feature-development`
- "Fix performance issues across the stack" → `/workflows:smart-fix`
- "Modernize legacy monolith" → `/workflows:legacy-modernize`

### Use Tools When:
- Task has a clear, specific scope
- Need precise control over implementation
- Working within a single domain
- Enhancing or refining existing work
- Integrating into manual workflows

**Examples:**
- "Create Kubernetes manifests" → `/tools:k8s-manifest`
- "Scan for security vulnerabilities" → `/tools:security-scan`
- "Generate API documentation" → `/tools:doc-generate`

## Best Practices

### Command Selection
1. Let Claude Code suggest commands automatically based on context
2. Start with workflows for complex tasks, then refine with tools
3. Chain commands strategically for comprehensive solutions

### Effective Usage
1. Provide comprehensive context including tech stack and constraints
2. Use workflow output as input for specific tools
3. Build incrementally on previous command outputs
4. Allow workflows to complete before applying modifications

### Performance Optimization
1. Use tools for known, specific problems
2. Use workflows for exploration and complex solutions
3. Provide detailed requirements upfront to reduce iterations
4. Keep simple edits in the main agent context

## Command Structure

Slash commands are markdown files with a simple structure:
- Filename becomes the command name (e.g., `tools/api-scaffold.md` → `/tools:api-scaffold`)
- File content contains the prompt/instructions executed when invoked
- `$ARGUMENTS` placeholder captures user input

## Contributing

To add new commands:

1. Create a `.md` file in `workflows/` or `tools/` directory
2. Use lowercase-hyphen naming convention
3. Include `$ARGUMENTS` placeholder for user input
4. For workflows: Focus on agent orchestration and delegation
5. For tools: Provide complete, production-ready implementations

## Troubleshooting

### Common Issues

**Command not found**
- Verify files exist in `~/.claude/commands/tools/` or `~/.claude/commands/workflows/`
- Check command syntax: `/tools:command-name` or `/workflows:command-name`
- Consider flattening directories if you prefer no prefixes

**Slow workflow execution**
- Normal behavior - workflows coordinate multiple agents
- Complex tasks require analysis and delegation time

**Generic or incomplete output**
- Provide more specific context about your technology stack
- Include constraints and requirements in your request

**Integration issues**
- Verify file paths are correct
- Check command sequencing and dependencies

## Featured Commands

### Security & DevOps Excellence

#### security-scan
Comprehensive security scanning with automated remediation:
- Multi-tool scanning (Bandit, Safety, Trivy, Semgrep, Snyk)
- Automated vulnerability fixes
- CI/CD security gate integration
- Container and secret scanning

#### docker-optimize
Advanced container optimization:
- Framework-specific multi-stage builds
- Modern build tools (BuildKit, Bun, UV)
- Security hardening with distroless images
- Cross-command integration support

#### k8s-manifest
Production-grade Kubernetes deployments:
- Pod Security Standards and Network Policies
- GitOps ready (FluxCD/ArgoCD)
- Built-in observability (Prometheus/OpenTelemetry)
- Auto-scaling and service mesh integration

### Database & Data Management

#### db-migrate
Advanced database migration strategies:
- Multi-database support (PostgreSQL, MySQL, MongoDB, DynamoDB)
- Zero-downtime migration patterns
- Event sourcing with Kafka/Kinesis
- Polyglot persistence handling

## Resources

- [Claude Code Documentation](https://docs.anthropic.com/en/docs/claude-code)
- [Slash Commands Documentation](https://docs.anthropic.com/en/docs/claude-code/slash-commands)
- [Subagents Documentation](https://docs.anthropic.com/en/docs/claude-code/sub-agents)
- [Claude Code GitHub](https://github.com/anthropics/claude-code)
- [Claude Code Subagents Collection](https://github.com/wshobson/agents)

## License

MIT License - See LICENSE file for details

## Support

For issues, questions, or contributions, please open an issue on [GitHub](https://github.com/wshobson/commands/issues).