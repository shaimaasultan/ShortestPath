<!-- Project Banner -->
<p align="center">
  <img src="Recordings/Copilot_20260601_224526.png" alt="Pixel Path Solver Banner" height="200" width="100%">
</p>

<!-- Project Icon -->
<p align="center">
  
</p>

<img src="Recordings/Copilot_20260601_224528.png" alt="Pixel Path Solver Icon" width="128">

# Pixel Path Solver

# Road Network Viewer + Pixel-Based Path Solver

This project provides a set of interactive HTML tools for loading road data,
visualizing rasterized road networks, selecting start/target nodes, and running
pixel-based pathfinding algorithms. The system supports magnetic snapping,
directional analysis, traversal visualization, and multi-step debugging.

---

## 📁 Project Structure

html/
├── index.html
├── drawRoads_magnatic_click.html
└── drawRoads_traversal_magnatic_click.html

data/
└── roads.geojson (or any user-provided file)
|__ Screenshots road images 

roads.pdf (new shortest path algorithims)

---

## 🚀 Features

### ✔ Pixel-based pathfinding  
- BFS (4-direction, 8-direction, 16-direction)  
- Magnetic snapping to nearest road pixel  
- Start/target selection by clicking  
- Direction totals (N/E/S/W)  
- Compass rose visualization  
- Turn counting, distance, complexity scoring  

### ✔ Road network visualization  
- Load GeoJSON road files  
- Draw roads as blue polylines  
- Highlight computed path in yellow  
- Show start (green) and target (red) markers  

### ✔ Traversal debugging  
- Step-by-step traversal animation  
- Pixel visitation order  
- Magnetic snapping visualization  

---

# 📄 HTML Tools

Below are the three main HTML interfaces included in this repository.

---

## 1️⃣ `./html/index.html`  
### **Load road data + click to set start/target + compute path**

This is the **main interface** of the project.

#### **Features**
- Load a road network from `data/roads.geojson`
- Convert the road network into a pixel grid
- Click to set:
  - **Start point** (green)
  - **Target point** (red)
- Run pixel-based BFS to compute the shortest path
- Display:
  - Steps  
  - Distance (meters)  
  - Turns  
  - Time estimate  
  - Path complexity  
  - Direction totals  
  - Compass rose visualization  

#### **Usage**
1. Open `index.html` in a browser  
2. Click **Choose File** → select your GeoJSON  
3. Click on the map to set **start**  
4. Click again to set **target**  
5. The solver runs automatically  

---

## 2️⃣ `./html/drawRoads_magnatic_click.html`  
### **Load GeoJSON + magnetic snapping + click to add start/target**

This tool focuses on **road visualization + snapping**.

#### **Features**
- Load any GeoJSON road file  
- Draw all roads in blue  
- Magnetic snapping:
  - When clicking near a road, the click snaps to the nearest road pixel  
- Add start/target nodes  
- Visualize snapped points  

#### **Usage**
1. Open the file  
2. Load your GeoJSON  
3. Click anywhere near a road  
4. The system snaps your click to the nearest valid road pixel  

This is ideal for debugging snapping accuracy.

---

## 3️⃣ `./html/drawRoads_traversal_magnatic_click.html`  
### **Show traversal order + magnetic snapping + path animation**

This tool is for **debugging traversal and BFS behavior**.

#### **Features**
- Load GeoJSON  
- Magnetic snapping  
- Visualize BFS traversal:
  - Pixel visitation order  
  - Frontier expansion  
  - Animated path reconstruction  
- Show the final path in yellow  

#### **Usage**
1. Open the file  
2. Load your GeoJSON  
3. Click to set start and target  
4. Watch the traversal animation  

This is ideal for understanding how the BFS explores the grid.

---

# 🧠 Algorithms Included

The project implements:

- Pixel-based maze solver  
- Longest-white-path solver  
- 16-direction BFS solver  
- Grid-based neighbor solver  
- Image-based traversal solver  
- Left/right/up/down directional solver  

Each algorithm is documented in the LaTeX document included in this repo.

---

# 📦 Requirements

No external libraries required.  
Everything runs in the browser using:

- HTML5 Canvas  
- JavaScript  
- GeoJSON parsing  

---

# ▶️ Running the Tools

Simply open the HTML files in any modern browser:

- Chrome  
- Firefox  
- Edge  

No server required.

---

# 📝 License

MIT License — free to use, modify, and distribute.

---

# 🙋‍♀️ Author

**Shaimaa Said Soltan**  
Pixel-based routing, GIS visualization, and algorithm design.

