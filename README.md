---
license: mit
viewer: true
language:
- en
pretty_name: AnthropicInterviewer
configs:
- config_name: AnthropicInterviewer
  default: true
  data_files:
  - split: workforce
    path: "interview_transcripts/workforce_transcripts.csv"
  - split: creatives
    path: "interview_transcripts/creatives_transcripts.csv"
  - split: scientists
    path: "interview_transcripts/scientists_transcripts.csv"
---

# AI Research - Interview Analysis

Analysis of interview transcripts exploring how professionals integrate AI into their work and their perspectives on its future role.

## Overview

This project analyzes interview transcripts from 1,250 professionals across three categories:
- **General Workforce** (N=1,000) - 356 conversations analyzed
- **Creatives** (N=125) - 27 conversations analyzed
- **Scientists** (N=125) - 61 conversations analyzed

**Total conversations analyzed**: 444 individual dialogs

## Project Structure

```
.
├── interview_transcripts/       # Source CSV files
│   ├── creatives_transcripts.csv
│   ├── scientists_transcripts.csv
│   └── workforce_transcripts.csv
├── output/                      # Generated analysis (gitignored)
│   ├── roles/                  # Individual conversations by role (30 categories)
│   └── source/                 # All conversations numbered sequentially
├── results/                     # Summary reports (gitignored)
│   ├── README.md               # Analysis overview
│   └── *-summary.md            # 9 professional role summaries
├── index.js                     # Analysis script
└── package.json                 # Project configuration
```

## Analysis Results

### Professional Roles Identified (30 categories)

**Major Categories** (with summary reports in `results/`):
1. Software Developers & Engineers (67 conversations)
2. Managers & Directors (56 conversations)
3. Teachers & Educators (40 conversations)
4. Writers & Content Creators (34 conversations)
5. Researchers & Scientists (27 conversations)
6. Sales Professionals (17 conversations)
7. Healthcare Professionals (12 conversations)
8. Marketing Professionals (8 conversations)
9. Lawyers (8 conversations)

**Additional Categories**: Accountants, Athletes, Consultants, Data Scientists, Graphic Designers, Illustrators, Nurses, Photographers, Product Managers, Real Estate Professionals, Tutors, and 10+ more specialized roles.

**Unclassified**: 133 conversations (30%) where professional role couldn't be determined

### Key Findings

#### Top AI Use Cases Across All Roles
1. Communication & Writing - Email drafting, document creation
2. Research & Learning - Information gathering, skill development
3. Content Generation - Creating various professional content
4. Analysis & Processing - Data interpretation, pattern recognition
5. Brainstorming & Ideation - Creative problem-solving support

#### Most Reported Benefits
- **Efficiency Gains** - Significant time savings on routine tasks
- **Quality Improvement** - Better outputs through AI assistance
- **Speed Enhancement** - Faster workflow completion
- **Enhanced Creativity** - New ideas and perspectives
- **Learning Support** - Skill development and knowledge expansion

#### Common Concerns
- **Accuracy & Reliability** - Need for verification and validation
- **Job Security** - Automation and displacement concerns
- **Skill Degradation** - Maintaining expertise while using AI
- **Authenticity** - Preserving personal voice and judgment
- **Over-reliance** - Balancing assistance with dependence

## Usage

### Run Analysis
```bash
node index.js
```

### View Results
- Browse individual conversations: `output/roles/[Role_Name]/`
- Read summary reports: `results/*-summary.md`
- See analysis overview: `results/README.md`

## Data Source

Based on the [Anthropic Interviewer dataset](https://huggingface.co/datasets/Anthropic/AnthropicInterviewer) - a tool for conducting AI-powered qualitative research interviews at scale.

All participants provided informed consent for public release.

## License

Data released under CC-BY, code released under MIT License

## Citation
```bibtex
@online{handa2025interviewer,
  author = {Kunal Handa and Michael Stern and Saffron Huang and Jerry Hong and Esin Durmus and Miles McCain and Grace Yun and AJ Alt and Thomas Millar and Alex Tamkin and Jane Leibrock and Stuart Ritchie and Deep Ganguli},
  title = {Introducing Anthropic Interviewer: What 1,250 professionals told us about working with AI},
  year = {2025},
  url = {https://anthropic.com/research/anthropic-interviewer},
}
```

## Contact

For inquiries about the original dataset, contact kunal@anthropic.com.
