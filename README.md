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
git clone https://github.com/ebrahimhossaincse/Automated-Testing-of-Rest-Booking-API-with-Newman-Report.git
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

---

### 💡 Contribution
Feel free to fork this repository and submit pull requests for improvements.
