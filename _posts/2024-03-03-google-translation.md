---
title: Using Google Cloud Translation
author: derek
date: 2024-03-03 08:55:00 -0400
categories: [Advanced]
tags: [advanced-configuration, translation, google]
permalink: /google-translation/
---

## Configuration

Trucaption can be configured to translate captured text into other languages using Google Cloud Translation. 

To use Google Cloud Translation, you will need:

- A [Google Cloud](https://console.cloud.google.com/) account
- Cloud Translation API enabled in the Google Cloud APIs

To configure the Google Cloud account:

1. [Enable the Cloud Translation API](https://console.cloud.google.com/apis/library/translate.googleapis.com) for your Google Cloud project.
2. Switch to the [Credentials](https://console.cloud.google.com/apis/credentials) page.
3. Click "Create Credentials", then "API Key".
4. Copy and save the displayed API key.
5. Click the "Edit Key" link.
6. Under "API Restrictions", click "Restrict Key".
7. Select "Cloud Translation API" in the selection window.
8. Click "Save".

Once you have created your API key, configure Trucaption for translation:

1. Within the editor window, click Settings, then Translation.
2. Enable Translation.
3. Paste the API key from the Google Console into the API Key box.
4. Select an option for "Translate Interim Transcripts":
    - Enabled: Trucaption will translate the word-by-word transcripts. Warning: this will significantly increase the translation API usage.
    - Disabled: Trucaption will only translate final transcripts. This will delay the translation, but can increase accuracy and will reduce API usage.
5. Add languages for translation using the drop-down and "Add Language" button.
