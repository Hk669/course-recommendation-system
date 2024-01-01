# Course Recommender System

## Overview

This Python application serves as a basic course recommender system based on content-based filtering. It uses the Flask framework to create a web service that recommends courses to users based on their specified interests.

## Features

- **Recommendations Endpoint:** The `/recommendations` endpoint accepts a `user's email` as a query parameter, retrieves their interests from a MongoDB database, and generates course recommendations using `content-based filtering.`

- **Content-Based Filtering:** The recommender system uses `TF-IDF vectorization` and `cosine similarity` to calculate the relevance of courses to a user's interests.

- **MongoDB Integration:** User data and course information are stored in a `MongoDB` database, and the application leverages the pymongo library for database connectivity.

### Getting Started:

- Clone Repository:
    ```bash
    git clone https://github.com/Hk669/course-recommendation-system.git
    
    ```
- Star the Repository🌟
    - click on the `star` at the top right


### Create virtual environment

    ```bash
    cd recommendations

    python -m venv venv
    .venv/Scripts/activate

    pip install -r requirements.txt
    ```

### Run the Flask API on 5000 port:

    ```bash
    python course_recommender.py
    ```

### API Usage
- **Recommendations Endpoint:**
    - URL: `/recommendations`
    - Method: `GET`
    - Parameters:
    - user_email (query parameter): User's email for fetching interests.
    - Response: `JSON` object containing recommended courses.

  ```bash
  GET http://127.0.0.1:5000/recommendations?user_email=testuser@gmail.com

  ```

- **JSON Object :**
  ```bash
  {"recommendedCourses": [
      { 
        "_id": "657dfd8327bd4eeac3b160de",
        "title": "Web Development for Begineers", "description":
        "This is a brand new web dev course for beginners",
        "slug": "web-development-for-begineers",
        "domain": "web development",
        "owner": "657d96853c49dea888c6e47d",
        "coverImage":
        "https://s3.ap-south-1.amazonaws.com/assets.advantagecommunity.in/course/1702755707016.jpg",
        "instructors": [],
        "price":0,
        "totalLectures": 20,
        "enrolledStudents": [],
        "sections": [],
        "ratings": [],
            "createdAt":"2023-12-16T19:41:55.196000",
            "updatedAt": "2023-12-16T19:41:55.196000",
            "__v": 0
            }
        ]
    }
  ```

---

## License

This project is licensed under the [MIT License](LICENSE).

## Contact

If you have any queries, encounter issues, or need assistance, feel free to reach out to me.

**Email:** hrushikesh.dokala@studentambassadors.com


`i'd greatly appreciate recieving some feedback. Thank you`