YouTube-Data-Harvesting-and-Warehousing-using-SQL-MongoDB-and-Streamlit.

Problem Statement: The problem statement is to create a Streamlit application that allows users to access and analyze data from multiple YouTube channels.

NAME : Ponsabareeswari shanmugam

BATCH: D78D79

DOMAIN : DATA SCIENCE

The application should have the following features:

$ Ability to input a YouTube channel ID and retrieve all the relevant data (Channel name, subscribers, total video count, playlist ID, video ID, likes, dislikes, comments of each video) using Google API.

$ Option to store the data in a MongoDB database as a data lake. Ability to collect data for up to 10 different YouTube channels and store them in the data lake by clicking a button. Option to select a channel name and migrate its data from the data lake to a SQL database as tables.

$ Ability to search and retrieve data from the SQL database using different search options, including joining tables to get channel details.

$ YouTube API: You'll need to use the YouTube API to retrieve channel and video data. You can use the Google API client library for Python to make requests to the API.

$ Store data in a MongoDB data lake: Once you retrieve the data from the YouTube API, you can store it in a MongoDB data lake. MongoDB is a great choice for a data lake because it can handle unstructured and semi-structured data easily.

$ Migrate data to a SQL data warehouse: After you've collected data for multiple channels, you can migrate it to a SQL data warehouse. You can use a SQL database such as MySQL or PostgreSQL for this.

$ Query the SQL data warehouse: You can use SQL queries to join the tables in the SQL data warehouse and retrieve data for specific channels based on user input. You can use a Python SQL library such as SQLAlchemy to interact with the SQL database.

$ Display data in the Streamlit app: Finally, you can display the retrieved data in the Streamlit app. Overall, this approach involves building a simple UI with Streamlit, retrieving data from the YouTube API, storing it in a MongoDB data lake, migrating it to a SQL data warehouse, querying the data warehouse with SQL, and displaying the data in the Streamlit app.

Importing Necessary Modules:
Libraries and tools required to run the application are imported. These include pandas for data manipulation, plotly for visualization, Streamlit for the web interface, connectors for MySQL and MongoDB for data storage, and the YouTube API client.

Setting Page Configurations:
st.set_page_config() sets properties of the Streamlit app, such as title, layout, and initial sidebar state.

Creating Option Menu with Streamlit:
Using the option_menu function (which seems to be a third-party plugin for Streamlit not included in the code), a sidebar is created that lets the user navigate between different sections of the app.

Database Connections:

A connection to a MongoDB database named youtube_data on a local instance is established.
A connection to a MySQL database with similar credentials is also established.
Connecting to YouTube API:
The YouTube API is initialized using the provided API key.

Data Extraction Functions:
There are four functions to extract data from YouTube:

get_channel_details: Fetches details of a specific channel.
get_channel_videos: Fetches video IDs of all videos in a channel.
get_video_details: Fetches detailed information about specific videos.
get_comments_details: Fetches comment details for a given video.
Function to Get Channel Names from MongoDB:
The channel_names function retrieves channel names that have been stored in MongoDB.

Home Page (Streamlit UI):
If the "Home" option is selected from the sidebar, it displays an introduction to the application.

Data Transformation Function:
prepare_data_for_mysql function is designed to convert the raw data from YouTube API to a format that can be inserted into a MySQL database.

Extract & Transform Page (Streamlit UI):
In this section, users can input a YouTube Channel ID to extract its data. The extracted data is then shown in a table, and users can choose to upload this data to MongoDB. In the Transform tab, users can pick a channel from MongoDB, transform its data, and then upload it to MySQL.

View Page (Streamlit UI):
This section offers users several predefined questions to get insights from the stored data. When a question is chosen, the relevant SQL query is executed, and the results are displayed.

Overall, the code provides a full cycle of data handling, starting from extraction from YouTube, warehousing in MongoDB, transformation, then moving to MySQL, and finally, offering a querying interface through Streamlit.

Contributions are welcome! 
Thank you!!





