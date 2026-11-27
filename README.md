# Cooking

A phone-friendly, installable (PWA) kitchen app – no server, no accounts, no external libraries. All data is stored privately in the browser on your phone.

## Features

- **Recipes** – name, description, serves, prep/cook times, ingredients (with section headings), method, notes, photo link, star rating, favourites
- **Origins** – where each recipe came from: type (website, cookbook, family…), source, author and web link
- **Comments** – dated comments on every recipe
- **Import** – from a website address (reads schema.org recipe data used by most recipe sites), copy & paste text, pasted page source, or a shared `.recipe.json` / `.txt` file. Once installed on Android, use Chrome's **Share → Cooking** on any recipe page
- **Tags, search & sort** – filter by one or more tags or favourites; search everything or just name / tags / ingredients / origin / comments; sort by date added, name, recently updated, recently/most cooked, rating, quickest, tag or origin
- **Recipe tools** – scale servings (quantities adjust), tick off ingredients and steps, keep screen on while cooking, mark as cooked, share, duplicate
- **Shopping list** – add a recipe's ingredients (untick what you have), add the whole week's planned ingredients, manual items, group by recipe, share the list
- **Weekly menu planner** – Breakfast / Lunch / Dinner (configurable), add recipes or free text, week navigation, copy last week, share the week
- **Conversions** – weight, volume (UK/US/metric), oven temperature °C / fan / °F / gas mark with table, cups → grams for common ingredients, handy reference tables
- **Data** – full JSON backup (download or share), restore (merge or replace), export recipes to CSV or text, planner to CSV, shopping list to text

## Install

Host the folder on any HTTPS web server (GitHub Pages, or Nginx Proxy Manager on the Pi), open it in Chrome on Android and choose **Install app** / **Add to Home screen**.

To use GitHub Pages: repo **Settings → Pages → Deploy from branch → main / (root)**, then open `https://pgs32.github.io/cooking/`.

## Website import note

Browsers don't let a web app read other sites directly, so imports go through a public relay (allorigins / corsproxy / codetabs). You can set your own relay in **Data → Settings** (`{url}` is replaced with the page address). If a site still blocks it, use **Paste text** or **Page source**.

## Releasing a new version

Bump `VERSION` in both `index.html` and `sw.js`, add a line to `CHANGELOG.md`, commit and tag `vYYYY-MM-DD.N`.
