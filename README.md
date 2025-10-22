# ShareVolume

## Overview
This is an automated web application generated to fulfill the following requirements.

## Requirements
Your assigned company: Booking Holdings (BKNG), CIK 0001075531.

Fetch https://data.sec.gov/api/xbrl/companyconcept/CIK0001075531/dei/EntityCommonStockSharesOutstanding.json (set a descriptive User-Agent per SEC guidance).
Read `.entityName`. Filter `.units.shares[]` for entries whose `fy` > "2020" and
includes a numeric `val`.
Save `data.json` with this structure:
`{"entityName": "Booking Holdings", "max": {"val": ..., "fy": ...}, "min": {"val": ..., "fy": ...}}`
where `max` and `min` refer to the highest and lowest `.val`. Break ties however you like.

Render a visually appealing `index.html` where:
- `<title>` and `<h1>` must include the live `entityName`.
- The max/min figures are clearly marked with these IDs:
  `share-entity-name`,
  `share-max-value`, `share-max-fy`,
  `share-min-value`, `share-min-fy`.

If the page is opened as `index.html?CIK=0001018724` (or any other 10-digit CIK),
`fetch()` from the SEC endpoint for that CIK using any proxy, e.g. AIPipe,
replace every ID listed above and the title and H1 without reloading the page.

Also commit the attachment uid.txt as-is.

## Evaluation Criteria
- Each required file exists on GitHub
- uid.txt matches the attached uid.txt
- LICENSE contains the MIT License text
- data.json exists and is valid JSON
- data.json has 'entityName' field matching 'Booking Holdings'
- data.json has 'max' object with 'val' (number) and 'fy' (string) fields
- data.json has 'min' object with 'val' (number) and 'fy' (string) fields
- data.json max.fy and min.fy are both > '2020'
- data.json max.val is greater than or equal to min.val
- index.html exists
- index.html <title> contains the entityName from data.json
- index.html <h1 id='share-entity-name'> contains the entityName from data.json
- index.html contains element with id='share-max-value' displaying max.val
- index.html contains element with id='share-max-fy' displaying max.fy
- index.html contains element with id='share-min-value' displaying min.val
- index.html contains element with id='share-min-fy' displaying min.fy
- index.html fetches data.json using fetch('https://data.sec.gov/api/xbrl/companyconcept/CIK0001075531/dei/EntityCommonStockSharesOutstanding.json')
- index.html supports ?CIK= query parameter to fetch alternate company data
- index.html dynamically updates all elements when ?CIK= is provided

## Setup
This is a static web application hosted on GitHub Pages. No installation required.

## Usage
1. Visit the live site: [GitHub Pages URL](https://shreyas20063.github.io/ShareVolume/)
2. The application loads automatically
3. Follow on-screen instructions

## Technical Implementation
- **Frontend**: HTML5, CSS3, JavaScript
- **Libraries**: Bootstrap 5, marked.js (if needed), highlight.js (if needed)
- **Hosting**: GitHub Pages
- **Architecture**: Single-page application with inline styles and scripts

## Code Structure
The application is contained in a single `index.html` file with:
- Inline CSS for styling
- Inline JavaScript for functionality
- CDN-hosted external libraries for enhanced features

## License
MIT License - See LICENSE file for details

## Author
Generated automatically via LLM-assisted development

**Source Code:** https://github.com/shreyas20063/llm-deployment-api

**Generated App:** https://github.com/shreyas20063/ShareVolume
