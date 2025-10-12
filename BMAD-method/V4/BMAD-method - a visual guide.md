**Helpful Learning BMAD Diagrams**

---

## PROMPT
Make a markdown file I can download with mermaid diagrams for: 1. Story Status flow (simplified) 2. Story Status flow (advanced) 3. SDLC (simplified) 4. SDLC (advanced)
### Settings
Sonnet 4.0

---

## RESPONSE
#### Response
Perfect! I've created a comprehensive markdown file with all four Mermaid diagrams you requested:

## 📊 **What's Included:**

### **1. Story Status Flow (Simplified)**

- Basic story progression from Draft → Done
- Clear decision points and status changes
- Color-coded for easy visual understanding

### **2. Story Status Flow (Advanced)**

- Complete story lifecycle with QA integration
- Risk assessment and test design phases
- Mid-development checkpoints and quality gates
- Technical debt management integration

### **3. SDLC (Simplified)**

- High-level software development lifecycle
- Major phases from idea to maintenance
- Clean, easy-to-understand flow

### **4. SDLC (Advanced) - Complete BMAD Method**

- Full planning phase workflow (Web UI)
- Complete development cycle (IDE)
- QA command integration (*risk, *design, *trace, *nfr, *review, *gate)
- Technical debt management process
- Post-epic activities

## 🎯 **Additional Features:**

- **QA Agent Command Reference** with flow integration
- **Greenfield vs Brownfield** process variations
- **Key Success Metrics** and performance indicators
- **Color-coded diagrams** for visual clarity

## 📥 **Ready to Download**

The artifact contains everything in a single markdown file that you can:

- Download and save locally
- View in any markdown editor with Mermaid support
- Share with team members
- Use for documentation and training

The diagrams capture your actual BMAD implementation process, including the lessons learned and improvements you've discovered during your videoFabricWithZoom project! 🚀✨

---

#### Document (Artifact)
# BMAD Method Process Flow Diagrams

This document contains comprehensive process flow diagrams for the BMAD Method, optimized for dark mode viewing and broken into digestible sections for better readability.

## 1. Story Status Flow (Simplified)

**What it shows:** Basic story lifecycle from creation to completion  
**When to use:** Quick reference for story status progression and decision points  
**Best for:** New team members learning the process

```mermaid
graph TD
    A["📝 Draft"] --> B["👀 User Review"]
    B --> C{"✅ Approved?"}
    C -->|Yes| D["⚡ In Development"]
    C -->|No| A
    D --> E["🏁 Implementation Complete"]
    E --> F["🧪 QA Review"]
    F --> G{"🚪 QA Gate"}
    G -->|PASS| H["✅ Done"]
    G -->|CONCERNS/FAIL| I["🔧 Address Issues"]
    I --> F
    
    style A fill:#FFD700,color:#000000,stroke:#000000,stroke-width:3px
    style B fill:#87CEEB,color:#000000,stroke:#000000,stroke-width:3px
    style C fill:#DDA0DD,color:#000000,stroke:#000000,stroke-width:3px
    style D fill:#9370DB,color:#FFFFFF,stroke:#FFFFFF,stroke-width:3px
    style E fill:#32CD32,color:#000000,stroke:#000000,stroke-width:3px
    style F fill:#00BFFF,color:#000000,stroke:#000000,stroke-width:3px
    style G fill:#FF69B4,color:#000000,stroke:#000000,stroke-width:3px
    style H fill:#00FF00,color:#000000,stroke:#000000,stroke-width:3px
    style I fill:#FF4500,color:#FFFFFF,stroke:#FFFFFF,stroke-width:3px
```

## 2. Story Creation & Planning Flow

**What it shows:** How stories are created with optional risk assessment  
**When to use:** Understanding when to involve QA early in story planning  
**Best for:** Planning complex or high-risk features

```mermaid
graph TD
    A1["👨‍💼 SM: Draft Story"] --> A2["📄 Story File Created"]
    A2 --> A3{"⚠️ High Risk Story?"}
    A3 -->|Yes| A4["🧪 QA: *risk Assessment"]
    A3 -->|No| B1["👀 User Review"]
    A4 --> A5["📋 QA: *design Test Strategy"]
    A5 --> B1
    B1 --> B2{"✅ User Decision"}
    B2 -->|Needs Changes| A1
    B2 -->|Approved| C1["🚀 Status: Ready"]
    
    style A1 fill:#00BFFF,color:#000000,stroke:#000000,stroke-width:3px
    style A2 fill:#98FB98,color:#000000,stroke:#000000,stroke-width:3px
    style A3 fill:#FFA500,color:#000000,stroke:#000000,stroke-width:3px
    style A4 fill:#FFD700,color:#000000,stroke:#000000,stroke-width:3px
    style A5 fill:#FFFF00,color:#000000,stroke:#000000,stroke-width:3px
    style B1 fill:#87CEEB,color:#000000,stroke:#000000,stroke-width:3px
    style B2 fill:#DDA0DD,color:#000000,stroke:#000000,stroke-width:3px
    style C1 fill:#00FF00,color:#000000,stroke:#000000,stroke-width:3px
```

