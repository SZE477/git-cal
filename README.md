# git-cal 🗓️

A command-line tool that visualizes Git commit history in a "GitHub contributions"-style calendar.  
**New in v0.9.2**: support for extended history beyond 13 months! (Fixes #58)

---

## 🚀 Features

- Visualize commit frequency with ASCII, ANSI, or Unicode blocks  
- Filter by author (`--author`)  
- Include all branches (`--all`)  
- Now supports `--period=-N` for any N months in the past (not limited to 11)  

---

## 🧱 Installation

Make sure you have Perl and Git installed:

bash
git clone https://github.com/k4rthik/git-cal.git
cd git-cal
perl Makefile.PL
make
sudo make install
Alternatively, install via Homebrew (macOS/Linux):
brew install git-cal

🏃 Running Locally
Generate the contribution calendar with:
git-cal [options] [<filepath>]
Example – Extended history:
git-cal --all --author="nferraz" --period=-36
Displays commits by nferraz across all branches over the past 36 months.
Other useful flags:
    • --ascii, --ansi, --unicode: choose output style
    • --author="Name": filter commits by author
    • --all: include all branches
    • --period=N:
        ◦ 1–12: specific month of the year
        ◦ -N (any negative): past N months (extended support)

👁️‍🗨️ Output Example
     Jun       Jul          Aug          Sep             Oct          Nov          Dec             Jan          Feb          Mar             Apr          May          Jun       
 Mon ▢ ⬚ ▣ ▤ ▢ ⬚ ▢ ⬚ ▢ ▢ ⬚ ▢ ⬚ ⬚ ⬚ ▢ ⬚ ⬚ ▢ ▢ ▣ ▢ ▤ ▢ ▢ ⬚ ▢ ▢ ⬚ ⬚ ▢ ▢ ⬚ ⬚ ▢ ⬚ ▢ ▢ ⬚ ▢ ⬚ ▢ ▤ ⬚ ⬚ ⬚ ▢ ⬚ ⬚ ⬚ ▢ ⬚ ⬚ 
 Wed ⬚ ⬚ ▤ ▢ ▢ ▢ ▢ ⬚ ▢ ▢ ▢ ⬚ ⬚ ▢ ▢ ⬚ ⬚ ▢ ▢ ▢ ⬚ ▢ ⬚ ▢ ▢ ⬚ ⬚ ⬚ ⬚ ⬚ ▢ ▢ ▢ ⬚ ▢ ▤ ⬚ ▢ ⬚ ⬚ ▢ ⬚ ⬚ ⬚ ▤ ▢ ▢ ⬚ ▢ ▢ ▢ ⬚ ⬚ 
 Fri ▢ ▢ ⬚ ▢ ▢ ▢ ▢ ⬚ ▢ ⬚ ⬚ ▢ ▢ ⬚ ▤ ⬚ ▢ ⬚ ▢ ▢ ⬚ ▢ ⬚ ⬚ ▢ ▢ ⬚ ⬚ ⬚ ⬚ ⬚ ▢ ▢ ⬚ ⬚ ▢ ▢ ⬚ ⬚ ⬚ ▢ ▢ ⬚ ▢ ▤ ⬚ ⬚ ⬚ ▤ ⬚ ▢ ▢ 
Total commits in the selected period: 697
Blocks represent daily commit ranges. The legend below shows intensity.

🛠️ Fixes & Changelog
v0.9.2
    • Fix #58: Removed hardcoded limit --since="13 months" (line 90)
        ◦ Now supports --period=-N for any N months
        ◦ Closes #58

📘 Usage Tips
    • To view all history of an author:
      git config calendar.period 12
      git-cal --all --author="nferraz"
    • For a specific month (e.g., April):
      git-cal --period=4

🚧 Contribution Guide
    1. Fork & clone the repo
    
    2. Create a branch: git checkout -b fix/issue-xx
    
    3. Apply your changes
    
    4. Commit with reference: git commit -m "fix(scope): description (closes #xx)"
    
    5. Push & open a Pull Request

📄 License
MIT (see LICENSE)

📚 See Also
    • Run git-cal --help for full details
    • Project repo: https://github.com/k4rthik/git-cal

---

### 🧠 Why this works**
- **Concise overview** at the top with a status badge  
- **Installation** & **Usage** sections follow best practices for CLI tools :contentReference[oaicite:22]{index=22}  
- **Examples** demonstrate the extended `--period=-N` feature  
- **Changelog** documents the fix so users understand the update  
- **Contribution guide** encourages future contributions

