# Smartpad Automation Project

This repository contains an end-to-end **Selenium + Java + TestNG automation framework** for testing the **Smartpad Customer Feedback** web application.

Website under test: [https://smartpad-customer-feedback.vercel.app](https://smartpad-customer-feedback.vercel.app)

The framework follows **Page Object Model (POM)** design with **explicit waits**, making it scalable and maintainable.

---

## 1. Tech Stack

* **Programming Language:** Java (11+)
* **Automation Tool:** Selenium WebDriver 4
* **Test Framework:** TestNG
* **Build Tool:** Maven
* **Design Pattern:** Page Object Model (POM)
* **Browser:** Google Chrome
* **Driver Management:** WebDriverManager

---

## 2. Project Structure

```
SMARTPAD-AUTOMATION
 ├── src
 │   ├── main/java
 │   │   ├── pages
 │   │   │   ├── BasePage.java
 │   │   │   ├── HomePage.java
 │   │   │   ├── OptionsPage.java
 │   │   │   ├── BrowsePage.java
 │   │   │   └── SearchPage.java
 │   │   └── utils
 │   │       └── DriverFactory.java
 │   └── test/java/tests
 │       └── SmartpadFlowTest.java
 ├── pom.xml
 └── testng.xml
```

---

## 3. Prerequisites

Ensure the following are installed on your system:

1. **Java JDK 11 or higher**

   ```bash
   java -version
   ```

2. **Maven**

   ```bash
   mvn -version
   ```

3. **Google Chrome (latest version)**

4. **IDE** (Recommended)

   * IntelliJ IDEA
   * Eclipse
   * VS Code (with Java & Maven extensions)

---

## 4. Project Setup

### Step 1: Clone the Repository

```bash
git clone <repository-url>
cd smartpad-automation
```

---

### Step 2: Import Project into IDE

* Open IDE
* Select **Open Existing Project**
* Choose the project root folder
* Wait for Maven dependencies to download

---

### Step 3: Verify Dependencies

Ensure all dependencies are resolved by running:

```bash
mvn clean install
```

If build is successful, the setup is complete.

---

## 5. Test Scenario Automated

The automation covers the following flow:

1. Open Smartpad website
2. Click **Get Started** on Home Page
3. Select **Others** option
4. Click **Continue without an account**
5. Search for **"wine"** in the search bar

---

## 6. Running the Tests

### Option 1: Run via Maven (Recommended)

From project root directory:

```bash
mvn clean test
```

This will:

* Launch Chrome browser
* Execute TestNG suite (`testng.xml`)
* Run the Smartpad end-to-end flow

---

### Option 2: Run via TestNG XML

1. Right-click on `testng.xml`
2. Select **Run as TestNG Suite**

---

### Option 3: Run via Test Class

1. Open `SmartpadFlowTest.java`
2. Right-click → **Run**

---

## 7. Browser & Wait Strategy

* **Explicit waits** are used via `WebDriverWait`
* No `Thread.sleep()` is used
* Synchronization handled in `BasePage`

---

## 8. Key Framework Highlights

* Page Object Model (POM)
* Centralized driver management
* Reusable BasePage methods
* Clean separation of test logic and UI logic
* Easy to extend for reports, CI/CD, and parallel execution

---

## 9. Common Issues & Fixes

### ChromeDriver Version Issue

This project uses **WebDriverManager**, so no manual ChromeDriver setup is required.

---

### Element Not Found Exception

* Ensure stable internet connection
* Verify XPath if UI changes
* Increase wait time in `DriverFactory` if needed

---

## 10. Future Enhancements (Optional)

* Extent / Allure Reporting
* Parallel execution
* Jenkins CI integration
* Headless browser execution
* Retry logic for flaky tests
* API + UI hybrid testing

---

## 11. Author
Kangkan Pathak
**QA Automation Engineer**
Java | Selenium | TestNG | Maven

---

## 12. Conclusion

This framework is suitable for:

* Real-world automation projects
* Interview demonstrations
* Scalable test automation needs


