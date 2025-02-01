# Soccer Stats API

This project demonstrates building a simple RESTful API for retrieving soccer statistics using FastAPI and Docker. The API fetches real-time data from the RapidAPI Football API.

## Key Features

- **Data Source:** Utilizes the RapidAPI Football API to fetch real-time soccer data.
- **Endpoints:**
  - `/player/{player_id}`: Retrieves player statistics for a given player ID.
  - `/topscorers/{league_id}`: Retrieves top scorers for a specified league.
- **FastAPI:** Leverages the FastAPI framework for efficient API development.
- **Dockerized:** Containerizes the application using Docker for easy deployment and portability.

## Project Structure

soccer-stats-docker/
├── src/
│   ├── init.py
│   └── soccer_stats.py
├── tests/
│   └── test_soccer_stats.py
├── Dockerfile
├── requirements.txt
├── README.md
├── .env
├── .gitignore

**Getting Started:**

### Step 1: Create a RapidAPI Account

- **Sign Up:** Create an account on [RapidAPI](https://rapidapi.com/).
- **Find the API:** Search for and select the **Football API** within the RapidAPI marketplace.
- **Subscribe:** Click the **Subscribe** button to gain access.
- **Obtain Your API Key:** Retrieve your unique API Key from your RapidAPI account dashboard.

### Step 2: Clone the Repository

Clone the GitHub repository to your local machine:

```bash
git clone https://github.com/danielhensha2/soccer-stats-app.git
cd soccer-stats-app
```

### Step 3: Environment Variables
Create a .env file in the project root and add your RapidAPI key:

```bash
RAPID_API_KEY=your_api_key_here
```

Note: Replace your_api_key_here with your actual RapidAPI key.
Also, ensure that the .env file is added to your .gitignore to prevent accidental exposure of sensitive information

### Step 4: Build and Run the Docker Image
**Build the Docker image:**

```bash
docker build -t soccer-stats .
```
**Run the Docker container:**
```bash
docker run -p 8000:8000 --env-file .env soccer-stats
```

### Step 5: Test the API
Open your web browser and navigate to **http://localhost:8000** to see the API in action. You can also use Postman or any API testing tool to interact with the endpoints

### Step 6: Clean Up Resources
When you're done testing, you can stop and remove the Docker containers with the following commands:

```bash
docker stop $(docker ps -q --filter ancestor=soccer-stats)
docker rm $(docker ps -aq --filter ancestor=soccer-stats)
```
Optionally, remove the Docker image:

```bash
docker rmi soccer-stats
```

### Conclusion
This project demonstrates a fundamental Soccer Stats API using FastAPI and Docker, leveraging the RapidAPI Football API to access real-time soccer statistics. Future improvements may include:
**Adding endpoints for team data, match timetables, live scores, etc.**
**Implementing more robust error handling and caching mechanisms.**
**Deploying the Dockerized app on cloud platforms like AWS, Azure, or Google Cloud for enhanced scalability and accessibility.***

**Connect with me on Linkedin: www.linkedin.com/in/daniel-osarobo**
**Read the full story on medium: https://medium.com/@danielosarobo/deploying-a-soccer-stats-api-with-fast-api-docker-369013b979fe**


## THANK YOU VERY MUCH ##