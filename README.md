# Employee Salary Slip API

A REST API built using Node.js, Express.js, and MySQL for generating employee salary slips from an HRMS database.

## Features

* Retrieve employee salary slip by employee ID and month
* View basic salary and final salary
* View attendance details
* View salary allowances
* View salary deductions
* MySQL database integration
* RESTful API architecture

## Tech Stack

* Node.js
* Express.js
* MySQL
* REST API
* Postman
* Git & GitHub

## API Endpoint

### Get Employee Salary Slip

GET /salaryslip/:employeeId/:month

### Example Request

GET /salaryslip/21/2024-11

### Sample Response

```json
{
  "employeeId": 21,
  "employeeName": "Avduth Kemble",
  "month": "2024-11",
  "basicSalary": "9500",
  "finalSalary": "5502.00",
  "presentDays": "13",
  "monthlyDays": 30,
  "allowances": [
    {
      "allowancename": "Basic + Special Allowance",
      "ssallowanceamount": "4117"
    },
    {
      "allowancename": "HRA",
      "ssallowanceamount": "412"
    }
  ],
  "deductions": [
    {
      "deductionname": "EPF Deduction",
      "ssdeductionamount": "894"
    },
    {
      "deductionname": "ESIC Deduction",
      "ssdeductionamount": "56"
    }
  ]
}
```

## Database Tables Used

* employee
* salaryslip
* salaryslip_allowance
* salaryslip_deduction
* allowance
* deduction

## Project Structure

employee-salary-slip-api

├── routes
│   └── salaryslip.js
│
├── db.js
├── server.js
├── package.json
└── README.md

## How to Run

### 1. Clone the Repository

```bash
git clone <repository-url>
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Configure Database

Update database credentials in:

```text
db.js
```

### 4. Start Server

```bash
node server.js
```

### 5. Test API

```http
http://localhost:3000/salaryslip/21/2024-11
```

## API Output

The API returns:

* Employee Information
* Salary Month
* Basic Salary
* Final Salary
* Present Days
* Monthly Days
* Salary Allowances
* Salary Deductions

## Author

Aryan Thakur
# employee-salary-slip-api
REST API built with Node.js, Express.js, and MySQL to generate employee salary slips, including salary details, allowances, deductions, attendance information, and final payable salary.
