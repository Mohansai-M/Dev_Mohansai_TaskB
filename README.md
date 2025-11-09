# Task B – Micro Scraper

This is a scraper API that extracts a webpage's title, meta description, and H1 tags . It handles timeouts, invalid URLs, and network errors safely, with user agent override and retry support. The endpoint is ready to use via Postman or any API client

## Objective
Build a lightweight scraper endpoint that extracts webpage information, including the page title, meta description, and the first H1 tag. The endpoint should handle common issues like timeouts, invalid URLs, and network errors gracefully.

---
[Demo - Loom](https://www.loom.com/share/ae160c28ee2a41de898f5028d93f53be)
## Endpoint Details

### GET `/api/scrape?url=...`

**Example Request:**

GET http://localhost:3000/api/scrape?url=https://example.com


**Successful Response (Status 200):**

```json
{
  "title": "Example Domain",
  "metaDescription": "This domain is for use in illustrative examples in documents.",
  "h1": "Example Domain",
  "status": 200
}
```
**Setup Instructions**

1. Clone the Repository

   ```git clone https://github.com/Mohansai-M/Dev_Mohansai_TaskB.git<br> ```
   ```cd Dev_Mohansai_TaskB ```

2. Install Dependencies

   ```npm install```


3. Run Development Server

   ```npm run dev```


4. Test the API
   Use a browser or Postman to access the endpoint:

   ```http://localhost:3000/api/scrape?url=https://example.com```

**Tech Stack**

- Framework: Next.js API Routes
- Language: JavaScript (Node.js)
- Library: Puppeteer

**Implementation Details**

- Requests have timeout of 20 seconds.
- The page is loaded until ```networkidle2``` to ensure all resources are ready.
- URL validation and error handling are implemented.
- User-Agent override and retry features are included for bonus functionality.

**Testing Checklist**

- A valid URL returns the title, meta description, and first H1 tag.
- Invalid or missing URLs return a 400 error.
- Requests that take longer than 20 seconds return a 504 timeout error.
- The browser instance closes safely in all situations.

  

