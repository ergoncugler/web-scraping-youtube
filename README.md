# **YouTubeScrap: A comprehensive tool for scraping YouTube data and transcripts**

This code ([**available on GitHub**](https://github.com/ergoncugler/web-scraping-youtube) or [**directly executable on Google Colab**](https://colab.research.google.com/drive/1W5tGxzvJetiNAXm-f5fU7hQ67bvmFm7i?usp=sharing)) was developed by [**Ergon Cugler de Moraes Silva**](https://github.com/ergoncugler) and [**Isabela Rocha**](https://www.linkedin.com/in/rocha-isabela/). It aims to **facilitate the extraction, analysis, and organization of YouTube video data and transcripts**. The tool is designed to extract detailed information from videos based on links, custom searches, and metadata, storing the results directly in Google Sheets. Key features include extracting video metrics (e.g., `title, views, likes, duration, channel details`), processing `video transcripts` (when available), and performing searches filtered by date ranges. This code is particularly useful for researchers, analysts, and content creators looking to gather and analyze YouTube data systematically and efficiently.

Designed to operate within Google Colab, YouTubeScrap leverages cloud-based infrastructure to eliminate installation barriers, offering a **ready-to-use environment suitable for users with varying technical expertise**. All extracted data is organized in Google Sheets, ensuring compliance with international data privacy standards while facilitating collaboration and analysis. In a time of increasing restrictions on online data access, YouTubeScraper’s key-free functionality **democratizes data collection**, supporting research in academic, media, and communication fields. It provides a scalable, ethical, and user-friendly solution for engaging with large-scale digital content, promoting innovation in the growing field of Computational Social Sciences.

---

## **Key Features**

1. **Automated Worksheet Setup**: Automatically creates or loads a Google Sheet with predefined column headers to structure the extracted data.
2. **YouTube Video Search**: Performs searches based on user-defined queries, filtering results by date ranges and limits, and saves video links directly to the worksheet.
3. **Video Metrics Extraction**: Processes video links to gather detailed metadata, including channel name, subscriber count, views, likes, tags, upload date, and more.
4. **Transcript Extraction**: Retrieves video transcripts (in multiple languages) and adds them to the worksheet for content analysis.

All data is stored directly in a Google Sheet, making it accessible, shareable, and ready for further processing. Integration with tools such as `yt_dlp` and `YouTubeTranscriptAPI` ensures accuracy and flexibility, while handling large datasets efficiently.

---

## **Data Storage Format**

All extracted data is organized into a Google Sheet with predefined columns, including:

- **Video Details**: Title, description, tags, video link, thumbnail, duration.
- **Channel Information**: Name, ID, URL, subscriber count, verification status.
- **Video Metrics**: Views, likes, dislikes, reposts, comments.
- **Transcripts**: Stored as full text in the "Transcript" column when available.

---

## **Applications and Use Cases**

The **YouTubeScrap** offers a wide range of applications:

1. **Academic Research**: Analyzing public discourse, studying misinformation, or exploring media trends on YouTube.
2. **Media Analysis**: Extracting engagement metrics and channel growth insights for journalists and media professionals.
3. **Social Science and Communication Studies**: Studying digital communities, content production, or propaganda on YouTube platforms.
4. **Marketing and Content Creation**: Gathering insights on competitor performance, video optimization, and viewer engagement.

---

## **Unique Advantages**

- Seamless integration with Google Sheets for easy data sharing and processing.
- Automatic transcript extraction in multiple languages, including English, Portuguese, and Spanish.
- Scalable tools such as `yt_dlp`, ensuring support for modern video formats and metadata.
- Efficient handling of large datasets, avoiding manual extraction limitations.

---

## **How to Cite the Code**

**SILVA, Ergon Cugler de Moraes; ROCHA, Isabela. *Web Scraping YouTube Metrics and Transcription*. (Dec) 2024. Available at: [https://github.com/ergoncugler/web-scraping-youtube](https://github.com/ergoncugler/web-scraping-youtube).**