## 3. Development Execution Flow

**What it shows:** Core development cycle with optional mid-development QA  
**When to use:** Understanding the development phase workflow  
**Best for:** Developers and project managers tracking progress

```mermaid
graph TD
    C1["🚀 Status: Ready"] --> C2["👩‍💻 Dev: Start Implementation"]
    C2 --> C3["⚙️ Dev: Execute Tasks"]
    C3 --> C4{"🔍 Mid-Dev Check?"}
    C4 -->|Yes| C5["🧪 QA: *trace or *nfr"]
    C4 -->|No| C6["🔧 Dev: Address Gaps"]
    C5 --> C6
    C6 --> C7["📋 Dev: Mark Ready for Review"]
    
    style C1 fill:#00FF00,color:#000000,stroke:#000000,stroke-width:3px
    style C2 fill:#32CD32,color:#000000,stroke:#000000,stroke-width:3px
    style C3 fill:#98FB98,color:#000000,stroke:#000000,stroke-width:3px
    style C4 fill:#FF69B4,color:#000000,stroke:#000000,stroke-width:3px
    style C5 fill:#00BFFF,color:#000000,stroke:#000000,stroke-width:3px
    style C6 fill:#FFD700,color:#000000,stroke:#000000,stroke-width:3px
    style C7 fill:#9370DB,color:#FFFFFF,stroke:#FFFFFF,stroke-width:3px
```

## 4. Quality Assurance Flow

**What it shows:** QA review process with gate decisions  
**When to use:** Understanding quality checkpoints and outcomes  
**Best for:** QA team members and quality-focused workflows

```mermaid
graph TD
    C7["📋 Ready for Review"] --> D1{"🤔 User QA Choice"}
    D1 -->|Full QA Review| D2["🧪 QA: *review Story"]
    D1 -->|Skip QA| D5["👀 User Verification"]
    D2 --> D3["📊 QA: Test Architecture Analysis"]
    D3 --> D4{"🚪 QA Gate Decision"}
    D4 -->|PASS| D6["💾 COMMIT Changes"]
    D4 -->|CONCERNS| D7["📝 Document Issues"]
    D4 -->|FAIL| D8["🔄 Back to Development"]
    D5 --> D6
    D7 --> D6
    D6 --> D9["✅ Status: Done"]
    
    style C7 fill:#9370DB,color:#FFFFFF,stroke:#FFFFFF,stroke-width:3px
    style D1 fill:#DDA0DD,color:#000000,stroke:#000000,stroke-width:3px
    style D2 fill:#FF8C00,color:#000000,stroke:#000000,stroke-width:3px
    style D3 fill:#FFA500,color:#000000,stroke:#000000,stroke-width:3px
    style D4 fill:#FF69B4,color:#000000,stroke:#000000,stroke-width:3px
    style D5 fill:#87CEEB,color:#000000,stroke:#000000,stroke-width:3px
    style D6 fill:#32CD32,color:#000000,stroke:#000000,stroke-width:3px
    style D7 fill:#FFFF00,color:#000000,stroke:#000000,stroke-width:3px
    style D8 fill:#FF4500,color:#FFFFFF,stroke:#FFFFFF,stroke-width:3px
    style D9 fill:#00FF00,color:#000000,stroke:#000000,stroke-width:3px
```

## 5. BMAD Planning Phase (Web UI)

**What it shows:** Complete planning workflow from idea to architecture  
**When to use:** Starting a new project or major feature  
**Best for:** Project kickoff and strategic planning

