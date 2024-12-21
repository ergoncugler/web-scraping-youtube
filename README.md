# **YouTubeScrap: A comprehensive tool for scraping YouTube data and transcripts**

This code ([**available here on Github**](https://github.com/ergoncugler/web-scraping-youtube/blob/main/YouTubeScrap_A_comprehensive_tool_for_scraping_YouTube_data_and_transcript.ipynb) */or/* [**directly on Google Colab, just play it**](https://colab.research.google.com/drive/1W5tGxzvJetiNAXm-f5fU7hQ67bvmFm7i?usp=sharing)) was developed by [**Ergon Cugler de Moraes Silva**](https://github.com/ergoncugler) and [**Isabela Rocha**](https://github.com/rocha-isabela). It aims to **facilitate the extraction, analysis, and organization of YouTube video data and transcripts**. The tool is designed to extract detailed information from videos based on links, custom searches, and metadata, storing the results directly in Google Sheets. Key features include extracting video metrics (e.g., `title, views, likes, duration, channel details`), processing `video transcripts` (when available), and performing searches filtered by date ranges. This code is particularly useful for researchers, analysts, and content creators looking to gather and analyze YouTube data systematically and efficiently.

Designed to operate within Google Colab, YouTubeScrap leverages cloud-based infrastructure to eliminate installation barriers, offering a **ready-to-use environment suitable for users with varying technical expertise**. All extracted data is organized in Google Sheets, ensuring compliance with international data privacy standards while facilitating collaboration and analysis. In a time of increasing restrictions on online data access, YouTubeScraper’s key-free functionality **democratizes data collection**, supporting research in academic, media, and communication fields. It provides a scalable, ethical, and user-friendly solution for engaging with large-scale digital content, promoting innovation in the growing field of Computational Social Sciences.

The code can collect the following metadata from the listed YouTube videos: 1. `Link`, 2. `ID`, 3. `Title`, 4. `Full Title`, 5. `Description`, 6. `Channel Name`, 7. `Channel ID`, 8. `Channel URL`, 9. `Timestamp`, 10. `Publish Date`, 11. `Channel Name (Alt)`, 12. `Channel ID (Alt)`, 13. `Channel URL (Alt)`, 14. `Subscribers`, 15. `Is Verified`, 16. `Location`, 17. `Length (s)`, 18. `Views`, 19. `Likes`, 20. `Dislikes`, 21. `Reposts`, 22. `Comments`, 23. `Tags`, 24. `Thumbnail`, 25. `Transcript`.

### Output example:
✅ It was requested to scrape 10 videos with the query `'presidente lula' -bolsonaro -eleição` and 10 videos with the query `'election usa' -biden -kamala -trump`, and then we got the following result:

![image](https://github.com/user-attachments/assets/46a22def-1f71-4c3f-88be-5f73c0cd42bc)

___
## Recommendation

### [Data] [Academic Research] [Scientific Research] [Public Policy] [Political Science] [Data Science]

Its use is highly encouraged and recommended for academic and scientific research, content analysis, sentiment analysis, and speech analysis. While it is free to use and modify, the responsibility for its use and any modifications lies with the user. Feel free to explore, utilize, and adapt the code to suit your needs, but please ensure you comply with Telegram's terms of service and data privacy regulations. This tool is released under a free and open-source license. When using or modifying the tool, please ensure to provide appropriate credit and citation. Referencing the tool in your research is appreciated and contributes to its continued development and improvement.
___

## Steps

| Tips |
|------|
| **1.** You **do not need to run all the steps**. The workflow is flexible and allows for selective execution. |
| **2.** You can manually add links to the spreadsheet and request only transcript extraction. |
| **3.** Alternatively, you can extract only video metrics without fetching transcripts. |
| **4.** Each step is **interdependent**, meaning you can mix and match tasks to suit your specific needs. For example, if you are only interested in collecting transcripts, skip Step 2 and Step 3 entirely. |

### 1. [ Required ] Create or load a Google Sheet

**This cell is required and must be run first** to initialize the Google Sheet used for storing data. It will either:
1. Create a new Google Sheet `sheet_name` with predefined columns, or
2. Load an existing sheet named in the `sheet_name` variable.

You will need to **authorize access to Google Drive** for this to work. This is secure, and no data will be exposed or shared beyond this script. Once run, a link to your worksheet will be provided. Without this step, subsequent cells will not work correctly, as you will not have the spreadsheet available to allocate metrics and transcripts.

![image](https://github.com/user-attachments/assets/3f1c9417-4919-4ffb-9525-fa1a4bf98974)

![image](https://github.com/user-attachments/assets/a01fcd2c-762c-45e0-8d1c-4e03914e1921)

### 2. [ Optional ] Search YouTube videos and save links

**This step is optional if you prefer to add links manually in the sheet.** Use this cell to **search YouTube videos** based on up to 5 queries and save their links in the Google Sheet.
- Define search terms in `query_1`, `query_2`, etc. Use operators like `-` to exclude terms (e.g., `'election -trump'`).
- Set `max_results` to limit the number of videos fetched per query (default: 10).
- Use `start_date` and `end_date` to restrict the search to a specific date range. Leave these blank to fetch all available videos.

![image](https://github.com/user-attachments/assets/f3477db1-5268-4b93-8402-6beb11a69fc0)

![image](https://github.com/user-attachments/assets/b0362307-03a0-4148-af29-266a1fe7001d)

### 3. [ Optional ] Extract metrics from videos *(with the worksheet already created in Step 1 and links either inserted manually or added in Step 2)*

Run this cell to **extract metadata** for video links stored in the Google Sheet. Data such as `title`, `views`, `likes`, `channel name`, and `upload date` will be automatically fetched and added to their respective columns. The script processes only links without existing metadata, ensuring efficient updates. Make sure the Google Sheet contains valid YouTube links in the `Link` column before running this cell.

![image](https://github.com/user-attachments/assets/230140b9-73a7-4045-91de-d4cbf53e2656)

![image](https://github.com/user-attachments/assets/46a22def-1f71-4c3f-88be-5f73c0cd42bc)

### 4. [ Optional ] Extract video transcripts *(with the worksheet already created in Step 1 and links either inserted manually or added in Step 2)*

Use this cell to retrieve **video transcripts** (if available) in supported languages like `English`, `Spanish`, and `Portuguese`. Transcripts will be added to the `Transcript` column in the Google Sheet. If no transcript is found, the entry will be marked as `[no subtitles]`. The script processes only rows without existing transcripts, skipping completed entries.

![image](https://github.com/user-attachments/assets/486e95e4-2cd9-48b2-badb-5e63f04e2d8a)

![image](https://github.com/user-attachments/assets/c0ab5519-1ee8-4a52-82a6-fcc00e60ae7f)

## Key Features

1. **Automated Worksheet Setup**: Automatically creates or loads a Google Sheet with predefined column headers to structure the extracted data.
2. **YouTube Video Search**: Performs searches based on user-defined queries, filtering results by date ranges and limits, and saves video links directly to the worksheet.
3. **Video Metrics Extraction**: Processes video links to gather detailed metadata, including channel name, subscriber count, views, likes, tags, upload date, and more.
4. **Transcript Extraction**: Retrieves video transcripts (in multiple languages) and adds them to the worksheet for content analysis.

All data is stored directly in a Google Sheet, making it accessible, shareable, and ready for further processing. Integration with tools such as `yt_dlp` and `YouTubeTranscriptAPI` ensures accuracy and flexibility, while handling large datasets efficiently.

---

## Data Storage Format

All extracted data is organized into a Google Sheet with predefined columns, including:

- **Video Details**: Title, description, tags, video link, thumbnail, duration.
- **Channel Information**: Name, ID, URL, subscriber count, verification status.
- **Video Metrics**: Views, likes, dislikes, reposts, comments.
- **Transcripts**: Stored as full text in the "Transcript" column when available.

---

## Applications and Use Cases

The **YouTubeScrap** offers a wide range of applications:

1. **Academic Research**: Analyzing public discourse, studying misinformation, or exploring media trends on YouTube.
2. **Media Analysis**: Extracting engagement metrics and channel growth insights for journalists and media professionals.
3. **Social Science and Communication Studies**: Studying digital communities, content production, or propaganda on YouTube platforms.
4. **Marketing and Content Creation**: Gathering insights on competitor performance, video optimization, and viewer engagement.

---

## Unique Advantages

- Seamless integration with Google Sheets for easy data sharing and processing.
- Automatic transcript extraction in multiple languages, including English, Portuguese, and Spanish.
- Scalable tools such as `yt_dlp`, ensuring support for modern video formats and metadata.
- Efficient handling of large datasets, avoiding manual extraction limitations.

---

___

## Authors info:

Ergon Cugler de Moraes Silva, from Brazil, mailto: [contato@ergoncugler.com](contato@ergoncugler.com) / Founded Researcher at the Brazilian Institute of Information in Science and Technology (IBICT). Graduated in Public Policy Management (USP) and Postgraduate in Data Science & Analytics (USP) and Master in Public Administration and Government (FGV). More info at: [http://ergoncugler.com/](http://ergoncugler.com/).

Isabela Rocha, from Brazil, mailto: [isabelarocha.contato@gmail.com](isabelarocha.contato@gmail.com) / Isabela Rocha is a Master of Science and PhD Candidate at the Institute of Political Science of the University of Brasília (IPOL-UnB). Coordinator of the Working Group on Strategy, Data and Sovereignty of the Study and Research Group on International Security of the Institute of Foreign Affairs of the University of Brasília (GEPSI IREL-UnB). Member of the Public Information and Elections Research Group at the Institute of Political Science of the University of Brasília (IPê UnB), the Research Laboratory in Political Behavior, Institutions, and Public Policies (LAPCIPP) and the International Political Science Association 50th Research Committee on the Politics of Language (IPSA RC50). Brasília, Federal District, Brazil. Web site: https://www.rochaisabela.com/. More info at: [https://www.rochaisabela.com/](https://www.rochaisabela.com/).

## How to cite it:

**SILVA, Ergon Cugler de Moraes; ROCHA, Isabela. *YouTubeScrap: A comprehensive tool for scraping YouTube data and transcript*. (Dec) 2024. Available at: [https://github.com/ergoncugler/web-scraping-youtube](https://github.com/ergoncugler/web-scraping-youtube).**
