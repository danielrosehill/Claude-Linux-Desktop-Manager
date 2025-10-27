I created this repository to develop a workspace for a Linux Desktop management interface based around Claude Code.

## Some Context

I'm a huge believer in the idea that AI CLIs (like Claude Code) hold enormous potential for streamlining desktop (or server) sysadmin.

I use Claude Code more for this purpose than for code generation/editing. I have been using Linux for more than 20 years. I have always dreamed of being able to manage a computer like this—one that provides the power of Linux but offloads the massive complication.

I'm building out a library of slash commands. I envision that I will continue to develop these as I figure out new ways to use Claude Code not just for Linux sysadmin, but even for things that would traditionally have needed standalone CLIs—and to eliminate redundant work in general. I'll share the links at the end of these notes.

## The Idea

Slash commands are great and can be complemented with a CLAUDE.md file at a level of the filesystem that says "your task here is desktop sysadmin" (this is a sort of workaround to dislodge the assumed context that Claude Code is for development/editing).

But... I think that a more elegant solution would be something more approaching a GUI.

Many of the slash commands envision/require the creation of things like documentation (for example, hardware benchmarking or logs).

These could be captured externally with MCP tools, but I think it would be more elegant to have a unified management environment for running the jobs and gathering the outputs—then users can decide where they wish to store outputs (if anywhere else).

---

## Implementation

Some initial ideas:

- Wrapper around Claude Code (CLI)
- Slash commands are presented as tasks with batch tasks that chain complementary operations
- GUI
- Backend for storing settings, Claude-captured context (like OS details) persistently
- Local-only tool initially, although down the line some cloud integrations could be added to upload output data

---

## Slash Command Library

Main repository: https://github.com/danielrosehill/Claude-Code-Linux-Desktop-Slash-Commands

### As Flat Structure

https://github.com/danielrosehill/Claude-Code-Linux-Desktop-Slash-Commands/tree/main/commands-flat

### With Hierarchy

https://github.com/danielrosehill/Claude-Code-Linux-Desktop-Slash-Commands/tree/main/commands
