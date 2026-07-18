run command to read all file latex and merge into single file
```powershell
uvx gitingest
```

to fix Error reading file with 'cp1252', run 
```powershell
$env:PYTHONUTF8=1 
uvx gitingest
```