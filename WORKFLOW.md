# Project Analyzer - Progressive Analysis Workflow

This guide extends the czz-project skill with systematic deep-dive analysis methodologies inspired by Kubernetes source code analysis.

## Analysis Modes

### 🚀 Quick Assessment Mode (6 topics)
**When to use**: Quick evaluations, basic understanding
**Time**: 10-15 minutes
**Topics**: 1, 3, 4, 9, 10, 12

### 📊 Standard Analysis Mode (12 topics)
**When to use**: General project analysis, architecture review
**Time**: 30-45 minutes
**Topics**: All standard topics

### 🔬 Deep-Dive Mode (20 topics)
**When to use**: Technical projects, source code analysis, internal mechanism understanding
**Time**: 1-2 hours
**Topics**: All standard + advanced topics

## Progressive Documentation Creation Process

### Analysis Cycle for Each Topic

For each topic, execute the following steps:

1. **📖 Analysis Phase** (Analyze)
   - Collect information and data
   - Create necessary diagrams
   - Analyze core content

2. **💾 Save Phase** (Save)
   - Create independent topic document: `topics/XX-[topic-name].md`
   - Save to project directory
   - Record timestamp and metadata

3. **📊 Update Phase** (Update)
   - Update corresponding sections in main comprehensive report
   - Update progress tracking document
   - Add links between documents

4. **📢 Report Phase** (Report)
   - Report completion status to user
   - Display key findings summary
   - Provide document location links

5. **➡️ Continue Phase** (Continue)
   - Automatically move to next topic
   - No user confirmation required

### Document Creation Timing

```
Topic Start → Analysis Complete → Create Document Immediately → Update Progress → Report → Next Topic
     ↓              ↓                    ↓                      ↓            ↓
   Start       Content Prep         File Save            Status Update   User Notification
```

### Document Save Strategy

**Immediate Save Principle**:
- Create independent document immediately after completing each topic analysis
- Don't wait for entire analysis to complete
- Prevent data loss
- Provide real-time progress visibility

**Save Content**:
- Detailed topic analysis content
- Relevant Mermaid diagrams
- Key findings and insights
- Reference resource links
- Analysis metadata (time, duration, confidence level)

## Progressive Analysis Strategy

### Phase 1: Foundation (Topics 1-3)
**Goal**: Understand project basics and structure
**Approach**:
- Start with GitHub API data collection
- Build mental model of project organization
- Identify main programming languages and frameworks

### Phase 2: Architecture (Topics 4-6)
**Goal**: Grasp design and implementation quality
**Approach**:
- Map core features and user flows
- Understand architecture patterns
- Evaluate code quality and testing approach

### Phase 3: Ecosystem (Topics 7-12)
**Goal**: Assess project health and usage
**Approach**:
- Review documentation quality
- Analyze community activity
- Form practical recommendations

### Phase 4: Deep Technical Analysis (Topics 13-20)
**Goal**: Understand internal mechanisms (optional)
**Approach**:
- Trace source code execution paths
- Analyze key algorithms and data structures
- Evaluate performance and security characteristics
- Document implementation details

## Code Analysis Methodology

### Entry Point Analysis
1. **Identify main entry points**:
   - `main()` functions for applications
   - API endpoints for web services
   - Library exports for SDKs
   - CLI command handlers

2. **Trace initialization sequences**:
   - Configuration loading
   - Dependency injection
   - Service startup
   - Resource allocation

### Data Structure Mapping
1. **Core entities**: Identify principal data structures
2. **Relationships**: Map dependencies and associations
3. **State management**: Understand state transitions
4. **Data flow**: Track data movement through the system

### Control Flow Analysis
1. **Request processing**: Follow typical request lifecycle
2. **Error handling**: Understand error propagation
3. **Resource management**: Track allocation/cleanup
4. **Concurrency**: Analyze parallel processing patterns

### Interface Analysis
1. **API contracts**: Document interface specifications
2. **Communication patterns**: Understand component interaction
3. **Protocol analysis**: Examine communication protocols
4. **Data serialization**: Analyze data format handling

