﻿# YouTube Video Notes Generator

## Overview
This Streamlit application allows users to convert YouTube videos into detailed notes, including summaries and mind maps. The app also provides translation capabilities, making it accessible to a global audience. It's ideal for students, professionals, and anyone looking to transform video content into readable and organized information quickly.

## Features
- **Transcript Extraction**: Automatically extracts the transcript from a provided YouTube video link.
- **Summary Generation**: Uses Google's Gemini-PRO LLM API to generate comprehensive and detailed summaries from the extracted transcript.
- **Mind Map Generation**: Converts summaries into visually structured mind maps.
- **Translation**: Supports translation of the generated summaries and mind maps into multiple languages using the Google Translator API.
- **Interactive UI**: Provides an easy-to-navigate user interface with tabs for introduction, note generation, and credits.

## Implementation Details

### Environment Setup
- Loads environment variables using `dotenv` to securely access API keys.
- Configures Google's Gemini-PRO LLM API for content generation.

### Session State
- Initializes session state variables to manage the transcript text, summary, translated text, mind map text, and translated mind map.

### User Interface
- Uses `streamlit_option_menu` for navigation and `streamlit_lottie` for animations.
- Provides a detailed introduction to the app and its features.
- Allows users to input a YouTube link and display the video thumbnail.

### Note Generation
- Extracts the transcript from the YouTube video using `YouTubeTranscriptApi`.
- Generates a detailed summary using the `gemini-pro` model based on a predefined prompt.
- Allows users to download the generated summary.

### Translation
- Users can select their target language from a dropdown menu.
- Translates the generated summary into the selected language and allows downloading of the translated text.

### Mind Map Generation
- Converts the summary into a markdown format suitable for mind maps.
- Uses `streamlit_markmap` to display the mind map.
- Provides translation capabilities for the mind map as well.

### Credits
- Displays developer information with links to social media profiles.
- Uses custom styles and social icons to create an engaging credits section.

## Code Structure

### Imports and Configuration
- Imports necessary libraries for the app functionality.
- Loads environment variables and configures the Google API.

### Session State Initialization
- Ensures session state variables are initialized to manage different stages of the note generation process.

### Prompt Definitions
- Defines prompts for generating summaries and mind maps using the Gemini model.

### Option Menu
- Sets up a horizontal navigation menu for different sections of the app.

### Functions
- `load_lottiefiles`: Loads Lottie animation files.
- `extract_transcript_details`: Extracts transcript from a YouTube video.
- `generate_gemini_content`: Generates content using the Gemini model.
- `generate_gemini_content_mindmap`: Generates markdown for mind maps.
- `translate_text`: Translates text using Google Translator.

### Tab Content
- **INTRO Tab**: Provides an overview and introduction to the app.
- **YT NOTES Tab**: Handles video input, transcript extraction, summary generation, translation, and mind map creation.
- **CREDITS Tab**: Displays developer credits and social media links.

## Getting Started

1. Clone the repository:
    ```sh
    git clone https://github.com/SilverStark18/youtubesummariser.git
   
    ```
2. Navigate to the project directory:
    ```sh
    cd youtubesummariser
    ```
3. Install the required dependencies:
    ```sh
    pip install -r requirements.txt
    ```
4. Create a `.env` file in the root directory and add your API keys:
    ```
    GOOGLE_API_KEY=your_google_api_key
    get your own key from google maker suite
    ```
5. Run the Streamlit app:
    ```sh
    streamlit run app.py
    ```

## Usage

1. Navigate to the **YT NOTES** tab.
2. Enter a YouTube video link.
3. Click **Generate Notes** to get a detailed summary.
4. Click **Translate NOTES** to translate the summary into a desired language.
5. Navigate to the **Mind Map** tab to generate a mind map.
6. Click **Translate Mindmap** to translate the mind map into a desired language.

## Credits
Crafted by: Amarnath Siliveri

### Social Links
- [GitHub](https://www.github.com/SilverStark18) [Instagram](http://www.instagram.com/itz..amar.)  [LinkedIn](http://www.linkedin.com/in/amarnath-siliveri18) [Medium](https://medium.com/@amartalks25603) [Twitter](https://www.x.com/Amarsiliveri) [Threads](https://www.threads.net/@itz..amar.)

Stay in the loop and level up your knowledge with every follow!
