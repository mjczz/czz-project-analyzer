# Project Analyzer - Documentation Organization Guide

## File Organization Structure

Each project analysis creates a structured documentation directory for easy management and reference.

### Directory Structure

Analysis documents are saved to the centralized hub at `~/ai/code-analysi/{project-name}/`.

```
~/ai/code-analysi/{project-name}/       # Centralized hub for all analysis documents
├── changelog.md                         # Analysis change log
├── {project-name}-analysis.md           # Main comprehensive report
├── {project-name}-progress-tracking.md  # Analysis progress tracking
├── analysis-todo.md                     # Analysis TODO list
├── topics/                              # Topic analysis documents (directly under project dir)
│   ├── 01-project-basic-info.md
│   ├── 02-project-structure.md
│   ├── 03-tech-stack.md
│   ├── 04-core-features.md
│   ├── 05-architecture-design.md
│   ├── 06-code-quality.md
│   ├── 07-documentation-quality.md
│   ├── 08-project-activity.md
│   ├── 09-strengths-weaknesses.md
│   ├── 10-use-cases.md
│   ├── 11-learning-value.md
│   ├── 12-summary.md
│   ├── 13-source-code-deep-dive.md         # Deep analysis mode
│   ├── 14-implementation-mechanics.md       # Deep analysis mode
│   ├── 15-key-component-analysis.md        # Deep analysis mode
│   ├── 16-protocol-interface-analysis.md   # Deep analysis mode
│   ├── 17-workflow-tracing.md              # Deep analysis mode
│   ├── 18-security-analysis.md             # Deep analysis mode
│   ├── 19-performance-analysis.md          # Deep analysis mode
│   └── 20-testing-strategy-analysis.md     # Deep analysis mode
└── assets/                              # Diagrams and images
    ├── diagrams/
    │   ├── architecture.mmd
    │   ├── sequence.mmd
    │   └── flowchart.mmd
    └── images/
```

## File Naming Conventions

### Main Documents
- **Comprehensive Report**: `[project-name]-analysis.md`
- **Progress Tracking**: `[project-name]-progress-tracking.md`

### Topic Documents
Format: `XX-[topic-name].md`
- `XX`: Two-digit sequence number (01-20)
- `[topic-name]`: Simplified topic name

**Examples**:
```
01-project-basic-info.md
13-source-code-deep-dive.md
```

### Diagram Files
Format: `[diagram-type]-[description].mmd`
- `architecture-overview.mmd`
- `sequence-user-flow.mmd`
- `flowchart-data-processing.mmd`

## Analysis Change Log (changelog.md)

Each analysis project includes a change log that records all document creation activities during the analysis process:

```markdown
# Project Analysis Change Log

## 📋 Analysis Overview
- **Project Name**: [Project Name]
- **Analysis Mode**: [Quick Assessment/Standard Analysis/Deep Analysis]
- **Analysis Start Time**: [Timestamp]
- **Current Status**: [In Progress/Completed]

## 🔄 Analysis Change Records

### [Date] - Analysis Initiation
**Time**: [Timestamp]
**Operation**: Started project analysis
**Created Files**: [List all initialization files]

## 📝 Topic Document Creation Records

### [Date] - [Topic Name] Completed
**Time**: [Timestamp]
**Topic**: [Topic Number]. [Topic Name]
**Progress**: [X/12]
**Created Document**: `topics/[XX]-[topic-name].md`
**Key Findings**: [List main discoveries]
**Updated Files**: [List updated files]

## 📊 Analysis Statistics
### Document Creation Statistics
| Category | Created Count | Total Size | Last Updated |
|----------|----------------|------------|--------------|
| Topic Documents | X/12 | [Total Size] | [timestamp] |

## 🎯 Milestones
- [x] [timestamp] - Analysis started
- [x] [timestamp] - First topic completed
- [ ] [timestamp] - Halfway through topics (6/12)
```

### Changelog Maintenance Rules

1. **Auto Update**: Update automatically after completing each topic
2. **Time Recording**: Precise timestamps to the second
3. **File Recording**: Record all created and updated files
4. **Statistics**: Real-time update of document statistics and progress
5. **Milestone Tracking**: Mark important analysis nodes

## Analysis TODO Document (analysis-todo.md)

Each analysis project includes a TODO document for tracking analysis plans and progress:

