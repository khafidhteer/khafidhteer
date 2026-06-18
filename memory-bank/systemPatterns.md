# System Patterns: khafidhteer GitHub Profile README

## Repository Architecture
```
khafidhteer/
├── .gitignore              # Public-facing file rules
├── .clinerules             # Cline AI configuration rules
├── memory-bank/            # Persistent project context (private)
│   ├── projectbrief.md
│   ├── productContext.md
│   ├── activeContext.md
│   ├── systemPatterns.md
│   └── techContext.md
├── README.md               # The only file visible on GitHub
├── CV_Khafidh Tri Ramdhani - Data Analyst_Scientist.pdf   # Source of truth (gitignored)
├── CV_Khafidh Tri Ramdhani - GTM Engineer.pdf              # Source of truth (gitignored)
├── CV_Khafidh Tri Ramdhani - Revenue Operation.pdf         # Source of truth (gitignored)
└── khafidhteer-summary.md # GitHub profile data (gitignored)
```

## Design Patterns

### Content Sourcing Pattern
1. **CV PDFs** → Extract factual work history, role titles, dates, achievements
2. **khafidhteer-summary.md** → Extract GitHub repo data, languages, topics
3. **Combine** into README.md with accurate attributions

### SEO Integration Pattern
- Keywords are placed in: H1/H2 headings, introductory paragraphs, skill sections, project descriptions
- Keywords are always used naturally within factual statements
- No keyword stuffing: each keyword appears 2-4 times maximum

### Gitignore Strategy
- `*` at root ignores everything
- `!` exceptions allow specific files to be tracked
- Only `README.md` is intended for public GitHub consumption
- Memory-bank and config files are tracked locally for AI tool context

### Update Pattern
- When career updates are needed: revise README.md using CV PDFs as source
- When GitHub repos change: re-run webdocs2md gh-profile to refresh summary
- Record all changes in activeContext.md