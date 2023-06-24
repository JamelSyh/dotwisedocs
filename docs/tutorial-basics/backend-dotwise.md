---
sidebar_position: 2
---


dotwise Backend Documentation
=============================

Installation
------------

To install the dotwise backend, follow the steps below:

1.  Clone the repository from GitHub:

    git clone https://github.com/your-username/dotwise.git

2.  Navigate to the project directory:

    cd dotwise

3.  Create a virtual environment:

    python -m venv venv

4.  Activate the virtual environment:

    source venv/bin/activate

5.  Install the required dependencies:

    pip install -r requirements.txt

6.  Set up the database:

    python manage.py migrate

7.  Start the development server:

    python manage.py runserver

API Endpoints
-------------

### Transcript

**Endpoint:** POST /api/transcript

**Description:** Transcribes the given text from the source language to the target language.

**Parameters:**

*   **text** (string): The text to be transcribed.
*   **source** (string): The source language code.
*   **target** (string): The target language code.
*   **key** (string, optional): API key for authentication.

**Example:**

    curl -X POST -H "Content-Type: application/json" -d '{
      "text": "Hello",
      "source": "en",
      "target": "fr",
      "key": "YOUR_API_KEY"
    }' http://localhost:8000/api/transcript

### Translate

**Endpoint:** POST /api/translate

**Description:** Translates the given text from the source language to the target language using an external translation service.

**Parameters:**

*   **text** (string): The text to be translated.
*   **source\_lang** (string): The source language code.
*   **source\_grade** (string): The source grade code.
*   **target\_lang** (string): The target language code.
*   **target\_grade** (string): The target grade code.
*   **key** (string, optional): API key for authentication.

**Example:**

    curl -X POST -H "Content-Type: application/json" -d '{
          "text": "Hello",
          "source_lang": "en",
          "source_grade": "A",
          "target_lang": "fr",
          "target_grade": "B",
          "key": "YOUR_API_KEY"
        }' http://localhost:8000/api/translate

### Spell Check

**Endpoint:** POST /api/spellcheck

**Description:** Performs spell checking on the given text.

**Parameters:**

*   **text** (string): The text to be spell checked.
*   **language** (string): The language code.
*   **key** (string, optional): API key for authentication.

**Example:**

    curl -X POST -H "Content-Type: application/json" -d '{
      "text": "Helo",
      "language": "en",
      "key": "YOUR_API_KEY"
    }' http://localhost:8000/api/spellcheck

### Grammar Check

**Endpoint:** POST /api/grammarcheck

**Description:** Performs grammar checking on the given text.

**Parameters:**

*   **text** (string): The text to be grammar checked.
*   **language** (string): The language code.
*   **key** (string, optional): API key for authentication.

**Example:**

    curl -X POST -H "Content-Type: application/json" -d '{
      "text": "He walk to school.",
      "language": "en",
      "key": "YOUR_API_KEY"
    }' http://localhost:8000/api/grammarcheck

