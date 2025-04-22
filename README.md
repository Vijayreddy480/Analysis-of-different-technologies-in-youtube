# Analysis-of-different-technologies-in-youtube
Analyzing the different technologies and different programming languages on youtube 
Data Collected through Youtube Api v3 
Data columns Consists Of 
Views
- Likes
- Subscriber Count
- Video Length
- Publish Date
- Channel Name

- API Used: YouTube Data API v3.

Implementation Details:
- API Request Setup:- Used the requests library to send GET requests to the YouTube search API.
- Passed parameters like q="Python programming", maxResults=50, and part="snippet".
- Extracted video IDs from the response.

- Fetching Video Statistics:- Used videos().list() to retrieve views, likes, duration, and other metrics based on extracted video IDs.

- Data Processing:- Converted API response into a structured DataFrame (pandas).
- Filtered results dynamically to refine data extraction.

- Challenges Encountered:- KeyError: 'videoId' issue resolved by filtering out non-video results.
- Handling API pagination for retrieving 500+ results.
- Error-handling strategies for invalid API keys or rate limits.
