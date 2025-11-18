# TestImagesAndVideos

This repository contains example Jupyter notebooks demonstrating simple image and video transformations. The notebooks are grouped into two folders: `Images/` and `Videos/`.

IMPORTANT: The notebooks are provided as examples. Do NOT edit them in-place unless you intentionally want to modify the examples — this README documents their contents and how to run them.

Repository structure
--------------------

- `Images/`
	- `GeometricTransformations.ipynb` — Example image operations showing geometric transforms such as rotation, scaling, translation, and affine/perspective transforms on sample images.
	- `WeatherTransformations.ipynb` — Example image manipulations that simulate simple weather effects (e.g., rain, fog, brightness changes).

- `Videos/`
	- `GeometricTransformation.ipynb` — Takes a single input image and synthesizes a video by applying continuous geometric transformations across frames (smooth rotation, scaling, translation, etc).
	- `WeatherAndGeometric.ipynb` — Takes a single input image and synthesizes a video by first applying weather transformations (for example: fog, rain overlays) to the image and then applying continuous geometric transformations across the weather-modified frames. The ordering (weather → geometric) ensures the rendered weather effects are transformed consistently over time.

How to open and run
-------------------

1. Install Python.
2. Install Jupyter or JupyterLab and the typical image/video libraries. A minimal list of packages used by the notebooks is shown below.
3. Start JupyterLab or Jupyter Notebook in the repository root and open the notebooks from the `Images/` and `Videos/` folders.

Example (Windows PowerShell):

```powershell

# install minimal packages (adjust names/versions as needed)
pip install jupyterlab notebook numpy matplotlib opencv-python


```

Minimal recommended packages
---------------------------

- jupyterlab or notebook
- numpy
- matplotlib
- opencv-python

Notes and tips
--------------
- The notebooks include code cells that read and display images/video frames. If a notebook expects local sample media files and they are not present, either provide sample media in the same folder or adapt the notebook to point to your files.
- If you want to run the notebooks programmatically, you can convert them to scripts with `jupyter nbconvert --to script`.

References
----------

https://arxiv.org/abs/1907.07484 — this paper has been used for the weather transformations image generation part.