```mermaid
graph TD
    A1["💡 Project Idea"] --> A2{"📊 Optional: Analyst Research"}
    A2 -->|Yes| A3["🔍 Analyst: Brainstorming"]
    A2 -->|No| A6["📋 Create Project Brief"]
    A3 --> A4["📈 Analyst: Market Research"]
    A4 --> A5["🏢 Analyst: Competitor Analysis"]
    A5 --> A6
    A6 --> A7{"📄 Project Brief Available?"}
    A7 -->|Yes| A8["👨‍💼 PM: Create PRD from Brief"]
    A7 -->|No| A9["👨‍💼 PM: Interactive PRD Creation"]
    A8 --> A10["📋 PRD Created"]
    A9 --> A10
    
    style A1 fill:#F0F0F0,color:#000000,stroke:#000000,stroke-width:3px
    style A2 fill:#87CEEB,color:#000000,stroke:#000000,stroke-width:3px
    style A3 fill:#98FB98,color:#000000,stroke:#000000,stroke-width:3px
    style A4 fill:#90EE90,color:#000000,stroke:#000000,stroke-width:3px
    style A5 fill:#ADFF2F,color:#000000,stroke:#000000,stroke-width:3px
    style A6 fill:#FFD700,color:#000000,stroke:#000000,stroke-width:3px
    style A7 fill:#DDA0DD,color:#000000,stroke:#000000,stroke-width:3px
    style A8 fill:#FF8C00,color:#000000,stroke:#000000,stroke-width:3px
    style A9 fill:#FFA500,color:#000000,stroke:#000000,stroke-width:3px
    style A10 fill:#00FF00,color:#000000,stroke:#000000,stroke-width:3px
```

## 6. Architecture & UX Design Phase

**What it shows:** Architecture creation with optional UX integration  
**When to use:** After PRD completion, before development  
**Best for:** Technical leads and architects

```mermaid
graph TD
    A10["📋 PRD Created"] --> A11{"🎨 UX Required?"}
    A11 -->|Yes| A12["🎨 UX Expert: Create Frontend Spec"]
    A11 -->|No| A13["🏗️ Architect: Create Architecture"]
    A12 --> A14["🎨 UX Expert: Generate UI Prompts"]
    A14 --> A15["🏗️ Architect: Architecture + UX"]
    A13 --> A16["👨‍💼 PO: Run Master Checklist"]
    A15 --> A16
    A16 --> A17{"✅ Documents Aligned?"}
    A17 -->|Yes| A18["🎉 Planning Complete"]
    A17 -->|No| A19["🔄 PO: Update Epics & Stories"]
    A19 --> A20["📝 Update PRD/Architecture"]
    A20 --> A16
    
    style A10 fill:#00FF00,color:#000000,stroke:#000000,stroke-width:3px
    style A11 fill:#FF69B4,color:#000000,stroke:#000000,stroke-width:3px
    style A12 fill:#00BFFF,color:#000000,stroke:#000000,stroke-width:3px
    style A13 fill:#9370DB,color:#FFFFFF,stroke:#FFFFFF,stroke-width:3px
    style A14 fill:#87CEEB,color:#000000,stroke:#000000,stroke-width:3px
    style A15 fill:#8A2BE2,color:#FFFFFF,stroke:#FFFFFF,stroke-width:3px
    style A16 fill:#FF8C00,color:#000000,stroke:#000000,stroke-width:3px
    style A17 fill:#DDA0DD,color:#000000,stroke:#000000,stroke-width:3px
    style A18 fill:#00FF32,color:#000000,stroke:#000000,stroke-width:3px
    style A19 fill:#FFD700,color:#000000,stroke:#000000,stroke-width:3px
    style A20 fill:#FFFF00,color:#000000,stroke:#000000,stroke-width:3px
```

## 7. Transition to Development

**What it shows:** Moving from planning to development execution  
**When to use:** After planning phase completion  
**Best for:** Understanding the handoff process

```mermaid
graph TD
    A18["🎉 Planning Complete"] --> A21["💻 Switch to IDE"]
    A21 --> A22["👨‍💼 PO: Shard Documents"]
    A22 --> B1["🚀 Ready for SM/Dev Cycle"]
    B1 --> B2["🔄 Begin Story Development"]
    
    style A18 fill:#00FF32,color:#000000,stroke:#000000,stroke-width:3px
    style A21 fill:#1E90FF,color:#000000,stroke:#000000,stroke-width:3px
    style A22 fill:#FF8C00,color:#000000,stroke:#000000,stroke-width:3px
    style B1 fill:#32CD32,color:#000000,stroke:#000000,stroke-width:3px
    style B2 fill:#98FB98,color:#000000,stroke:#000000,stroke-width:3px
```

## 8. QA Command Reference

**What it shows:** All QA agent commands and their purposes  
**When to use:** Reference for QA workflow and command usage  
**Best for:** QA team members and process understanding

