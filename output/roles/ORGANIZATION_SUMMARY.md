# Dialog Files Organized by Professional Role

## Overview
All 444 interview dialog files have been analyzed and organized into role-specific folders based on the professional position/job profile of each interviewee.

## Analysis Date
December 5, 2025

## Organization Results

### Summary Statistics
- **Total files processed:** 444
- **Successfully categorized:** 311 (70%)
- **Unknown role:** 133 (30%)
- **Total role categories:** 30

## Role Categories (Ranked by File Count)

### Major Professional Categories (10+ files)

1. **Software Developer / Engineer** - 67 files (660 KB)
   - Game developers, full-stack developers, backend/frontend engineers
   - Programmers, software architects

2. **Manager / Director** - 56 files (540 KB)
   - Team leads, project managers, directors
   - Product managers, business managers

3. **Teacher / Educator** - 40 files (436 KB)
   - K-12 teachers, professors, educators
   - Instructors across various subjects

4. **Writer / Content Creator** - 34 files (344 KB)
   - Authors, novelists, screenwriters
   - Content creators, copywriters

5. **Researcher / Scientist** - 27 files (244 KB)
   - Academic researchers, PhD students
   - Research scientists across disciplines

6. **Sales Professional** - 17 files (172 KB)
   - Sales representatives, account executives
   - Business development professionals

7. **Healthcare Professional** - 12 files (116 KB)
   - Medical data analysts
   - Healthcare practitioners working with patient data

### Medium-Sized Categories (5-10 files)

8. **Marketing Professional** - 8 files (80 KB)
   - Marketing managers, campaign creators
   - Social media and content marketers

9. **Lawyer** - 8 files (80 KB)
   - Attorneys, legal professionals
   - Civil litigation and corporate law

10. **Tutor** - 5 files (52 KB)
    - Private tutors, academic coaches
    - Subject-specific tutors

### Small Categories (2-4 files)

11. **Graphic Designer** - 4 files (36 KB)
12. **Illustrator** - 3 files (32 KB)
13. **Real Estate Professional** - 3 files (32 KB)
14. **Accountant** - 3 files (32 KB)
15. **Consultant** - 3 files (32 KB)
16. **Nurse** - 3 files (36 KB)
17. **Voice Actor** - 2 files (20 KB)
18. **Legal Assistant** - 2 files (20 KB)
19. **Data Scientist / Analyst** - 2 files (20 KB)
20. **Small Business Owner** - 2 files (20 KB)
21. **Athlete** - 2 files (20 KB)

### Individual Professionals (1 file each)

22. **Music Producer / Audio Engineer** - 1 file
23. **Media Composer** - 1 file
24. **Pet Sitter** - 1 file
25. **Travel Agent** - 1 file
26. **Photographer** - 1 file
27. **Product Manager** - 1 file
28. **Bioinformatician** - 1 file
29. **Dietitian** - 1 file

### Unclassified

30. **Unknown** - 133 files (1.1 MB)
    - Conversations where professional role could not be clearly identified
    - Users who didn't explicitly state their profession
    - Roles that didn't fit standard categories

## Folder Structure

```
output/roles/
├── Software_Developer_Engineer/   (67 files)
├── Manager_Director/              (56 files)
├── Teacher_Educator/              (40 files)
├── Writer_Content_Creator/        (34 files)
├── Researcher_Scientist/          (27 files)
├── Sales_Professional/            (17 files)
├── Healthcare_Professional/       (12 files)
├── Marketing_Professional/        (8 files)
├── Lawyer/                        (8 files)
├── Tutor/                         (5 files)
├── Graphic_Designer/              (4 files)
├── Illustrator/                   (3 files)
├── Real_Estate_Professional/      (3 files)
├── Accountant/                    (3 files)
├── Consultant/                    (3 files)
├── Nurse/                         (3 files)
├── Voice_Actor/                   (2 files)
├── Legal_Assistant/               (2 files)
├── Data_Scientist_Analyst/        (2 files)
├── Small_Business_Owner/          (2 files)
├── Athlete/                       (2 files)
├── Music_Producer_Audio_Engineer/ (1 file)
├── Media_Composer/                (1 file)
├── Pet_Sitter/                    (1 file)
├── Travel_Agent/                  (1 file)
├── Photographer/                  (1 file)
├── Product_Manager/               (1 file)
├── Bioinformatician/              (1 file)
├── Dietitian/                     (1 file)
└── Unknown/                       (133 files)
```

## File Format

Each file maintains:
- Original filename (00001.md to 00444.md)
- Complete dialog content
- Transcript ID reference
- Markdown formatting

## Categorization Method

Files were categorized using:
1. **Explicit role declarations** - "I'm a...", "I work as..."
2. **Contextual analysis** - Work descriptions, tasks mentioned, domain-specific vocabulary
3. **Pattern matching** - Professional terminology and workflow descriptions

## Usage Examples

### View all Software Developer conversations:
```bash
cd output/roles/Software_Developer_Engineer
ls -1
```

### Search for specific topics within a role:
```bash
grep -r "machine learning" output/roles/Data_Scientist_Analyst/
```

### Count conversations by role:
```bash
ls -1 output/roles/*/ | wc -l
```

## Notes

- Files are copied (not moved) from the source folder, so originals remain in `output/source/`
- Role names use underscores for folder compatibility
- The categorization prioritizes explicit self-identification over inference
- Files in the "Unknown" folder may benefit from manual review and recategorization