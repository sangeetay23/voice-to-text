## Text to Speech Converter Documentation

This documentation describes the functionality of the Text to Speech Converter application.

**1. Files:**

* **index.html:** The main HTML file responsible for the structure and layout of the application.
* **styles.css:** Contains the styling rules for the application's user interface.
* **voice.js:**  Handles the functionality of converting text to speech.

**2. index.html:**

* **DOCTYPE html:**  Declares the document as HTML5.
* **lang="en":**  Specifies the document language as English.
* **meta charset="UTF-8":**  Defines the character encoding for the page.
* **meta name="viewport"...:**  Sets up the viewport for responsiveness across different devices.
* **title:**  Sets the title of the webpage displayed in the browser tab.
* **link rel="stylesheet" href="styles.css":**  Includes the CSS file for styling the application.

**3. styles.css:**

* **@import url(...):** Imports the Poppins font from Google Fonts for consistent styling.
* **body:**  Resets default styles, sets font family to Poppins, and ensures consistent box sizing.
* **.container:**  Centers the main content horizontally and vertically, uses a linear gradient for the background.
* **.app-container:**  Houses the application's components, centers content, and sets the text color.
* **.headings-container:**  Styles the heading elements with padding.
* **.interaction-container:**  Organizes the text input area, button, and error message.
* **.text-control:**  Styles the text input area, provides background and border styling, and removes the default outline.
* **.error-para:**  Displays error messages in red.
* **.btn:**  Styles the conversion button with gradient background, rounded corners, and hover effects.
* **.footer_section:** Styles the footer section with fixed positioning, background color, text alignment, and padding.

**4. voice.js:**

* **const text = ...:**  Selects the text input element by its ID.
* **const convertBtn = ...:**  Selects the conversion button element by its ID.
* **convertBtn.addEventListener('click', ...):**  Adds an event listener to the button, triggering the speech conversion logic when clicked.
* **const speechSynth = window.speechSynthesis:**  Initializes the Web Speech API.
* **const enteredText = text.value:**  Gets the text from the input area.
* **const error = ...:**  Selects the error message element.
* **if (!speechSynth.speaking && !enteredText.trim().length):**  Checks if the speech synthesis engine is busy or if the input text is empty, then displays an error message.
* **if (!speechSynth.speaking && enteredText.trim().length):**  Checks if the speech synthesis engine is busy and the input text is not empty, then proceeds with conversion.
* **const newUtter = new SpeechSynthesisUtterance(enteredText):**  Creates a new utterance object with the input text.
* **speechSynth.speak(newUtter):**  Starts speaking the text using the Speech Synthesis API.
* **convertBtn.textContent = "Sound is Playing...":**  Changes the button text while the conversion is in progress.
* **setTimeout(...):**  Sets a timer to reset the button text back to its original state after 5 seconds.

**5. Application Functionality:**

1. Users enter text in the text area.
2. Clicking the "Play Converted Sound" button triggers the conversion process.
3. The JavaScript code checks for empty input and checks if the speech synthesis engine is busy.
4. If the input is valid and the engine is available, the text is converted to speech and played.
5. The button text changes to indicate that the sound is playing.
6. The button text reverts back after 5 seconds.

**Note:** This application utilizes the Web Speech API for text-to-speech functionality. It requires a browser that supports this API.

This README provides a comprehensive overview of the Text to Speech Converter application. By understanding the code and functionality, users can customize and extend the application for their needs.
