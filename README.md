# Cardiovascular Biomaterial CFD Simulator - User Manual

## Code
Google Drive Link :- https://drive.google.com/drive/folders/1GCOl1OseVWv-vcIJs74oCQBDtJTKqjdg?usp=drive_link

## Table of Contents
1. [Introduction](#introduction)
2. [Installation](#installation)
3. [Getting Started](#getting-started)
4. [User Interface](#user-interface)
5. [Input Parameters](#input-parameters)
6. [Running Simulations](#running-simulations)
7. [Visualization](#visualization)
8. [Results and Analysis](#results-and-analysis)
9. [Exporting and Reporting](#exporting-and-reporting)
10. [Troubleshooting](#troubleshooting)
11. [FAQ](#faq)
12. [Support](#support)

## Introduction

The Cardiovascular Biomaterial CFD Simulator is a professional-grade application for simulating blood flow around cardiovascular biomaterials using Computational Fluid Dynamics (CFD). This software enables researchers, engineers, and medical professionals to analyze the hemodynamic performance of various cardiovascular devices such as stents, heart valves, and vascular grafts.

### Key Features

- Advanced CFD simulations with optional OpenFOAM integration
- Detailed biomaterial models for stents, heart valves, and vascular grafts
- High-quality 2D and 3D visualization
- GPU acceleration for faster computations
- Comprehensive PDF report generation
- Data export in multiple formats

### System Requirements

- **Operating System**: Windows 10/11, macOS 10.15+, or Linux (Ubuntu 20.04+ recommended)
- **Processor**: Intel Core i5/AMD Ryzen 5 or better
- **Memory**: 8 GB RAM minimum, 16 GB recommended
- **Graphics**: Dedicated GPU recommended for 3D visualization
- **Storage**: 1 GB available space
- **Optional**: CUDA-compatible GPU for acceleration
- **Optional**: OpenFOAM installation for advanced simulations

## Installation

### Standard Installation

1. Download the installer from the provide Google Drive Link.
2. Run the installer and follow the on-screen instructions.

### Advanced Installation Options

#### OpenFOAM Integration (Optional)

To enable OpenFOAM integration for advanced CFD simulations:

1. Install OpenFOAM following the instructions at [openfoam.org](https://openfoam.org/download/).
2. During the CFD Simulator installation, select the "OpenFOAM Integration" option.
3. Provide the path to your OpenFOAM installation when prompted.

#### GPU Acceleration (Optional)

To enable GPU acceleration:

1. Ensure you have a CUDA-compatible NVIDIA GPU or OpenCL-compatible GPU.
2. Install the latest drivers for your GPU.
3. During installation, select the "GPU Acceleration" option.
4. Choose the appropriate acceleration type (CUDA or OpenCL).

## Getting Started

### First Launch

Upon first launch, the application will display the main window with the Input Parameters panel active. The application uses a tab-based interface with three main sections:

1. Input Parameters
2. Visualization
3. Results & Export

### Quick Start Guide

To run your first simulation:

1. Select a biomaterial type (Stent, Heart Valve, or Vascular Graft).
2. Configure the parameters for your selected biomaterial.
3. Set blood properties and simulation settings.
4. Click "Run Simulation" to start the CFD analysis.
5. Once complete, switch to the Visualization tab to view the results.
6. Export your results or generate a report from the Results & Export tab.

## User Interface

The application features a modern, intuitive interface divided into three main panels:

### Main Window

The main window contains:
- Menu bar with File, Simulation, Export, View, and Help options
- Tab widget for navigating between different panels
- Status bar showing application status and messages

### Input Panel

The Input Panel is where you configure simulation parameters:
- Blood properties section
- Biomaterial selection and configuration
- Simulation settings
- Run button and progress indicator

### Visualization Panel

The Visualization Panel displays simulation results graphically:
- 2D visualization tab with contour plots
- 3D visualization tab with interactive 3D view
- Controls for adjusting visualization parameters

### Results Panel

The Results Panel shows numerical results and provides export options:
- Key results in tabular format
- Biomaterial-specific metrics
- Export options (PDF)
- Comparison with previous results

## Input Parameters

### Blood Properties

- **Velocity**: Blood flow velocity in m/s (typical range: 0.1-1.5 m/s)
- **Viscosity**: Blood viscosity in Pa·s (typical value: 0.0035 Pa·s)
- **Density**: Blood density in kg/m³ (typical value: 1060 kg/m³)
- **Hematocrit**: Percentage of red blood cells in blood (typical range: 35-50%)
- **Non-Newtonian Model**: Optional advanced blood model (Casson, Power Law, or Carreau-Yasuda)

### Biomaterial Parameters

#### Stent Parameters

- **Stent Type**: Bare Metal, Drug Eluting, or Bioresorbable
- **Diameter**: Stent diameter in mm (typical range: 2.5-5.0 mm)
- **Length**: Stent length in mm (typical range: 8-38 mm)
- **Strut Thickness**: Thickness of stent struts in mm (typical range: 0.05-0.15 mm)
- **Strut Width**: Width of stent struts in mm (typical range: 0.05-0.15 mm)
- **Number of Struts**: Number of struts around the circumference (typical range: 6-12)
- **Drug Coating**: Optional drug coating with selectable drug type

#### Heart Valve Parameters

- **Valve Type**: Mechanical, Bioprosthetic, or Transcatheter
- **Diameter**: Valve diameter in mm (typical range: 19-31 mm)
- **Leaflet Thickness**: Thickness of valve leaflets in mm (typical range: 0.3-0.8 mm)
- **Number of Leaflets**: Number of valve leaflets (typically 2-3)
- **Opening Angle**: Maximum opening angle in degrees (typical range: 60-90 degrees)

#### Vascular Graft Parameters

- **Graft Type**: Synthetic, Biological, or Hybrid
- **Diameter**: Graft diameter in mm (typical range: 4-30 mm)
- **Length**: Graft length in mm (typical range: 40-500 mm)
- **Wall Thickness**: Thickness of graft wall in mm (typical range: 0.2-0.8 mm)
- **Porosity**: Graft porosity in percentage (typical range: 0-90%)

### Simulation Settings

- **Mesh Density**: Resolution of the computational mesh (Low, Medium, High, Very High)
- **Time Steps**: Number of simulation time steps (typical range: 50-500)
- **OpenFOAM**: Option to use OpenFOAM for advanced CFD (requires OpenFOAM installation)
- **Acceleration Type**: Option to use GPU acceleration (None, CUDA, or OpenCL)

## Running Simulations

### Starting a Simulation

To start a simulation:

1. Configure all required parameters in the Input Panel.
2. Click the "Run Simulation" button or press F5.
3. The progress bar will show the simulation progress.
4. Once complete, the application will automatically switch to the Visualization tab.

### Simulation Modes

The simulator offers three simulation modes:

1. **Standard CPU Simulation**: Default mode using CPU computation.
2. **GPU-Accelerated Simulation**: Faster simulation using GPU acceleration (if available).
3. **OpenFOAM Simulation**: Advanced simulation using OpenFOAM (if installed).

### Saving and Loading Parameters

You can save your parameter configurations for future use:

- To save parameters: Click "Save Parameters" or use Ctrl+S.
- To load parameters: Click "Load Parameters" or use Ctrl+O.

Parameter files are saved in JSON format and can be shared with colleagues.

## Visualization

### 2D Visualization

The 2D visualization tab provides contour plots of:

- **Velocity**: Blood flow velocity distribution
- **Pressure**: Pressure distribution
- **Wall Shear Stress**: Distribution of shear stress on the biomaterial and vessel walls

Controls allow you to:
- Select the plot type
- Choose a colormap
- Export the current plot as an image

### 3D Visualization

The 3D visualization tab provides an interactive 3D view of:

- **Velocity**: 3D blood flow velocity field
- **Pressure**: 3D pressure distribution
- **Wall Shear Stress**: 3D wall shear stress distribution

Controls allow you to:
- Select the visualization type
- Choose a colormap
- Adjust opacity
- Rotate, pan, and zoom the 3D view
- Export the current view as an image

## Results and Analysis

### Key Results

The Results Panel displays key numerical results:

- **Reynolds Number**: Dimensionless number characterizing the flow regime
- **Maximum Velocity**: Maximum blood flow velocity in m/s
- **Maximum Pressure**: Maximum pressure in Pa and mmHg
- **Maximum Wall Shear Stress**: Maximum wall shear stress in Pa
- **Computation Time**: Time taken to complete the simulation

### Biomaterial-Specific Results

Additional metrics specific to each biomaterial type:

#### Stent Results

- **Strut Coverage**: Percentage of vessel area covered by struts
- **Flow Disturbance Index**: Measure of flow disturbance caused by the stent
- **Restenosis Risk Index**: Estimated risk of restenosis based on flow patterns

#### Heart Valve Results

- **Effective Orifice Area**: Functional opening area of the valve in cm²
- **Regurgitation Fraction**: Percentage of backward flow during valve closure
- **Energy Loss Coefficient**: Measure of valve efficiency

#### Vascular Graft Results

- **Compliance**: Percentage radial change per 100 mmHg pressure
- **Estimated Tissue Integration Rate**: Predicted rate of tissue integration
- **Anastomotic Flow Pattern Index**: Measure of flow disturbance at anastomoses

### Result Comparison

You can compare current results with previously saved results:

1. Run a simulation and view the results.
2. Click "Load Previous Results for Comparison".
3. Select a previously saved result file.
4. The comparison will show differences in key metrics.

## Exporting and Reporting

### Data Export

The simulator supports exporting results in multiple formats:

- **CSV Export**: Tabular data suitable for spreadsheet applications
- **JSON Export**: Structured data suitable for programmatic analysis
- **Images**: Export visualizations as PNG, JPG, or SVG files

To export data:
1. Go to the Results & Export tab.
2. Select the desired export format.
3. Choose a destination file.
4. Click "Export".

### PDF Report Generation

Generate comprehensive PDF reports of your simulation:

1. Go to the Results & Export tab.
2. Click "Generate PDF Report".
3. Select report options:
   - Report type (Summary, Detailed, Technical, or Clinical)
   - Sections to include
   - Custom title or logo (optional)
4. Choose a destination file.
5. Click "Generate".

The PDF report includes:
- Title page with simulation information
- Executive summary
- Input parameters
- Key results
- Visualizations
- Analysis and conclusions
- References and appendices

## Troubleshooting

### Common Issues

#### Application Won't Start

- Ensure your system meets the minimum requirements.
- Check for conflicting software.
- Try reinstalling the application.

#### Simulation Fails to Complete

- Check that all parameters are within valid ranges.
- Ensure you have sufficient system resources.
- For OpenFOAM simulations, verify your OpenFOAM installation.
- For GPU-accelerated simulations, ensure your GPU drivers are up to date.

#### Visualization Issues

- Ensure your graphics drivers are up to date.
- Try reducing the mesh density for better performance.
- For 3D visualization issues, try switching to 2D visualization.

#### Export Errors

- Ensure you have write permissions to the destination folder.
- Check that no other application is using the destination file.
- Try exporting to a different format.

### Error Messages

| Error Message | Possible Cause | Solution |
|---------------|----------------|----------|
| "Invalid parameter value" | Parameter outside valid range | Check parameter ranges in documentation |
| "OpenFOAM not found" | OpenFOAM not installed or not in path | Install OpenFOAM or check installation |
| "GPU acceleration failed" | GPU not compatible or driver issues | Update GPU drivers or switch to CPU mode |
| "Out of memory" | Simulation too large for available RAM | Reduce mesh density or use a computer with more RAM |
| "File access denied" | Permission issues when saving files | Check file permissions or save to a different location |

## FAQ

### General Questions

**Q: Is this software suitable for clinical decision-making?**  
A: The software is designed for research and educational purposes. Clinical decisions should not be based solely on simulation results without proper validation.

**Q: Can I simulate patient-specific geometries?**  
A: The current version uses parametric models. Patient-specific geometries will be supported in a future release.

**Q: How accurate are the simulations?**  
A: The accuracy depends on the input parameters and mesh density. Validation studies have shown good correlation with experimental data for standard cases.

### Technical Questions

**Q: Which CFD solver is used?**  
A: The software uses a built-in solver for standard simulations and can integrate with OpenFOAM for advanced simulations.

**Q: Does GPU acceleration work with AMD GPUs?**  
A: Yes, AMD GPUs are supported through OpenCL acceleration.

**Q: Can I run batch simulations?**  
A: Batch processing will be available in a future release. Currently, simulations must be run individually.

**Q: How can I validate the simulation results?**  
A: Compare with experimental data or published literature. The software also provides validation metrics in the Results panel.

## Support

### Getting Help

For additional support:

- **Email Support**: Contact vikrantkrd@gmail.com for technical assistance.

### Reporting Bugs

If you encounter a bug:

1. Check if you're using the latest version of the software.
2. Check the FAQ and troubleshooting sections for known issues.
3. Report the bug through our website or email support with:
   - Detailed description of the issue
   - Steps to reproduce the problem
   - Screenshots if applicable
   - Log files (located in the application's log directory)

### Feature Requests

We welcome suggestions for new features:

- Submit feature requests through our email.
- Include a detailed description of the feature and its potential benefits.
