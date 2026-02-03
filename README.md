# Apache Fancy Index Theme

A modern, minimalist Apache directory listing theme that transforms default server indexes into a sleek, professional interface. Built with custom CSS styling and comprehensive icon support for enhanced user experience.

## Overview

This project provides a complete theming solution for Apache's `mod_autoindex` module, replacing the default directory listings with a clean, responsive design that's perfect for file servers, download centers, and web-based file repositories.

## Key Features

### 🎨 Modern UI/UX Design
- **Clean & Minimal Interface**: Inspired by the Apaxy theme with contemporary aesthetics
- **Responsive Layout**: Fully optimized for desktop, tablet, and mobile devices
- **Custom Typography**: Google Fonts integration (Open Sans) for enhanced readability
- **Smooth Interactions**: CSS3 transitions and hover effects for better user feedback

### 📁 Comprehensive File Type Support
Custom icon set supporting **70+ file types** including:
- **Programming Languages**: C, C++, Python, Java, PHP, JavaScript, Ruby, SQL
- **Documents**: PDF, DOC/DOCX, Excel, RTF, TeX, Markdown
- **Media Files**: Images (PNG, JPG, GIF, BMP, TIFF), Audio (MP3, FLAC, WAV), Video (MP4, AVI, MKV)
- **Archives**: ZIP, RAR, TAR, GZ, 7Z, DEB, RPM
- **Web Files**: HTML, CSS, JS, JSON, XML, RSS
- **Design Files**: PSD, AI, EPS, SVG

### 🔧 Advanced Configuration
- **Smart Sorting**: Folders-first organization with case-insensitive sorting
- **Breadcrumb Navigation**: Automatic path generation with clickable navigation
- **Selective Indexing**: Built-in ignore rules for system and hidden files
- **UTF-8 Support**: Full international character support
- **Icon Linking**: Icons function as clickable elements for improved accessibility

### 🚀 Performance Optimized
- **Lightweight**: Minimal CSS and HTML overhead
- **No JavaScript Dependencies**: Core functionality works without JS (enhanced features use vanilla JavaScript)
- **Browser Optimized**: Cross-browser compatible with modern CSS standards

## Installation

### Prerequisites
- Apache web server with `mod_autoindex` enabled
- Server access to modify `.htaccess` files

### Quick Setup

1. **Clone or download this repository**:
   ```bash
   git clone https://github.com/yourusername/apache-fancy-index.git
   ```

2. **Upload files to your web directory**:
   ```
   your-directory/
   ├── .htaccess
   └── apache_theme/
       ├── header.html
       ├── footer.html
       ├── style.css
       ├── .htaccess
       └── icons/
   ```

3. **Verify paths in `.htaccess`**:
   - Update icon paths if your theme folder location differs
   - Adjust `HeaderName`, `ReadmeName`, and `IndexStyleSheet` directives

4. **Enable directory indexing** (if not already enabled):
   ```apache
   Options +Indexes
   ```

5. **Test** by navigating to your directory in a web browser

## Configuration

### Customizing Ignored Files

Edit `.htaccess` to exclude specific files/folders from listing:
```apache
IndexIgnore .git .DS_Store *.tmp your-folder
```

### Changing Theme Location

If you move the `apache_theme` folder, update all paths in `.htaccess`:
```apache
AddIcon /your-new-path/icons/folder.png ^^DIRECTORY^^
HeaderName /your-new-path/header.html
ReadmeName /your-new-path/footer.html
IndexStyleSheet "/your-new-path/style.css"
```

### Custom Branding

Modify `footer.html` to add your own branding:
```html
<div class="footer">
    Your Custom Footer Text or Links
</div>
```

## Technical Details

### Built With
- **Apache mod_autoindex**: Core directory listing module
- **HTML5 & CSS3**: Modern web standards
- **Vanilla JavaScript**: Minimal scripting for breadcrumb navigation
- **Google Fonts API**: Typography enhancement

### Browser Support
- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- Opera (latest)

### Directory Structure
```
apache-fancy-index/
├── .htaccess              # Main Apache configuration
├── apache_theme/
│   ├── .htaccess          # Theme directory protection
│   ├── header.html        # HTML head and opening wrapper
│   ├── footer.html        # Closing wrapper and footer
│   ├── style.css          # Complete theme styling
│   └── icons/             # 70+ file type icons (PNG)
└── README.md              # This file
```

## Use Cases

- **Personal File Server**: Share files with friends and family
- **Development Server**: Quick file distribution for development teams
- **Download Center**: Host software, documents, or media files
- **Backup Server**: Web-accessible backup file browser
- **CDN Alternative**: Simple content delivery solution
- **Archive Hosting**: Historical document or software repositories

## Customization Examples

### Change Color Scheme
Edit `style.css` to modify the color palette:
```css
html {
    border-top: 10px solid #YOUR_COLOR;
    color: #YOUR_TEXT_COLOR;
}
a:hover {
    color: #YOUR_HOVER_COLOR;
}
```

### Adjust Layout Width
Modify the wrapper width in `style.css`:
```css
.wrapper {
    max-width: 70%; /* Default is 50% */
}
```

## Security Considerations

- **Directory Protection**: Sensitive directories should use authentication
- **Index Control**: Only enable indexes where appropriate
- **File Permissions**: Ensure proper file system permissions
- **Hide System Files**: Use `IndexIgnore` for configuration and system files

## Credits

- **Apaxy Theme**: Original design inspiration by [@adamwhitcroft](https://github.com/adamwhitcroft/apaxy)
- **Icon Set**: Custom curated collection for comprehensive file type coverage

## License

This project is intended for personal and commercial use. Please verify compatibility with your organization's policies.

## Contributing

Contributions are welcome! Areas for improvement:
- Additional file type icons
- Dark mode support
- Enhanced mobile responsiveness
- Additional sorting options
- Search functionality

## Contact

For questions or suggestions regarding this implementation, feel free to open an issue or submit a pull request.

---

**Made with ❤️ for better web file browsing**
