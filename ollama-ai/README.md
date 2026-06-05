# Spring AI Chat Application

A simple Spring Boot application demonstrating how to integrate Spring AI with OpenAI to create a chat endpoint.

## Prerequisites

* Java 21 or higher
* Maven
* An OpenAI API Key

## Setup

1. **Set the OpenAI API Key:**
   The application requires an OpenAI API key to function. Set it as an environment variable before running the application:

   **Linux/macOS:**
   ```bash
   export OPENAI_API_KEY="your_api_key_here"
   ```
   
   **Windows (Command Prompt):**
   ```cmd
   set OPENAI_API_KEY=your_api_key_here
   ```
   
   **Windows (PowerShell):**
   ```powershell
   $env:OPENAI_API_KEY="your_api_key_here"
   ```

## Running the Application

You can run the application using the included Maven Wrapper:

```bash
./mvnw spring-boot:run
```

## Usage

The application exposes a single REST endpoint for interacting with the AI model.

**Endpoint:** `GET /api/chat`

**Parameters:**
* `message`: The message/prompt to send to the AI.

**Example Request:**
```bash
curl "http://localhost:8080/api/chat?message=Tell me a joke"
```

**Example Response:**
```text
Why did the scarecrow win an award? Because he was outstanding in his field!
```

## Technologies Used

* Spring Boot
* Spring AI (OpenAI Starter)
* Java 21
* Maven
