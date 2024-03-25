# My Web Scraping Adventure with Python and AI

## From Data Gathering to Insightful Automation

### Journey Overview
This adventure started as a curious dive into using Python and the wonders of artificial intelligence for web scraping. It turned into a comprehensive exploration of how data, once collected, can be transformed into actionable insights, and how tasks, no matter how intricate, can be automated with precision. It's been a real journey of growth, from initial curiosity to developing a meaningful project.

### What I Learned
- Advanced Data Extraction: Starting with basics, I gradually mastered scraping techniques for dynamic websites using Selenium and BeautifulSoup, achieving detailed data retrieval.
- AI-Enhanced Analysis: Incorporating Large Language Models allowed me to see data in a new light, transforming raw figures into insightful analyses.
- Workflow Optimization: I learned the value of automating repetitive tasks, making more room for creative problem solving and innovation.
- Full Spectrum Data Analysis: Taking charge from data collection to analysis taught me how to convert extensive datasets into usable intelligence.
- Exploration of AI Tools: The project gave me the chance to play with the latest Large Language Models, like Ollama and LLama 2, expanding my understanding of what's possible in tech.

### How To Follow This Journey
Whether you're dipping your toes into the world of web scraping and AI or looking to understand my process, here's how you can walk this path.

### Essentials
- Python 3.10+
- A Proxy Server (for those tricky web scraping tasks)
- ffmpeg (essential for working with audio via OpenAI Whisper)

### A Proxy-based Web Scraping approach
Using a proxy service makes our requests more reliable. You can see the actual code for the Selenium-based remote connection here `src/helpers/brightdata.py`.

### A comparative look at how requests flow with and without a proxy
**With Remote Proxy:** 

`our computer` -> `request` -> `proxy` -> `web server` -> `proxy` -> `response` -> `our computer`

**Without Remote Proxy:**

`our computer` -> `request` -> `web server` -> `response` -> `our computer`

### Usage
```python
# from 'src/2 - Connection Sample.ipynb'
from selenium.webdriver import Remote, ChromeOptions

# import this function
from helpers.brightdata import get_sbr_connection

options = ChromeOptions()

# options.headless = True # old method
options.add_argument("--headless=new") # new method

url = 'https://news.ycombinator.com'

with Remote(sbr_connection, options=options) as driver:
    driver.get(url)
    print(driver.page_source)
```

#### Getting Started
1. **Clone the Project Repository**:
   ```
   mkdir -p ~/dev/smarter-scraping
   cd ~/dev/smarter-scraping
   git clone https://github.com/acamara19/smarter-web-scrapping-python-AI .
   ```

2. **Set Up the Python Environment**:
   - Create a virtual environment:
     ```bash
     # MAC/LINUX
     python3 -m venv venv
     ```
   - Activate the virtual environment:
     ```bash
     source venv/bin/activate
     ```
   - Install the required packages:
     ```bash
     (venv) python -m pip install pip --upgrade
     (venv) python -m pip install -r requirements.txt
     ```

3. **Configure Environment Variables**:
   Rename the `sample-env-file` to `.env` for sensitive information such as Proxy API keys for Bright Data and Ollama configurations. Sample configuration commands for different operating systems are provided in the documentation.

4. **Dive into the Notebooks**:
   - Launch Jupyter Notebook to explore interactive coding sessions:
     ```bash
     jupyter-notebook
     ```

### The Practical Side
This isn't just theory. It's about applying what I learned to tackle real-world challenges, using detailed examples and guides to help you make your own discoveries and innovations.

### Inviting Contributions
Your insights and improvements are welcome! There's always room to enhance the scraping algorithms, dive deeper into AI analysis, or streamline the workflows even further.

### Learning Resources
Heartfelt thanks to [Coding for Entrepreneurs](https://www.codingforentrepreneurs.com/) for the [Smarter Web Scraping with Python + AI course](https://www.codingforentrepreneurs.com/courses/smarter-web-scraping-with-python-ai/). It was a treasure trove of knowledge that significantly influenced my journey, providing a solid foundation and inspiring innovation at every step.

### Acknowledgments
Special thanks to [Coding for Entrepreneurs](https://www.codingforentrepreneurs.com/) for lighting the way on this incredible learning path.
---
