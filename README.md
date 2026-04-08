> **Note about this fork**
> This is a project I worked on with [@RockRar484](https://github.com/RockRar484).
> I contributed to the JOSAA scraping pipeline using BeautifulSoup and Selenium and 
> the Next.js frontend
> The original repository lives on my collaborator's account because I didn't
> have a GitHub account during development. I forked it here to showcase it
> on my profile.
>
> **Original repo:** https://github.com/RockRar484/GuideU

---

# GuideU

GuideU is a web application designed to explore the JOSAA (Joint Seat Allocation Authority) seat allotment statistics up to 2023. It extracts data from the JOSAA website for the years 2016 to 2022 and 2023, allowing users to gain interesting insights from the data through visualization tools like charts and tables.

## Project Overview

The goal of this project is to create a portal where users can explore and analyze seat allotment statistics from JOSAA. By scraping data from the JOSAA website using Python libraries, cleaning and storing it in a SQLite database, and then visualizing the data on a frontend built with Next.js, users can ask and answer questions such as:
- Which branches are getting more popular?
- What is the flow of students among the IITs over the years?

## Goals
- Web scraping JOSAA data using Python libraries and converting it into a dataframe
- Cleaning the data and performing some Exploratory Data Analysis (EDA)
- Creating a SQLite database from the obtained data and performing queries on it
- Developing a website to display the analysis with various charts (using Chart.js)

## Tech Stack/Frameworks
- **Frontend:** Next.js (React framework), HTML, CSS, JavaScript
- **Backend:** Django, SQLite
- **Data Scraping:** Beautiful Soup, Selenium
- **Data Cleaning:** Numpy, Pandas
- **Visualization:** Chart.js

## Features
- Data scraping from JOSAA website
- Data cleaning and analysis
- Storage of data in a SQLite database
- Interactive charts and tables to visualize data trends

## Installation

### Prerequisites
- Python 3.x
- Node.js
- SQLite
- Django
- TailwindCSS

### Backend Setup
1. Clone the repository:
    ```bash
    git clone https://github.com/RockRar484/GuideU.git
    cd GuideU
    ```

2. Set up a virtual environment and activate it:
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3. Install backend dependencies:
    ```bash
    pip install -r requirements.txt
    ```

5. Run the Django server:
    ```bash
    python manage.py migrate
    python manage.py runserver
    ```

### Frontend Setup
1. Install frontend dependencies:
    ```bash
    cd client-side
    npm install
    ```

2. Run the Next.js development server:
    ```bash
    npm run dev
    ```

### Data Scraping
1. Ensure you have the necessary drivers for Selenium (e.g., ChromeDriver for Chrome).
2. Make a superuser using the admin panel of backend server.
3. The before mentioned step is necessary since the webapp has been developed in a way such that only admin can scrape the data from josaa website. After logging in as the superuser you can access the url "<base url>/api/admin-view/" (by default the base url has been set to http://127.0.0.1:8000). This will scrape the  [JOSAA website(Joint Seat Allocation Authority)](https://josaa.admissions.nic.in/applicant/seatmatrix/openingclosingrankarchieve.aspx) and store the data in sqlite database.

## Usage
1. Access the Django backend at `http://localhost:8000`.
2. Access the Next.js frontend at `http://localhost:3000`.

## Contributing
Contributions are welcome! Please open an issue or submit a pull request for any changes.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgements
- The JOSAA website for providing the data.
- The developers of Beautiful Soup and Selenium for their powerful web scraping libraries.
- The Django and Next.js communities for their extensive documentation and support.

