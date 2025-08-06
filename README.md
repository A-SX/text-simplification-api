# Text Simplification API (v3.0)

## 🚀 Overview

The **Text Simplification API** is a powerful, AI-driven solution designed to transform complex, dense, or jargon-filled text into clear, concise, and easily understandable content. Leveraging the advanced capabilities of **Google Gemini 2.5 Flash**, this API is ideal for enhancing accessibility, improving user experience, and streamlining communication across various domains.

Whether you need to simplify legal documents for general audiences, make academic papers digestible for students, or clarify technical manuals for non-experts, our API provides precise and context-aware simplification across multiple reading levels and languages.

## ✨ Key Features

*   **Advanced AI Simplification:** Powered by Google Gemini 2.5 Flash, ensuring high-quality, nuanced, and contextually relevant simplification.
*   **Multilingual Output Support:** Simplify text and receive output in over 70 languages, including the ability to simplify in the original input language (e.g., Arabic to simplified Arabic).
*   **Automatic Language Detection:** Intelligently identifies the language of your input text, making it seamless to use with diverse content.
*   **Multiple Reading Levels:** Choose from `simple`, `intermediate`, and `advanced` simplification to tailor the output to your target audience.
*   **Long Text Processing:** Capable of handling substantial text inputs, suitable for documents, articles, and reports.
*   **Robust & Reliable:** Built with a resilient architecture and fallback mechanisms for consistent performance.
*   **Cost-Effective:** Designed for efficiency, offering powerful simplification at competitive rates.

## 💡 Use Cases

*   **Education:** Adapt textbooks, research papers, and learning materials for students of all ages and reading proficiencies.
*   **Accessibility:** Make web content, legal documents, and medical information accessible to individuals with cognitive disabilities or limited literacy.
*   **Content Creation:** Quickly rephrase complex ideas for blog posts, marketing materials, or social media updates.
*   **Customer Service:** Simplify FAQs, product descriptions, and support articles for clearer customer communication.
*   **Translation & Localization:** Enhance cross-language communication by simplifying content before or after translation.

## 🛠️ Getting Started

### Accessing the API

To use the Text Simplification API, you need to subscribe to it on the [RapidAPI Marketplace](https://rapidapi.com/A-SX/api/text-simplification-api). RapidAPI handles all authentication and access to the API.

### Authentication

This API uses an `X-RapidAPI-Key` for authentication. You will obtain this key upon subscribing to the API on RapidAPI Marketplace.

### Endpoints

*   **`GET /api/health`**: Check the API\`s operational status and capabilities.
*   **`POST /api/simplify`**: The main endpoint for text simplification.

For detailed request/response schemas and examples, please refer to the [API Documentation](API_DOCUMENTATION.md) on RapidAPI.

### Quick Example (Python)

```python
import requests

# The API URL provided by RapidAPI after subscription
api_url = "https://text-simplification-api.p.rapidapi.com/api/simplify"

headers = {
    "Content-Type": "application/json",
    "X-RapidAPI-Key": "YOUR_RAPIDAPI_KEY", # Replace with your actual RapidAPI Key
    "X-RapidAPI-Host": "text-simplification-api.p.rapidapi.com" # Replace with your RapidAPI Host
}

payload = {
    "text": "The intricate interplay between syntactic parsing algorithms and semantic vector embeddings necessitates a reevaluation of traditional natural language understanding frameworks.",
    "target_reading_level": "simple",
    "output_language": "en" # Use "same" for original language, or a 2-letter ISO code (e.g., "ar", "es")
}

response = requests.post(api_url, headers=headers, json=payload)

if response.status_code == 200:
    simplified_data = response.json()
    print("Simplified Text:", simplified_data["simplified_text"])
    print("Input Language:", simplified_data["input_language"])
    print("Output Language:", simplified_data["output_language"])
else:
    print(f"Error: {response.status_code} - {response.text}")

```

## 💰 Pricing

Our flexible pricing plans are designed to accommodate a wide range of usage needs, from individual developers to large enterprises. We offer a generous free tier to get you started, with scalable paid plans for higher volumes.

For detailed pricing information, please see our [Pricing Guide](PRICING.md).

## 🌐 Supported Languages

The API supports simplification and output in over 70 languages. Some of the most commonly used languages include:

*   English (en)
*   Arabic (ar)
*   Spanish (es)
*   French (fr)
*   German (de)
*   Italian (it)
*   Portuguese (pt)
*   Russian (ru)
*   Japanese (ja)
*   Korean (ko)
*   Chinese (zh)
*   Hindi (hi)
*   ...and many more!

## ❓ Support & Feedback

If you have any questions, need assistance, or would like to provide feedback, please reach out through the RapidAPI support channels.

## 📄 License

This API is provided under the [MIT License](https://github.com/A-SX/text-simplification-api/blob/main/LICENSE.md).
