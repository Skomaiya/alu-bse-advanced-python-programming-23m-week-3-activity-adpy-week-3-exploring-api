# advanced-python-programming-week-3-exercise

**Exercise Title:** Exploring the GitHub API with Your Code Editor

**Objective:** To get familiar with the basics of making API requests and understanding API responses using either the HTTP Client in JetBrains IDEs or the REST Client extension in VS Code.

**Prerequisites:**

  * **JetBrains IDE (e.g., PyCharm) or VS Code Installed:** Students should have one of these editors installed.
  * **HTTP Client (JetBrains) or REST Client Extension (VS Code):**
      * **JetBrains:** The HTTP Client comes bundled with most JetBrains IDEs.
      * **VS Code:** Students need to install the "REST Client" extension by Huachao Mao from the VS Code Marketplace.
  * **Basic Understanding of APIs:** A basic understanding of what an API is.

**Part 1: Setting Up Your Editor**

**A. JetBrains HTTP Client (PyCharm, IntelliJ IDEA, etc.)**

1.  **Create a New HTTP Request File:**
      * In your project, right-click on a directory where you want to store your requests.
      * Go to `New` -\> `HTTP Request`.
      * Name the file something like `github_api.http`.
2.  **Familiarize with the Interface:**
      * The `.http` file is where you'll write your API requests using a simple syntax.
      * You'll see green "play" buttons next to each request to execute them.
      * The response will be displayed in a separate "Run" or "Services" tool window.

**B. VS Code REST Client**

1.  **Install the REST Client Extension:**
      * Open VS Code.
      * Go to the Extensions Marketplace (Ctrl+Shift+X or Cmd+Shift+X).
      * Search for "REST Client" by Huachao Mao.
      * Click "Install."
2.  **Create a New Request File:**
      * In your project, create a new file named `github_api.http` or `github_api.rest` (either extension works).
3.  **Familiarize with the Interface:**
      * The `.http` or `.rest` file is where you'll write your API requests.
      * You'll see a "Send Request" link above each request to execute it.
      * The response will be displayed in a separate editor pane to the right.

**Part 2: Making Your First API Request (10 minutes)**

1.  **Introduction to the GitHub API:**
      * Briefly explain that the GitHub API allows you to interact with GitHub data programmatically.
      * Mention that the GitHub API is well-documented ([https://docs.github.com/en/rest](https://www.google.com/url?sa=E&source=gmail&q=https://docs.github.com/en/rest)).
2.  **Constructing the Request:**
      * **HTTP Method:** `GET`
      * **Request URL:** `https://api.github.com/users/octocat`

**A. JetBrains HTTP Client:**

```http
GET https://api.github.com/users/octocat

### (Optional separator between requests)
```

**B. VS Code REST Client:**

```http
GET https://api.github.com/users/octocat

### (Optional separator between requests)
```

3.  **Sending the Request:**
      * **JetBrains:** Click the green "play" button next to the request.
      * **VS Code:** Click the "Send Request" link that appears above the request.
4.  **Analyzing the Response:**
      * **Status Code:** Observe the status code (it should be `200 OK`).
      * **Response Body:** Examine the JSON response body. Point out fields like `login`, `id`, `name`, etc.
      * **Headers:** Briefly mention the response headers.

**Part 3: Exploring Different Endpoints (15 minutes)**

1.  **GitHub API Documentation:** Guide students to the GitHub API documentation. Show them how to find different endpoints.
2.  **Trying Different Endpoints:**
      * **List User Repositories:**
          * **Request URL:** `https://api.github.com/users/octocat/repos`
      * **Get a Specific Repository:**
          * **Request URL:** `https://api.github.com/repos/octocat/Hello-World`
          * **Headers:** Show how to add an `Accept` header:
              * **JetBrains:**

<!-- end list -->

```http
            GET https://api.github.com/repos/octocat/Hello-World
            Accept: application/vnd.github.v3+json

            ###
```

   * **VS Code:**

```http
            GET https://api.github.com/repos/octocat/Hello-World
            Accept: application/vnd.github.v3+json

            ###
```

**Part 4: Understanding Authentication (Optional)**

1.  **Public vs. Private Data:** Explain that some endpoints require authentication.
2.  **GitHub Personal Access Tokens:** If you want to demonstrate authenticated requests, show students how to create a Personal Access Token on GitHub.
3.  **Using the Token:**
      A.  **JetBrains:**

<!-- end list -->

```http
    GET https://api.github.com/user/repos
    Authorization: Bearer YOUR_TOKEN

    ###
```
   B.  **VS Code:**
```

```http
    GET https://api.github.com/user/repos
    Authorization: Bearer YOUR_TOKEN

    ###
```

**Tips for Beginners:**

  * **Start Simple:** Focus on `GET` requests initially.
  * **Visualize:** Use diagrams or analogies to explain concepts.
  * **Relate to Familiar Experiences:** Connect API interactions to everyday web activities.
  * **Encourage Experimentation:** Encourage trying different endpoints and parameters.
  * **Error Handling:** Use errors as learning opportunities.
