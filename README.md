# IndicWiki Data Collection & Annotation Project

This repository contains guidelines and workflows for collecting raw data from various sources and annotating them using NER (Named Entity Recognition) tagging for the IndicWiki project.

## 📁 Repository Structure

```
IndicWiki_Project/
└── Languages/
    └── Your_Name/
        ├── Raw/           # Upload raw collected data here
        └── Annotated/     # Upload annotated files here
```



## 📋 Raw Data Collection Guidelines

### File Naming Convention

**Format:** `<source>_<topic/article_name>.txt`

**Examples:**
- Wikipedia Tourism page for Hyderabad: `wiki_hyderabad_tourism.txt`
- Blog article on Artificial Intelligence: `blog_artificial_intelligence.txt`
- News article on Cricket: `news_cricket_worldcup.txt`

### File Content Structure

Each raw data file must include the following header information:

```
#URL: [Full URL with http:// or https://]
#Time: [Collection timestamp in DD-MM-YYYY HH:MM format]
#Domain: [Content domain - tourism, technology, sports, general, etc.]
         ➤ If no domain fits, write: General

[Your collected content starts here...]
```

**Example:**
```
#URL: https://en.wikipedia.org/wiki/Tourism_in_Hyderabad
#Time: 04-06-2025 14:43
#Domain: Tourism

Hyderabad, the capital city of Telangana, is known for its rich history...
```

## 🚀 Getting Started

### First Time GitHub Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Soumyadip0806/indicWiki_Data.git
   cd indicWiki_Data
   ```

2. **Set up Git branch:**
   ```bash
   git checkout indicWiki
   ```

3. **Create your folder structure:**
   - Navigate to `Languages/`
   - Create a folder with your name
   - Ensure you have both `Raw/` and `Annotated/` subfolders




### Uploading Raw Data Files

1. **Place your files:**
   - Put your collected raw data files in `Languages/Your_Name/Raw/`
   - Follow the naming convention and content structure

2. **Commit and push:**
   ```bash
   git add .
   git commit -m "Add raw data files: [brief description of files added]"
   git push origin indicWiki
   ```

## 🏷️ Annotation Process

### Step 1: Prepare for Annotation

1. **Update your local repository:**
   ```bash
   git pull origin indicWiki
   ```

2. **Locate your raw files:**
   - Navigate to `Languages/Your_Name/Raw/`
   - Select files that need annotation

### Step 2: Using the Annotation Tool

1. **Access the tool:**
   - Open [Annotation Tool](https://plural.iiit.ac.in/ner-annotator/) in your browser

2. **Upload and annotate:**
   - Upload your raw data file
   - Select words or word spans
   - Apply appropriate NER tags according to guidelines
   - Download the annotated file when complete

3. **Tag Guidelines:**
   - Refer to `guideline.pdf` in the project folder for detailed tagging instructions
   - Ensure consistency in tag application

### Step 3: Upload Annotated Files

1. **Save annotated files:**
   - Place downloaded annotated files in `Languages/Your_Name/Annotated/`
   - Keep the same filename with appropriate suffix if needed

2. **Commit changes:**
   ```bash
   git pull origin indicWiki  # Always pull before pushing
   git add .
   git commit -m "Add annotated files: [description of annotated content]"
   git push origin indicWiki
   ```

## 📝 Best Practices

### Commit Messages
- Use clear, descriptive commit messages
- Examples:
  - `Add raw data: Wikipedia articles on Indian festivals`
  - `Update annotations: Tourism content for major Indian cities`
  - `Fix formatting: Corrected header structure in technology articles`

### File Organization
- Keep raw and annotated files organized in respective folders
- Use consistent naming conventions
- Maintain proper file headers with metadata

### Quality Assurance
- Always review your annotations before uploading
- Follow the tag guidelines strictly
- Ensure URL accessibility and accuracy

## 🔗 Important Links

- **Repository:** [Repo](https://github.com/Soumyadip0806/indicWiki_Data.git)
- **Annotation Tool:** [Tool](https://plural.iiit.ac.in/ner-annotator/)
- **Tag Guidelines:** [Tag Guideline](https://github.com/Soumyadip0806/indicWiki_Data/blob/indicWiki/NER_Guideline.pdf)
- **Working Branch:** [indicWiki](https://github.com/Soumyadip0806/indicWiki_Data/tree/indicWiki)

## ❓ Troubleshooting

### Common Issues

1. **Git conflicts:**
   ```bash
   git pull origin indicWiki
   # Resolve conflicts manually
   git add .
   git commit -m "Resolve merge conflicts"
   git push origin indicWiki
   ```

2. **File upload issues:**
   - Ensure you're in the correct directory
   - Check file naming conventions
   - Verify branch is set to `indicWiki`

3. **Annotation tool problems:**
   - Clear browser cache
   - Try a different browser
   - Ensure stable internet connection

## 📞 Support

If you have any doubt then please ask to [github issues](https://github.com/Soumyadip0806/indicWiki_Data/issues) section.

---

**Remember:** Always pull the latest changes before making new commits to avoid conflicts!
