## LangChain: Summarize Text From YouTube or Website

This Streamlit application uses LangChain, ChatGroq, and document loaders to summarize content from either YouTube videos or website URLs. With this app, users can extract and condense information from long-form video content or web pages into a concise, 300-word summary.

## Features

* **Supports YouTube and Website Summarization**:
Automatically detects YouTube video URLs or generic website URLs and processes their content for summarization.

* **Secure Input**:
Users need to provide a Groq API key for accessing the Gemma LLM. Inputs, including the URL, are validated to ensure they are in the correct format.

* **Dynamic Summarization**:
The app uses a customizable prompt template to generate summaries in under 300 words.

* **Error Handling**:
Displays appropriate error messages for invalid inputs or API issues.


## How It Works

1. **User Input:**
Enter your Groq API key in the sidebar.
Paste a YouTube video URL or a website URL in the input field.

2. **Content Validation:**
The app validates the provided API key and URL.
If the URL is a YouTube video, it uses YoutubeLoader to extract video information.
For websites, it uses UnstructuredURLLoader to fetch the page content.

3. **Summarization Process:**
The app sends the extracted content to the Gemma-7b-It model via the Groq API.
The PromptTemplate generates a summary of the content.

4. **Display Results:**
The app displays the summarized content in the interface.