# CNEW 2026 — Tutorial: Visual Event Downscaling with Tonic
**Canadian Neuromorphic Engineering Workshop · University of Waterloo, 16th June 2026**  
*Luca Peres, The University of Manchester*

Following this morning's presentation, in this tutorial we will look at visual event downscaling techniques using Tonic.

The tutorial is available at this link [``Visual Event Donwscaling with Tonic``](https://github.com/lucaperes/CNEW2026_events_downscaling_tutorial). 

Please, clone the repository to get started. This tutorial will run as Jupyter notebook. Below you can find information on how to run it. All the dependencies will be automatically installed.


## Technical Details

This project has its Python packages managed with [``uv``](https://docs.astral.sh/uv/getting-started/) (make sure you have that installed).

The following commands will run the tutorial:

- Add the virtual environment as a kernel for Jupyter:
  - ``uv run ipython kernel install --user --env VIRTUAL_ENV $(pwd)/.venv --name=project``
- Run Jupyter Lab:
  - ``uv run jupyter lab``
- Find the tutorial in [your browser](http://localhost:8888/lab)
