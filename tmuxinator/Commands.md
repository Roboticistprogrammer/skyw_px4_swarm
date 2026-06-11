# Tmuxinator Commands & Shortcuts

## Installation
```bash
# Install tmuxinator (if not already installed)
gem install tmuxinator
```

## Basic Commands

### Create a new project configuration
```bash
tmuxinator new <project_name>
```

### List all projects
```bash
tmuxinator list
# or
tmuxinator ls
```

### Start a project
```bash
tmuxinator start <project_name>
# or
tmuxinator <project_name>
```

### Stop a project
```bash
tmuxinator stop <project_name>
```

### Open project configuration in editor
```bash
tmuxinator open <project_name>
# or
tmuxinator edit <project_name>
```

### Delete a project
```bash
tmuxinator delete <project_name>
# or
tmuxinator destroy <project_name>
```

## Common Shortcuts (within tmux sessions)

### Session Management
- `Ctrl-b d` - Detach from session
- `Ctrl-b s` - List all sessions
- `Ctrl-b $` - Rename current session

### Window Management
- `Ctrl-b c` - Create new window
- `Ctrl-b w` - Choose window from list
- `Ctrl-b n` - Next window
- `Ctrl-b p` - Previous window
- `Ctrl-b 0-9` - Switch to window number
- `Ctrl-b ,` - Rename current window

### Pane Management
- `Ctrl-b |` - Split window vertically
- `Ctrl-b -` - Split window horizontally
- `Ctrl-b o` - Switch to next pane
- `Ctrl-b ;` - Switch to last pane
- `Ctrl-b Ctrl-o` - Rotate panes
- `Ctrl-b {` - Swap with previous pane
- `Ctrl-b }` - Swap with next pane
- `Ctrl-b x` - Kill current pane

### Copy Mode (for scrolling)
- `Ctrl-b [` - Enter copy mode
- `Space` - Start selection
- `Enter` - Copy selection
- `Ctrl-b ]` - Paste from buffer

## Useful Tips

1. **Project Configuration Location**: 
   - Config files are typically stored in `~/.tmuxinator/`
   - Each project has its own YAML configuration file

2. **Quick Start**:
   ```bash
   # Create a new project
   tmuxinator new myproject
   
   # Edit the configuration
   tmuxinator edit myproject
   
   # Start the project
   tmuxinator start myproject
   ```

3. **Environment Variables**:
   - You can use environment variables in your tmuxinator configs
   - Access with: `$VAR_NAME` syntax

4. **Multiple Sessions**:
   - Tmuxinator creates one session per project
   - Use `tmux` directly for multiple sessions within a project