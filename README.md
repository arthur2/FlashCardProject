# Full Stack .NET and Blazor WebAssembly Development Project

## Project Setup Instructions

### 1. Setting Up ASP.NET Core and Blazor WebAssembly

#### Step-by-Step Guide

1. **Install .NET SDK**
   - Download the latest .NET SDK from [Microsoft .NET](https://dotnet.microsoft.com/download).
   - Follow the installation instructions for your operating system (Windows, macOS, Linux).

2. **Create a New Blazor WebAssembly Project**
   - Open a command-line terminal.
   - Run the following command to create a new Blazor WebAssembly project:
     ```bash
     dotnet new blazorwasm -o FlashcardApp
     ```
   - Navigate to the project directory:
     ```bash
     cd FlashcardApp
     ```

3. **Set Up ASP.NET Core Backend**
   - Create a new ASP.NET Core Web API project:
     ```bash
     dotnet new webapi -o FlashcardApp.Server
     ```
   - Modify the `.sln` file to include both the Blazor WebAssembly project and the ASP.NET Core project.

4. **Run the Projects**
   - Start the Web API project:
     ```bash
     cd FlashcardApp.Server
     dotnet run
     ```
   - Start the Blazor WebAssembly project:
     ```bash
     cd ../FlashcardApp
     dotnet run
     ```

#### Useful Reading Material
- [Microsoft Docs: Get started with Blazor](https://learn.microsoft.com/en-us/aspnet/core/blazor/?view=aspnetcore-7.0)
- [Microsoft Docs: Introduction to ASP.NET Core](https://learn.microsoft.com/en-us/aspnet/core/?view=aspnetcore-7.0)

### 2. Download, Install, and Use Visual Studio and Visual Studio Code

#### Installing Visual Studio

1. **Download Visual Studio**
   - Go to the [Visual Studio website](https://visualstudio.microsoft.com/).
   - Download the **Community** version (it's free).

2. **Install Workloads**
   - During installation, select the following workloads:
     - `.NET desktop development`
     - `ASP.NET and web development`
     - `.NET Core cross-platform development`

3. **Create and Open Projects**
   - Open Visual Studio and click **Create a new project**.
   - Choose **Blazor WebAssembly App** or **ASP.NET Core Web API** as needed.

#### Installing Visual Studio Code

1. **Download Visual Studio Code**
   - Go to the [Visual Studio Code website](https://code.visualstudio.com/).
   - Download and install VS Code for your operating system.

2. **Install Extensions**
   - Recommended extensions for this project:
     - `C#` - Official C# extension for .NET development
     - `C# Dev Kit` - Improved .NET development experience
     - `REST Client` - To test APIs

3. **Using Visual Studio Code**
   - Open your project folder using **File > Open Folder**.
   - Use the integrated terminal to run commands:
     ```bash
     dotnet run
     ```

#### Useful Reading Material
- [Microsoft Docs: Install Visual Studio](https://learn.microsoft.com/en-us/visualstudio/install/install-visual-studio)
- [Visual Studio Code Documentation](https://code.visualstudio.com/docs)

---

## Project Explanation

### 1. Login/Logout Mechanism
**Functionality:**
- Users can log in and log out of the application.
- Implements password hashing for security.
- Uses JWT (JSON Web Tokens) for authentication to ensure secure, stateless sessions.
- The backend manages user credentials, while the front end handles login forms and token storage.

### 2. Membership Management Interface
**Functionality:**
- Admin users can add new members using their email and password.
- Provides an interface to manage user data (e.g., password reset, account deletion).
- Uses secure input fields and backend validation to ensure data integrity.

### 3. Homepage / Catalog Page
**Functionality:**
- Displays all flashcard topics available for study.
- Users can browse topics by category.
- Shows brief descriptions of each topic and the number of flashcards available.

### 4. Repository of Flashcards
**Functionality:**
- Backend database stores flashcards, categorized by topics.
- CRUD (Create, Read, Update, Delete) operations available for managing flashcards.
- Each flashcard includes a question, answer, and optional hints.

### 5. Flashcard Learning Interface
**Functionality:**
- Users can select a topic and review flashcards in a study mode.
- Provides an intuitive interface to flip through cards, mark them as "known" or "unknown," and revisit them.
- Uses adaptive learning techniques to help users focus on flashcards they struggle with.

### 6. Flashcard Testing Interface
**Functionality:**
- Users can take a quiz on a selected topic.
- Randomly selects flashcards from the repository to form a test.
- Tracks correct and incorrect answers, providing feedback after each question.
- Users can view results and analyze their performance.

### 7. Skill System and Interface
**Functionality:**
- Tracks user's mastery of each topic based on their study and testing results.
- Displays progress bars and skill levels for each topic.
- Encourages consistent practice by providing rewards (badges, achievements) as users improve their mastery.

---

## Recommended Reading Materials

### .NET Core and ASP.NET Core
- [Microsoft Docs: ASP.NET Core Fundamentals](https://learn.microsoft.com/en-us/aspnet/core/fundamentals/)
- [Pro ASP.NET Core 7 by Adam Freeman](https://www.apress.com/gp/book/9781484279566)

### Blazor WebAssembly
- [Microsoft Docs: Blazor WebAssembly](https://learn.microsoft.com/en-us/aspnet/core/blazor/hosting-models?view=aspnetcore-7.0#blazor-webassembly)
- [Blazor in Action by Chris Sainty](https://www.manning.com/books/blazor-in-action)

### General Web Development
- [You Don't Know JS (Book Series)](https://github.com/getify/You-Dont-Know-JS) - Good for understanding JavaScript concepts, which may be helpful in understanding web mechanics.
- [Frontend Masters](https://frontendmasters.com/) - Courses on web development.
