Hi
This is main
# Default

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
