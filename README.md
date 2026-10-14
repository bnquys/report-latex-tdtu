# TDTU Report LaTeX Template (Vietnamese Version)

This repository is built upon the original **[Master Thesis Template for TDTU version Vietnamese](https://www.overleaf.com/latex/templates/master-thesis-templete-for-tdtu-version-vietnamese/phrsbqgqvqch)** hosted on Overleaf.

<p align="center">
  <img src="https://i.ibb.co/k2bfQTJP/img-demo-1.jpg" alt="Trang bìa" border="0" width="33%">
  <img src="https://i.ibb.co/XZjs98zY/img-demo-2.jpg" alt="Mục lục" border="0" width="33%">
  <img src="https://i.ibb.co/vCLDPSFS/11.jpg" alt="Nội dung" border="0" width="33%">
</p>

## Recommended Setup

To ensure your document renders perfectly without missing characters or formatting glitches, you can choose one of the following setups:

### Option 1: Overleaf (Cloud-based)

* **Editor:** [Overleaf](https://overleaf.com)
* **Compiler:** `pdfLaTeX` set to **Normal mode** (Avoid using Fast[Draft] mode)
* **TeX Live Version:** 2025

> **Quick Tip:** If your recent edits do not show up in the compiled PDF, your editor might be holding onto cached build artifacts. Simply clear the cache in the Overleaf menu and recompile the project.

> **Note:** Overleaf Free tier frequently hits compilation timeout limits on complex documents or large bibliographies. If your build times out, strongly consider switching to local environments (Option 2 or Option 3).

### Option 2: VS Code + MiKTeX (Local)

* **TeX Distribution:** [MiKTeX](https://miktex.org/) (ensure automatic package installation is enabled)
* **Editor:** [Visual Studio Code](https://code.visualstudio.com/)
* **Extension:** [LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop)
* **Compiler Configuration:** Configure the build recipe in `.vscode/settings.json` to compile using `pdflatex -> biber -> pdflatex * 2`:
```json
"latex-workshop.latex.recipes": [
  {
    "name": "pdflatex -> biber -> pdflatex * 2",
    "tools": [
      "pdflatex",
      "biber",
      "pdflatex",
      "pdflatex"
    ]
  }
]
```

### Option 3: TeXstudio + MiKTeX (Local)

* **TeX Distribution:** [MiKTeX](https://miktex.org/)
* **Editor:** [TeXstudio](https://www.texstudio.org/)
* **Build Settings:**
* Navigate to **Options** -> **Configure TeXstudio** -> **Build**.
* Set **Default Compiler** to `PdfLaTeX`.
* Ensure the TeX distribution binary path points correctly to your MiKTeX installation.

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
