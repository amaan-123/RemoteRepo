# Clone a Remotely Created Repo on GitHub to Local Machine

## Create a New Repo on GitHub Web

For example, if your repository name is **RemoteRepo** (replace *RemoteRepo* with your actual repo name), follow these good practices while setting it up:

1) Provide a **clear & concise description**.
2) **Add a README** file.
3) **Add a `.gitignore` file**: Select **Visual Studio** (if you use it).
   - **Why?** This prevents unnecessary files like compiled binaries, temporary files, and user-specific settings from being committed.
4) **Choose a license**: MIT License.
   - **Why?** The MIT License is a permissive open-source license that allows others to use, modify, and distribute your code with minimal restrictions while protecting you from legal liabilities.

### Set Branch Protection Rules

After creating the **RemoteRepo** repository on GitHub, navigate to **Settings** → **Code and Automation** → **Branches**:

- **Branch name pattern**: `main`
- **Protect matching branches**:  
  - Select **"Require a pull request before merging"** checkbox.
  - **Why?** This ensures that code changes are reviewed before being merged, preventing accidental changes and maintaining project integrity.

### Edit Files Online

You can **edit** or **create new files** in your **RemoteRepo** repository on GitHub, such as modifying the `README.md` file, and commit the changes online.

---

## Clone & Check Status

### Clone the Repository

To **clone** a remote repository to your local machine (e.g., cloning the **RemoteRepo** from GitHub to your local PC/laptop), use the following command:

#### Steps

1) Obtain your GitHub repository's **HTTPS link**:
   - Navigate to your repository on GitHub.
   - Click the **Code** button (green).
   - Under **Local**, copy the **HTTPS link**.
2) Open **VS Code** and select your default terminal profile as **Git Bash**.
3) Run the following command:

```bash
git clone "https://github.com/username/RemoteRepo.git"
```

### Configure Git User Information (If Not Already Set)

Before making any commits, ensure Git is configured with your user details:

```bash
git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"
```

### Check Repository Status

After cloning, verify the repository status:

```bash
ls -a  # Should display .git directory (indicating a Git repo)
git status  # Shows the types of file status
```

---

## Add & Commit Changes

### Add Files to Staging Area

```bash
git add "file_name"  # Add a specific file
git add .  # Adds all modified and new files
git status  # Check status after adding
```

### Commit Changes

```bash
git commit -m "Some message"
git status  # Verify commit status
```

---

## Pull Latest Changes (Best Practice Before Pushing)

Before pushing changes, it's a good practice to **pull the latest changes** from the remote repository to avoid conflicts:

```bash
git pull origin main
```

---

## Push to GitHub

```bash
git push origin main
```

> ⚠️ Authorization occurs at this step between **VS Code** & **GitHub**.
