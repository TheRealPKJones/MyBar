# MyBar Community Edition — beginner setup

No Node.js, PowerShell, paid API, or hosting bill required. GitHub Pages is available for public repositories on GitHub Free. Google Forms and Sheets are used for suggestions; publishing is manual.

## A. Put MyBar online (GitHub Pages)
1. Go to https://github.com/signup and create a free GitHub account (or sign in).
2. Select **New repository**. Name it `mybar`, choose **Public**, then **Create repository**. Public means anyone can view the site's source code; don't put passwords, API keys, or private information in these files.
3. In the repository, select **Add file > Upload files**. Upload `index.html`, `community-recipes.json`, and `admin.html` from this ZIP's `mybar-community` folder. Choose **Commit changes**. Upload the files at the repository root, not inside an extra folder.
4. Open **Settings > Pages**. Under **Build and deployment**, select **Deploy from a branch**, branch **main**, folder **/(root)**, and **Save**.
5. Wait a few minutes, then visit `https://YOUR-GITHUB-USERNAME.github.io/mybar/` (replace the username). You can also find the actual URL in Settings > Pages.
6. Send this URL to your friends. They can use it from their phones or computers. You do NOT need to leave your PC running.

## B. Create the suggestion form (Google Forms)
1. Open https://forms.google.com and select **Blank form**. Name it `MyBar Drink Suggestions`.
2. Add these questions. Use **Short answer** for `Drink name`, `Your name or nickname` (optional), `Ingredients (one per line)`, and `Measurements (one per line)` (you may prefer **Paragraph** for the latter two). Use **Paragraph** for `Instructions` and `Description`. Mark Drink name, Ingredients, and Instructions as required.
3. Under **Responses**, choose **Link to Sheets** / **View in Sheets** and create a response spreadsheet. You can now review suggestions there.
4. Check form **Settings** to ensure respondents are allowed to submit; turn off restrictions to your organization if applicable. Avoid requiring email addresses unless you want that. Use the form's **Publish** / **Send** / **Copy responder link** option (wording varies) to get the link people can open.
5. On your computer, open `index.html` in a text editor (Notepad is fine). Search for `REPLACE_WITH_YOUR_GOOGLE_FORM_LINK`. Replace only that text with your actual Google Forms responder URL, inside the quotation marks. Save the file.
6. Upload the changed `index.html` to your GitHub repository to replace the old version: open the existing file on GitHub, click the pencil **Edit** button, paste the revised file contents, and **Commit changes**. Alternatively use GitHub's file upload/replace flow. Wait for Pages to redeploy.
7. Test the **Suggest a drink** button on the public site using a private browser window. Submit a test recipe and confirm it appears in the Google Sheet.

## C. Approve and publish a submitted recipe
1. Open the linked Google Sheet and read your friend's suggested recipe. Only approve recipes you want to share publicly.
2. Open the `admin.html` file locally on your computer (you do NOT need to publish this helper on GitHub, but it is included for convenience).
3. In the admin page, select the current `community-recipes.json` file. On your first run use the empty file in this ZIP. On later runs, download the latest JSON from your GitHub repository first: open `community-recipes.json`, choose **Raw** and save the file, or use the download icon.
4. Copy the approved recipe details from the Google Sheet into the form on the admin page. Enter one ingredient per line, matching the ingredient names your friends will see in MyBar. Click **Add to approved list**.
5. Repeat for any other approved recipes, then click **Download community-recipes.json**.
6. On GitHub, open the repository's `community-recipes.json`, choose **Edit** (pencil), replace its contents with the contents of the downloaded JSON file (open it in Notepad), and **Commit changes**. Alternatively upload and replace the file.
7. Wait a minute or two for GitHub Pages to deploy, then refresh MyBar. Approved drinks will appear in the shared collection and be included in ingredient matching. Friends may need to refresh their browser.
8. Reject a submission by simply not publishing it. You can mark its row as rejected in Google Sheets for your own tracking.

## Important notes
- Personal ingredients and personal custom drinks stay on each device in browser localStorage. They are NOT synchronized between devices. Clearing browser site data may erase them.
- Approved community recipes are PUBLIC and shared with every visitor. Never publish private personal information or secrets in a recipe.
- There is no real login or private admin authentication in this version. `admin.html` is a local publishing helper, NOT a protected server admin panel. Only someone with write access to your GitHub repository can publish the shared JSON.
- The Google Form link is public. Do not use a Google Sheets edit link as the suggestion link.
- Google Forms does NOT automatically add submitted drinks to MyBar. You review and publish them manually.
- This version does not use AI or incur OpenAI API costs.
- GitHub and Google may change their free-tier limits or interface labels. Check their current policies.
- If you later change the website URL or browser, personal inventory may not follow. Export/sync isn't built in yet.
