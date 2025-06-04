# IndicWiki Data Collection and Annotation Guidelines

Welcome to the IndicWiki Data repository! This README provides clear instructions on how to:

1. Collect and format raw data files.
2. Upload raw and annotated files to the GitHub repository.
3. Organize files within the GitHub folder structure.
4. Perform annotation using our annotation tool and tagging guidelines.

---

## 1. Raw Data Collection Format

To maintain consistency, each raw text file must follow the naming convention and internal structure outlined below.

### 1.1 File Naming Convention
```
<source>_<topic_or_article_name>.txt
```
- `<source>`: The origin of the text (e.g., `wiki`, `blog`, `news`).
- `<topic_or_article_name>`: A concise descriptor of the content.

**Examples:**
- If the source is Wikipedia and the article is about Hyderabad tourism:
  ```
wiki_hyderabad.txt
  ```
- If the source is a blog and the article is about artificial intelligence:
  ```
blog_artificial_intelligence.txt
  ```

### 1.2 Inside Each File
Each raw text file should begin with three metadata fields (URL, Time, Domain), followed by the actual content.

```
URL: <full URL including http:// or https://>
Time: <DD-MM-YYYY HH:MM>   # e.g., 04-06-2025 14:43
Domain: <domain category>   # e.g., tourism, technology, sports, General

<Your article's content goes here...>
```

**Example:**
```
URL: https://en.wikipedia.org/wiki/Hyderabad
Time: 04-06-2025 14:43
Domain: tourism

Hyderabad is the capital of the southern Indian state of Telangana...
```

- **URL**: Copy the exact URL of the source article.
- **Time**: Record the date and time at which you collected the data (format: DD-MM-YYYY HH:MM).
- **Domain**: Specify the category or domain. If no specific domain applies, write `General`.
- **Content**: The body text of the article.

---

## 2. GitHub Repository Setup & Upload Instructions

All contributors should use the `indicWiki` branch for uploading raw and annotated data.

### 2.1 Cloning the Repository (First Time)
1. Open your Terminal (or Git Bash).
2. Run:
   ```bash
   git clone https://github.com/Soumyadip0806/indicWiki_Data.git
   ```
3. Navigate into the cloned folder:
   ```bash
   cd indicWiki_Data
   ```

### 2.2 Placing Your Files
1. Within the `indicWiki_Data` root folder, locate the `Languages` directory.
2. Inside `Languages`, create a new folder named after yourself (e.g., `Soumya`, `Alex`, `Priya`).
3. Within your named folder, you will find two sub-folders: `Raw` and `Annotated`.
   - **Raw**: Place all newly collected raw text files here.
   - **Annotated**: Place finalized annotation files (after using the annotation tool) here.

### 2.3 Uploading Changes to GitHub
1. From the `indicWiki_Data` root folder, ensure you are on the `indicWiki` branch:
   ```bash
   git checkout indicWiki
   ```
2. Add your new/modified files:
   ```bash
   git add .
   ```
3. Commit with a clear, understandable message describing your changes (e.g., `Add raw tourism data for Hyderabad`):
   ```bash
   git commit -m "<Your commit message>"
   ```
4. Push to the `indicWiki` branch:
   ```bash
   git push origin indicWiki
   ```

> **Note:** If you encounter any merge conflicts, please resolve them locally before pushing. Use `git pull origin indicWiki` to fetch the latest changes first.

---

## 3. GitHub Folder Structure

```text
indicWiki_Data/
├── Languages/
│   ├── <Your_Name>/
│   │   ├── Raw/         # Place raw collected data files here
│   │   └── Annotated/   # Place annotated files here
│   └── <Other_Contributor_Names>/
│       ├── Raw/
│       └── Annotated/
└── README.md            # This file
```

- **Languages/**: Root directory for all language contributors.
- **<Your_Name>/**: A personal folder for each contributor (replace `<Your_Name>` with your actual name).
- **Raw/**: Sub-folder for uploading raw, unannotated text files.
- **Annotated/**: Sub-folder for uploading NER-annotated files after using the annotation tool.

---

## 4. Annotation Workflow

To annotate raw text files with NER tags, follow the steps below.

### 4.1 Cloning or Pulling Latest Changes
1. If you have not cloned the repository yet, follow Section 2.1.
2. If you already have a local copy, navigate to the `indicWiki_Data` folder and run:
   ```bash
   git checkout indicWiki
   git pull origin indicWiki
   ```

### 4.2 Selecting Files to Annotate
1. Go to your named folder under `Languages/<Your_Name>/Raw/`.
2. Choose a raw text file (e.g., `wiki_hyderabad.txt`) that you want to annotate.

### 4.3 Using the Annotation Tool
1. Open your web browser and navigate to the annotation tool:
   > **Annotation Tool:** [Headline Annotator](https://plural.iiit.ac.in/headline-annotator/)
2. Upload your selected raw text file.
3. For each word or word span:
   - Select the appropriate NER tag (e.g., `b-PER`, `i-LOC`, etc.).
   - Annotate entities consistently following the Tag Guideline.
4. After completing all annotations, download the annotated file.

### 4.4 Saving and Uploading Annotated Files
1. Move the downloaded annotated file into your `Languages/<Your_Name>/Annotated/` folder.
2. Return to the `indicWiki_Data` root folder in your terminal:
   ```bash
   cd ../../               # Adjust path if needed
   git add .
   git commit -m "Add annotated NER data for <Filename>"
   git push origin indicWiki
   ```

> **Tip:** Always run `git pull origin indicWiki` before starting new annotations to ensure you have the latest version of the repository.

---

## 5. Tagging Guidelines

- Detailed tagging guidelines can be found in the `guideline.pdf` file located in the `Tag_Guideline/` folder at the repository root.
- Please review the guidelines carefully to ensure consistent annotation across all contributors.

---

## 6. Additional Notes

- If you discover any issues with file naming, formatting, or annotation, please open an issue on GitHub or reach out to the repository owner.
- For questions about the annotation schema or tags, refer to the `guideline.pdf` or contact the annotation team.
- Always keep your local `indicWiki` branch up to date with the remote repository to minimize conflicts.

---

Thank you for contributing to the IndicWiki Data project! Your efforts are essential in building high-quality NER and language resources for Indic languages.