## Progressive Deep-Dive Steps

### Level 1: Surface Understanding
- Read README and documentation
- Examine directory structure
- Run basic functionality
- Review examples

### Level 2: Structural Analysis
- Map module dependencies
- Identify key components
- Understand configuration system
- Review testing approach

### Level 3: Implementation Details
- Trace core algorithms
- Analyze data structures
- Review error handling
- Study optimization techniques

### Level 4: Advanced Topics
- Performance characteristics
- Security mechanisms
- Extension points
- Integration patterns

## Mermaid Diagram Strategy

### When to Create Diagrams
1. **Early analysis**: Simple structure diagrams
2. **Mid analysis**: Add sequence and flow diagrams
3. **Deep analysis**: Comprehensive technical diagrams

### Diagram Selection Guide

| Analysis Phase | Diagram Types | Purpose |
|---------------|--------------|---------|
| Foundation | Module graphs | Show structure |
| Architecture | Architecture diagrams | Show layers |
| Implementation | Sequence diagrams | Show flows |
| Deep Analysis | Data flow, State diagrams | Show mechanisms |

## Code Reference Format

### Standard Format
```
Location: pkg/module/file.go:123
Function: ProcessRequest()
Context: HTTP request handling in API server
```

### Progressive Detail Levels
1. **Basic**: Module and file name
2. **Detailed**: File name and line number
3. **Comprehensive**: Function signature and context

## Analysis Continuation Framework

### Handoff Strategy
When analysis needs to continue:
1. **Current state**: Document completed topics
2. **Next priorities**: Identify remaining areas
3. **Entry points**: Provide specific locations for continued analysis
4. **Context**: Share key findings and insights

### Re-analysis Triggers
- Major version updates
- Architecture changes
- Performance issues
- Security vulnerabilities

## Quality Indicators

### Analysis Completeness Checklist
- [ ] All required topics covered
- [ ] Key findings documented with evidence
- [ ] Diagrams included where appropriate
- [ ] Code references provided for technical claims
- [ ] Practical recommendations included
- [ ] Sources cited

### Technical Depth Indicators
- **Surface**: Basic feature description
- **Moderate**: Architecture understanding
- **Deep**: Implementation details with code references
- **Expert**: Performance, security, and optimization analysis

## Example Progressive Analysis Flow

### Initial Analysis (Standard Mode)
```
1. Quick overview (15 min)
2. Feature mapping (10 min)
3. Architecture understanding (15 min)
4. Quality assessment (10 min)
```

### Deep Analysis (Deep-Dive Mode)
```
1. Standard analysis (50 min)
2. Source code mapping (20 min)
3. Mechanism analysis (20 min)
4. Performance/security (15 min)
5. Implementation comparison (15 min)
```

### Expert Analysis (Research Mode)
```
1. Complete deep-dive (2 hours)
2. Historical evolution analysis
3. Comparative study with alternatives
4. Future development trajectory
5. Research paper preparation
```

## Tools and Resources

### Data Collection
- GitHub API: Repository metadata, statistics
- Code search: Find specific implementations
- Documentation: Official docs and guides
- Community: Issues, discussions, PRs

### Analysis Tools
- Code browsers: Source code navigation
- Dependency analyzers: Module relationships
- Profiling tools: Performance data (if available)
- Static analysis: Code quality metrics

### Output Generation
- Markdown documentation: Structured reports
- Mermaid diagrams: Visual representations
- Code examples: Practical illustrations
- Comparison tables: Feature analysis

## Best Practices

### Time Management
- Set clear time limits per topic
- Prioritize based on user requirements
- Use progressive deepening approach
- Document assumptions and limitations

### Accuracy and Validation
- Cross-verify information from multiple sources
- Test claims against actual code when possible
- Document uncertainty areas
- Provide confidence levels for assessments

### Communication
- Use clear, non-technical language where possible
- Provide technical details in separate sections
- Include visual diagrams for complex concepts
- Offer practical, actionable recommendations

---

*This workflow guide integrates the systematic analysis methodology from Kubernetes deep-dive analysis into the czz-project skill.*