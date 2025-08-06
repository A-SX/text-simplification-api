# Text Simplification API v3.0 🚀
Transform complex text into clear, accessible language with Google Gemini 2.5 Flash AI.

## 🎯 What This API Does
The Text Simplification API v3.0 uses Google's advanced Gemini 2.5 Flash AI to transform complex, jargon-heavy text into clear, easy-to-understand language. Perfect for:

- **Educational platforms** - Adapt content for different reading levels
- **Accessibility tools** - Make information accessible to everyone
- **Content management** - Create multiple versions of the same content
- **Legal/Medical documents** - Convert professional language to plain English
- **Customer support** - Improve communication clarity
- **Healthcare** - Simplify medical information for patients

## 🚀 Quick Start

### Test the API Right Now
```bash
curl -X POST https://text-simplification-api.p.rapidapi.com/api/simplify \
  -H "Content-Type: application/json" \
  -H "X-RapidAPI-Key: YOUR_RAPIDAPI_KEY" \
  -H "X-RapidAPI-Host: text-simplification-api.p.rapidapi.com" \
  -d '{
    "text": "The proliferation of artificial intelligence technologies necessitates a paradigm shift in the operational frameworks of modern enterprises.",
    "target_reading_level": "simple"
  }'
```

### Response:
```json
{
  "simplified_text": "Smart computers, called AI, are growing very fast.\nBecause of this, companies need to change.\nThey must change how they do things every day.\nThis helps them stay better than other businesses.\nThe world where businesses compete is now very digital.",
  "original_length": 147,
  "simplified_length": 247,
  "target_reading_level": "simple",
  "model_used": "gemini-2.5-flash"
}
```

## 🛠️ Integration Examples

### JavaScript
```javascript
const response = await fetch('https://text-simplification-api.p.rapidapi.com/api/simplify', {
  method: 'POST',
  headers: {
    'Content-Type': 'application/json',
    'X-RapidAPI-Key': 'YOUR_RAPIDAPI_KEY',
    'X-RapidAPI-Host': 'text-simplification-api.p.rapidapi.com'
  },
  body: JSON.stringify({
    text: "Your complex text here",
    target_reading_level: "simple"
  })
});
const result = await response.json();
```

### Python
```python
import requests

response = requests.post('https://text-simplification-api.p.rapidapi.com/api/simplify',
  headers={
    'Content-Type': 'application/json',
    'X-RapidAPI-Key': 'YOUR_RAPIDAPI_KEY',
    'X-RapidAPI-Host': 'text-simplification-api.p.rapidapi.com'
  },
  json={"text": "Your complex text here", "target_reading_level": "simple"}
)
result = response.json()
```

## 📚 Documentation

- Complete API Documentation
- Getting Started Guide
- Monetization Guide

## 🎛️ API Features

### Endpoints

| Endpoint         | Method | Description                         |
|------------------|--------|-------------------------------------|
| /api/health      | GET    | Check API status and capabilities   |
| /api/simplify    | POST   | Simplify text with AI               |

### Reading Levels

- `simple`: For 10-year-olds (max 15 words per sentence)
- `intermediate`: For general adult audience
- `advanced`: For professionals (technical clarity)

### Request Format
```json
{
  "text": "Text to simplify (max 10,000 chars)",
  "target_reading_level": "simple|intermediate|advanced",
  "output_language": "same|en|ar|es|..." 
}
```

### Response Format
```json
{
  "simplified_text": "...",
  "original_length": 147,
  "simplified_length": 247,
  "target_reading_level": "simple",
  "model_used": "gemini-2.5-flash"
}
```

## ✨ What's New in v3.0

- 🤖 Google Gemini 2.5 Flash AI
- 📏 Handles up to 10,000 characters
- 🎯 Enhanced Quality & Accuracy
- 🔧 Better Error Handling
- 📊 Model and Metrics Included
- 🌐 Multilingual Output (70+ Languages)

## 💰 Business Model

| Plan   | Price | Requests/hour | Goal               |
|--------|-------|----------------|--------------------|
| Basic  | $0    | 1,000          | User acquisition   |
| Pro    | $25   | 10,000         | $1,000/month       |
| Ultra  | $75   | 50,000         | $1,125/month       |
| Mega   | $200  | 200,000        | $1,000/month       |

## 🧱 Built With

- Flask (Backend)
- Google Gemini 2.5 Flash (AI)
- CORS enabled
- Secure API Key Management

## 📈 Market Opportunity

- Education, Healthcare, Content Marketing, Developer Tools
- Professional-grade AI for plain language use cases

## 📞 Support

- API Issues → Use /api/health
- Integration → RapidAPI Docs
- Business → Use contact info on RapidAPI

## 📄 License

MIT License
