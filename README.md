# Movie-Catalog-Web-App---Automated-Testing-with-Selenium-WebDriver

  This repository contains the automated UI tests for the "Movie Catalog" web application using Selenium WebDriver and NUnit. The project ensures that the key functionalities of the Movie Catalog app are tested, such as user registration, login, and movie management (add, edit, delete, and mark movies as watched). The tests are designed using the Page Object Model (POM) for maintainability and scalability.

  **Project Overview**
Movie Catalog is a web application that helps users manage their movie collections. The platform allows users to:

Register and log in to the system.
Add, edit, and delete movies.
Mark movies as watched or unwatched.
View all movies or filter by watched/unwatched.
The primary objective of this project is to ensure the application's core functionalities work as expected by running automated tests on the UI.

**Application URL**
Access the "Movie Catalog" web app at:
http://moviecatalog-env.eba-ubyppecf.eu-north-1.elasticbeanstalk.com

**Automated Tests**
This project includes several tests written in C# using Selenium WebDriver. The tests cover the following main functionalities of the application:

**1. Add Movie Tests**
AddMovieWithoutTitle: Tests the behavior when a user tries to add a movie without a title.
AddMovieWithoutDescription: Tests the behavior when a user tries to add a movie without a description.
AddMovieWithTitleAndDescription: Tests adding a movie with both a title and description and validates that the movie is correctly added to the catalog.

**2. Edit Movie Tests**
EditLastMovie: Edits the most recently added movie, changes its title and description, and verifies that the changes are successfully saved.

**3. Mark Movie as Watched**
MarkLastMovieAsWatched: Marks the last added movie as watched and verifies that it appears in the "Watched Movies" list.

**4. Delete Movie Test**
DeleteMovie: Deletes the most recent movie added and verifies that the deletion was successful.

**Test Frameworks and Tools**
Selenium WebDriver: For automating browser interactions.
NUnit: For organizing and running the tests.
Page Object Model (POM): For organizing page-related actions and elements to improve test maintainability.
C#: The programming language used to write the tests.
ChromeDriver: The browser driver used for Chrome browser automation.

Description of Each Folder/File:

**Pages**: This directory contains the Page Object Models (POM) that encapsulate the interactions with the different pages of the web application.

  **AddMoviePage.cs**: Manages the "Add Movie" page functionalities.
  
  **AllMoviesPage.cs**: Manages the functionalities for viewing all movies.
  
  **BasePage.cs**: Provides common functionalities and properties for all page objects.
  
  **DeletePage.cs**: Handles actions related to deleting a movie.
  
  **EditMoviePage.cs**: Manages the editing of movie details.
  
  **LoginPage.cs**: Handles user login functionalities.
  
  **WatchedMoviesPage.cs**: Manages the functionalities for viewing watched movies.
  
  
**Tests**: This directory contains the test classes that execute the tests for the application.

  **BaseTest.cs**: Sets up the testing environment and common test functions.
  
  **MovieCatalogTests.cs**: Contains specific test cases for the Movie Catalog functionalities.
 
**Drivers**: This folder contains the necessary browser drivers for Selenium tests.

  **ChromeDriver.exe**: The executable file for the Chrome browser driver.
  
**MovieCatalogPomTests.csproj**: The project file for your C# application.

**README.md**: A markdown file that provides information about the project, installation instructions, and usage details.

**.gitignore**: A file that specifies which files and directories should be ignored by Git version control.

**Setup and Running the Tests**
Prerequisites
To run the tests, ensure you have the following installed on your machine:

Visual Studio or any C# IDE
.NET SDK
Chrome Browser
ChromeDriver

**Steps to Set Up the Project**

**1. Clone the repository:**

git clone   https://github.com/DimitrinaPanova/Movie-Catalog-Web-App---Automated-Testing-with-Selenium-WebDriver.git

cd movie-catalog-automated-tests

**2. Install the required dependencies (if not already installed):**

Open the project in Visual Studio.
Ensure that the following NuGet packages are installed:
Selenium.WebDriver
Selenium.Support
NUnit
Selenium.Chrome.WebDriver

**3. Run the tests:**

Use the Visual Studio Test Explorer to run the tests.
Alternatively, you can run the tests from the command line:

dotnet test

Running Tests with Selenium WebDriver
Tests are run in the Chrome browser by default using ChromeDriver. The browser window will open and execute each test, validating the corresponding functionality.

Example Test Execution: When you run the MovieCatalogTests, Selenium WebDriver will:
Open the Movie Catalog app.
Log in with test credentials.
Perform the respective actions (add/edit/delete movies, etc.).
Verify the expected results (for example, checking whether a movie has been added or removed successfully).

**Future Enhancements**

Some additional tests and features that can be included in the future:

Negative Tests: Add more tests to validate handling of incorrect input (e.g., invalid email format).
Visual Regression Testing: Use specialized tools like Percy or Applitools to check for unintended UI changes.
Cross-browser Testing: Extend the testing to cover other browsers (e.g., Firefox, Safari).
API Testing: Add tests to validate the backend APIs directly.

Happy Testing! 🎬📽️ 