```mermaid
graph TD
    Q1["🎯 *risk"] --> Q1A["⚠️ Risk Profile Document"]
    Q2["📋 *design"] --> Q2A["📊 Test Design Document"]
    Q3["🔍 *trace"] --> Q3A["📈 Traceability Matrix"]
    Q4["⚡ *nfr"] --> Q4A["📏 NFR Assessment"]
    Q5["🧪 *review"] --> Q5A["📊 QA Results + Gate File"]
    Q6["🚪 *gate"] --> Q6A["📝 Updated Gate Status"]
    
    style Q1 fill:#FFD700,color:#000000,stroke:#000000,stroke-width:3px
    style Q1A fill:#FFFF00,color:#000000,stroke:#000000,stroke-width:3px
    style Q2 fill:#FFA500,color:#000000,stroke:#000000,stroke-width:3px
    style Q2A fill:#FF8C00,color:#000000,stroke:#000000,stroke-width:3px
    style Q3 fill:#00BFFF,color:#000000,stroke:#000000,stroke-width:3px
    style Q3A fill:#87CEEB,color:#000000,stroke:#000000,stroke-width:3px
    style Q4 fill:#1E90FF,color:#000000,stroke:#000000,stroke-width:3px
    style Q4A fill:#00CED1,color:#000000,stroke:#000000,stroke-width:3px
    style Q5 fill:#FF69B4,color:#000000,stroke:#000000,stroke-width:3px
    style Q5A fill:#DDA0DD,color:#000000,stroke:#000000,stroke-width:3px
    style Q6 fill:#9370DB,color:#FFFFFF,stroke:#FFFFFF,stroke-width:3px
    style Q6A fill:#8A2BE2,color:#FFFFFF,stroke:#FFFFFF,stroke-width:3px
```

## 9. QA Command Flow

**What it shows:** Recommended sequence for QA commands  
**When to use:** Planning QA activities for a story  
**Best for:** Understanding when to use each QA command

```mermaid
graph LR
    A["📝 Story Draft"] --> B["🎯 *risk"]
    B --> C["📋 *design"]
    C --> D["👩‍💻 Development"]
    D --> E["🔍 *trace (optional)"]
    E --> F["⚡ *nfr (optional)"]
    F --> G["🧪 *review"]
    G --> H["🚪 *gate (if needed)"]
    
    style A fill:#F0F0F0,color:#000000,stroke:#000000,stroke-width:3px
    style B fill:#FFD700,color:#000000,stroke:#000000,stroke-width:3px
    style C fill:#FFA500,color:#000000,stroke:#000000,stroke-width:3px
    style D fill:#32CD32,color:#000000,stroke:#000000,stroke-width:3px
    style E fill:#00BFFF,color:#000000,stroke:#000000,stroke-width:3px
    style F fill:#1E90FF,color:#000000,stroke:#000000,stroke-width:3px
    style G fill:#FF69B4,color:#000000,stroke:#000000,stroke-width:3px
    style H fill:#9370DB,color:#FFFFFF,stroke:#FFFFFF,stroke-width:3px
```

## 10. Technical Debt Management

**What it shows:** How technical debt is identified, tracked, and managed  
**When to use:** When QA identifies non-blocking issues  
**Best for:** Understanding debt acceptance vs. fixing decisions

```mermaid
graph TD
    TD1["🔍 Identify Non-Blocking Issues"] --> TD2["📝 Document in technical-debt.md"]
    TD2 --> TD3["⚠️ Accept CONCERNS Gate"]
    TD3 --> TD4["📊 Track Priority & Effort"]
    TD4 --> TD5["📅 Review During Sprint Planning"]
    TD5 --> TD6{"🤔 Address Now?"}
    TD6 -->|Yes| TD7["🔧 Create Fix Story"]
    TD6 -->|No| TD8["📋 Keep in Backlog"]
    
    style TD1 fill:#FFD700,color:#000000,stroke:#000000,stroke-width:3px
    style TD2 fill:#FF8C00,color:#000000,stroke:#000000,stroke-width:3px
    style TD3 fill:#FFA500,color:#000000,stroke:#000000,stroke-width:3px
    style TD4 fill:#87CEEB,color:#000000,stroke:#000000,stroke-width:3px
    style TD5 fill:#DDA0DD,color:#000000,stroke:#000000,stroke-width:3px
    style TD6 fill:#FF69B4,color:#000000,stroke:#000000,stroke-width:3px
    style TD7 fill:#32CD32,color:#000000,stroke:#000000,stroke-width:3px
    style TD8 fill:#F0F0F0,color:#000000,stroke:#000000,stroke-width:3px
```

## 11. Greenfield vs Brownfield Decision

