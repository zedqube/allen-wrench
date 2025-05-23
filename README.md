# Chronicles of a Curious Mind - A Personal Blog

This project is a simple, elegant personal blog website titled "Chronicles of a Curious Mind." It's designed to share thoughts and explorations on technology, design, and the spaces in between. The site features a clean, responsive layout with interactive elements.

## Features

*   **Single-Page Design:** All blog posts are accessible from the main page.
*   **Collapsible Articles:** Each article initially shows a preview. Users can click "Read more" or the article title to expand and read the full content, and "Read less" to collapse it.
*   **Responsive Layout:** The website is designed to work well on various screen sizes, from desktops to mobile devices.
*   **Clean Aesthetics:** Styled with Tailwind CSS for a modern and readable look.
*   **Dynamic Content:** JavaScript is used for the interactive collapsible sections and to keep the copyright year in the footer up-to-date.

## Technologies Used

*   **HTML5:** For the basic structure of the website.
*   **Tailwind CSS:** A utility-first CSS framework for styling.
*   **Vanilla JavaScript:** For interactive elements like collapsible content and dynamic year display.
*   **Google Fonts:** Utilizes 'Poppins' for headings and 'Inter' for body text to enhance typography.

## Project Structure

*   `index.html`: The main HTML file containing all the content and structure of the blog.
*   `README.md`: This file, providing information about the project.
*   Other `.md` files (`cool.md`, `feature.md`, `main.md`): These appear to be supplementary or draft markdown files and are not directly part of the displayed blog.

## How to View

Simply open the `index.html` file in your web browser to view the blog. No special build steps or server setup is required.

## Content Management

This site loads articles dynamically from Markdown files listed in `articles.json`.

### Adding a New Article
1.  Create a new `.md` file in the root directory (e.g., `my-new-article.md`).
2.  Write your article content in Markdown format. You can use `---MORE---` as a separator if you want a "Read more" fold. Content before the separator will be immediately visible; content after will be in the collapsible section.
3.  Add an entry for your new article in `articles.json`. This JSON file lists all articles to be displayed. Each entry needs a `filename`, `title`, and `date` (YYYY-MM-DD). For example:
    ```json
    {
      "filename": "my-new-article.md",
      "title": "My Awesome New Article",
      "date": "YYYY-MM-DD"
    }
    ```
4.  Ensure your new entry in `articles.json` is placed appropriately if you want chronological order (the script sorts by date, newest first, but maintaining order in the JSON file itself is good practice).

### Archiving an Old Article
To archive an article and remove it from the main page:
1.  Move the corresponding `.md` file from the root directory to the `archive/` directory.
2.  Remove its entry from the `articles.json` file.
Archived articles are not currently displayed anywhere on the site but are kept in the `archive/` directory for historical purposes.

## Potential Future Enhancements

*   **Markdown-driven Content:** Convert blog posts into separate Markdown files and dynamically load them into the `index.html` template.
*   **Tagging/Categorization:** Add tags or categories to posts for easier navigation.
*   **Dark Mode:** Implement a theme switcher for dark mode.
