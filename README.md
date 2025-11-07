# Eloqua Campaign Generator

A powerful web application that generates multilingual email campaign templates using Google's Gemini AI. Perfect for creating professional email content for Eloqua campaigns in multiple languages from any source (URL, text, or file).

## Features

- **Multiple Input Sources**: Generate content from URLs, plain text, or uploaded files
- **Multilingual Support**: Generate email content in 7 languages (English, German, Dutch, French, Polish, Italian, Spanish)
- **AI-Powered Content**: Uses Google Gemini 2.5 Flash for intelligent content generation
- **Campaign Assets**: Generate LinkedIn posts, Twitter posts, image prompts, and audience personas
- **Content Refinement**: Refine email body tone (formal, concise) with AI
- **Subject Line Variations**: Generate A/B testing variations for subject lines
- **Export Options**: Export results as JSON, CSV, or email format
- **Modern UI**: Beautiful, responsive interface built with Tailwind CSS

## Quick Start

### Prerequisites

- A modern web browser
- Google Gemini API key ([Get one here](https://aistudio.google.com/app/apikey))

### Installation

1. Clone this repository or download the files
2. No build process required - this is a static HTML application!

### Configuration

**No manual code editing required!** The application provides a user-friendly interface to configure your API key:

1. Open the application in your browser
2. Click the **"Configure API"** button in the top-right corner
3. Enter your Google Gemini API key
4. Click **"Save Key"**

Your API key is securely stored in your browser's localStorage and persists across sessions. You can update or clear it anytime using the same configuration modal.

### Running the Application

#### Option 1: Using npm (Recommended)

```bash
npm start
```

This will start a local server and automatically open the application in your browser at `http://localhost:8080`.

#### Option 2: Using Python

```bash
# Python 3
python -m http.server 8080

# Python 2
python -m SimpleHTTPServer 8080
```

Then open `http://localhost:8080` in your browser.

#### Option 3: Direct File Opening

Simply open `index.html` directly in your browser. Note that some features may not work due to CORS restrictions when accessing URLs.

### First-Time Setup

When you first open the application:

1. You'll see a **"Configure API"** button in the top-right corner
2. Click it and enter your [Google Gemini API key](https://aistudio.google.com/app/apikey)
3. Click "Save Key" - your key will be stored securely in your browser
4. The button will change to **"API Key Set"** (green) when configured
5. You're ready to generate content!

## Usage

### Step 1: Choose Your Source

Select one of three input methods:
- **URL**: Enter a website URL to scrape content from
- **Text**: Paste article or content directly
- **File**: Upload a text file (.txt, .md)

### Step 2: Select Languages

Click on the language flags to select which languages you want to generate content for. You can select multiple languages.

### Step 3: Generate

Click the "Generate with Gemini" button to start the AI content generation process. The application will:
- Process each language concurrently (max 3 at a time)
- Generate subject lines, preheaders, email body, and CTAs
- Display results in real-time as they complete

### Step 4: Review & Refine

For each generated email:
- **Copy individual elements** using the copy buttons
- **Generate subject variations** for A/B testing
- **Refine body tone** (make it more formal or concise)
- **Generate campaign assets** (social media posts, image prompts, personas)

### Step 5: Export

Export your results in multiple formats:
- **Send by E-mail**: Copy all content formatted for email
- **Export JSON**: Download structured data as JSON
- **Export CSV**: Download as spreadsheet-compatible CSV

## Generated Content Structure

Each email includes:
- **Subject Line**: Compelling, client-focused (max 15 words)
- **Preheader**: Engaging preview text (max 20 words)
- **Email Body**: Professional content (150-200 words) with proper formatting
- **Call-to-Action**: Short, actionable text (max 5 words)
- **Key Insights**: 2-3 relevant business insights

## Campaign Assets

Generate additional marketing materials:
- **LinkedIn Post**: Professional post with formatting
- **X (Twitter) Post**: Concise post under 280 characters
- **Image Prompt**: AI-ready prompt for use with external image generators (DALL-E, Midjourney, etc.)
- **Audience Personas**: 3 target audience descriptions

## API Limits & Costs

This application uses Google's Gemini API which has:
- **Free tier**: Generous rate limits for testing
- **Paid tier**: Available for production use

Monitor your API usage at the [Google Cloud Console](https://console.cloud.google.com/).

## Project Structure

```
eloqua-automailer/
├── index.html          # Main application (HTML, CSS, JS all-in-one)
├── package.json        # NPM configuration and scripts
├── .env.example        # Example environment variables
├── .gitignore         # Git ignore rules
└── README.md          # This file
```

## Technologies Used

- **Google Gemini 2.5 Flash**: AI content generation
- **Tailwind CSS**: Utility-first CSS framework
- **Lucide Icons**: Beautiful icon library
- **Vanilla JavaScript**: No framework dependencies

## Security Notes

⚠️ **Important**: This application stores the API key in your browser's localStorage, which is accessible to client-side JavaScript. This is suitable for personal/development use, but for production deployments you should:

1. Move API calls to a backend server
2. Store API keys securely in environment variables on the server
3. Implement proper authentication and rate limiting
4. Never commit API keys to version control

**Current Security Features:**
- API key stored locally in browser (not in code)
- Key persists across sessions via localStorage
- Easy to update or clear through UI
- Password-masked input field

## Browser Compatibility

Works best in modern browsers:
- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+

## Troubleshooting

### API Key Issues
- Click "Configure API" button and ensure your key is saved
- Verify your API key is active at [Google AI Studio](https://aistudio.google.com/)
- Try clearing and re-entering your API key if you get authentication errors
- Check browser console for specific API error messages

### CORS Errors
- Use a local server (npm start) instead of opening the file directly
- Some URLs may block scraping due to CORS policies

### Content Not Generating
- Check browser console for errors (F12 → Console)
- Verify API rate limits haven't been exceeded
- Ensure you have an active internet connection

## Contributing

Contributions are welcome! Please feel free to submit issues or pull requests.

## License

ISC License - See package.json for details.

## Support

For issues or questions:
1. Check the troubleshooting section
2. Review browser console for error messages
3. Verify API key configuration
4. Check Google Gemini API status

---

**Built with ❤️ using Google Gemini AI**
