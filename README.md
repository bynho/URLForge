# URLForge

A simple yet powerful web application for managing and transforming URLs with variable parameters.

![URLForge Logo](https://via.placeholder.com/800x400?text=URLForge)

## 🌟 Features

- **Variable URL Templates**: Create URL templates with variables in {curly braces}
- **Dynamic Parameter Editing**: Easily edit URL parameters through a generated form interface
- **Real-time Preview**: See your URL changes instantly with highlighted variables
- **Persistent Storage**: Save and organize URL templates for future use
- **Domain Organization**: Templates automatically organized by domain for easy access
- **Search Functionality**: Quickly find saved templates with full-text search
- **Mobile Responsive**: Works great on both desktop and mobile devices
- **GitHub Gist Sync**: Optional synchronization with GitHub Gists (requires API setup)
- **Copy to Clipboard**: One-click copying of generated URLs
- **Offline Capable**: Works without an internet connection

## 📋 Use Cases

- Managing API URLs with changing parameters
- Storing and switching between different versions of tracking URLs
- Saving and organizing dashboard URLs with various query parameters
- Quickly generating URLs for different environments (dev, staging, production)
- Sharing common URL structures with team members

## 🚀 Getting Started

### Installation

URLForge is a single HTML file application with no dependencies or build process required.

1. Download the `index.html` file from this repository
2. Open it in any modern web browser
3. That's it! No server or installation needed

Alternatively, you can serve it using any web server:

```bash
# Using Python's built-in server
python -m http.server 8000

# Or using Node.js http-server
npx http-server
```

### GitHub Integration (Optional)

To enable GitHub Gist synchronization:

1. [Create a new GitHub OAuth App](https://github.com/settings/applications/new)
2. Set the homepage URL to where you'll host URLForge
3. Set the callback URL to the same location
4. Copy your Client ID and replace `YOUR_GITHUB_CLIENT_ID` in the code

## 💻 Usage Examples

### Basic URL Template

1. Enter a URL template with variables in curly braces:
   ```
   https://api.example.com/users/{user_id}/profile?detail={detail_level}
   ```

2. Click "Parse URL" to generate the variable form

3. Fill in variable values:
   - user_id: `12345`
   - detail_level: `full`

4. Click "Copy" to copy the generated URL to clipboard:
   ```
   https://api.example.com/users/12345/profile?detail=full
   ```

### Business URL Example

For a Facebook Business URL like:
```
https://business.facebook.com/latest/settings/whatsapp_account?business_id=599966726031135
```

URLForge will:
1. Extract `business_id` as a variable
2. Allow you to save multiple business IDs
3. Group them under the `business.facebook.com` domain
4. Provide quick access to these saved templates

## 🛠️ Technology

URLForge is built using only:
- HTML5
- CSS3
- Vanilla JavaScript

### Storage
- Primary: IndexedDB
- Fallback: LocalStorage

## 🧩 Project Structure

```
└── index.html          # Complete application in a single file
    ├── CSS             # Embedded styles
    ├── HTML            # Application structure
    └── JavaScript      # Application logic
        ├── Utilities   # Helper functions
        ├── Storage     # IndexedDB/localStorage management
        ├── UI          # User interface handlers
        └── GitHub      # GitHub Gist integration
```

## 🤝 Contributing

Contributions are welcome! Here are ways you can contribute:

1. Reporting bugs
2. Suggesting enhancements
3. Sending pull requests
4. Improving documentation

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgements

- Inspired by the common need to manage variable URLs across various platforms
- Built with modern web standards for maximum compatibility
- Icons and design inspiration from various open-source projects

---

Made with ❤️ by [Your Name]