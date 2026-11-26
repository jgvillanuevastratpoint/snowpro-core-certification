# Contributing
 
Thanks for helping improve this study repository. Fixes, new material, and suggestions are all welcome.

## Repository structure
 
```text
.
├── README.md                  # What this repo is and where to start
├── CONTRIBUTING.md            # This guide
├── .github/
│   ├── PULL_REQUEST_TEMPLATE.md
│   └── ISSUE_TEMPLATE/        # Issue templates
├── study-guide/               # Outline, notes, quick references
└── quiz/                      # One file per exam domain
    ├── domain-1-architecture.md
    ├── domain-2-governance.md
    ├── domain-3-loading.md
    ├── domain-4-performance.md
    └── domain-5-collaboration.md
```
 
## What you can contribute
 
- Corrections to answers, explanations, or typos
- New quiz questions
- Study notes and useful references
- Fixes for broken or outdated links
## How to contribute
 
1. **Open an issue** for anything bigger than a small fix, so others know you are working on it.
2. **Create a branch** from an up-to-date `main`. Do not commit directly to `main`.
3. **Make your change.** Keep each pull request focused on one thing.
4. **Commit** with a short, clear message, such as `Fix answer for D1-012`.
5. **Open a pull request** and describe what changed and why.
6. **Get one approval** from someone other than yourself, then merge.
### Using the GitHub website
 
Open the file, select the pencil icon, make your edit, then choose the option to create a new branch and start a pull request.
 
### Using the command line
 
```bash
git clone <repository-url>       # first time only
cd <repository-folder>
 
git switch main
git pull
git switch -c fix/short-description
 
# edit your files, then:
git add <file>
git commit -m "Describe your change"
git push -u origin fix/short-description
```
 
Then open a pull request on GitHub.
 
### Branch names
 
| Prefix | Use for | Example |
|---|---|---|
| `fix/` | Corrections | `fix/d1-012-answer` |
| `add/` | New content | `add/domain-3-questions` |
| `docs/` | Guides and README | `docs/update-readme` |
 
## Quiz questions
 
- Give four options with exactly one correct answer.
- Number by domain (`D1-001`, `D2-001`) and do not reuse numbers.
- Put the answer, a short explanation, and a source link in the answer key at the bottom of the same file.
```markdown
**D1-048.** Question text?
 
- A. Option
- B. Option
- C. Option
- D. Option
```
 
Answer key row:
 
```markdown
| ID | Answer | Explanation | Source |
|---|---|---|---|
| D1-048 | B | One-sentence reason. | [Doc title](https://docs.snowflake.com/...) |
```
 
## Content rules
 
- **No real exam questions or exam dumps.** Sharing them can breach the exam agreement and put certifications at risk.
- **Check facts** against the [official Snowflake documentation](https://docs.snowflake.com/).
- **Use your own words.** Do not paste text from documentation, courses, or books.
- **Never commit secrets**, such as passwords, keys, or account details.
## Review checklist
 
- [ ] The information is correct and has a source
- [ ] It does not duplicate existing content
- [ ] The answer key matches the question
- [ ] Links work and the Markdown displays properly
## Be respectful
 
Comment on the content, not the person. Explain why you suggest a change, and ask when unsure.
 