**What it shows:** Different workflows for new vs existing projects  
**When to use:** Deciding which BMAD workflow to follow  
**Best for:** Project initialization and process selection

```mermaid
graph TD
    A["🚀 Project Type"] --> B{"🤔 Greenfield or Brownfield?"}
    B -->|New Project| C["✨ Standard Planning Workflow"]
    B -->|Existing Project| D["📖 Document Existing System First"]
    
    C --> C1["👥 Analyst → PM → Architect → PO"]
    D --> D1["🏗️ Architect: *document-project"]
    D1 --> D2["👨‍💼 PM: *create-brownfield-prd"]
    D2 --> D3["🏗️ Architect: *create-brownfield-architecture"]
    D3 --> C1
    
    C1 --> E["📂 Shard Documents"]
    E --> F["🔄 SM/Dev Cycle"]
    
    style A fill:#F0F0F0,color:#000000,stroke:#000000,stroke-width:3px
    style B fill:#DDA0DD,color:#000000,stroke:#000000,stroke-width:3px
    style C fill:#00FF00,color:#000000,stroke:#000000,stroke-width:3px
    style D fill:#FF8C00,color:#000000,stroke:#000000,stroke-width:3px
    style C1 fill:#87CEEB,color:#000000,stroke:#000000,stroke-width:3px
    style D1 fill:#FFA500,color:#000000,stroke:#000000,stroke-width:3px
    style D2 fill:#FFD700,color:#000000,stroke:#000000,stroke-width:3px
    style D3 fill:#FFFF00,color:#000000,stroke:#000000,stroke-width:3px
    style E fill:#98FB98,color:#000000,stroke:#000000,stroke-width:3px
    style F fill:#32CD32,color:#000000,stroke:#000000,stroke-width:3px
```

## 12. Epic Completion & Next Steps

**What it shows:** What happens after completing an epic  
**When to use:** End of epic planning and transition  
**Best for:** Understanding post-development activities

```mermaid
graph TD
    C1["🎉 Epic Complete"] --> C2["🔗 Integration Testing"]
    C2 --> C3["⚡ Performance Validation"]
    C3 --> C4["👥 User Acceptance Testing"]
    C4 --> C5{"✅ Ready for Production?"}
    C5 -->|Yes| C6["🚀 Production Deployment"]
    C5 -->|No| C7["🔧 Address Issues"]
    C6 --> C8["📊 Monitoring & Maintenance"]
    C7 --> C2
    
    style C1 fill:#00FF00,color:#000000,stroke:#000000,stroke-width:3px
    style C2 fill:#87CEEB,color:#000000,stroke:#000000,stroke-width:3px
    style C3 fill:#1E90FF,color:#000000,stroke:#000000,stroke-width:3px
    style C4 fill:#FF69B4,color:#000000,stroke:#000000,stroke-width:3px
    style C5 fill:#DDA0DD,color:#000000,stroke:#000000,stroke-width:3px
    style C6 fill:#32CD32,color:#000000,stroke:#000000,stroke-width:3px
    style C7 fill:#FF4500,color:#FFFFFF,stroke:#FFFFFF,stroke-width:3px
    style C8 fill:#9370DB,color:#FFFFFF,stroke:#FFFFFF,stroke-width:3px
```

## Key Success Metrics

### Quality Indicators

- **Story Clarity Score**: Target 9+ / 10
- **QA Quality Score**: Target 90+ / 100
- **Gate Pass Rate**: Target 85%+ PASS
- **Technical Debt**: Managed, not blocking

### Performance Metrics

- **Development Velocity**: Stories per week
- **Context Efficiency**: Agent response quality over time
- **Error Rate**: Missing file references, alignment issues
- **Time to First Code**: Planning phase duration

## Color Legend

- 🟡 **Bright Yellow/Gold** (#FFD700, #FFFF00): Draft states, planning, risk assessment
- 🟢 **Bright Green** (#00FF00, #32CD32): Success, completion, ready states
- 🔵 **Bright Blue** (#00BFFF, #1E90FF): Information, QA processes, reviews
- 🟠 **Bright Orange** (#FF8C00, #FFA500): Planning phases, architecture work
- 🟣 **Purple** (#9370DB, #8A2BE2): Quality gates, decisions - WHITE TEXT
- 🔴 **Red-Orange** (#FF4500): Issues, failures, rework needed - WHITE TEXT
- ⚪ **Light Gray** (#F0F0F0): Neutral processes, starting points

---

_These diagrams represent the complete BMAD Method workflow optimized for dark mode viewing with maximum contrast and readability._
