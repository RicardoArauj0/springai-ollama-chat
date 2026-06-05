# springai-ollama-chat
Simple application that uses spring ai to connect with your local LLM using Ollama for simple messages.

# Spring Boot AI with Ollama

This is a sample Spring Boot application demonstrating how to integrate [Spring AI](https://spring.io/projects/spring-ai) with [Ollama](https://ollama.com/) to build a simple chat application.

## Prerequisites

- **Java 21** or higher
- **Maven**
- **Ollama** installed and running locally.

## Project Configuration

The application is configured to use the Ollama model `gemma4:e2b` as defined in `application.properties`:

```properties
spring.application.name=ai
spring.ai.model.chat=ollama
spring.ai.ollama.chat.model=gemma4:e2b
```

## How to Run

1. **Start Ollama** and ensure you have pulled the required model. 
   ```bash
   ollama run gemma4:e2b
   ```

2. **Run the Spring Boot application** from the project root:
   ```bash
   ./mvnw spring-boot:run
   ```
   *(Or run the `OllamaAiApplication` class directly from your IDE)*

3. **Test the Chat API**. The application exposes a REST endpoint at `/api/chat`.
   You can test it using a browser, Postman, or `curl`:
   ```bash
   curl "http://localhost:8080/api/chat?message=Tell%20me%20a%20programming%20joke"
   ```

## Dependencies

- **Spring Boot Web** (`spring-boot-starter-webmvc`)
- **Spring AI Ollama** (`spring-ai-starter-model-ollama`)

## Project Structure

- `ChatController.java`: Defines the REST API endpoint and uses `ChatClient` to send prompts to the Ollama model and return its response.
- `OllamaAiApplication.java`: The main Spring Boot application class.

