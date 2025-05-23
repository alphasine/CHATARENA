# AI Speakers' Corner Debate

## Description

AI Speakers' Corner Debate is a web-based application that simulates a dynamic debate between two AI agents. Users can define topics, customize AI personas and core instructions, and witness the debate unfold with text-to-speech (TTS) audio output for AI responses. The application also features an interactive AI judge that provides scores and feedback on the debate rounds.

## Features

*   **AI vs. AI Debates:** Engage two AI agents in a debate on a user-specified topic.
*   **Customizable AIs:** Define unique roles, personas, and detailed instructions for each AI debater.
*   **LLM-Powered Enhancements:** Utilize a Large Language Model (Gemini) to:
    *   Suggest debate topics.
    *   Enhance AI instructions for more compelling personas.
    *   Provide strategic insights into the debate setup.
    *   Offer post-debate analysis.
*   **Text-to-Speech (TTS):** AI responses are read aloud using the browser's built-in speech synthesis.
*   **Decoupled Speech Playback:** AI text generation and the debate's text flow proceed independently of audio playback. A speech queue system buffers responses, allowing the text debate to advance rapidly while audio playback follows, ensuring a smoother listening experience without holding up the debate itself.
*   **Interactive Judge:** An AI judge evaluates debate rounds, providing scores and textual feedback.
*   **Theme Toggle:** Switch between dark and light user interface themes.
*   **Voice Selection & Samples:** Choose from available system voices for each AI and play samples.

## Setup and Running

This application is a single-page web application built with HTML, CSS, and JavaScript.

1.  **Get the Code:**
    *   Clone this repository or download the `index_CANVAS.html` file.
2.  **Open in Browser:**
    *   Open the `index_CANVAS.html` file directly in a modern web browser (e.g., Chrome, Firefox, Edge).
3.  **API Key Configuration:**
    *   **Crucial:** This application requires a Google Gemini API key to function.
    *   The API key should be entered into the "Gemini API Key" input field provided in the application's control bar at the bottom.
    *   **Security Note:** The application stores the API key in browser local storage for convenience during a session. Be aware that storing API keys in client-side local storage is generally a security risk for production applications. Use this feature for personal testing only with appropriate caution. Do not use an API key that has broad permissions or access to sensitive data.

## Codebase Overview

All the application's logic, including the HTML structure, CSS styling, and JavaScript, is contained within the `index_CANVAS.html` file. The JavaScript section handles:

*   User interface interactions and DOM manipulation.
*   Debate logic, turn management, and phase progression.
*   API calls to the Google Gemini models for AI response generation, judge evaluations, and other LLM-driven features.
*   Text-to-speech synthesis using the browser's SpeechSynthesis API.
*   The speech queue system for decoupled audio playback.
*   State management for the debate.

## Potential Future Enhancements / Known Issues

*   **Fully Decoupled Judge Evaluations:** The current implementation for judge evaluations involves API calls that temporarily pause the main AI text debate flow. A future enhancement would be to make these judge evaluations fully asynchronous (similar to the speech queue) so that the AI text debate can proceed to completion without any pauses for judge "thinking" time.
*   **Advanced Voice Customization:** Explore options beyond system voices, potentially integrating with more advanced TTS services if available.
*   **Persistent State:** Implement a backend or more robust local storage solution for saving debate configurations, history, or user preferences beyond a single session.
*   **Error Handling:** While basic error handling for API calls exists, it could be made more comprehensive and user-friendly.

## License

Please add your desired open-source license here if you plan to share this project. Common choices include MIT, Apache 2.0, or GPL. If unsure, resources like [choosealicense.com](https://choosealicense.com/) can help.
