
# LinkedIn Job Scraper

## Overview

This project is a Python-based web scraper that automates the process of collecting job listings from LinkedIn using Selenium. The script is designed to navigate LinkedIn, log in with your credentials, search for "Junior Data Analyst" positions in Germany, and extract various details about the job postings. The extracted data is then stored in a CSV file for easy analysis.

## Features

- **Automated Login:** The script automatically logs into LinkedIn using stored credentials.
- **Cookie Handling:** It handles the cookie pop-up by accepting cookies to proceed with the browsing.
- **Job Search Automation:** The script navigates to the LinkedIn jobs section and searches for "Junior Data Analyst" positions in Germany.
- **Pagination Handling:** It continuously collects job posting links across multiple pages.
- **Data Extraction:** For each job posting, the script extracts:
  - Job Title
  - Company Name
  - Company Location
  - Job Description
  - Work Method (Hybrid, Remote, On-Site)
  - Experience Level
  - Post Date
- **Data Storage:** The extracted data is saved into a CSV file, and the job descriptions are stored in a separate text file.

## Requirements

- Python 3.x
- Selenium
- Chrome WebDriver (compatible with your version of Chrome)
- Pandas

## Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/YeganeHosseini/LinkedIn-Job-Scraper.git
   ```

2. **Install the required packages:**
   ```bash
   pip install selenium pandas
   ```

3. **Download ChromeDriver:**
   - Ensure that ChromeDriver is installed and added to your system PATH.
   - [ChromeDriver Download](https://sites.google.com/chromium.org/driver/)

4. **Set Up Credentials:**
   - Create a `user_credentials.txt` file in the project root directory containing your LinkedIn username and password on two separate lines:
     ```
     your-email@example.com
     yourpassword
     ```

## Usage

1. **Run the Script:**
   - Ensure that the Chrome browser is closed before running the script to avoid any potential conflicts.
   ```bash
   python script_name.py
   ```
   - The script will automatically open a Chrome browser, navigate to LinkedIn, log in, and start scraping job data.

2. **Output:**
   - The job data will be saved into `job_offers.csv`.
   - The detailed job descriptions will be saved in `job_descriptions.txt`.

## Example Output

### job_offers.csv:
| job_title         | company_name | company_location | work_method | post_date    | work_time  |
|-------------------|--------------|------------------|-------------|--------------|------------|
| Junior Data Analyst | ExampleCorp  | Berlin, Germany  | Remote      | 2 days ago   | Full-time  |

### job_descriptions.txt:
```
Job Description for Junior Data Analyst at ExampleCorp:
- Analyze data...
- Work with...
...
```

## Contributing

Contributions are welcome! Feel free to submit a pull request or open an issue for any bug reports or feature requests.

## License

This project is licensed under the MIT License.

