# ⚡ PDF Speed Reader

A lightweight, single-file HTML5 speed reading tool designed to help you consume PDFs and text content faster using **RSVP** (Rapid Serial Visual Presentation). It runs entirely in your browser without backend servers.


## ✨ Features


### 📖 Reading Modes



* **PDF Mode:** robust parsing using pdf.js to extract text while maintaining structure.
    * Auto-detects chapters/bookmarks for navigation.
    * Filters out headers, footers, and page numbers to keep reading flow smooth.
    * Visual "Map" tracks your position on the actual PDF page in real-time.
* **Text Mode:** Simply paste any text to start reading immediately.
    * Edit text on the fly.
    * Real-time highlighting of the current word in the text block (Desktop).


### ⚡ RSVP Engine (Rapid Serial Visual Presentation)



* **Optimal Viewing Position (OVP):** Highlights a specific "Focus Letter" in red to reduce eye movement.
* **Dynamic Timing:** Automatically pauses longer on long words, punctuation (periods, commas), and paragraph breaks to improve comprehension.
* **Adaptive Font Sizing:** Automatically adjusts text size based on word length to prevent overflow.


### 📱 Responsive Design



* **Desktop:** Split-screen layout.
    * Left: Reader & Controls.
    * Right: Large PDF Preview or Text Editor.
* **Mobile:** Swipeable Card Interface.
    * Top Widget: Carousel between Controls and Page Map.
    * Bottom Widget: Reader display (swipe right to edit text in Text Mode).
    * Full support for notch/status bar safe areas (viewport-fit=cover).


### 🎮 Controls & Interaction



* **Speed:** Adjustable from **50 to 1000 WPM** (Words Per Minute).
* **Navigation:** Jump to specific chapters or pages.
* **Gestures:**
    * **Pinch-to-Zoom:** Zoom into PDF pages in the full-screen modal.
    * **Swipe Navigation:** Swipe to change pages in the modal.
* **Keyboard Shortcuts:**
    * Space: Play / Pause.
    * Left Arrow: Rewind 10 words.
    * Right Arrow: Skip forward 10 words.


## 🚀 How to Use



1. **Open the Website:** You can open the website under **Deployments** or follow this link: [https://vlctqr.github.io/SpeedReader/](https://vlctqr.github.io/SpeedReader/).
2. **Load Content:**
    * Click **Upload PDF** to select a local file.
    * Click **Paste Text** to enter raw text.
3. **Adjust Settings:** Use the slider to set your desired WPM.
4. **Read:** Press the **Play** button or Spacebar to start.
5. **Navigate:** Use the dropdown to jump to chapters or use the slider to scrub through the text.


## 🛠️ Technical Details

This project is built as a **Single File Application**. All HTML, CSS, and JavaScript are contained within speed_reader.html.



* **Frameworks:** None (Vanilla JS).
* **Styling:** [Tailwind CSS](https://tailwindcss.com/) (via CDN).
* **PDF Engine:** [PDF.js](https://mozilla.github.io/pdf.js/) (via CDN) for parsing and rendering.
* **Icons:** [Font Awesome](https://fontawesome.com/) (via CDN).


### Key Logic



* **Text Extraction:** The tool uses coordinate-based heuristic analysis to detect paragraphs (vertical gaps) and skip headers/footers (top/bottom page margins).
* **Hyphen Merging:** Automatically glues words split across lines (e.g., "con- \n nection" becomes "connection").
* **Punctuation Merging:** Ensures punctuation marks stick to their preceding word to prevent "flashing" symbols.


## 📄 License

This project is open-source and free to use.