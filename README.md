# Bulk Word Counter

A simple, client-side web application that counts words from multiple web pages simultaneously and exports the results to CSV format.

## 🌟 Features

- **Bulk Processing**: Count words from multiple URLs at once
- **Real-time Progress**: See which URL is currently being processed
- **CSV Export**: Automatically download results as a CSV file
- **Copy to Clipboard**: Easily copy results for pasting elsewhere
- **Error Handling**: Graceful handling of failed URL requests
- **Clean Word Counting**: Excludes scripts, styles, and other non-visible content
- **Modern UI**: Clean, responsive design with loading states

## 🚀 How to Use

1. **Open the Application**: Open `index.html` in any modern web browser
2. **Enter URLs**: Paste one URL per line in the text area
3. **Generate Report**: Click "Generate Word Count CSV" to start processing
4. **View Results**: Results appear in a table showing URL and word count
5. **Export Data**: CSV file automatically downloads with timestamped filename
6. **Copy Results**: Use "Copy to Clipboard" button to copy data as CSV format

## 📊 Example Input

```
https://example.com/blog/post1
https://example.com/blog/post2
https://example.com/about
```

## 📁 Example Output

The application generates a CSV file named `word-count-YYYY-MM-DD.csv`:

```csv
URL,Word Count
https://example.com/blog/post1,542
https://example.com/blog/post2,387
https://example.com/about,156
```

## 🛠️ Technical Details

### How It Works

1. **CORS Proxy**: Uses `api.allorigins.win` to bypass CORS restrictions
2. **HTML Parsing**: Utilizes the browser's DOMParser to extract content
3. **Content Filtering**: Removes non-visible elements (scripts, styles, navigation)
4. **Word Counting**: Splits text on whitespace and filters empty strings
5. **CSV Generation**: Creates downloadable CSV using Blob API

### Technologies Used

- **HTML5**: Structure and semantic markup
- **CSS3**: Modern styling with flexbox and animations
- **Vanilla JavaScript**: No external dependencies
- **Web APIs**: DOM Parser, Fetch API, Clipboard API, Blob API

### Browser Compatibility

- ✅ Chrome 60+
- ✅ Firefox 55+
- ✅ Safari 12+
- ✅ Edge 79+

## 🔧 Installation & Setup

No installation required! This is a simple client-side application.

### Option 1: Direct Use
1. Download or clone this repository
2. Open `index.html` in your web browser
3. Start counting words!

### Option 2: Local Server (Optional)
If you prefer running it on a local server:

```bash
# Using Python
python -m http.server 8000

# Using Node.js (if you have npx)
npx serve .

# Using PHP
php -S localhost:8000
```

Then navigate to `http://localhost:8000`

## ⚠️ Limitations

- **CORS Dependency**: Relies on third-party CORS proxy service
- **Rate Limiting**: Proxy service may have rate limits for high volume usage
- **Content Type**: Only processes HTML content effectively
- **Authentication**: Cannot access password-protected or authenticated pages
- **JavaScript Rendering**: Does not execute JavaScript on target pages

## 🤝 Contributing

This is a simple single-file application. To contribute:

1. Fork the repository
2. Make your improvements
3. Test thoroughly across different browsers
4. Submit a pull request

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

## 🆘 Troubleshooting

### Common Issues

**"Failed to process URL"**
- Check if the URL is publicly accessible
- Verify the URL format is correct (include http:// or https://)
- Some websites may block access through CORS proxies

**"No results showing"**
- Ensure JavaScript is enabled in your browser
- Check browser console for error messages
- Try with a different URL to isolate the issue

**"Copy to clipboard not working"**
- Ensure you're using HTTPS or localhost
- Check if clipboard permissions are enabled in your browser

## 🔮 Future Enhancements

- [ ] Support for batch URL upload via file
- [ ] Word counting statistics (average, total, etc.)
- [ ] Support for different export formats (JSON, Excel)
- [ ] Advanced filtering options for content types
- [ ] Progress bar with percentage completion
- [ ] Retry mechanism for failed URLs
- [ ] Caching for repeated URL requests

---

Made with ❤️ for content creators, SEO professionals, and anyone who needs to quickly analyze word counts across multiple web pages. 