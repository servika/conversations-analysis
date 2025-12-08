# Individual Dialog Files

## Overview
This folder contains all interview transcripts split into individual dialog files, numbered sequentially.

## File Details
- **Total Dialogs:** 444
- **File Format:** Markdown (.md)
- **Naming Convention:** 5-digit zero-padded numbers (00001.md to 00444.md)
- **Total Size:** ~4.2 MB

## File Structure

Each file contains:
- **Header:** Dialog number
- **Transcript ID:** Original identifier from source CSV
- **Content:** Complete conversation between Assistant/AI and User

## Source Distribution

### Creatives (Dialogs 00001-00027)
- 27 conversations from `creatives_transcripts.csv`
- Topics: AI use in creative professions (artists, designers, composers, etc.)

### Scientists (Dialogs 00028-00088)
- 61 conversations from `scientists_transcripts.csv`
- Topics: AI use in scientific research and data analysis

### Workforce (Dialogs 00089-00444)
- 356 conversations from `workforce_transcripts.csv`
- Topics: AI use across various professional roles and industries

## Example Usage

To read a specific dialog:
```bash
cat 00001.md
```

To search across all dialogs:
```bash
grep -l "specific term" *.md
```

To count total lines across all dialogs:
```bash
wc -l *.md
```

## File Format Example

```markdown
# Dialog 00001

**Transcript ID:** creativity_0009

---