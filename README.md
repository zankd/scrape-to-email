# RSS News Workflow for n8n
This repository contains an automated RSS feed aggregator workflow built with n8n , designed to collect, process, and deliver news from multiple sources in the fishing industry.

## Features
- Aggregates news from 15+ fishing industry sources
- Processes and deduplicates news items
- Generates a beautifully formatted HTML email newsletter
- Groups news by source for easy reading
- Includes error handling and retry mechanisms
- Sends daily digests with the latest news
## How It Works
1. Data Collection : The workflow fetches RSS feeds from multiple sources using n8n's RSS nodes
2. Processing : News items are processed to extract titles, links, and content
3. Deduplication : A static data store prevents sending duplicate news items
4. Formatting : News is organized by source and formatted into a responsive HTML email
5. Delivery : The newsletter is sent via email to configured recipients
## Setup Requirements
- n8n instance (self-hosted or cloud)
- SMTP credentials for sending emails
- Basic knowledge of n8n workflows
## Configuration
1. Import the RSS-News-Workflow.json file into your n8n instance
2. Configure the SMTP credentials in the "Send Email" node
3. Update email recipients in the "Send Email" node
4. Adjust the schedule trigger as needed (default: every minute)
5. Activate the workflow
## Customization
- Add or remove RSS sources by duplicating existing RSS nodes
- Modify the email template in the "Process News" node
- Adjust the domain mapping in the processing code to properly categorize sources
## License
This project is available under the MIT License.
