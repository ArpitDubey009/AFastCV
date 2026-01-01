# AFastCV
This is Resume - Builder website 
Core Technology Stack
Frontend Logic: Pure JavaScript (ES6+) for state management and DOM manipulation.

Styling: Tailwind CSS for a modern, responsive UI with custom CSS for PDF-specific print dimensions (A4).

Graphics & PDF: * html2canvas: Captures the live DOM element and converts it into a high-resolution raster image.

jsPDF: Generates the final PDF document using the captured image to ensure the output perfectly matches the preview.

Key Features
Dynamic Preview: As you type in the sidebar, the resume preview on the right updates instantly. This is handled via oninput event listeners that sync data between the input fields and the preview <span> or <div> elements.

Stateful Sections: The "Experience" and "Education" sections use an array-based data structure. You can add or remove items dynamically, and the app re-renders the specific section without refreshing the page.

Image Processing: The profile photo feature uses the FileReader API. It reads your local file as a Base64 string and injects it into the preview, allowing for a personalized resume without needing a backend server.

Theming System: The app features a theme switcher that updates a currentTheme variable. This changes the primary color accents (Blue, Red, Emerald, or Slate) across the entire document simultaneously using Tailwind's utility classes.

Adaptive Scaling: The preview window uses CSS transform: scale() to fit a full A4 page into your browser window, ensuring you can see the whole layout regardless of your screen size.

Dark Mode: A global toggle switches the editor interface between light and dark modes, providing a comfortable editing experience in different lighting conditions.

Architecture Highlights
Single-File Build: All HTML, CSS, and JS are contained in one file, making it extremely portable and fast to load.

Vector Icons: The app uses standard emojis and CSS-based shapes for icons to keep the file size minimal and avoid external image dependencies.

A4 Precision: The #pdf-content container is strictly defined as 210mm x 297mm, ensuring that the "Download PDF" function produces a document ready for professional printing and standard HR software.
