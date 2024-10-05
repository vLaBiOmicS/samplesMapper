<img src="/map.png" width="200"/>

# samplesMapper

# **samplesMapper Documentation**

## **1. Overview**

**samplesMapper** is an interactive tool designed to visualize geographic data points on a map. Users can input sample information either manually or by uploading a CSV file. The tool allows for customization of sample colors and provides various methods to handle overlapping points on the map. It is primarily used for mapping biological, environmental, or other types of geographic samples.

### **Key Features:**
- Manual sample input (name, latitude, longitude, and color).
- CSV file upload with bulk sample processing.
- Color-coded markers for each sample.
- Multiple methods to handle overlapping points (default, jitter, cluster).
- Responsive map with clustering for better visualization.
- Ability to hide or edit individual samples.

---

## **2. Purpose**

**samplesMapper** was developed to provide researchers, scientists, and other professionals a simple and interactive way to map and visualize sample data. It is ideal for:
- Geospatial data visualization.
- Biological or environmental studies.
- Analyzing sample distribution in a specific geographic area.

Users can manage individual samples, adjust visual elements, and explore geographic relationships between data points.

---

## **3. Functionalities**

### **3.1. Manual Sample Input**

Users can add individual samples manually by entering the following information:
- **Sample Name**: Unique identifier for the sample (e.g., ID, code).
- **Latitude**: Geographic latitude of the sample location (between -90 and 90).
- **Longitude**: Geographic longitude of the sample location (between -180 and 180).
- **Color**: Color selected from a color picker to represent the sample on the map.

Once the information is filled out, clicking the "Add Sample" button will place a marker on the map at the specified location.

### **3.2. CSV File Upload**

The **samplesMapper** allows bulk sample uploads via a CSV file. The CSV should have the following columns:
- **Sample**: Sample name or identifier.
- **Latitude**: Latitude of the sample's location.
- **Longitude**: Longitude of the sample's location.
- **Color** (optional): RGB value or hex code for the sample color. If omitted, a default color will be applied.

Once the file is selected and uploaded, the samples will be processed in batches to ensure performance and displayed on the map.

### **3.3. Overlap Handling Methods**

The tool provides different methods to handle overlapping sample points:
- **Default**: Displays all points as they are, without any adjustment.
- **Jitter**: Slightly shifts overlapping points to reduce overlap.
- **Cluster**: Groups nearby points into clusters, especially useful for larger datasets.

These options can be selected via the dropdown menu at the top of the interface.

### **3.4. Editing and Managing Samples**

Each sample can be:
- **Edited**: By clicking the "Edit" button next to the sample in the table, the form will populate with the current sample details, allowing changes to be made.
- **Deleted**: The "Delete" button allows users to remove samples from both the map and the list.
- **Toggled (Visible/Hidden)**: A checkbox in the sample table lets users control whether the sample is visible on the map.

### **3.5. Interactive Map**

The map provides an interactive environment where users can zoom in and out, and view detailed information about each sample by clicking on the markers. The marker pop-up shows the sample's name, coordinates, and color.

---

## **4. How to Use**

### **4.1. Adding Samples Manually**
1. Navigate to the form under "Manual Sample Input."
2. Enter the sample name, latitude, longitude, and select a color.
3. Click **Add Sample**. A marker will be added to the map, and the sample will appear in the table below.

### **4.2. Uploading a CSV File**
1. Prepare a CSV file with the required columns (Sample, Latitude, Longitude, and optionally Color).
2. Click **Choose File** to select the CSV file from your device.
3. Click **Upload CSV** to start processing the file.
4. The map will display the uploaded samples, with colors and locations corresponding to the CSV data.

### **4.3. Managing Samples**
- To **edit** a sample, click the **Edit** button next to the corresponding entry in the table. The form will populate with the sample’s data, allowing you to modify it.
- To **delete** a sample, click the **Delete** button, which will remove the sample from both the map and the table.
- To **hide** or **show** a sample, use the checkbox in the "Visible" column of the sample table. Unchecking the box will hide the sample from the map, while checking it will display the sample again.

### **4.4. Handling Overlaps**
1. Select the method of handling overlapping points from the dropdown menu at the top.
2. Choose between **Default**, **Jitter**, or **Cluster** to control how points that are close together are displayed on the map.

---

## **5. Technical Details**

### **5.1. Dependencies**
- **Leaflet.js**: Used for rendering the interactive map.
- **PapaParse.js**: Handles the parsing of CSV files.
- **IndexedDB**: Used for storing and managing sample data within the browser.
- **Leaflet MarkerCluster**: Manages marker clustering for improved visualization with large datasets.

### **5.2. Performance Optimizations**
- **Debouncing**: Applied to the latitude and longitude inputs to minimize unnecessary updates while typing.
- **Batch Processing**: CSV uploads are processed in batches to prevent blocking the user interface and ensure smooth handling of large files.
- **IndexedDB**: Samples are stored in the browser's IndexedDB, allowing the tool to manage and update data efficiently without the need for server-side storage.

### **5.3. Responsiveness**
The tool is designed to be fully responsive, meaning it adapts to different screen sizes, including desktops, tablets, and mobile devices. The map and forms resize appropriately to ensure usability across devices.

---

## **6. Future Improvements**

- **Geospatial Analysis**: Add support for more complex geospatial queries and data analysis directly within the tool.
- **Advanced Visualization Options**: Integrate different marker shapes or icons to represent different types of samples.
- **Export Data**: Add functionality to export the map with the marked samples in SVG or PDF format for use in presentations or reports.
- **Data Validation**: Improve input validation to ensure latitude and longitude values are within a valid range and prevent errors from occurring during upload or manual entry.

---

## **7. Conclusion**

**samplesMapper** is a user-friendly and versatile tool for mapping sample data with minimal setup. It allows users to input data manually or upload it in bulk via CSV, with various customization options to ensure clarity in data visualization. This tool is ideal for researchers, scientists, and professionals who need to map and explore geospatial data efficiently.

---

This documentation provides a comprehensive guide to understanding and using **samplesMapper** effectively.
