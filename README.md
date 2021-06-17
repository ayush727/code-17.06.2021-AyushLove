# BMI CALCULATOR 

**Version 1.0.0**

This project demonstrates ACalculation of BMI. 
It will enlight users on the concepts of Connecting to database (mongoDB), Setting up the middleware using Express.js, Use of functions for calculation and Writing test cases.

## Steps for running the APIs :
1. Make sure you have mongoDB installed in your system.
2. Run the following command from the mongoDB bin directory to make sure mongoDB server is running:
    mongo
3. Import the folder structure in Visual Studio Code.
4. Make sure all the dependencies and modules are installed using the following command:
    npm install --save
5. To run the APIs, run the following command from the terminal:
    npm start
6. To run the test cases, run the following command:
    npm test

## API Calls :

ADD A NEW USER AND CALCULATE THE BMI : 
URL ---- http://localhost:3000/calculatebmi
Method ---- POST
Payload ---- 
{
    "Gender":"Female",
    "Height":170,
    "Weight":80
}
Response ---- 
{
    "_id": "60c630d574087f044886de23",
    "Gender": "Female",
    "HeightCm": 170,
    "WeightKg": 80,
    "BMI": 27.68,
    "BMI_Category": "Overweight",
    "Health_Risk": "Enhanced risk",
    "__v": 0
}

CALCULATING BMI OF ALL THE USERS IN THE DATABASE :
URL ---- http://localhost:3000/usersbmi
Method ---- POST
Response ----
[
    {
        "_id": "60c630d574087f044886de23",
        "Gender": "Female",
        "HeightCm": 170,
        "WeightKg": 80,
        "BMI": 27.68,
        "BMI_Category": "Overweight",
        "Health_Risk": "Enhanced risk",
        "__v": 0
    }
]

COUNTING THE NUMBER OF USERS FOR A SPECIFIC CATEGORY :
URL ---- http://localhost:3000/count/Overweight
Method ---- GET
Response ----
{
    "Count": 4
}

