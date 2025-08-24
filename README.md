#  OutreachAI

**OutreachAI** is an AI-powered lead generation tool that combines live business data from Google Maps with intelligent enrichment to deliver verified, context-rich leads in minutes.  

Unlike traditional outreach platforms that come with complex setups and high costs, OutreachAI is lightweight, fast, and accessible.

---

## **Key Features**

- **Google Maps Data**  
  Pulls live business listings from Google Maps via the Serper API.  

- **Automated Website Scraping**  
  Extracts company details, emails, and social media links directly from websites.  

- **AI-Powered Enrichment**  
  Uses **LLaMA 3 (via Groq)** to generate structured insights including:  
  - Business description  
  - Unique selling points (USPs)  
  - Target audience profiles  

- **CSV Export**  
  One-click export of enriched leads into a ready-to-use CSV file.  

- **Fast & Lightweight**  
  Generates 20 leads in under 2 minutes with a **15% higher enrichment rate** compared to raw Google Maps data.  

---

## **Tech Stack**

- **Frontend:** Streamlit  
- **Backend:** FastAPI  
- **AI Model:** LLaMA 3 via Groq (LangChain integration)  
- **Data Source:** Google Maps via Serper API  
- **Storage/Export:** CSV (Pandas)  

---

## **Workflow**

1. **User Input**  
   Enter business type, location, and lead count in the Streamlit interface.  

2. **Lead Generation**  
   Fetch business data using Serper API (Google Maps).  

3. **Website Scraping**  
   Collect raw text, emails, and social links from business websites.  

4. **AI Enrichment**  
   LLaMA 3 model refines and structures insights into descriptions, USPs, and audience profiles.  

5. **Export**  
   Save enriched data to a CSV file and download directly from the app.  

---

## **Contributors**

- Mujtaba Junaid


---

## **Getting Started**

### **1. Clone the Repository**
```bash
git clone https://github.com/your-username/outreachai.git
cd outreachai
### **2. SetUp **
# Create virtual environment
python -m venv venv
source venv/bin/activate   # Mac/Linux
venv\Scripts\activate      # Windows

# Install dependencies
pip install -r requirements.txt

# Add environment variables in .env file
SERPER_API_KEY=your_serper_api_key
GROQ_API_KEY=your_groq_api_key

# Run backend
uvicorn main:app --reload

# Run frontend
streamlit run app.py

