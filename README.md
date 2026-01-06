# YouTube Transcript Summarizer (Generative AI Internship)

> Small Python pipeline to fetch YouTube transcripts and produce a concise summary using a Hugging Face summarization model.

## Overview
This project extracts the transcript of a YouTube video, splits the text into chunks that fit model limits, summarizes each chunk with a pretrained transformer (facebook/bart-large-cnn), and combines chunk summaries into a final summary.

It was built as part of an LLM / Generative AI internship to practice data collection, preprocessing and using pretrained models from Hugging Face.

## Features
- Download transcript text from YouTube videos (English).
- Split long transcripts into model-safe chunks.
- Summarize each chunk using a Hugging Face pipeline.
- Combine chunk summaries into a single, readable final summary.
- Minimal, easy-to-run Python scripts for experimentation.

## Demo / Example
# Example usage (after installing requirements)
python summarize_youtube.py "https://www.youtube.com/watch?v=iG9CE55wbtY"
# Outputs:
summary.txt — combined summary of the video.

## Implementation notes & limitations
- Current chunking uses a character-based approach; token-based chunking (e.g., using tokenizer) is more robust.
- The script requests English transcripts; videos without English transcripts will raise an error.
- Running facebook/bart-large-cnn locally requires enough RAM/VRAM; consider smaller models for a personal laptop.