```markdown
# [Project Name] Analysis TODO List

## 📋 Analysis Overview

- **Project Name**: [Project Name]
- **Analysis Mode**: [Quick Assessment/Standard Analysis/Deep Analysis]
- **Creation Time**: [Timestamp]
- **Estimated Completion**: [Timestamp]
- **Current Status**: In Progress

## 🎯 Analysis Plan

### Standard Analysis Phase (12 Topics)

- [ ] **01. Project Basic Information**
  - Status: ⏳ Not Started
  - Priority: 🔥 High
  - Estimated Time: 5-10 minutes
  - Content: GitHub data collection, basic information organization

- [ ] **02. Project Structure**
  - Status: ⏳ Not Started
  - Priority: 🔥 High
  - Estimated Time: 10-15 minutes
  - Content: Directory structure analysis, module relationship diagrams

### Deep Analysis Phase (8 Topics) - Optional

- [ ] **13. Source Code Deep Dive**
  - Status: ⏳ Not Started
  - Priority: 🔥 High
  - Estimated Time: 20-30 minutes
  - Content: Core code paths, function call chains

## 📊 Progress Statistics

### Completion Overview

- **Standard Analysis**: X/12 (X%)
- **Deep Analysis**: X/8 (X%)
- **Overall Progress**: X/20 (X%)

### Time Statistics

- **Time Spent**: XX minutes
- **Estimated Remaining**: XX minutes
- **Total Estimated Time**: XX minutes

## 🔄 Workflow

### Current Task

**Currently Working**: [Topic Name]
- **Start Time**: [timestamp]
- **Estimated Completion**: [timestamp]
- **Key Points**:
  - [ ] Point 1
  - [ ] Point 2

### Next Steps

1. [Next topic name]
2. [Following topic name]

## 📝 Notes and Observations

### Technical Challenges
- [Challenge 1]: [Description]
- [Challenge 2]: [Description]

### Interesting Findings
- [Finding 1]: [Description]
- [Finding 2]: [Description]

### Future Deep Dive Directions
- [Direction 1]: [Description]
- [Direction 2]: [Description]

---

*Creation time: [timestamp]*
*Last updated: [timestamp]*
*Updated by: Claude Code*
```

## Progress Tracking Document

Each analysis project includes a progress tracking document:

```markdown
# [Project Name] Analysis Progress Tracking

## 📊 Analysis Overview

- **Project Name**: [Project Name]
- **Analysis Mode**: [Quick Assessment/Standard Analysis/Deep Analysis]
- **Start Time**: [Timestamp]
- **Estimated Completion**: [Timestamp]
- **Current Status**: In Progress (X/20)

## ✅ Completion Progress

### Standard Analysis Phase (X/12)

- [x] 01. Project Basic Information - [Completion Time]
- [x] 02. Project Structure - [Completion Time]
- [ ] 03. Tech Stack - In Progress
- [ ] 04. Core Features - Not Started
- [ ] 05. Architecture Design - Not Started
- [ ] 06. Code Quality - Not Started
- [ ] 07. Documentation Quality - Not Started
- [ ] 08. Project Activity - Not Started
- [ ] 09. Strengths/Weaknesses - Not Started
- [ ] 10. Use Cases - Not Started
- [ ] 11. Learning Value - Not Started
- [ ] 12. Summary - Not Started

### Deep Analysis Phase (X/8) - Optional

- [ ] 13. Source Code Deep Dive - Not Started
- [ ] 14. Implementation Mechanics - Not Started
- [ ] 15. Key Component Analysis - Not Started
- [ ] 16. Protocol Interface Analysis - Not Started
- [ ] 17. Workflow Tracing - Not Started
- [ ] 18. Security Analysis - Not Started
- [ ] 19. Performance Analysis - Not Started
- [ ] 20. Testing Strategy Analysis - Not Started

## 📝 Analysis Log

### [Date] - Topic Name Completed
- **Time Spent**: XX minutes
- **Key Findings**:
  - Finding 1
  - Finding 2
- **Next Step**: [Next topic]

## 🔗 Quick Links

- [Comprehensive Report](./[project-name]-analysis.md)
- [Topic Documents Directory](./topics/)
- [Diagram Resources](./assets/)

---

*Last updated: [timestamp]*
```

## Topic Document Template

Each topic document follows a unified structure:

