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
| `scripts/export_kml.py` | Export any GeoJSON / Shapefile / GeoPackage layer to **KML** (keeps attributes & CRS). |
| `scripts/shp_to_tif.py` | Generic **Shapefile → GeoTIFF** converter – supports geometry repair, size limits, float-32 attribute rasterisation (e.g. `DEPTH2D`). |

Planned additions (📅 Q3 2025):

* `scripts/coordinate_transformer.py` – batch re-project layers to target EPSG
* `scripts/clip_by_polygon.py` – vector & raster clipping
* `notebooks/analysis_templates/` – ready-to-run Jupyter notebooks for common analyses

---

## 🔧 Quick start

```bash
# 1. clone
git clone https://github.com/<your-user>/geodata-toolkit.git
cd geodata-toolkit

# 2. create environment (conda recommended)
conda env create -f environment.yml
conda activate geodata

# 3. run a script
python scripts/shp_to_tif.py --input data/shp_root --output data/tif_out

