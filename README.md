# Palliative Care Legislative Tracker

A web application that tracks state legislation on palliative care and serious illness policy across the United States. This interactive dashboard provides visualizations, filtering capabilities, and detailed bill information sourced from Yale's palliative care policy database.

## Features

- **Interactive US Map**: Visual representation of legislative activity by state
- **Statistical Dashboard**: Key metrics including total bills, enacted legislation, and success rates
- **Advanced Filtering**: Filter by region, state, disposition, category, and text search
- **Data Visualizations**: Charts showing bills by region, outcomes, top states, and categories
- **Detailed Bill Table**: Comprehensive listing of all bills with metadata
- **Real-time Data**: Sources data directly from Yale's live database

## Live Demo

Visit the live application at: `https://[your-github-username].github.io/PC-GPS`

## Setup for GitHub Pages

### Prerequisites

- A GitHub account
- Basic knowledge of Git

### Deployment Steps

1. **Create a new GitHub repository**:
   - Go to GitHub and create a new repository named `PC-GPS` (or any name you prefer)
   - Make it public (required for free GitHub Pages)
   - Initialize with a README if desired

2. **Upload the files**:
   - Clone the repository to your local machine:
     ```bash
     git clone https://github.com/[your-username]/PC-GPS.git
     cd PC-GPS
     ```
   - Copy the `index.html` file to the repository directory
   - Add and commit the files:
     ```bash
     git add index.html
     git commit -m "Add palliative care legislative tracker"
     git push origin main
     ```

3. **Enable GitHub Pages**:
   - Go to your repository on GitHub
   - Click on "Settings" tab
   - Scroll down to "Pages" in the left sidebar
   - Under "Source", select "Deploy from a branch"
   - Select "main" branch and "/ (root)" folder
   - Click "Save"

4. **Access your site**:
   - GitHub will provide a URL like: `https://[your-username].github.io/PC-GPS`
   - The site may take a few minutes to be available initially

### Alternative: Using GitHub's Web Interface

If you prefer not to use Git locally:

1. Create a new repository on GitHub
2. Click "Add file" → "Create new file"
3. Name it `index.html`
4. Copy and paste the HTML content
5. Commit the file
6. Enable GitHub Pages in Settings → Pages

## Data Source

The application fetches data from Yale's Palliative Care Policy Database:
- **URL**: https://live-palliativecare-cms-yale-edu.pantheonsite.io/billtrack_data
- **Format**: CSV with legislative bill information
- **Updates**: The data is maintained by Yale and updates reflect the latest legislative activity

## Technology Stack

- **HTML5/CSS3**: Modern web standards with responsive design
- **Vanilla JavaScript**: No framework dependencies
- **D3.js**: Interactive map visualization
- **Chart.js**: Statistical charts and graphs
- **PapaParse**: CSV data parsing
- **TopoJSON**: US map geographic data

## Browser Support

- Chrome 60+
- Firefox 60+
- Safari 12+
- Edge 79+

## Features in Detail

### Interactive Map
- Color-coded states based on legislative activity
- Hover tooltips showing bill counts
- Click states to filter data

### Filtering System
- **Region**: Filter by US geographic regions
- **State**: Select specific states
- **Disposition**: Filter by bill status (Enacted, Pending, etc.)
- **Category**: Filter by policy categories
- **Search**: Text search in bill titles

### Visualizations
- Bills by region (bar chart)
- Legislative outcomes (doughnut chart)
- Top 10 states by activity (horizontal bar chart)
- Bills by category (bar chart)

### Data Table
- Sortable columns
- First 100 results displayed for performance
- Links to full bill text where available
- Color-coded disposition badges

## Customization

To modify the application:

1. **Styling**: Update the CSS in the `<style>` section
2. **Data Source**: Change the fetch URL in the `loadData()` function
3. **Visualizations**: Modify Chart.js configurations in the `createCharts()` function
4. **Filtering**: Add new filters in the `initializeFilters()` and `applyFilters()` functions

## Troubleshooting

### Common Issues

1. **Data not loading**: 
   - Check browser console for CORS errors
   - Verify the data source URL is accessible
   - Ensure internet connection

2. **Charts not displaying**:
   - Check that Chart.js library loads properly
   - Verify canvas elements exist in HTML

3. **Map not showing**:
   - Confirm D3.js and TopoJSON libraries load
   - Check browser console for JavaScript errors

### Performance Notes

- The table displays only the first 100 results by default
- Large datasets may cause slower filtering operations
- Consider implementing pagination for very large datasets

## Contributing

This is a static site project. To contribute:

1. Fork the repository
2. Make your changes
3. Test locally by opening `index.html` in a browser
4. Submit a pull request

## License

This project displays data from Yale's Palliative Care Policy Database. Please respect their terms of service and give appropriate attribution.

## Contact

For questions about the data source, contact Yale's Palliative Care Policy Database team.
For technical issues with this visualization, create an issue in this GitHub repository.