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

# Anthropic Interviewer

A tool for conducting AI-powered qualitative research interviews at scale. In this study, we used Anthropic Interviewer to explore how 1,250 professionals integrate AI into their work and how they feel about its role in their future.

## Overview

This repository contains both the raw interview transcripts and comprehensive analysis of conversations with professionals across various industries. The analysis reveals detailed insights into AI adoption patterns, use cases, benefits, concerns, and future perspectives across different professional roles.

## Dataset

### Data Source

This project uses the **Anthropic Interviewer** dataset, publicly available on Hugging Face:

**🔗 [Anthropic/AnthropicInterviewer on Hugging Face](https://huggingface.co/datasets/Anthropic/AnthropicInterviewer)**

The dataset contains interview transcripts from 1,250 professionals:
- **General Workforce** (N=1,000)
- **Creatives** (N=125)
- **Scientists** (N=125)

All participants provided informed consent for public release.

**Loading the Dataset:**
```python
from datasets import load_dataset

# Load full dataset
dataset = load_dataset("Anthropic/AnthropicInterviewer")

# Load specific splits
workforce = load_dataset("Anthropic/AnthropicInterviewer", split="workforce")
creatives = load_dataset("Anthropic/AnthropicInterviewer", split="creatives")
scientists = load_dataset("Anthropic/AnthropicInterviewer", split="scientists")
```

### Analysis Coverage

**Processing Status:**

| Category | Available | Processed | Coverage |
|----------|-----------|-----------|----------|
| Workforce | 1,000 | 1,000 | 100% ✅ |
| Creatives | 125 | 125 | 100% ✅ |
| Scientists | 125 | 125 | 100% ✅ |
| **Total** | **1,250** | **1,250** | **100%** ✅ |

**Analysis Statistics:**
- **Total Conversations Processed**: 1,250 individual dialogs (100% of dataset)
- **Professional Roles Identified**: 31 distinct categories
- **Conversations Categorized**: 910 (72.8%)
- **Detailed Analysis Reports**: 9 major professional roles
- **Time Period**: 2024-2025
- **Last Updated**: December 2025

## Project Structure

```
AI research/
├── interview_transcripts/          # Raw interview data
│   ├── workforce_transcripts.csv   # General workforce interviews (N=1,000)
│   ├── creatives_transcripts.csv   # Creative professionals (N=125)
│   └── scientists_transcripts.csv  # Scientists and researchers (N=125)
│
├── scripts/                        # Analysis and processing scripts
│   ├── parse_transcripts.js        # Parse CSV transcripts into individual files
│   ├── split_dialogs.js            # Split conversations into dialog format
│   ├── parse_by_position.js        # Organize transcripts by professional position
│   ├── organize_by_role.js         # Categorize conversations by role
│   └── analyze_all_roles.js        # Generate comprehensive role-based analysis
│
├── output/                         # Processed transcript files
│   ├── source/                     # All 1,250 conversations (individual markdown files)
│   ├── roles/                      # Conversations organized by 31 professional roles
│   └── missing_transcripts/        # Analysis of processing coverage
│
├── results/                        # Analysis reports and summaries
│   ├── README.md                   # Detailed methodology and overview
│   ├── SUMMARY.md                  # High-level findings across all roles
│   └── *-summary.md                # 9 role-specific analysis reports
│
├── README.md                       # This file
├── package.json                    # Node.js dependencies
└── index.js                        # Main entry point
```

## Results & Analysis

The `results/` folder contains comprehensive analysis reports for different professional roles. Each report provides deep insights into how professionals in that field use AI.

### Available Analysis Reports

1. **[Software Developers & Engineers](results/software_developer_engineer-summary.md)** (192 conversations)
   - Primary uses: Code generation, debugging, API integration, testing
   - Comprehensive analysis of AI usage in software development

2. **[Writers & Content Creators](results/writer_content_creator-summary.md)** (149 conversations)
   - Primary uses: Writing & drafting, editing, brainstorming, research
   - Focus: Maintaining creative voice while leveraging AI

3. **[Managers & Directors](results/manager_director-summary.md)** (136 conversations)
   - Primary uses: Email & communication, brainstorming, HR
   - Focus: Leadership and organizational efficiency

4. **[Teachers & Educators](results/teacher_educator-summary.md)** (124 conversations)
   - Primary uses: Student support, lesson planning, parent communication
   - Focus: Educational quality and student outcomes

5. **[Researchers & Scientists](results/researcher_scientist-summary.md)** (75 conversations)
   - Primary uses: Data analysis, literature review, paper writing, coding
   - Focus: Balance between AI assistance and rigorous validation

6. **[Sales Professionals](results/sales_professional-summary.md)** (51 conversations)
   - Primary uses: Customer communication, pitch development
   - Focus: Personalization and relationship building

7. **[Healthcare Professionals](results/healthcare_professional-summary.md)** (21 conversations)
   - Primary uses: Patient documentation, clinical communication
   - Focus: Accuracy and compliance

8. **[Marketing Professionals](results/marketing_professional-summary.md)** (15 conversations)
   - Primary uses: Content creation, strategy, social media
   - Focus: Creative applications with data-driven insights

9. **[Lawyers](results/lawyer-summary.md)** (15 conversations)
   - Primary uses: Legal research, document drafting
   - Focus: Verification and professional responsibility

**Total Analyzed**: 778 conversations across 9 major professional roles

### Report Structure

Each summary report includes:
- Executive Summary with key statistics
- Top Use Cases ranked by frequency
- Primary Benefits reported by professionals
- Tools & Platforms mentioned
- Representative Insights (direct quotes)
- Concerns & Challenges
- Future Perspectives
- Conclusions and key takeaways

### Key Findings Across All Roles

**Most Common AI Use Cases:**
1. Communication & Writing (email drafting, document creation)
2. Research & Learning (information gathering, skill development)
3. Content Generation (creating professional content)
4. Analysis & Processing (data interpretation, pattern recognition)
5. Brainstorming & Ideation (creative problem-solving)

**Top Benefits Reported:**
- Efficiency Gains - Significant time savings on routine tasks
- Quality Improvement - Better outputs through AI assistance
- Speed Enhancement - Faster completion of workflows
- Creativity Boost - New ideas and perspectives
- Learning Support - Skill development and knowledge expansion

**Common Concerns:**
- Accuracy & Reliability - Need for verification
- Job Security - Concerns about automation
- Skill Degradation - Maintaining expertise while using AI
- Authenticity - Preserving personal voice and judgment
- Over-reliance - Balance between assistance and dependence

**Most Mentioned Tools:**
- ChatGPT - Most frequently mentioned across all roles
- Claude - Growing usage for various professional tasks
- GitHub Copilot - Popular among developers
- Gemini - Emerging in various professional contexts

## Usage

### Accessing Raw Transcripts

```bash
# View a specific transcript
cat output/source/00001.md

# Search across all transcripts
grep -r "keyword" output/source/
```

### Reading Analysis Reports

```bash
# View a specific role's summary
cat results/software_developer_engineer-summary.md

# View overall summary
cat results/SUMMARY.md

# Search across all analysis reports
grep -r "ChatGPT" results/*-summary.md
```

### Running Analysis Scripts

```bash
# Install dependencies
npm install

# Parse raw transcripts
node scripts/parse_transcripts.js

# Organize by professional role
node scripts/organize_by_role.js

# Generate analysis reports
node scripts/analyze_all_roles.js
```

## License

Data released under CC-BY, code released under MIT License

## Contact

For inquiries about the dataset or research, contact kunal@anthropic.com

## Citation
```bibtex
@online{handa2025interviewer,
  author = {Kunal Handa and Michael Stern and Saffron Huang and Jerry Hong and Esin Durmus and Miles McCain and Grace Yun and AJ Alt and Thomas Millar and Alex Tamkin and Jane Leibrock and Stuart Ritchie and Deep Ganguli},
  title = {Introducing Anthropic Interviewer: What 1,250 professionals told us about working with AI},
  year = {2025},
  url = {https://anthropic.com/research/anthropic-interviewer},
}
```
