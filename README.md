Backend - Event Scraper API 🛠️
Features
✅ Scrapes event details (title, date, location, description).
✅ Stores data in a database (PostgreSQL/MySQL/MongoDB).
✅ Provides RESTful API for event access.
✅ Uses schedule for automated scraping.

Tech Stack
Python (FastAPI/Flask/Django)
BeautifulSoup/Scrapy/Selenium (for scraping)
PostgreSQL/MongoDB (for storage)
Celery + Redis (for background tasks)


Setup Instructions

1️⃣ Clone the Repository
git clone https://github.com/yourusername/event-scraper-backend.git
cd event-scraper-backend

2️⃣ Create a Virtual Environment
python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate

3️⃣ Install Dependencies
pip install -r requirements.txt

4️⃣ Set Up Environment Variables
Create a .env file and configure database details:
DATABASE_URL=postgresql://user:password@localhost:5432/eventsdb
SCRAPING_INTERVAL=24  # Run scraper every 24 hours

5️⃣ Run the Scraper Manually
python scraper.py

6️⃣ Start the API Server
uvicorn main:app --reload  # For FastAPI
# or
python manage.py runserver  # For Django

7️⃣ API Endpoints
GET /events → Fetch all events
GET /events/{id} → Get event details
GET /search?q=keyword → Search events
