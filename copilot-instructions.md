# Tnsr-Q CLI MCP Copilot Instructions

This is an MCP (Model Context Protocol) server that provides access to Tnsr-Q CLI functionality through a standardized interface.

## Project Structure

- `tnsr_q_cli_mcp/` - Main package directory
  * `server.py` - MCP server implementation
  * `__init__.py` - Package initialization

## Available Tools

1. **execute_tnsr_q_command** - Execute any Tnsr-Q CLI command
   - Parameters: `command` (string), `args` (array of strings)
   - Returns: Command output, exit code, and any errors

2. **get_tnsr_q_help** - Get help information for Tnsr-Q CLI commands
   - Parameters: `command` (optional string)
   - Returns: Help text for the specified command or general help

3. **list_tnsr_q_commands** - List all available Tnsr-Q CLI commands
   - Parameters: None
   - Returns: List of available commands

## Usage Guidelines

- Always validate command parameters before execution
- Handle timeout and error cases gracefully
- Provide clear feedback on command success/failure
- Use appropriate logging for debugging

## Development Notes

- The server uses asyncio for handling MCP communication
- Commands are executed with a 30-second timeout
- All commands are prefixed with 'tnsr-q' automatically