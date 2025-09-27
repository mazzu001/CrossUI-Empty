# Testing the CrossUI App

## Automatic Deployment

This app is automatically deployed to GitHub Pages when changes are merged to the master branch.

**Live URL**: https://mazzu001.github.io/CrossUI-Empty

## Local Testing

To test the app locally:

1. Clone the repository
2. Serve the files using a web server (required for external library loading):
   ```bash
   # Using Python
   python3 -m http.server 8000
   
   # Using Node.js
   npx http-server
   
   # Using PHP
   php -S localhost:8000
   ```
3. Open http://localhost:8000 in your browser

**Note**: Do not open the HTML files directly in the browser using `file://` protocol, as this will prevent the CrossUI libraries from loading due to CORS restrictions.

## Expected Behavior

When properly deployed:
- The app should load without the "Can not find CrossUI library" error
- The loading animation should appear briefly
- The CrossUI framework should initialize and launch the app module from `App/js/index.js`

## Debugging

- Use `debug.html` for development with additional debugging features
- Check browser console for any JavaScript errors
- Ensure external CrossUI libraries can be loaded from crossui.com