# Environmental Data Documentation Tool

A React-based web application for standardizing metadata documentation across ecological research datasets. Originally developed to streamline data management workflows for environmental monitoring projects at the University of Guelph.

## Overview

This tool was created to address the challenge of maintaining consistent documentation across diverse environmental datasets. It automatically extracts structure from CSV files and guides researchers through creating comprehensive, machine-readable metadata that follows established standards.

## Features

- **Automatic CSV Analysis**: Extracts column headers and detects common environmental data patterns (time-series, spatial data, temperature readings, etc.)
- **Guided Metadata Entry**: Structured forms for documenting dataset properties, collection methods, and variable descriptions
- **Multi-format Export**: Generate metadata in JSON, DataCite XML, or Markdown formats
- **Pattern Detection**: Automatically identifies temporal data, coordinates, and common environmental variables
- **Search & Organization**: Filter and manage multiple datasets with persistent browser storage

## File Structure
```bash
environmental-data-documentation-tool/
├── README.md
├── package.json
├── .gitignore
├── src/
│   ├── App.js
│   ├── App.css
│   ├── index.js
│   ├── index.css
│   └── components/
│       └── EnvironmentalDataDocTool.jsx
└── public/
    └── index.html
```

## Installation

### Prerequisites
- Node.js (v14 or higher)
- npm or yarn package manager

### Setup Instructions

1. Clone the repository:
```bash
git clone https://github.com/yourusername/environmental-data-documentation-tool.git
cd environmental-data-documentation-tool
```

2. Install dependencies:
```bash
npm install
```

3. Start the development server:
```bash
npm start
```

4. Open your browser and navigate to `http://localhost:3000`

## Usage

### Basic Workflow

1. **Upload a Dataset**: Click the "Upload" button and select a CSV file containing environmental data
2. **Review Auto-detected Information**: The tool will extract column names and identify data patterns
3. **Complete Metadata Form**: Fill in the guided form with information about:
   - Dataset title and description
   - Collection location and date range
   - Sampling methods and equipment
   - Variable units and descriptions
   - Data quality indicators
   - Access and licensing information
4. **Export Documentation**: Choose your preferred format (JSON, DataCite XML, or Markdown)

### Supported Data Patterns

The tool automatically detects:
- Timestamps and time-series data
- Geographic coordinates
- Temperature measurements
- Precipitation data
- pH values
- Species/taxonomic information

## Technical Details

### Built With
- React 18
- Tailwind CSS for styling
- Lucide React for icons
- Browser LocalStorage for data persistence

### Data Standards Supported
- DataCite Metadata Schema 4.4
- JSON-LD structured data
- Markdown documentation format

## Use Cases

This tool is particularly useful for:
- Research groups managing multiple environmental monitoring datasets
- Graduate students organizing thesis data
- Labs preparing datasets for repository submission
- Creating consistent documentation for data sharing

## Example Output

### JSON Format
```json
{
  "title": "Lake Water Quality Monitoring 2024",
  "description": "Weekly water quality measurements from five sampling sites",
  "location": "Guelph Lake, Ontario",
  "variables": [
    {
      "name": "water_temp",
      "unit": "°C",
      "description": "Surface water temperature"
    }
  ]
}
```

### DataCite XML
The tool generates DataCite-compliant XML suitable for DOI registration and repository submission.

## Future Enhancements

Potential improvements identified during development:
- Support for additional file formats (Excel, NetCDF)
- Integration with institutional repositories
- Batch processing for multiple files
- API endpoints for programmatic access

## Contributing

Contributions are welcome! Please feel free to submit issues or pull requests.

## License

MIT License - See LICENSE file for details

## Acknowledgments

Developed as part of graduate research at the University of Guelph's School of Computer Science, with input from environmental science researchers managing long-term monitoring datasets.
