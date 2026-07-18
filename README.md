original latex template [Master Thesis Templete for TDTU version Vietnamese](https://www.overleaf.com/latex/templates/master-thesis-templete-for-tdtu-version-vietnamese/phrsbqgqvqch)

latex editor: [Overleaf](overleaf.com), pdfLaTeX compiler normal mode (not Fast[Draf] mode), Tex live version: 2025

advice: in the first compile, you should clear cache in overleaf to it compile for the best result render into pdf

run command to read all file latex and merge into single file
```powershell
uvx gitingest
```

to fix `Error reading file with 'cp1252'`, run 
```powershell
$env:PYTHONUTF8=1 
uvx gitingest
```