```markdown
# [Number]. [Topic Name] - [Project Name]

## 📋 Topic Overview
- **Analysis Topic**: [Topic Name]
- **Project**: [Project Name]
- **Analysis Time**: [YYYY-MM-DD HH:MM:SS]
- **Time Spent**: XX minutes
- **Analysis Status**: ✅ Completed
- **Analysis Mode**: [Quick Assessment/Standard Analysis/Deep Analysis]

## 🎯 Analysis Objectives
[Analysis objectives and focus for this topic]

## 🔍 Detailed Analysis

### 1. [Sub-topic 1]
[Detailed analysis content]

### 2. [Sub-topic 2]
[Detailed analysis content]

## 📊 Key Findings

### Core Discoveries
- **Finding 1**: [Detailed description]
  - Impact Scope: [Description]
  - Importance: [High/Medium/Low]
- **Finding 2**: [Detailed description]
  - Impact Scope: [Description]
  - Importance: [High/Medium/Low]

### Data and Metrics
| Metric | Value | Description |
|--------|-------|-------------|
| | | |

## 📈 Visualization

```mermaid
[Relevant diagrams]
```

## 🔗 Source Code References
| Function/Component | File Location | Line Number | Description |
|-------------------|---------------|-------------|-------------|
| | | | |

## 📚 Reference Resources
- **Official Documentation**: [Link]
- **Source Location**: [path/to/file]
- **Related Topics**: [Links to other topic documents]

## 💡 Insights and Recommendations

### Strengths
- [Strength 1]
- [Strength 2]

### Areas for Improvement
- [Improvement suggestion 1]
- [Improvement suggestion 2]

### Practice Recommendations
- [Recommendation 1]
- [Recommendation 2]

---

## 📋 Analysis Metadata

- **Analysis Tool**: czz-project skill
- **Data Source**: [GitHub API/Documentation/Source Code]
- **Confidence Level**: [High/Medium/Low]
- **Verification Status**: [Verified/Pending Verification]
- **Related Issues/PRs**: [Links]

## 🔄 Update History

| Time | Update Content | Updated By |
|------|----------------|------------|
| [timestamp] | Initial analysis | Claude Code |

---

*This document was auto-generated by czz-project skill*
*Generated at: [timestamp]*
*Document version: 1.0*
```

## Comprehensive Report Structure

The main report document integrates analysis results from all topics:

```markdown
# [Project Name] Project Analysis Report

## 📊 Executive Summary

[Overall project overview and key findings]

## 📋 Table of Contents

1. [Project Basic Information](#1-project-basic-information)
2. [Project Structure](#2-project-structure)
...
20. [Testing Strategy Analysis](#20-testing-strategy-analysis) (if applicable)

## 📊 Detailed Analysis

### 1. Project Basic Information

[Integrated core content from topics/01-project-basic-info.md]

### 2. Project Structure

[Integrated core content from topics/02-project-structure.md]

...

## 🎯 Core Conclusions

### Main Strengths
1. [Strength 1]
2. [Strength 2]

### Main Challenges
1. [Challenge 1]
2. [Challenge 2]

### Recommended Use Cases
- [Use case 1]
- [Use case 2]

## 📈 Scorecard

| Dimension | Score | Description |
|-----------|-------|-------------|
| Architecture Design | ⭐⭐⭐⭐⭐ | [Description] |
| Code Quality | ⭐⭐⭐⭐⭐ | [Description] |
| Documentation Completeness | ⭐⭐⭐⭐⭐ | [Description] |
| Community Activity | ⭐⭐⭐⭐⭐ | [Description] |
| **Overall Score** | **⭐⭐⭐⭐⭐** | [Description] |

## 🔗 Related Documents

- [Detailed Topic Analysis](./topics/)
- [Analysis Progress](./[project-name]-progress-tracking.md)
- [Diagram Resources](./assets/)

---

*Report generation time: [timestamp]*
*Analysis mode: [Mode name]*
*Analysis tool: czz-project skill*
```

## Documentation Management Best Practices

### Automated Creation
1. Create corresponding topic documents immediately after completing each topic
2. Update progress tracking documents simultaneously
3. Update relevant sections in the main comprehensive report

### Document Linking
- Use relative links to connect related documents
- Cross-reference between topic documents
- Link main report to all topic documents

### Version Control
- Include generation timestamp at the bottom of each document
- Record update history for major updates
- Maintain document version consistency

### Quality Control
- Use unified templates and formats
- Ensure all links are valid
- Verify diagrams render correctly

This progressive documentation creation strategy ensures:
1. **Real-time Saving**: Each topic is saved immediately upon completion, preventing data loss
2. **Flexible Viewing**: Can view detailed analysis of any topic individually
3. **Progress Transparency**: Clearly shows analysis progress and status
4. **Easy Maintenance**: Structured organization facilitates subsequent updates and expansion