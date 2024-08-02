# Conda Cheatsheet

## 

### Options

    -h, --help          Show this help message and exit.
    -v, --verbose       Can be used multiple times. Once for detailed output, twice for INFO logging, thrice for DEBUG logging, four times for TRACE logging.
    --no-plugins        Disable all plugins that are not built into conda.
    -V, --version       Show the conda version number and exit.


### Commands

    activate              Activate a conda environment.
    clean                 Remove unused packages and caches.
    compare               Compare packages between conda environments.
    config                Modify configuration values in .condarc.
    content-trust         Signing and verification tools for Conda
    create                Create a new conda environment from a list of specified packages.
    deactivate            Deactivate the current active conda environment.
    doctor                Display a health report for your environment.
    export                Export a given environment
    info                  Display information about current conda install.
    init                  Initialize conda for shell interaction.
    install               Install a list of packages into a specified conda environment.
    list                  List installed packages in a conda environment.
    notices               Retrieve latest channel notifications.
    package               Create low-level conda packages. (EXPERIMENTAL)
    remove (uninstall)    Remove a list of packages from a specified conda environment.
    rename                Rename an existing environment.
    repoquery             Advanced search for repodata.
    run                   Run an executable in a conda environment.
    search                Search for packages and display associated information using the MatchSpec format.
    update (upgrade)      Update conda packages to the latest compatible version.


## Environments

### Creating an Environment
```bash
conda create --name myenv
# Specify Python version
conda create --name myenv python=3.8
# Specify packages
conda create --name myenv numpy pandas
```

### Activating an Environment
```bash
conda activate myenv
```

### Deactivating an Environment
```bash
conda deactivate
```

### Listing Environments
```bash
conda env list
# or
conda info --envs
```

### Removing an Environment
```bash
conda remove --name myenv --all
```

### Exporting an Environment
```bash
conda env export --name myenv > environment.yml
```

### Creating an Environment from a File
```bash
conda env create --file environment.yml
```


## Informations

### Conda or Python Version
```powershell
conda --version
python --version
conda list -n myenv
```

### Add Conda to PowerShell
```powershell
# Ouvrir le fichier de profil PowerShell
notepad $PROFILE
```
```powershell
# >>> conda initialize >>>
# !! Contents within this block are managed by 'conda init' !!
(& "C:\Miniconda3\condabin\conda.bat" "shell.powershell" "hook") | Out-String | Invoke-Expression
# <<< conda initialize <<<
```
