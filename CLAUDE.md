# CLAUDE.md - Linux Desktop Manager

## Project Overview

This repository is dedicated to developing a Linux Desktop management interface built around Claude Code. The primary purpose is to leverage AI-powered CLI tools for streamlining desktop and server system administration tasks.

## Context File

This project includes a `context.md` file that contains detailed background information, the user's motivations, and vision for the project. The context file may contain voice-transcribed content and serves as the user's working scratchpad. Refer to `context.md` when you need deeper insight into the project's origins, philosophy, or long-term vision.

## Project Vision

The core vision is to create a management interface that:

- Provides the power of Linux system administration
- Offloads the complexity traditionally associated with Linux desktop management
- Leverages Claude Code beyond traditional code generation/editing use cases
- Eliminates redundant work and replaces standalone CLIs where possible

## Primary Use Case

This is NOT a traditional code development project. The focus is on **desktop system administration** rather than software development or code editing. Claude Code should operate in a sysadmin capacity when working in this repository.

## Implementation Requirements

### Core Components

1. **Wrapper Around Claude Code CLI**
   - Build a layer on top of the Claude Code CLI
   - Present slash commands as executable tasks
   - Support batch tasks that chain complementary operations

2. **GUI Interface**
   - Develop a graphical user interface for task execution
   - Provide visual feedback for running jobs
   - Display outputs in an organized manner

3. **Persistent Backend**
   - Store settings and configurations
   - Capture and persist Claude-gathered context (OS details, hardware info, etc.)
   - Maintain state between sessions

4. **Output Management**
   - Unified environment for running jobs and gathering outputs
   - Documentation generation (hardware benchmarking, logs, etc.)
   - Allow users to decide where to store outputs
   - Initially local-only, with potential for cloud integrations later

### Slash Command Library Integration

This project integrates with an extensive library of slash commands designed for Linux desktop management:

**Repository**: https://github.com/danielrosehill/Claude-Code-Linux-Desktop-Slash-Commands

**Available Structures**:
- Flat structure: `/commands-flat`
- Hierarchical structure: `/commands`

The slash commands cover various system administration tasks including:
- System configuration
- Hardware diagnostics
- Security auditing
- Package management
- Network diagnostics
- AI/ML environment setup
- And more

### Design Philosophy

- **Task-Oriented**: Present operations as actionable tasks rather than raw commands
- **Batch Operations**: Support chaining related tasks together
- **Persistent Context**: Remember system state and configuration
- **Output Organization**: Centralized management of generated documentation and logs
- **User Choice**: Allow flexibility in where outputs are stored

## Technical Approach

1. **Initial Phase**: Local-only tool
2. **Future Enhancements**: Cloud integrations for output storage and synchronization
3. **Alternative to MCP**: While MCP tools could capture outputs externally, a unified management environment is preferred

## Success Criteria

The project will be successful when:
- System administration tasks can be executed through an intuitive interface
- Slash commands are accessible as organized, executable tasks
- Outputs (logs, benchmarks, documentation) are automatically captured and organized
- The complexity of Linux desktop management is significantly reduced
- The tool feels like a cohesive desktop management solution rather than a collection of scripts

## Development Context

User: Daniel Rosehill
- 20+ years of Linux experience
- Heavy Claude Code user for sysadmin purposes
- Actively developing slash command library
- Vision: AI-powered desktop management that preserves Linux power while eliminating complexity
