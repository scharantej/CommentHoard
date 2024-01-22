## Flask Application Design: Online Comment Collector
### HTML Files
* **index.html**:
    * This is the homepage of the application.
    * Contains a form with a text field for the Facebook post's URL.
    * Includes a submit button to initiate the comment collection process.
* **results.html**:
    * Displays the collected comments from the specified Facebook post.
    * Includes a list of individual comments extracted from the post.

### Routes
* **home**:
    * Maps to the route `/`.
    * Function linked to this route is responsible for rendering the `index.html` file.
* **collect_comments**:
    * Maps to the route `/collect_comments`.
    * Function linked to this route handles the collection of comments.
    * Uses the URL provided in the form on `index.html` to access the Facebook post.
    * Extracts all comments from the post.
    * Renders the `results.html` file, passing the extracted comments as data.

### How It Works
1. User visits the application's homepage at `/`.
2. User enters the URL of a Facebook post into the text field on `index.html` and clicks "Submit."
3. The browser sends a request to the `/collect_comments` route.
4. The server-side code linked to the `/collect_comments` route executes.
5. It extracts all comments from the provided Facebook post using appropriate logic and APIs.
6. The extracted comments are passed to the `results.html` file as data.
7. The `results.html` file is rendered, displaying the collected comments.
8. The user can view the collected comments on the `results.html` page.