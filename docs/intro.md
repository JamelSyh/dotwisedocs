---
sidebar_position: 1
---

Braille API Documentation

Braille API Documentation
=========================

Introduction
------------

The Braille API allows you to transcribe and translate text into braille. This API provides the following endpoints:

*   [Transcript](#transcript): Transcribes text from one language to another.
*   [Translate](#translate): Translates text from one language to another and transcribes it into braille.
*   [Download File](#download-file): Downloads a braille file.
*   [Get Transcribe Options](#get-transcribe-options): Retrieves the available transcribe options.
*   [Get Translate Options](#get-translate-options): Retrieves the available translate options.
*   [Get Contraction List](#get-contraction-list): Retrieves the list of contractions for a specific language.
*   [Get Search Options](#get-search-options): Retrieves the available search options.

Authentication
--------------

To access the API endpoints, you need to include an API key in the request header. The API key should be passed in the `key` parameter.

### Example:

    key: YOUR_API_KEY

Transcript
----------

Transcribes text from one language to another.

#### Endpoint

    POST /api/transcript

#### Request Parameters

*   `text` (string): The text to be transcribed.
*   `source` (string): The source language of the text.
*   `target` (string): The target language for transcription.
*   `key` (string): The API key for authentication.

#### Response

*   `result` (string): The transcribed text.

#### Example

    import requests
    
    url = "https://api.example.com/api/transcript"
    data = {
        "text": "Hello world",
        "source": "en",
        "target": "fr",
        "key": "YOUR_API_KEY"
    }
    
    response = requests.post(url, data=data)
    result = response.json()["result"]
    print(result)
