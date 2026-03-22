# ServiceNow KB Article Editor

A visual editor for ServiceNow Knowledge Base articles that helps clean and edit HTML content.

## How to Run

### Option 1: Open HTML File Directly (Simplest)

1. Open `index.html` in any modern web browser (Chrome, Firefox, Edge, Safari)
2. The application will load automatically with all dependencies from CDN

### Option 2: Use the React Component (For Development)

1. The main component is in `ServiceNowKBEditor.jsx`
2. You can import this into any React project that has:
   - React 18+
   - Tailwind CSS
   - lucide-react icons

```jsx
import ServiceNowKBEditor from './ServiceNowKBEditor.jsx';

function App() {
  return <ServiceNowKBEditor />;
}
```

### Option 3: Local Development Server (Recommended for Development)

If you want to run it with a local server:

```bash
# Using Python (if installed)
python -m http.server 8000

# Using Node.js (if installed)
npx serve .

# Using PHP (if installed)
php -S localhost:8000
```

Then open `http://localhost:8000` in your browser.

## How to Use

1. **IMPORT Mode**: 
   - Paste HTML from ServiceNow's source code view
   - Click "Clean & Import" to process the HTML

2. **EDIT Mode**: 
   - Edit the content visually like a document
   - Select text to see formatting toolbar
   - Make your changes directly in the visual editor

3. **EXPORT Mode**: 
   - Copy the cleaned HTML
   - Paste it back into ServiceNow's source code view

## Features

- ✅ Cleans ServiceNow's messy HTML automatically
- ✅ Visual editing with floating toolbar
- ✅ Preserves all important HTML structure
- ✅ Clipboard integration
- ✅ Character and tag counting
- ✅ Preview mode
- ✅ Dark theme interface

## Browser Requirements

- Modern browser with ES6+ support
- Clipboard API support (for paste/copy features)
- ContentEditable support

Works best in Chrome, Firefox, Edge, and Safari.
