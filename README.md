# Haotian Xie - Personal Academic Homepage

This is a personal academic homepage template designed for researchers to showcase their publications, experiences, and more. It includes interactive components such as a BibTeX modal and PDF viewer for easy access to references and publications.

## Features

- **Sidebar Navigation**: Easy access to different sections of the website, including Home, Biography, Research, and Publications.
- **Publications Section**: Showcases academic papers with clickable buttons to view BibTeX entries and PDF files in modals.
- **Modals**: 
  - **BibTeX Modal**: Displays the BibTeX citation for the publication.
  - **PDF Modal**: Allows users to view the PDF of the publication directly in the browser.
- **Responsive Layout**: The website adapts to different screen sizes for optimal viewing.

## How to Use

1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/academic-homepage.git
   ```

2. **Set up the project**:
   - Navigate to the folder where you cloned the repository.
   - Open `index.html`, `biography.html`, `publications.html`, or any other page in your preferred text editor.

3. **Add your publications**:
   - Navigate to `publications.html`.
   - For each publication, you can change the information, add new `<div class="publication">` blocks, and add corresponding `BibTeX` and `PDF` links.

4. **Customize the PDF**:
   - In the `showPopup` function, update the `iframe src` URL to link to your actual PDF file:
     ```javascript
     showPopup('pdf-popup-1', 'https://example.com/sample.pdf');
     ```

5. **Style Customization**:
   - Modify `style.css` to adjust the visual appearance of the page, fonts, colors, layout, and more.
   - The layout is fully customizable for the user’s needs.

6. **Publish**:
   - Once you have added your content and customized the page, upload the files to your preferred hosting service (e.g., GitHub Pages, Netlify, etc.).

## File Structure

- `index.html` - The main homepage that can be modified to introduce yourself.
- `biography.html` - A section for your biography and research interests.
- `publications.html` - A section to list your publications with interactive buttons.
- `style.css` - The CSS file for styling the entire webpage.
- `scripts.js` - Contains the JavaScript functions for handling the modal popup behavior.
- `images/` - Folder for storing images used on your website (e.g., profile image).

## Customizing BibTeX and PDF Modals

For each publication, you can add a `BibTeX` modal and a `PDF` modal:

### Example of Adding a New Publication:
```html
<div class="publication">
    <img src="publication-image.jpg" alt="Publication Image">
    <div class="publication-details">
        <h3>Title of the Publication</h3>
        <p><b>Author Name</b></p>
        <p><i>Journal Name, Year</i></p>
        <div class="pub-buttons">
            <a href="#">ECCV 2021</a>
            <a href="#">ARXIV</a>
            <a href="#" onclick="showPopup('bib-popup-1')">BIB</a>
            <a href="#" onclick="showPopup('pdf-popup-1', 'your-pdf-link.pdf')">PDF</a>
            <a href="#">CODE</a>
        </div>
    </div>
</div>
```

### Example of BibTeX Modal:
```html
<div id="bib-popup-1" class="popup">
    <span class="close-btn" onclick="closePopup('bib-popup-1')">×</span>
    <pre>
    @inproceedings{your_bib_entry,
      title={Title of the Paper},
      author={Author Name},
      booktitle={Journal or Conference},
      year={2021}
    }
    </pre>
</div>
```

### Example of PDF Modal:
```html
<div id="pdf-popup-1" class="popup">
    <span class="close-btn" onclick="closePopup('pdf-popup-1')">×</span>
    <iframe src=""></iframe>
</div>
```

## Requirements

- **Web Browser**: Any modern browser (Chrome, Firefox, Safari, etc.)
- **Text Editor**: Any code editor (e.g., Visual Studio Code, Sublime Text, Atom)
- **Hosting Service**: (Optional) GitHub Pages, Netlify, or any other static site hosting service.

## Contributing

Feel free to contribute by:
- Submitting issues.
- Sending pull requests with improvements or new features.

## License

This project is open-source and available under the [MIT License](LICENSE).
