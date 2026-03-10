# Study Camp Programme (SCP) Landing Page

Landing page for the Study Camp Programme at the University of Economics and Law (UEL).

## 🚀 Deploy to Vercel

### Quick Deploy

1. **Install Vercel CLI** (optional):
```bash
npm install -g vercel
```

2. **Deploy via Vercel Dashboard**:
   - Go to [vercel.com](https://vercel.com)
   - Click "Add New Project"
   - Import your Git repository (GitHub, GitLab, or Bitbucket)
   - Vercel will automatically detect the configuration from `vercel.json`
   - Click "Deploy"

3. **Deploy via CLI**:
```bash
vercel
```

### Configuration

The project includes a `vercel.json` file with the following configuration:
- Static file serving for HTML, CSS, and images
- CORS headers for component loading
- Clean URL routing

## 📁 Project Structure

```
├── index.html          # Main landing page
├── header.html         # Header component
├── footer.html         # Footer component
├── navbar.html         # Navigation bar component
├── style.css           # Landing page styles
├── components.css      # Component styles (header, footer, navbar)
├── global.css          # Global styles and fonts
├── images/             # Image assets
├── vercel.json         # Vercel deployment configuration
└── package.json        # Project metadata
```

## 🛠️ Local Development

To run locally, use any static file server:

**Python:**
```bash
python -m http.server 8000
```

**Node.js (http-server):**
```bash
npx http-server -p 8000
```

**VS Code Live Server:**
- Install "Live Server" extension
- Right-click on `index.html` and select "Open with Live Server"

Then open `http://localhost:8000` in your browser.

## 🎨 Features

- Responsive design
- Modular component architecture
- Auto-hiding header on scroll
- Interactive sections
- Optimized for SEO

## 📝 Notes

- All component files (header.html, footer.html, navbar.html) are loaded dynamically via JavaScript fetch API
- Images should be placed in the `images/` folder
- The site uses Google Fonts: Oswald and Libre Franklin

## 🔗 Links

- UEL Website: [www.uel.edu.vn](https://www.uel.edu.vn/en)
- FIS Department: [is.uel.edu.vn](https://is.uel.edu.vn)
