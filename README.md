# Computer Networks Lab Programs (NS-2)

This repository contains Network Simulator 2 (NS-2) simulation scripts (`.tcl`), AWK trace analysis scripts (`.awk`), and pre-generated trace/animation output files (`.tr`, `.nam`) for Computer Networks lab experiments.

## Repository Structure

* **`lab1.tcl` – `lab5.tcl`**: TCL simulation scripts defining network topologies, traffic agents, link parameters, and error models.
* **`lab1.awk` – `lab5.awk`**: AWK scripts used to parse trace files and compute performance metrics.
* **`lab1.tr` – `lab5.tr`**: Generated event trace files containing packet-level simulation logs.
* **`lab1.nam` – `lab5.nam`**: Network Animator output files.

---

## Running via GitHub Codespaces (Recommended)

Since NS-2 requires a Linux environment and setting it up locally can be difficult for non-Linux users, **GitHub Codespaces** provides an instant, pre-configured cloud development environment directly in your browser. 

*Note: GitHub Codespaces is a headless Linux environment. **There is no built-in graphical user interface (GUI)**, meaning commands like `nam` (Network Animator) will not open a visual window, and tools like `xgraph` are not installed or supported out of the box.*

### Step 1: Open in Codespaces
1. Go to the main page of your repository.
2. Click the green **`<> Code`** button.
3. Select the **Codespaces** tab and click **Create codespace on main** to launch your cloud workspace.

### Step 2: Install NS-2 and AWK
Once your terminal is ready in the browser, run the following commands to install the simulator:
```bash
sudo apt update
sudo apt install -y ns2 nam gawk
```

### Step 3: Execute the Simulation
Run any of the lab `.tcl` scripts using the `ns` command
```bash
ns lab1.tcl
```

This will successfully generate your simulation trace (.tr) and animation (.nam) files in your file explorer.

### Step 4: Analyze Trace Files
Use the provided AWK scripts to process the generated trace data and view performance metrics
```bash
awk -f lab1.awk lab1.tr
```
