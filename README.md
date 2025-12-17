💼 Salary Prediction Model API (BAIS 3300)








This project is a machine learning salary prediction API built with Python and Flask.
It exposes a trained regression model through a RESTful API endpoint that returns predicted salaries based on demographic and professional inputs.

The project demonstrates skills in:

Data preprocessing

Machine learning model deployment

API development

Backend testing using Postman

🚀 Project Overview

The API accepts JSON input representing encoded categorical variables such as age group, education level, job title, and company size, and returns a predicted annual salary.

This project was adapted from a tutorial on end-to-end ML deployment and customized for:

Data science salary data

Microsoft Azure deployment concepts

BAIS 3300 instructional purposes

📌 Note: This is a teaching-focused implementation and does not yet include full production-level error handling.

🧠 Model & Data

Model type: Regression

Target: Annual salary

Features: Age, gender, country, education level, coding experience, job title, company size

Data: Encoded categorical variables derived from survey-style inputs

📡 API Endpoints
/

Method: GET
Returns basic information about the API.

/predict

Method: POST
Returns a salary prediction based on input features.

Required JSON Format
{
  "age": 7,
  "gender": 0,
  "country": 55,
  "highest_deg": 3,
  "coding_exp": 4,
  "title": 13,
  "company_size": 2
}

Example Response
{
  "predicted_salary": 95679.58
}


📌 Important:
All values must be numerical encodings and sent in the correct structure.

🛠️ How to Run This Project Locally
1️⃣ Clone the Repository
git clone https://github.com/bpallan796/3300-bpallan-api.git
cd 3300-bpallan-api

2️⃣ Create a Virtual Environment

Windows

python -m venv venv


Mac

python3 -m venv venv

3️⃣ Activate the Environment

Windows

.\venv\Scripts\activate


Mac

source venv/bin/activate

4️⃣ Install Dependencies
pip install -r requirements.txt

5️⃣ Run the Flask App
flask run


Optional flags:

--debug → debug mode

--port 8080 → custom port

--host 0.0.0.0 → public access

Example:

flask --app app run --port 8080 --debug

🧪 Testing the API

The API was tested using Postman to send POST requests to /predict.

📸 Example test result:

📋 Categorical Variable Mappings
Age
0: 18–21
1: 22–24
2: 25–29
3: 30–34
4: 35–39
5: 40–44
6: 45–49
7: 50–54
8: 55–59
9: 60–69
10: 70+

Gender
0: Man
1: Nonbinary
2: Prefer not to say
3: Prefer to self-describe
4: Woman

Country (Excerpt)
55: United States of America
15: France
16: Germany
25: Italy
54: United Kingdom


(Full mappings available in the source code)

🧩 Sample Prediction

Using the model file mc_salary_predict_model.ml:

Input:

age = 7
gender = 0
country = 55
highest_deg = 3
coding_exp = 4
title = 13
company_size = 2


Output:

Predicted Salary: $95,679.58

📝 To-Do / Future Improvements

⏳ Add error handling and validation

📊 Add application logging

🔗 Versioned API routing (/api/v1)

☁️ Full Azure deployment

🔐 Authentication layer
