AI Research Summarizer Agent
Project Overview
This project designs and implements a lightweight AI agent focused on automating the research summarization process. Developed as part of an AI Agent Developer Internship assignment for Scoreazy, an education-first company, this tool demonstrates core skills in automation logic, tool usage, and prompt engineering.

The primary objective is to take a list of URLs related to a specific topic, simulate content fetching from these sources, and then leverage a Large Language Model (LLM) to generate a concise, bullet-point summary of the key findings. This aims to simplify and accelerate the research phase for students and educators.

Features
Topic-Based Summarization: Generates summaries based on a user-defined research topic.

Multi-URL Input: Accepts 1 to 5 comma-separated URLs for comprehensive content aggregation.

Simulated Content Fetching: Includes a mock browsing tool to simulate fetching content from web articles for demonstration purposes.

AI-Powered Summarization: Utilizes the Google Gemini API (specifically gemini-2.5-flash-preview-05-20) to process aggregated text and produce structured summaries.

User-Friendly Interface: A simple, responsive web interface built with HTML and Tailwind CSS for easy interaction.

Loading Indicators & Error Handling: Provides visual feedback during processing and displays clear error messages for invalid inputs or API issues.

Robust API Calls: Implements exponential backoff for API requests to handle potential rate limits and network transient issues.

How It Works
The agent follows a clear, step-by-step workflow:

Input Collection: The user provides a research Topic and a list of Article URLs via the web interface.

Content Fetching (Simulated): For each provided URL, the application calls a simulateBrowse function. This function acts as a placeholder for a real web scraping tool, returning predefined mock content for specific URLs.

Content Aggregation: All successfully "fetched" content is combined into a single, large text block.

LLM Interaction: The aggregated content, along with the user's topic, is sent to the Google Gemini API with a carefully crafted prompt.

Summary Generation: The LLM processes the input and generates a concise, bullet-point summary.

Output Display: The generated summary is then displayed on the web page for the user.

Technologies Used
HTML5: For structuring the web application.

CSS3 (Tailwind CSS): For modern, responsive, and utility-first styling.

JavaScript (ES6+): For client-side logic, DOM manipulation, and API interaction.

Google Gemini API (gemini-2.5-flash-preview-05-20): The core AI model for text summarization.

Setup and Running Locally
This project is a single-file web application, making it incredibly easy to run!

Save the Code: Copy the entire code block provided in index.html into a new file on your computer.

Name the File: Save this file as index.html.

Open in Browser: Double-click the index.html file, or drag and drop it into your web browser (e.g., Chrome, Firefox, Edge).

The application will open directly in your browser, ready for use.

Usage
Enter Research Topic: In the "Research Topic" field, type the subject you want to summarize (e.g., Learning Styles in High School Students).

Enter Article URLs: In the "Article URLs" textarea, paste or type the URLs of the articles you want to summarize, separated by commas.

To test with mock data, use the following URLs (you can use any combination of 1 to 5 of them):

https://example.com/learning-styles-1

https://example.com/high-school-pedagogy

https://example.com/research-on-learning-styles

https://example.com/student-engagement-strategies

https://example.com/cognitive-science-learning

Click "Summarize Research": The button will change to "Summarizing..." and a spinner will appear while the AI processes your request.

View Summary: The generated bullet-point summary will appear in the "Summary" section below. Any errors (e.g., invalid input, AI issues) will also be displayed there.

Mock Data & Real-World Application
It's important to note that the simulateBrowse function in this client-side application uses mock data. In a real-world scenario, fetching content from arbitrary URLs would require a server-side component (due to browser Same-Origin Policy restrictions) that performs actual web scraping using libraries like Python's Beautiful Soup or a dedicated web scraping API. This project focuses on the AI agent's logic and workflow, simulating the data acquisition step.

Future Enhancements
Live Web Scraping Integration: Replace simulateBrowse with a backend service that genuinely scrapes content from provided URLs.

URL Validation: More robust validation of URL formats and accessibility.

Advanced Summarization Options: Allow users to specify summary length, tone, or format (e.g., paragraph vs. bullet points).

Source Attribution: Include direct links or citations within the summary to indicate which points came from which article.

User Authentication & History: Implement user accounts to save past summaries and preferences.

Error Handling Refinements: More specific error messages for different types of failures (e.g., URL unreachable, content not found).

License
This project is open-sourced under the MIT License.

Contact
For any questions or feedback, please reach out.
