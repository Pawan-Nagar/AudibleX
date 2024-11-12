---

# **AudibleX: AI-Powered Audio Transcription Service**

[![Build Status](https://img.shields.io/badge/build-passing-brightgreen)](link_to_ci) 
[![License](https://img.shields.io/badge/license-MIT-blue)](LICENSE)  
[![Java](https://img.shields.io/badge/java-17-blue)](https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html) 
[![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.3.5-brightgreen)](https://spring.io/projects/spring-boot)

AudibleX is a Spring Boot application that uses OpenAI’s Whisper model to convert audio files into accurate, high-quality transcriptions. Designed with both developers and non-technical users in mind, AudibleX offers a seamless API for transforming speech into readable text, providing a flexible solution for various industries.

---

## **Table of Contents**

- [Why AudibleX?](#why-audiblex)
- [Features](#features)
- [Use Cases](#use-cases)
- [Technology Stack](#technology-stack)
- [Installation](#installation)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Contributing](#contributing)
- [License](#license)

---

## **Why AudibleX?**

AudibleX was created to address the growing need for accessible and efficient audio transcription. By automating the process with AI, it allows users to save time and increase productivity, especially in industries where documentation, accessibility, and content management are critical.

## **Features**

- **High-Quality Transcriptions**: Powered by OpenAI Whisper for precise and natural speech-to-text conversion.
- **Simple API Integration**: Designed as a RESTful API for easy integration into applications.
- **Multiple File Format Support**: Supports popular audio formats like WAV, MP3, etc.
- **Fast Processing**: Returns transcriptions quickly, ideal for real-time applications.
- **Customizable Settings**: Adjustable language and response formats for diverse needs.

## **Use Cases**

1. **Education**: Convert lectures and discussions into text for students and educators.
2. **Podcasting**: Make audio content accessible by providing transcripts to your audience.
3. **Business Meetings**: Generate text records of meetings for better documentation.
4. **Content Accessibility**: Make audio content readable for those with hearing impairments.
5. **Personal Notes**: Use as a tool for transcribing voice memos or brainstorming sessions.

## **Technology Stack**

- **Backend**: Java 17, Spring Boot 3.3.5
- **AI**: OpenAI Whisper model for speech-to-text processing
- **Build**: Maven for dependency management and project build
- **APIs**: RESTful services for easy access and integration

---

## **Installation**

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/AudibleX.git
   cd AudibleX
   ```

2. **Configure API Key**:
   In your `application.properties`, add your OpenAI API key:
   ```properties
   spring.ai.openai.api-key=YOUR_OPENAI_API_KEY
   ```

3. **Build and Run the Application**:
   ```bash
   mvn clean install
   mvn spring-boot:run
   ```

The application should now be running on `http://localhost:8080`.

---

## **Usage**

AudibleX provides a simple API endpoint to upload audio files and receive a transcription. Make a POST request to `/api/transcribe` with your audio file.

### **Example Request**

```bash
curl -X POST -F "file=@path_to_audio_file.wav" http://localhost:8080/api/transcribe
```

### **Example Response**

```json
{
  "transcription": "Your transcribed text here..."
}
```

---

## **API Endpoints**

- **POST `/api/transcribe`**
  - **Description**: Accepts an audio file and returns the transcribed text.
  - **Parameters**:
    - `file` (MultipartFile): The audio file to be transcribed.
  - **Response**:
    - **200 OK**: JSON response with the transcription result.
    - **400 Bad Request**: If the file format is unsupported or the request is invalid.

---

## **Contributing**

Contributions are welcome! If you would like to enhance AudibleX.
