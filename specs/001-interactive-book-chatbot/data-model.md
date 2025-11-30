# Data Model for Interactive Book with RAG Chatbot

## Entities

### Book
Represents the entire content of the book.

-   **id**: string (unique identifier)
-   **title**: string
-   **chapters**: array of Chapter

### Chapter
A section of the book.

-   **id**: string (unique identifier)
-   **title**: string
-   **pages**: array of Page

### Page
A single page within a chapter.

-   **id**: string (unique identifier)
-   **title**: string
-   **content**: string (the text content of the page)

### Chatbot
The interactive widget that answers user questions.

-   (No specific data model for the chatbot itself, as it's a UI component)

### Question
A query submitted by the user to the chatbot.

-   **id**: string (unique identifier)
-   **text**: string (the user's question)
-   **context**: string (optional, the user-selected text)
-   **timestamp**: datetime

### Answer
The response provided by the chatbot.

-   **id**: string (unique identifier)
-   **text**: string (the chatbot's answer)
-   **question_id**: string (foreign key to Question)
-   **timestamp**: datetime

## Relationships

-   A **Book** has many **Chapters**.
-   A **Chapter** has many **Pages**.
-   A **Question** has one **Answer**.

## State Transitions

-   (Not applicable for this feature)
