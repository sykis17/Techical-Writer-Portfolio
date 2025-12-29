--8<-- "includes/revision_header.md"

# Technical Enviroment Setup

To maintain a consistent documentation environment, the following commands are used to initialize the Docs-as-Code workspace.


## 1. Initializing the MkDocs Framework

### Prerequisites:

#### Python 3.x installed
#### Git installed and configured with a GitHub account
#### VS Code with the "Markdown All in One" extension (recommended)

### Install the MkDocs engine
`pip install mkdocs`

### Create the project structure
`mkdocs new .`

### Create file hierarchy
mkdocs.yml : The Configuration file

docs/index.md : The project landing page

docs/ : The directory containing all source Markdown files

## 2. Initializing Github

### Connect the local folder to the remote GitHub repository
`git remote add origin [https://github.com/YOUR_USERNAME/portfolio.git](https://github.com/YOUR_USERNAME/portfolio.git)`

### Set the primary branch to 'main'
`git branch -M main`

### Perform the initial upload
`git push -u origin main`
## 3. Deployment SOP (Sending changes to GitHub)

### Phase 1: Pre-Deployment Verification
1.  **Edit:** Modify `.md` source files.
2.  **Audit Trail:** Update `docs/revision-history.md` with the new Revision Number/Date.
3.  **Local Check:** Run `mkdocs serve` to verify formatting and hyperlinks.

### Phase 2: Version Control
1.  **Status Check:** `git status` (Confirm only intended files are modified).
2.  **Staging:** `git add .` (Stage for commit).
3.  **Log Entry:** `git commit -m "Rev X.X: [Brief description]"`

### Phase 3: Publication
1.  **Sync:** `git push` (Upload source to repository).
2.  **Live Deploy:** `mkdocs gh-deploy` (Update the production website).
3.  **Final Clean-up:** `git status` (Verify 'working tree clean').



## 4. Local Development (Live Preview)
`mkdocs serve`
The documentation will be available at http://127.0.0.1:8000



