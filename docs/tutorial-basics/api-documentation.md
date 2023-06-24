---
sidebar_position: 1
---

API Documentation
=================

Register as a Developer
-----------------------

To access the API, you need to register as a developer on [dotwise.online](https://dotwise.online) and obtain an API key.

Endpoints
---------

### 1\. Transcript

Transcribes a given text from one language to another language in Braille.

#### Endpoint:

`POST /transcript`

#### Request Body:

`{ "text": "The text to transcribe", "source": "en", "target": "fr", "key": "YOUR_API_KEY" }`

#### Response:

`{ "result": "The transcribed text in Braille" }`

### 2\. Translate

Translates a given text from one language to another language in Braille.

#### Endpoint:

`POST /translate`

#### Request Body:

`{ "text": "The text to translate", "source_lang": "en", "source_grade": "1", "target_lang": "fr", "target_grade": "1", "key": "YOUR_API_KEY" }`

#### Response:

`{ "result": "The translated text in Braille" }`

### 3\. Download File

Downloads a file containing the given Braille text.

#### Endpoint:

`GET /download_file`

#### Query Parameters:

`braille: The Braille text to download as a file key: YOUR_API_KEY`

### 4\. Get Transcribe Options

Retrieves a list of available language options for transcription.

#### Endpoint:

`GET /get_transcribe_options`

#### Query Parameters:

`key: YOUR_API_KEY`

#### Response:

`[ { "code": "en", "name": "English" }, { "code": "fr", "name": "French" }, { "code": "ar", "name": "Arabic" } ]`

### 5\. Get Translate Options

Retrieves a list of available language options for translation.

#### Endpoint:

`GET /get_translate_options`

#### Query Parameters:

`key: YOUR_API_KEY`

#### Response:

`[ { "code": "en", "name": "English" }, { "code": "fr", "name": "French" }, { "code": "ar", "name": "Arabic" } ]`

### 6\. Get Contraction List

Retrieves a list of contractions for a specific language.

#### Endpoint:

`GET /get_contraction_list`

#### Query Parameters:

`lang: The language code (en, ar, fr) key: YOUR_API_KEY`

#### Response:

`[ { "word": "Word", "contraction": "Contraction", "braille": "Braille representation" }, ... ]`

### 7\. Get Search Options

Retrieves a list of available search options.

#### Endpoint:

`GET /get_search_options`

#### Query Parameters:

`key: YOUR_API_KEY`

#### Response:

`[ { "code": "text", "name": "Search by Text" }, { "code": "braille", "name": "Search by Braille" } ]`
