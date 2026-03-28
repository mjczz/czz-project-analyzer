# Project Analyzer Heartbeat Template

This template defines how the czz-project-analyzer skill uses OpenClaw's memory system for heartbeat detection during project analysis.

## Purpose

Heartbeat tracking prevents analysis interruption by:
- Recording progress in OpenClaw memory (`memory/YYYY-MM-DD.md`)
- Enabling resume capability if analysis is interrupted
- Providing analysis state visibility across sessions
- Supporting long-running analysis tasks

## Heartbeat Entry Format

### Analysis Start Entry

```markdown
## Project Analysis Started: [Project Name]

**Status**: 🟢 In Progress
**Mode**: [Standard/Deep-Dive/Quick Assessment]
**Started**: [YYYY-MM-DD HH:MM:SS]
**Project Path**: [Full path to analyzed project]
**Analysis ID**: [Unique identifier - timestamp or project name]

**Progress**: 0/12 topics completed

**Next Topic**: Project Basic Info
```

### Topic Progress Entry

```markdown
### 🔄 Topic Update: [Topic Name]

**Progress**: [X]/12 topics completed
**Current Topic**: [Topic Name]
**Status**: [In Progress/Completed]
**Updated**: [YYYY-MM-DD HH:MM:SS]

**Files Created**:
- [File path 1]
- [File path 2]

**Next Topic**: [Next topic name]
```

### Analysis Completion Entry

```markdown
## ✅ Project Analysis Completed: [Project Name]

**Status**: ✅ Complete
**Completed**: [YYYY-MM-DD HH:MM:SS]
**Duration**: [Approximate duration]
**Total Topics**: [12/20 depending on mode]
**Project Path**: [Full path to analyzed project]
**Analysis ID**: [Unique identifier]

**Final Documents Location**: `~/ai/code-analysi/{project-name}/`

**Key Deliverables**:
- Main analysis: {project-name}-analysis.md
- Topic documents: 12 individual files in topics/ directory
- Progress tracking: analysis-todo.md
- Changelog: changelog.md

**Analysis Summary**: [Brief 2-3 sentence summary]
```

### Analysis Interruption Entry (Optional)

```markdown
## ⚠️ Analysis Interrupted: [Project Name]

**Status**: 🟡 Paused
**Last Update**: [YYYY-MM-DD HH:MM:SS]
**Progress**: [X]/12 topics completed
**Last Completed Topic**: [Topic name]
**Next Topic**: [Next topic to resume with]

**Resume Instructions**: Use "resume analysis of [project-path]" to continue from topic [X+1]
```

## Memory File Location

Heartbeat entries are written to: `~/.openclaw/workspace/memory/YYYY-MM-DD.md`

## Usage in Analysis Workflow

### Step 0: Analysis Preparation
1. Create initial "Analysis Started" entry in memory
2. Record analysis mode and project details
3. Set progress to 0/12

### During Analysis (Each Topic)
1. Before starting topic: Update memory with "In Progress" status
2. After completing topic: Update memory with "Completed" status
3. Record file creation and progress increment
4. Update next topic pointer

### Final Step: Analysis Completion
1. Create "Analysis Completed" entry in memory
2. Calculate duration and summary
3. Clear active analysis state
4. Provide final document locations

## Resume Capability

If analysis is interrupted, the memory entry enables:
- **Automatic detection**: Check memory for incomplete analyses
- **State restoration**: Know exactly which topic to resume from
- **Progress continuity**: Continue without repeating completed work
- **File integrity**: Verify which documents were already created

## Heartbeat Timing

- **Start**: Once during Step 0 (Preparation)
- **Topic Updates**: At the beginning and end of each topic analysis
- **Completion**: Once during Final Step
- **Total writes**: 1 + (topics × 2) + 1 = approximately 26 memory writes for standard analysis

## Best Practices

1. **Consistent format**: Use the template structure for all entries
2. **Timestamps**: Include precise timestamps for progress tracking
3. **File paths**: Record full paths for all created documents
4. **Status clarity**: Use clear status indicators (🟢 In Progress, ✅ Complete, 🟡 Paused)
5. **Resume info**: Always include next topic for continuation capability

## Integration with OpenClaw Memory System

This heartbeat system integrates with OpenClaw's built-in memory capabilities:
- **Storage**: Plain markdown files in `memory/` directory
- **Searchable**: Memory search can find previous analyses
- **Persistent**: Survives agent restarts and system reboots
- **Compact**: Minimal overhead, only essential tracking data

---

*This heartbeat template ensures robust project analysis with interruption recovery and progress visibility.*