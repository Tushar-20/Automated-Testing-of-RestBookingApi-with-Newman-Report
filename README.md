# Automated-Testing-of-RestBookingApi-with-Newman-Report
This project demonstrates API testing using Postman, providing a collection of tests to validate various endpoints of the API.
## Features

- ✅ Comprehensive test cases for **GET, POST, PUT, DELETE** requests  
- ✅ Organized test collection covering multiple API endpoints  
- ✅ Configurable **environment setup** for easy switching between different environments  
- ✅ **Pre-request scripts** for dynamic data setup before executing requests  
- ✅ **Test scripts** for automated assertions and response validations
# API Testing with Postman & Newman

This project demonstrates API testing using **Postman** and **Newman**, providing an automated way to validate various API endpoints with detailed reporting.

## 📄 API Documentation
[View API Documentation](https://documenter.getpostman.com/view/13082503/2sA2xmUAJ1)

## 🚀 Technologies Used
- **Postman** – API testing tool
- **Newman** – Command-line runner for Postman collections
- **Newman HTML Report Library** – For generating detailed test reports

## 📌 Prerequisites
Ensure you have the following installed before proceeding:
- **Node.js** (Download from [Node.js Official Site](https://nodejs.org/))
- **Newman** (for running collections from CLI)
- **Newman HTML Report Library** (for generating test reports)

## 🔧 Installation
### 1️⃣ Install Postman
If you haven’t already, [download and install Postman](https://www.postman.com/downloads/).

### 2️⃣ Clone the Repository
```sh
git clone https://github.com/Tushar-20/Automated-Testing-of-RestBookingApi-with-Newman-Report.git
cd Automated-Testing-of-Rest-Booking-API-with-Newman-Report
```

### 3️⃣ Import the Postman Collection
1. Open **Postman**.
2. Click on the **Import** button.
3. Select and import the collection file from the cloned repository.

### 4️⃣ Import the Postman Environment
1. In **Postman**, click on the **gear icon** in the top right corner.
2. Select **Import** and choose the environment file.

## ⚙️ Newman & Report Installation
### Install Newman
```sh
npm install -g newman
```
### Install Newman HTML Report Library
```sh
npm install -g newman-reporter-htmlextra
```

## 🛠 Usage
### 1️⃣ Select Environment
- In **Postman**, select the appropriate environment (e.g., Development, Production) from the top-right dropdown.

### 2️⃣ Run the Collection
- Select the imported collection from the **Collections** sidebar.
- Click the **Runner** button to open the Collection Runner.
- Choose the desired environment.
- Click **Start Test** to execute the collection.

### 3️⃣ View Results
- Once the tests are complete, view the results in the **Runner** tab.
- Detailed test results can be inspected for each request.
## 📝 Testing
### Test Case Scenarios:

#### 1️⃣ Create New Booking
**Request URL:** `https://restful-booker.herokuapp.com/booking/`  
**Request Method:** `POST`

**Pre-request Script:**
```javascript
var firstName = pm.variables.replaceIn("{{$randomFirstName}}")
pm.environment.set("firstName", firstName)
console.log("First Name Value "+firstName)

var lastName = pm.variables.replaceIn("{{$randomLastName}}")
pm.environment.set("lastName", lastName)
console.log("Last Name Value "+lastName)

var totalPrice = pm.variables.replaceIn("{{$randomInt}}")
pm.environment.set("totalPrice", totalPrice)
console.log(totalPrice)

var depositPaid = pm.variables.replaceIn("{{$randomBoolean}}")
pm.environment.set("depositPaid", depositPaid)
console.log(depositPaid)

const moment = require('moment')
const today = moment()
pm.environment.set("checkin", today.add(1,'d').format("YYYY-MM-DD"))
pm.environment.set("checkout",today.add(5,'d').format("YYYY-MM-DD"))

var additionalNeeds = pm.variables.replaceIn("{{$randomNoun}}")
pm.environment.set("additionalNeeds", additionalNeeds)
```

**Request Body:**
```json
{
    "firstname" : "{{firstName}}",
    "lastname" : "{{lastName}}",
    "totalprice" : {{totalPrice}},
    "depositpaid" : {{depositPaid}},
    "bookingdates" : {
   	  "checkin" : "{{checkin}}",
   	  "checkout" : "{{checkout}}"
    },
    "additionalneeds" : "{{additionalNeeds}}"
}
```

**Response Body:**
```json
{
    "bookingid": 4334,
    "booking": {
        "firstname": "Joelle",
        "lastname": "Krajcik",
        "totalprice": 266,
        "depositpaid": true,
        "bookingdates": {
            "checkin": "2024-03-15",
            "checkout": "2024-03-20"
        },
        "additionalneeds": "monitor"
    }
}
```
---

### 💡 Contribution
Feel free to fork this repository and submit pull requests for improvements.
