# 🌍 Global Earthquake Visualization

This project visualizes recent global earthquake data using interactive maps generated with Plotly in Python. The data is sourced from the USGS (United States Geological Survey) API in JSON format.

## 🧪 How It Works

1. **Load JSON Data**  
   Raw earthquake data is loaded from USGS `.json` files located in the `data/` folder.

2. **Extract Relevant Information**  
   For each earthquake, the script extracts:
   - Magnitude (`mag`)
   - Longitude (`lon`)
   - Latitude (`lat`)
   - Title/Description (only in the 30-day data)

3. **Plotting with Plotly**  
   Using Plotly's `Scattergeo`, earthquakes are visualized on an interactive world map:
   - The size of each marker corresponds to the earthquake's magnitude.
   - The 30-day map includes hover text and a color scale to indicate severity.

4. **Export to HTML**  
   The interactive maps are saved as `.html` files and can be opened in any browser.

## 🛠 Technologies Used

- **Python 3**
- **Jupyter Notebook**
- **Plotly** – For interactive visualizations
- **JSON** – For reading and parsing earthquake data files

## 🔍 Sample Output

- **`global_earthquakes.html`**: Shows global earthquakes from the past day with marker sizes based on magnitude.
- **`global_earthquakes_30day.html`**: Shows global earthquakes from the past 30 days with color-coded markers and hover text showing details.

## 🚀 How to Run

1. **Clone the repository:**

   ```bash
   git clone https://github.com/sanajjadhav15/Global-Earthquake-Visualization.git

3. **Install required library:**

   This project only uses Plotly (apart from Python standard libraries), so install it using pip:

   ```bash
   pip install plotly

4. **Run the notebooks:**

   - Open a terminal (or use Anaconda Navigator).
   - Start Jupyter Notebook
   - Open the following notebooks in your browser:
     - `eq_explore_data.ipynb` – For visualizing 1-day earthquake data
     - `eq_world_map.ipynb` – For visualizing 30-day earthquake data
   - Run all the cells in each notebook to process the data and generate the interactive maps.

5. **View the interactive maps:**

   - After running the notebooks, two HTML files will be created:
     - `global_earthquakes.html`
     - `global_earthquakes_30day.html`
   - Open these files in your web browser to explore the earthquake visualizations. The maps are fully interactive, allowing you to zoom, pan, and hover over data points for more information.

## 📝 Notes

- The data files were downloaded manually from the USGS earthquake feeds and stored locally in the `data/` folder.
- `readable_eq_data.json` and `readable2_eq_data.json` are formatted versions of the raw JSON files for easier inspection.
- Marker size on the maps is scaled using the earthquake magnitude (`mag`), and color scaling is applied only in the 30-day map.
- Plotly generates standalone HTML files, which can be shared without requiring any Python environment to view them.
- You can update the JSON files anytime by re-downloading the latest data from [USGS feeds](https://earthquake.usgs.gov/earthquakes/feed/).

## 🙌 Credits

- This project is inspired by the **Data Visualization** chapter in the book *Python Crash Course* by **Eric Matthes**.
- Earthquake data is provided by the **United States Geological Survey (USGS)**.
- Interactive map visualizations are created using **Plotly**.
