# NHI.gereedschapskist

## Lokaal webpagina's bouwen

Webpagina's worden gebouwd aan de hand van de tabel
`NHI-gereedschapskist_inventarisatie.csv`. Deze wordt met het script
`convert_master_table.py` omgezet tot `.rst` en `.csv` files die vervolgens weer
door Sphinx omgezet worden naar HTML pagina's.

### Installatie

Installeer
[mambaforge](https://github.com/conda-forge/miniforge/releases/latest/download/Mambaforge-Windows-x86_64.exe),
open vervolgens het Windows Start Menu en start *Miniforge Prompt*. `cd` naar de
repository, en draai vervolgens `mamba create -f environment.yml`

### Bouwen

`cd` naar de `./scripts` folder, en draai daar `make.bat`. De HTML pagina's
staan onder `./docs/_build/docs_out`.