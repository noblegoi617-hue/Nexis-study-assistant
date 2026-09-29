# Nexis Study Assistant — v1.3.5.1
**Nexis Study Assistant** is a Manifest V3 Chrome extension designed as a configurable educational study assistant. It detects multiple-choice question content on the configured LMS/test page, sends the normalized question and options to the selected AI provider, and presents the AI-generated answer, explanation, key concepts, and confidence in a compact glass-style overlay.

### Features

- Dynamic question detection using DOM observation and navigation detection.
- Gemini and OpenAI provider support.
- Gemini `gemini-2.5-flash-lite` as the default model in the current configuration.
- Automatic fallback for temporary Gemini capacity/rate-limit errors.
- AI-generated answer and explanation display.
- Correct-option visual highlighting for the configured study/test workflow.
- Question fingerprinting to avoid duplicate processing.
- Minimize mode that keeps processing active while hiding the assistant body.
- Close/hide mode that keeps processing active without showing the overlay.
- Extension popup control to restore the hidden assistant.
- Draggable glassmorphism UI.
- NEXIS brand link to the creator's Guns.lol page with a supplied click sound.
- Instagram, Discord, and GitHub social icon area.
- API keys stored in Chrome extension storage rather than hard-coded into source.
- No broad `<all_urls>` content-script permission.

### Permissions

- `storage` for settings and session state.
- LMS host permission for the configured website.
- Gemini API host permission.
- OpenAI API host permission.
- A web-accessible sound asset used only when the NEXIS brand is clicked.

### Privacy and security

The extension does not intentionally collect passwords, cookies, CAPTCHA data, or authentication tokens. API credentials are entered by the user and stored in Chrome extension storage. Users should use appropriately restricted API keys and rotate keys that have been publicly exposed.

### Installation

1. Extract the ZIP.
2. Open `chrome://extensions/`.
3. Enable **Developer mode**.
4. Select **Load unpacked**.
5. Choose the extracted extension folder.
6. Open the configured LMS/test website.
7. Configure the AI provider and API key in NEXIS Settings.

### Repository publishing checklist

Before pushing to GitHub:

1. Replace the Instagram placeholder with the actual profile URL.
2. Add the GitHub repository URL to the `SOCIAL.github` value if the icon should be clickable.
3. Never commit a real Gemini or OpenAI API key.
4. Keep API keys in Chrome storage/user settings rather than source files.
5. Review `manifest.json` host permissions before publishing.
6. Test install, minimize, close/hide, Show Assistant, NEXIS link/sound, social links, question detection, AI response, and next-question detection.

## Important scope

Nexis is intended for the user's configured study/test website. It does not bypass authentication, CAPTCHA, cookies, or security controls, and it does not automatically submit answers, click Next, Finish, or Submit controls.

this contant only education perpose 
