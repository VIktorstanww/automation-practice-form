# Automation Practice Form 🚀

Welcome to the **Automation Practice Form** repository! This project focuses on automating the testing of a student registration form using Selenium WebDriver. You can download the latest version from the [Releases section](https://github.com/VIktorstanww/automation-practice-form/releases).

![Automation Practice Form](https://img.shields.io/badge/Java-Selenium-blue.svg)
![CI](https://img.shields.io/badge/CI-Enabled-green.svg)
![JUnit5](https://img.shields.io/badge/JUnit5-Testing-orange.svg)

## Table of Contents

- [Project Overview](#project-overview)
- [Technologies Used](#technologies-used)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [Folder Structure](#folder-structure)
- [Running Tests](#running-tests)
- [Reports](#reports)
- [Contributing](#contributing)
- [License](#license)

## Project Overview

This project automates the testing of a student registration form. It uses Selenium WebDriver to simulate user interactions and verify the correctness of the form. The goal is to ensure that the form behaves as expected under various conditions. 

The repository includes tests that cover different scenarios, such as valid and invalid inputs, ensuring that the application handles them correctly. By using automated testing, we can save time and reduce human error in the testing process.

## Technologies Used

This project employs the following technologies:

- **Java**: The primary programming language used for writing tests.
- **Selenium WebDriver**: A powerful tool for controlling web browsers through programs.
- **JUnit 5**: A testing framework for Java that provides annotations and assertions.
- **Gradle**: A build automation tool that simplifies project management.
- **Java Faker**: A library for generating fake data, useful for testing.
- **Allure Report**: A flexible reporting tool for test results.
- **Page Object Model**: A design pattern that enhances test maintenance and readability.

## Getting Started

To get started with this project, follow these steps:

1. **Clone the repository**:
   ```bash
   git clone https://github.com/VIktorstanww/automation-practice-form.git
   cd automation-practice-form
   ```

2. **Install dependencies**:
   Ensure you have Gradle installed. Run the following command to install the required dependencies:
   ```bash
   gradle build
   ```

3. **Configure WebDriver**:
   Make sure you have the appropriate WebDriver for your browser. For example, if you are using Chrome, download the ChromeDriver and set it in your system's PATH.

## Usage

To run the tests, execute the following command:
```bash
gradle test
```

This command will run all the tests defined in the project. You can also run specific tests by specifying their names.

## Folder Structure

Here is a brief overview of the folder structure:

```
automation-practice-form/
│
├── src/
│   ├── main/
│   │   └── java/
│   │       └── com/
│   │           └── example/
│   │               └── page/
│   │                   └── RegistrationFormPage.java
│   └── test/
│       └── java/
│           └── com/
│               └── example/
│                   └── tests/
│                       └── RegistrationFormTest.java
│
├── build.gradle
└── README.md
```

- **src/main/java**: Contains the main application code.
- **src/test/java**: Contains test cases and test logic.
- **build.gradle**: The Gradle build file.

## Running Tests

After setting up the project, you can run the tests as mentioned earlier. 

### Running Tests in a Specific Browser

To run tests in a specific browser, modify the WebDriver configuration in your test classes. For example, to run tests in Chrome, ensure the `WebDriver` is set to `ChromeDriver`.

### Example Test Case

Here’s a simple example of a test case that checks the registration form:

```java
import org.junit.jupiter.api.Test;
import static org.junit.jupiter.api.Assertions.*;

public class RegistrationFormTest {

    @Test
    public void testSuccessfulRegistration() {
        RegistrationFormPage form = new RegistrationFormPage();
        form.fillForm("John Doe", "john@example.com", "password123");
        assertTrue(form.isRegistrationSuccessful());
    }
}
```

## Reports

This project generates reports using Allure. To view the reports, run the following command after executing your tests:

```bash
gradle allureReport
```

You can then open the generated report in your browser. Check the `build/reports/allure-report` directory for the report files.

## Contributing

Contributions are welcome! If you would like to contribute to this project, please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/YourFeature`).
3. Make your changes.
4. Commit your changes (`git commit -m 'Add some feature'`).
5. Push to the branch (`git push origin feature/YourFeature`).
6. Create a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

For more details, you can visit the [Releases section](https://github.com/VIktorstanww/automation-practice-form/releases) to download the latest version and check for updates.

Happy testing!