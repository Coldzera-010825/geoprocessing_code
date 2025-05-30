# GeoData Toolkit 🚀

A growing collection of **Python utilities for geospatial data processing, analysis, and visualisation**.  
The goal is to keep each script **self-contained** and **easy to reuse** in day-to-day GIS workflows, whether you are a data scientist, cartographer, or researcher.

---

## ✨ What you can do with this repo

| Category | Capabilities (present & planned) |
|----------|----------------------------------|
| **Data processing** | • Batch convert between vector/raster formats (e.g. `shp → tif`, `shp ↔ kml`) <br>• Coordinate-system transformations <br>• CRUD operations on attribute tables |
| **Data analysis**   | • Spatial joins & overlays <br>• Zonal statistics <br>• Terrain & hydrological analysis (road-mapped) |
| **Visualisation**   | • Quick-look PNG generation for QA <br>• Matplotlib-based thematic maps (planned) |

> **Status:** _active development_ – scripts are added & refined continuously.  
> Pull Requests and feature ideas are welcome!

---

## 📂 Current script list

| Path | Description |
|------|-------------|
| `/kml_ouput` | Create a user-defined **bounding rectangle** (by centre + size / by lat-lon extent) and save it as **KML**.  Optional flags let you export the same rectangle as Shapefile or GeoJSON. |
| `/shp2tif_workflow` | Generic **Shapefile → GeoTIFF** converter – supports geometry repair, size limits, float-32 attribute rasterisation (e.g. `DEPTH2D`). |
| `/trans_CRS` | **Batch re-projection utility**: recursively scans a folder, assigns a CRS if missing, and converts all vector layers to **WGS-84 (EPSG 4326)**. Supports Shapefile / GeoJSON / GPKG; writes a mirrored directory tree under `output_root/`. |
| `/b54_to_wgs84_raster` | **Beijing 54 → WGS-84 raster re-projection**: ingests a GeoTIFF in Beijing 1954, reads a **54_to_84.csv** table of ground-control points, attaches GCPs, and warps the image to EPSG 4326 via GDAL (TPS / polynomial). Outputs a GeoTIFF and prints size & CRS diagnostics. |

Planned additions (📅 Q3 2025):

* `scripts/clip_by_polygon` – vector & raster clipping
* `notebooks/analysis_templates/` – ready-to-run Jupyter notebooks for common analyses

---

## 🔧 Quick start

```bash
# 1. clone
git clone https://github.com/<your-user>/geoprocessing_code.git
cd geoprocessing_code

# 2. create environment (conda recommended)
conda env create -f environment.yml
conda activate geodata

# 3. launch JupyterLab / Notebook
jupyter lab   # or  jupyter notebook

# 4. open a notebook and run all cells
#    e.g. notebooks/make_rectangle_kml.ipynb

