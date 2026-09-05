CHARLES KIDS WORLD — Games, Stories & Cartoons for Curious Kids
==================================================================

WHAT'S INSIDE
-------------
index.html    Home page — links to the Games Zone and the Storybook.

games.html    33 learning games in two worlds:
                Little Explorers (age 3-10, 15 games) and
                Challenge Zone (age 10-15, 18 games).
                Includes English, maths, geography, science, vocabulary,
                a Bible Quiz, a Typing Trainer, a 60-second timed Speed
                Typing Challenge, a high score board, and cartoon-style
                sound effects for correct/incorrect answers.

stories.html  36 stories starring the Charles family, organised into
              10 categories (Character & Values, Friendship & Family,
              Learning & Growth, Nature & Animals, Money & Responsibility,
              Feelings & Kindness, Courage & Perseverance, Bolken
              Montessori School, Charles Family Adventures, and Bible
              Stories), plus The Treasure Hunt — an interactive adventure
              with branching choices and 4 different endings.

              The story library has a search box and category filter
              pills. Every story page has:
                - A "Read Aloud" button with real Play/Pause and Stop
                  controls, and a pulsing dot while it's reading.
                - A "Moral of the Story" box and a "What Did You Learn?"
                  reflection question.
                - Previous Story / Next Story buttons at the bottom of
                  every page, so a child can read straight through all
                  35 stories without ever going back to the library.

HOW TO OPEN IT RIGHT NOW
-------------------------
Just double-click index.html and it will open in your default web
browser. No installation, no internet connection required (the only
online request is for the Google Fonts stylesheet — if you're offline
it will simply fall back to your system font, everything else still
works).

HOW TO DEPLOY IT AS A REAL WEBSITE (free options)
---------------------------------------------------
Any static hosting service will work, since this is a plain HTML/CSS/
JS site with no backend or database. A few easy options:

1. Netlify Drop
   Go to https://app.netlify.com/drop and drag this whole folder in.
   You'll get a live URL in seconds.

2. GitHub Pages
   Create a new GitHub repository, upload these files, then turn on
   GitHub Pages in the repository Settings (Pages section), pointing
   it at the main branch.

3. Cloudflare Pages / Vercel
   Both let you drag-and-drop a static folder the same way as Netlify.

4. Any regular web host (cPanel, etc.)
   Upload the files to your site's public_html (or www) folder via
   FTP or the file manager. Make sure index.html stays at the top
   level so it loads as the homepage.

ABOUT THE "READ ALOUD" FEATURE
--------------------------------
Read Aloud uses your browser's own built-in text-to-speech (the Web
Speech API) — it does not use pre-recorded voice actor audio. This
means:
  - It works completely offline once the page is loaded.
  - Play/Pause/Stop use the browser's native pause and resume where
    supported; on browsers that don't support pausing mid-speech,
    "Pause" will simply stop and "Read Aloud" will start again from
    the top of the page.
  - The voice quality depends on the device and browser (Chrome,
    Edge and Safari generally have the best-sounding voices).
  - No API key, account, or internet service is required.

ABOUT THE HIGH SCORES
------------------------
High scores are kept in the browser's memory for the current visit
only — they are not saved permanently and will reset if the page is
reloaded or closed. Adding permanent, cross-visit high scores would
require a small backend or database, which isn't included here.

HOW TO ADD MORE STORIES LATER
--------------------------------
Open stories.html in a text editor and find the line:
    var STORY_DATA = {
Each story is one entry in that object, in this shape:

    yourstoryid: {
      title:"Your Story Title", subtitle:"Life Lesson", category:"values",
      icon:"⭐", cover:"cover-teal", blurb:"One-sentence teaser for the card.",
      pages:[
        "First paragraph of the story.",
        "Second paragraph.",
        "...and so on."
      ],
      moral:"The moral of the story, one or two sentences.",
      reflection:"A short question inviting the child to reflect."
    },

Valid "category" values are: values, friendship, growth, nature, money,
feelings, courage, school, family — these map to the filter pills and
are defined in the CATEGORIES list just above STORY_DATA. "cover" can
be cover-teal, cover-marigold, or cover-coral (just for card colour
variety — pick any).

Then scroll down to:
    var READING_ORDER = [
and add "yourstoryid" wherever you'd like it to appear in the
Previous/Next reading sequence. That's it — it will automatically
appear as a card in the library, be searchable, be filterable by its
category, and be readable end-to-end with the rest.

HOW TO ADD MORE GAMES LATER
------------------------------
Open games.html and find:
    var GAMES = [
Each game is one entry with an id, category ('explorer' or
'challenge'), icon, title, description, and a start function. The
easiest way to add a simple multiple-choice game is to copy the
pattern used by "gameGrammar" or "gameTimesTable" earlier in the file
— both use small reusable helpers (bankGame / proceduralGame) that
handle the rounds, scoring, and sounds for you.

CUSTOMISING
-----------
Everything is in plain HTML, CSS and JavaScript inside each .html
file, so it's easy to open in any text/code editor (VS Code, etc.)
and change text, colours, or add new games and stories.

© 2026 All rights reserved Hontech Technology.
