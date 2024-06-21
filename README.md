# Connect3 Radar Chart Generator

This project is a Node.js application that generates radar charts and badge minting visualizations based on social data metrics and roles. It utilizes Chart.js for radar chart rendering and Canvas API for image manipulation.

## Features

- **Radar Chart Generation**: Generate radar charts depicting social metrics such as posts, followers, comments, likes, and NFTs.
- **Badge Minter Visualization**: Create visual representations of badges based on specified roles (e.g., creator, curator, influencer, reviewer).
- **HTML and Image API**: Supports endpoints for retrieving charts and minting visuals in both HTML and image formats.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/connect3world/connect3-radar-score.git
   cd connect3-radar-score
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Run the server:
   ```bash
   npm start
   ```

## Usage

### Endpoints

- `/image`: Generates a radar chart as an image based on provided social data metrics.
    - Parameters:
        - `data`: Comma-separated list of integers representing metrics.
        - `score`: Overall score to display on the chart.
        - `labels`: Comma-separated list of labels for each metric.
        - `role`: Comma-separated list of roles for badge display.
        - `title`: Title for the chart.
    - Returns: JSON with image data URL.

- `/imageMinted`: Generates a badge minter visualization based on specified roles.
    - Parameters:
        - `role`: Comma-separated list of roles to mint badges for.
    - Returns: JSON with image data URL.

- `/html`: Generates an HTML page with embedded radar chart based on provided social data metrics.
    - Parameters: Same as `/image`.
    - Returns: HTML page with embedded chart.

- `/htmlMinted`: Generates an HTML page with embedded badge minter visualization based on specified roles.
    - Parameters: Same as `/imageMinted`.
    - Returns: HTML page with embedded badges.

## Acknowledgments

- Built using Node.js, Canvas, and Chart.js libraries.
- Inspired by the need to visualize social media data and generate badge minting canvases for Connect3.