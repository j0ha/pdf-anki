# PDF to Anki

## Introduction

PDF to Anki program using GPT3.5-turbo from OpenAI. Streamlit is the web-GUI. Shout-out to OpenAI and Streamlit for saving me a ton of work!.

Version 0.5 alpha (Not perfect, but usable).

## Requirements:

- Anki running with AnkiConnect installed (Addon #: 2055492159)
    - Add "https://pdf-anki.streamlit.app" to "webCorsOriginList" under Tools -> Addons -> Config, then restart Anki.

*If compiling to run locally:*
- An OpenAI key
    - Needs to be added as OPENAI_API_KEY="[Key here]" in .streamlit\secrets.toml
 - "Add "http://localhost:8501" to "webCorsOriginList" under Tools -> Addons -> Config, then restart Anki."

## Usage:

1. Select a page range and a language for the flashcards.
2. Choose a PDF file. Cards will automatically be created for each page.
3. Flash cards are displayed and can then be modified before being added to Anki.

### To do:

- Option to add card
- Add option to choose title of deck and possibly call up available decks in Anki to choose location
- Allow user to change prompt options
- Add formatting in response

### Changelog:

0.5 alpha

- Lowered chance that GPT returns non-parseable result by moving to functions
- Skip pages without relevant info

0.46 alpha
- Added JPEG compression to reduce image size
- Fixed key error causing Streamlit crash
- Stopped unnecessary regenerations of flashcards

0.45 alpha
- Improved memory usage
- Can now add flashcards to Anki without running locally
- Added filename and page as tag
- Max. uploaded file size reduced to 50MB

0.4 alpha
- Can now add without running locally
- Can now add page range and change on-the-fly
- Option to select returned language

0.3 alpha
- User is updated on status and errors
- Improved GPT prompt

0.2 alpha
- Changed to Streamlit Web-GUI
- Removed image detection
- Shifted flashcards view to show alongside page preview
- Using pymupdf instead of pdf2image to reduce reliance on external libraries

0.1 alpha
- First release
