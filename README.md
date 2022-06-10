# NHI.gereedschapskist

Dit is repository van de NHI gereedschapskist inventarisatie. Hierin is een
overzicht gemaakt van alle gereedschappen die gemaakt zijn in het kader van het
[Nederlands Hydrologisch Instrumentarium](http://nhi.nu/).

De webpagina's zijn te vinden via de volgende link:
https://helpdesknhi.github.io/NHI.gereedschapskist/

## Werking

Webpagina's worden gebouwd aan de hand van de tabel
`NHI-gereedschapskist_inventarisatie.csv`. Deze wordt met het script
`convert_master_table.py` omgezet tot `.rst` en `.csv` files die vervolgens weer
door [Sphinx](https://www.sphinx-doc.org/en/master/) omgezet worden naar HTML
pagina's.

## Verbeteringen

Wil je een verbetering/aanpassing doorvoeren? 
Dan zijn er twee manieren.

1. Post een issue
2. Voer zelf een verbetering door

Indien je zelf een verbetering wil doorvoeren:
 * [Fork dan de
repository](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/about-forks)
* Doe vervolgens je aanpassing in `scripts/NHI-gereedschapskist_inventarisatie.csv`. 
* Test eerst lokaal of je aanpassing resulteert in het gewenste resultaat. Zie
  uitleg onder om lokaal pagina's te bouwen.
* Maak vervolgens een [Pull 
Request](https://docs.github.com/en/enterprise-server@3.2/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request-from-a-fork)
aan, waarna wij hem kunnen mergen in de hoofd repository.

## Lokaal webpagina bouwen

De webpagina's kunnen als volgt gebouwt worden, om lokaal te testen:

### Installatie

Installeer
[mambaforge](https://github.com/conda-forge/miniforge/releases/latest/download/Mambaforge-Windows-x86_64.exe),
open vervolgens het Windows Start Menu en start *Miniforge Prompt*. 

### Manier 1

```
cd pad/naar/repository
pip install tox
tox -e build
```

De HTML pagina's staan onder `./.tox/docs_out`.


### Manier 2

```
cd pad/naar/repository
mamba create -f environment.yml
cd scripts
make
```

De HTML pagina's staan onder `./docs/_build/docs_out`.
