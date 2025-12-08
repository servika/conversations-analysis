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

## Dataset

This repository contains interview transcripts from 1,250 professionals:
- **General Workforce** (N=1,000)
- **Creatives** (N=125)
- **Scientists** (N=125)

All participants provided informed consent for public release.

## License

Data released under CC-BY, code released under MIT License

## Contact

For inquiries, contact kunal@anthropic.com. 

## Citation
```bibtex
@online{handa2025interviewer,
  author = {Kunal Handa and Michael Stern and Saffron Huang and Jerry Hong and Esin Durmus and Miles McCain and Grace Yun and AJ Alt and Thomas Millar and Alex Tamkin and Jane Leibrock and Stuart Ritchie and Deep Ganguli},
  title = {Introducing Anthropic Interviewer: What 1,250 professionals told us about working with AI},
  year = {2025},
  url = {https://anthropic.com/research/anthropic-interviewer},
}
```
