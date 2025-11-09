# Task B – Micro Scraper

## Objective  
A lightweight scraper endpoint that extracts webpage information (title, meta description, and h1) and handles timeouts, invalid URLs, and network issues gracefully.  

---

## Endpoint Details  

### **GET /api/scrape?url=...**

**Example Request**  

GET http://localhost:3000/api/scrape?url=https://example.com


**Successful Response (200):**

```json
{
  "title": "Example Domain",
  "metaDescription": "This domain is for use in illustrative examples in documents.",
  "h1": "Example Domain",
  "status": 200
}
