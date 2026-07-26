# TDTU Report LaTeX Template (Vietnamese Version)

This repository is built upon the original **[Master Thesis Template for TDTU version Vietnamese](https://www.overleaf.com/latex/templates/master-thesis-templete-for-tdtu-version-vietnamese/phrsbqgqvqch)** hosted on Overleaf.

## Recommended Setup

To ensure your document renders perfectly without missing elements, configure your environment with the following settings:

* **Editor online:** [Overleaf](https://overleaf.com)
* **Compiler:** `pdfLaTeX` set to **Normal mode** (Avoid using Fast[Draft] mode)
* **TeX Live Version:** 2025

> **Quick Tip:** If your recent edits do not show up in the compiled PDF, your editor might be holding onto old data. Simply clear the cache in the Overleaf menu and recompile the project.

## Consolidating Project Files

If you need to scan your entire directory and merge all separate LaTeX files into a single continuous file for easier review, you can utilize `gitingest`.

Open **Terminal** and execute the following command:

```terminal
uvx gitingest
```

### Handling Encoding Issues

When you run `uvx gitingest` command on **PowerShell**, you might encounter a character encoding error like `Error reading file with 'cp1252'`. You can easily bypass this by forcing Python to operate in UTF-8 mode. Run this command instead:

```powershell
$env:PYTHONUTF8=1 
uvx gitingest
```